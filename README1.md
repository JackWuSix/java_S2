[INFO] data-service 5.1.22 ................................ FAILURE [  5.364 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  13.342 s
[INFO] Finished at: 2026-01-11T21:26:27+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal on project data-service: Could not collect dependencies for project com.zili.1chego.data:data-service:jar:5.1.22
[ERROR] Failed to read artifact descriptor for com.zili.1chego.track:track-api:jar:0.0.5
[ERROR]         Caused by: The following artifacts could not be resolved: com.zili.1chego.track:track:pom:0.0.1-SNAPSHOT (absent): Could not find artifact com.zili.1chego.track:track:pom:0.0.1-SNAPSHOT in maven-public (http://192.168.112.244:8081/repository/maven-public/)
[ERROR]
[ERROR] -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/DependencyResolutionException
[ERROR]
[ERROR] After correcting the problems, you can resume the build with the command
[ERROR]   mvn <args> -rf :data-service
PS D:\java\1chego\1chego-data> 
