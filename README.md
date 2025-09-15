# prog-7
check it up


My program is a Gradle project developed in IntelliJ IDEA. I'm currently unable to run the application because the build process is failing with a file deletion error.

The specific error message is: Unable to delete directory 'C:\Users\User\OneDrive\Desktop\lab7finall\src\common\build\classes\java\main'

The error indicates that Gradle cannot clean the previous build files because another process has a lock on one or more files in the build directory. This is preventing the build task from completing successfully.

I've already tried several solutions, including:

Stopping the Gradle Daemon using ./gradlew.bat --stop.

Closing and restarting IntelliJ IDEA.

Pausing OneDrive's file synchronization.

Manually attempting to delete the directory from the command line using Remove-Item -Recurse -Force, which also fails because the files are locked.

It appears a persistent process is holding a lock on the build directory, which is a required step for Gradle to complete a new build and generate the runnable JAR file. This prevents me from compiling and running my latest code.



