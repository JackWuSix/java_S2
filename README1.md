Microsoft Windows [版本 10.0.19045.6456]
(c) Microsoft Corporation。保留所有权利。

D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1>mvn org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file -Dfile="D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1\xxl-job-tenant-core-2.3.1.jar" -DgroupId="com.xuxueli" -DartifactId="xxl-job-tenant-core" -Dversion="2.3.1" -Dpackaging=jar -DgeneratePom=true
[INFO] Scanning for projects...
[INFO]
[INFO] -------------------------< temp:temp-install >--------------------------
[INFO] Building temp-install 1.0.0
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- install:2.5.2:install-file (default-cli) @ temp-install ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.564 s
[INFO] Finished at: 2026-01-12T10:26:50+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file (default-cli) on project temp-install: Cannot install artifact. Artifact is already in the local repository.
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

D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1>mvn install:install-file -Dfile="D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1\xxl-job-tenant-core-2.3.1.jar" -DgroupId="com.xuxueli" -DartifactId="xxl-job-tenant-core" -Dversion="2.3.1" -Dpackaging=jar -DgeneratePom=true
[INFO] Scanning for projects...
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-clean-plugin/3.2.0/maven-clean-plugin-3.2.0.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-clean-plugin/3.2.0/maven-clean-plugin-3.2.0.pom (5.3 kB at 45 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/35/maven-plugins-35.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/35/maven-plugins-35.pom (9.9 kB at 381 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/35/maven-parent-35.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/35/maven-parent-35.pom (45 kB at 1.5 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/25/apache-25.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/25/apache-25.pom (21 kB at 708 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-clean-plugin/3.2.0/maven-clean-plugin-3.2.0.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-clean-plugin/3.2.0/maven-clean-plugin-3.2.0.jar (36 kB at 1.4 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-resources-plugin/3.3.1/maven-resources-plugin-3.3.1.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-resources-plugin/3.3.1/maven-resources-plugin-3.3.1.pom (8.2 kB at 326 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/39/maven-plugins-39.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/39/maven-plugins-39.pom (8.1 kB at 261 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/39/maven-parent-39.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/39/maven-parent-39.pom (48 kB at 2.4 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/29/apache-29.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/29/apache-29.pom (21 kB at 1.2 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-resources-plugin/3.3.1/maven-resources-plugin-3.3.1.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-resources-plugin/3.3.1/maven-resources-plugin-3.3.1.jar (31 kB at 998 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-jar-plugin/3.4.1/maven-jar-plugin-3.4.1.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-jar-plugin/3.4.1/maven-jar-plugin-3.4.1.pom (7.8 kB at 411 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/42/maven-plugins-42.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/42/maven-plugins-42.pom (7.7 kB at 334 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/42/maven-parent-42.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/42/maven-parent-42.pom (50 kB at 2.1 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/32/apache-32.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/32/apache-32.pom (24 kB at 1.1 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/junit/junit-bom/5.10.2/junit-bom-5.10.2.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/junit/junit-bom/5.10.2/junit-bom-5.10.2.pom (5.6 kB at 246 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-jar-plugin/3.4.1/maven-jar-plugin-3.4.1.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-jar-plugin/3.4.1/maven-jar-plugin-3.4.1.jar (34 kB at 1.4 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-compiler-plugin/3.13.0/maven-compiler-plugin-3.13.0.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-compiler-plugin/3.13.0/maven-compiler-plugin-3.13.0.pom (10 kB at 387 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/41/maven-plugins-41.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-plugins/41/maven-plugins-41.pom (7.4 kB at 350 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/41/maven-parent-41.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/maven-parent/41/maven-parent-41.pom (50 kB at 2.1 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/31/apache-31.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/apache/31/apache-31.pom (24 kB at 1.2 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-compiler-plugin/3.13.0/maven-compiler-plugin-3.13.0.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-compiler-plugin/3.13.0/maven-compiler-plugin-3.13.0.jar (83 kB at 2.9 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-surefire-plugin/3.2.5/maven-surefire-plugin-3.2.5.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-surefire-plugin/3.2.5/maven-surefire-plugin-3.2.5.pom (5.3 kB at 231 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/surefire/surefire/3.2.5/surefire-3.2.5.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/surefire/surefire/3.2.5/surefire-3.2.5.pom (22 kB at 879 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/junit/junit-bom/5.9.3/junit-bom-5.9.3.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/junit/junit-bom/5.9.3/junit-bom-5.9.3.pom (5.6 kB at 235 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-surefire-plugin/3.2.5/maven-surefire-plugin-3.2.5.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-surefire-plugin/3.2.5/maven-surefire-plugin-3.2.5.jar (45 kB at 969 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-install-plugin/3.1.2/maven-install-plugin-3.1.2.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-install-plugin/3.1.2/maven-install-plugin-3.1.2.pom (8.5 kB at 471 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-install-plugin/3.1.2/maven-install-plugin-3.1.2.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/plugins/maven-install-plugin/3.1.2/maven-install-plugin-3.1.2.jar (32 kB at 1.7 MB/s)
[INFO]
[INFO] -------------------------< temp:temp-install >--------------------------
[INFO] Building temp-install 1.0.0
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- install:3.1.2:install-file (default-cli) @ temp-install ---
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-util/1.9.18/maven-resolver-util-1.9.18.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-util/1.9.18/maven-resolver-util-1.9.18.pom (2.9 kB at 143 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver/1.9.18/maven-resolver-1.9.18.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver/1.9.18/maven-resolver-1.9.18.pom (22 kB at 770 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-api/1.9.18/maven-resolver-api-1.9.18.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-api/1.9.18/maven-resolver-api-1.9.18.pom (2.7 kB at 92 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-utils/4.0.1/plexus-utils-4.0.1.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-utils/4.0.1/plexus-utils-4.0.1.pom (7.8 kB at 326 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus/17/plexus-17.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus/17/plexus-17.pom (28 kB at 972 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-xml/3.0.0/plexus-xml-3.0.0.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-xml/3.0.0/plexus-xml-3.0.0.pom (3.7 kB at 178 kB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus/13/plexus-13.pom
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus/13/plexus-13.pom (27 kB at 1.1 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-util/1.9.18/maven-resolver-util-1.9.18.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-util/1.9.18/maven-resolver-util-1.9.18.jar (196 kB at 7.5 MB/s)
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-api/1.9.18/maven-resolver-api-1.9.18.jar
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-utils/4.0.1/plexus-utils-4.0.1.jar
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-xml/3.0.0/plexus-xml-3.0.0.jar
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/apache/maven/resolver/maven-resolver-api/1.9.18/maven-resolver-api-1.9.18.jar (157 kB at 5.2 MB/s)
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-xml/3.0.0/plexus-xml-3.0.0.jar (93 kB at 3.1 MB/s)
Downloaded from maven-public: http://192.168.112.244:8081/repository/maven-public/org/codehaus/plexus/plexus-utils/4.0.1/plexus-utils-4.0.1.jar (193 kB at 5.7 MB/s)
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.212 s
[INFO] Finished at: 2026-01-12T10:33:04+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-install-plugin:3.1.2:install-file (default-cli) on project temp-install: Cannot install artifact. Artifact is already in the local repository.
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

D:\mavne3\com\xuxueli\xxl-job-tenant-core\2.3.1>
