<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>com.zili.1chego.data</groupId>
        <artifactId>data</artifactId>
        <version>0.0.1-SNAPSHOT</version>
    </parent>

    <artifactId>data-service</artifactId>
    <name>data-service</name>
    <version>5.1.22</version>

    <dependencies>

        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-web</artifactId>
        </dependency>

        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-cache</artifactId>
        </dependency>

        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-security</artifactId>
        </dependency>

        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-swagger</artifactId>
        </dependency>

        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-mybatis</artifactId>
        </dependency>

        <!--测试包-->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>com.zili.1chego.system</groupId>
            <artifactId>system-api</artifactId>
        </dependency>
        <dependency>
            <groupId>com.zili.1chego.track</groupId>
            <artifactId>track-api</artifactId>
        </dependency>
        <!--freemarker-->
        <dependency>
            <groupId>org.freemarker</groupId>
            <artifactId>freemarker</artifactId>
        </dependency>

        <dependency>
            <groupId>com.zili.1chego.data</groupId>
            <artifactId>data-api</artifactId>
        </dependency>


        <dependency>
            <groupId>com.zili.framework.1chego</groupId>
            <artifactId>framework-job</artifactId>
        </dependency>
    </dependencies>

    <build>
        <finalName>${project.artifactId}</finalName>
        <pluginManagement>
            <plugins>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-resources-plugin</artifactId>
                    <configuration>
                        <delimiters>
                            <delimiter>@</delimiter>
                        </delimiters>
                        <useDefaultDelimiters>false</useDefaultDelimiters>
                    </configuration>
                </plugin>
            </plugins>
        </pluginManagement>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <executions>
                    <execution>
                        <goals>
                            <goal>repackage</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-deploy-plugin</artifactId>
                <configuration>
                    <skip>true</skip>
                </configuration>
            </plugin>
        </plugins>
        <resources>
            <resource>
                <directory>src/main/resources</directory>
                <filtering>true</filtering>
            </resource>
        </resources>
    </build>
    <profiles>
        <profile>
            <id>dev</id>
            <activation>
                <activeByDefault>true</activeByDefault>
            </activation>
            <properties>
                <profileActive>dev</profileActive>
            </properties>
        </profile>
        <profile>
            <id>test</id>
            <properties>
                <profileActive>test</profileActive>
            </properties>
        </profile>
        <profile>
            <id>prod</id>
            <properties>
                <profileActive>prod</profileActive>
            </properties>
        </profile>
    </profiles>
</project>
