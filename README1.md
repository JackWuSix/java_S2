Microsoft Windows [版本 10.0.19045.6456]
(c) Microsoft Corporation。保留所有权利。

D:\mavne3\com\xuxueli\xxl-job-tenant-core>mvn install:install-file -Dfile="D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1\xxl-job-tenant-core-2.3.1.jar" -DgroupId=com.xuxueli -DartifactId=xxl-job-tenant-core -Dversion=2.3.1 -Dpackaging=jar -DgeneratePom=true -Dmaven.repo.local=D:\mavne3
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- install:3.1.2:install-file (default-cli) @ standalone-pom ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.546 s
[INFO] Finished at: 2026-01-12T10:42:44+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-install-plugin:3.1.2:install-file (default-cli) on project standalone-pom: Cannot install artifact. Artifact is already in the local repository.
[ERROR]
[ERROR] File in question is: D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1\xxl-job-tenant-core-2.3.1.jar
[ERROR]
[ERROR] -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException

D:\mavne3\com\xuxueli\xxl-job-tenant-core>
