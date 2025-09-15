# prog-7
check it up


Build and Deployment Issues

My application is a Gradle-based project developed in IntelliJ IDEA. I am currently facing two primary issues that prevent successful execution:

1. Local Build Failure (Windows Environment)

Error: Gradle build process fails during cleanup phase

Message: Unable to delete directory 'C:\Users\User\OneDrive\Desktop\lab7finall\src\common\build\classes\java\main'

Root Cause: File locking by external processes prevents directory deletion

Attempted Solutions:

Stopped Gradle daemon (./gradlew.bat --stop)

Restarted IntelliJ IDEA

Paused OneDrive synchronization

Manual deletion attempts (unsuccessful due to file locks)

2. Database Connection Error (Runtime)

Issue: Server application (server.jar) fails to start

Error: Connection to PostgreSQL at localhost:5433 refused

Status: Application built but cannot run without database access

Conclusion:
The build issue appears to be environment-specific (file locking on Windows/OneDrive). The runtime dependency on PostgreSQL must be resolved before the application can function. Both issues are environmental rather than code-related.
