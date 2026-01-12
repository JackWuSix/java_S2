<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>temp</groupId>
    <artifactId>temp-install</artifactId>
    <version>1.0.0</version>
</project>


mvn org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file `
 -Dfile=xxl-job-tenant-core-2.3.1.jar `
 -DgroupId=com.xuxueli `
 -DartifactId=xxl-job-tenant-core `
 -Dversion=2.3.1 `
 -Dpackaging=jar `
 -DgeneratePom=true
