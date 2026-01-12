Microsoft Windows [版本 10.0.19045.6456]
(c) Microsoft Corporation。保留所有权利。

D:\mavne3\com\xuxueli\xxl-job-tenant-core>mvn install:install-file ^
More?
More?  -Dfile="D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1\xxl-job-tenant-core-2.3.1.jar" ^
More?
More?  -DgroupId=com.xuxueli ^
More?
More?  -DartifactId=xxl-job-tenant-core ^
More?
More?  -Dversion=2.3.1 ^
More?
More?  -Dpackaging=jar ^
More?
More?  -DgeneratePom=true ^
More?
More?  -Dmaven.repo.local=D:\mavne3
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
[INFO] Total time:  0.567 s
[INFO] Finished at: 2026-01-12T10:39:54+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-install-plugin:3.1.2:install-file (default-cli) on project standalone-pom: The parameters 'file' for goal org.apache.maven.plugins:maven-install-plugin:3.1.2:install-file are missing or invalid -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/PluginParameterException

D:\mavne3\com\xuxueli\xxl-job-tenant-core>
