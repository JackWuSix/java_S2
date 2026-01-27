2026-01-27 11:45:53.355 [main] INFO  c.a.otter.canal.adapter.launcher.CanalAdapterApplication - Starting CanalAdapterApplication using Java 11.0.29 on Community-Elasticsearch-Test with PID 1411721 (/usr/local/canal_adapter/lib/client-adapter.launcher-1.1.7.jar started by root in /usr/local/canal_adapter/bin)
2026-01-27 11:45:53.360 [main] INFO  c.a.otter.canal.adapter.launcher.CanalAdapterApplication - No active profile set, falling back to default profiles: default
2026-01-27 11:45:54.040 [main] INFO  org.springframework.cloud.context.scope.GenericScope - BeanFactory id=a6cee8d1-48d1-3e64-a5f9-a1d1e90caee9
2026-01-27 11:45:54.298 [main] INFO  o.s.boot.web.embedded.tomcat.TomcatWebServer - Tomcat initialized with port(s): 8081 (http)
2026-01-27 11:45:54.306 [main] INFO  org.apache.coyote.http11.Http11NioProtocol - Initializing ProtocolHandler ["http-nio-8081"]
2026-01-27 11:45:54.307 [main] INFO  org.apache.catalina.core.StandardService - Starting service [Tomcat]
2026-01-27 11:45:54.307 [main] INFO  org.apache.catalina.core.StandardEngine - Starting Servlet engine: [Apache Tomcat/9.0.52]
2026-01-27 11:45:54.395 [main] INFO  o.a.catalina.core.ContainerBase.[Tomcat].[localhost].[/] - Initializing Spring embedded WebApplicationContext
2026-01-27 11:45:54.395 [main] INFO  o.s.b.w.s.context.ServletWebServerApplicationContext - Root WebApplicationContext: initialization completed in 997 ms
2026-01-27 11:45:54.732 [main] INFO  com.alibaba.druid.pool.DruidDataSource - {dataSource-1} inited
2026-01-27 11:45:55.146 [main] INFO  org.apache.coyote.http11.Http11NioProtocol - Starting ProtocolHandler ["http-nio-8081"]
2026-01-27 11:45:55.160 [main] INFO  o.s.boot.web.embedded.tomcat.TomcatWebServer - Tomcat started on port(s): 8081 (http) with context path ''
2026-01-27 11:45:55.165 [main] INFO  c.a.o.canal.adapter.launcher.loader.CanalAdapterService - ## syncSwitch refreshed.
2026-01-27 11:45:55.166 [main] INFO  c.a.o.canal.adapter.launcher.loader.CanalAdapterService - ## start the canal client adapters.
2026-01-27 11:45:55.170 [main] INFO  c.a.otter.canal.client.adapter.support.ExtensionLoader - extension classpath dir: /usr/local/canal_adapter/plugin
2026-01-27 11:45:55.262 [main] INFO  c.a.o.canal.adapter.launcher.loader.CanalAdapterLoader - Load canal adapter: logger succeed
2026-01-27 11:45:55.266 [main] ERROR c.a.o.canal.adapter.launcher.loader.CanalAdapterLoader - Load canal adapter: es8 failed
java.lang.RuntimeException: java.lang.NullPointerException
	at com.alibaba.otter.canal.client.adapter.es8x.ES8xAdapter.init(ES8xAdapter.java:48)
	at com.alibaba.otter.canal.client.adapter.ProxyOuterAdapter.init(ProxyOuterAdapter.java:32)
	at com.alibaba.otter.canal.adapter.launcher.loader.CanalAdapterLoader.loadAdapter(CanalAdapterLoader.java:115)
	at com.alibaba.otter.canal.adapter.launcher.loader.CanalAdapterLoader.init(CanalAdapterLoader.java:71)
	at com.alibaba.otter.canal.adapter.launcher.loader.CanalAdapterService.init(CanalAdapterService.java:60)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor$LifecycleElement.invoke(InitDestroyAnnotationBeanPostProcessor.java:389)
	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor$LifecycleMetadata.invokeInitMethods(InitDestroyAnnotationBeanPostProcessor.java:333)
	at org.springframework.beans.factory.annotation.InitDestroyAnnotationBeanPostProcessor.postProcessBeforeInitialization(InitDestroyAnnotationBeanPostProcessor.java:157)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.applyBeanPostProcessorsBeforeInitialization(AbstractAutowireCapableBeanFactory.java:422)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1778)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:602)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:524)
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$1(AbstractBeanFactory.java:374)
	at org.springframework.cloud.context.scope.GenericScope$BeanLifecycleWrapper.getBean(GenericScope.java:376)
	at org.springframework.cloud.context.scope.GenericScope.get(GenericScope.java:179)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:371)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208)
	at org.springframework.context.support.AbstractApplicationContext.getBean(AbstractApplicationContext.java:1154)
	at org.springframework.cloud.context.scope.refresh.RefreshScope.eagerlyInitialize(RefreshScope.java:125)
	at org.springframework.cloud.context.scope.refresh.RefreshScope.start(RefreshScope.java:117)
	at org.springframework.cloud.context.scope.refresh.RefreshScope.onApplicationEvent(RefreshScope.java:112)
	at org.springframework.cloud.context.scope.refresh.RefreshScope.onApplicationEvent(RefreshScope.java:67)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.doInvokeListener(SimpleApplicationEventMulticaster.java:176)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.invokeListener(SimpleApplicationEventMulticaster.java:169)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.multicastEvent(SimpleApplicationEventMulticaster.java:143)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:421)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:378)
	at org.springframework.context.support.AbstractApplicationContext.finishRefresh(AbstractApplicationContext.java:938)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:586)
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:145)
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:754)
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:434)
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:338)
	at com.alibaba.otter.canal.adapter.launcher.CanalAdapterApplication.main(CanalAdapterApplication.java:22)
Caused by: java.lang.NullPointerException: null
	at com.alibaba.otter.canal.client.adapter.es8x.ES8xAdapter.init(ES8xAdapter.java:40)
	... 37 common frames omitted
