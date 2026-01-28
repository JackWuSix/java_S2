package com.example.canal.config;

import com.alibaba.otter.canal.client.CanalConnector;
import com.alibaba.otter.canal.client.CanalConnectors;
import com.google.common.collect.Lists;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import java.net.InetSocketAddress;

@Configuration
public class CanalConfig {

    @Bean
    public CanalConnector canalConnector(
            @Value("${canal.host}") String canalHost,
            @Value("${canal.port}") int canalPort,
            @Value("${canal.destination}") String canalDestination,
            @Value("${canal.username}") String canalUsername,
            @Value("${canal.password}") String canalPassword
    ) {
        return CanalConnectors.newClusterConnector(
                Lists.newArrayList(
                        new InetSocketAddress(canalHost, canalPort)
                ),
                canalDestination,
                canalUsername,
                canalPassword
        );
    }
}




package com.example.canal.client;

import com.alibaba.otter.canal.client.CanalConnector;
import jakarta.annotation.PostConstruct;
import jakarta.annotation.PreDestroy;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.context.event.EventListener;
import org.springframework.boot.context.event.ApplicationReadyEvent;
import org.springframework.stereotype.Component;

@Component
public class CanalClient {

    private static final Logger logger = LoggerFactory.getLogger(CanalClient.class);

    private final CanalConnector canalConnector;

    public CanalClient(CanalConnector canalConnector) {
        this.canalConnector = canalConnector;
    }

    /**
     * Spring 启动完成后再连接 Canal（最稳）
     */
    @EventListener(ApplicationReadyEvent.class)
    public void start() {
        try {
            canalConnector.connect();
            canalConnector.subscribe();
            canalConnector.rollback();
            logger.info("Canal 客户端启动成功");
        } catch (Exception e) {
            logger.error("Canal 客户端启动失败", e);
        }
    }

    /**
     * Spring 容器关闭时释放资源
     */
    @PreDestroy
    public void stop() {
        try {
            canalConnector.disconnect();
            logger.info("Canal 客户端已关闭");
        } catch (Exception e) {
            logger.warn("Canal 客户端关闭异常", e);
        }
    }
}
