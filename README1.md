PS D:\java\车联网\1chego-system\system-api> mvn clean install
[INFO] Scanning for projects...
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/com/zili/framework/1chego/1chego/0.0.1-SNAPSHOT/maven-metadata.xml
Downloading from maven-public: http://192.168.112.244:8081/repository/maven-public/com/zili/framework/1chego/1chego/0.0.1-SNAPSHOT/1chego-0.0.1-SNAPSHOT.pom
[ERROR] [ERROR] Some problems were encountered while processing the POMs:
[FATAL] Non-resolvable parent POM for com.zili.1chego.system:system:0.0.1-SNAPSHOT: The following artifacts could not be resolved: com.zili.framework.1chego:1chego:pom:0.0.1-SNAPSHOT (absent): Could not find artifact com.zili.framework.1chego:1chego:pom:0.0.1-SNAPSHOT in maven-public (http://192.168.112.244:8081/repository/maven-public/) and 'parent.relativePath' points at no local POM @ com.zili.1chego.system:system:0.0.1-SNAPSHOT, D:\java\车联网\1chesystem\pom.xml, line 6, column 13
 @ 
[ERROR] The build could not read 1 project -> [Help 1]
[ERROR]   
[ERROR]   The project com.zili.1chego.system:system-api:0.2.4 (D:\java\车联网\1chego-system\system-api\pom.xml) has 1 error
[ERROR]     Non-resolvable parent POM for com.zili.1chego.system:system:0.0.1-SNAPSHOT: The following artifacts could not be resolved: com.zili.framework.1chego:1chego:pom:0.0.1-SNAPSHOT (absent): Could not find artifact com.zil
i.framework.1chego:1chego:pom:0.0.1-SNAPSHOT in maven-public (http://192.168.112.244:8081/repository/maven-public/) and 'parent.relativePath' points at no local POM @ com.zili.1chego.system:system:0.0.1-SNAPSHOT, D:\java\车联网\1chego-system\pom.xml, line 6, column 13 -> [Help 2]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/ProjectBuildingException
[ERROR] [Help 2] http://cwiki.apache.org/confluence/display/MAVEN/UnresolvableModelException
PS D:\java\车联网\1chego-system\system-api> 
