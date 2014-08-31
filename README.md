GradleFirstProject
==================

Simple project build with gradle

Main article url:
http://spring.io/guides/gs/gradle/




Build your project with Gradle Wrapper

The Gradle Wrapper is the preferred way of starting a Gradle build. It consists of a batch script for Windows and a shell script for OS X and Linux. These scripts allow you to run a Gradle build without requiring that Gradle be installed on your system. To make this possible, add the following block to the bottom of your build.gradle.

task wrapper(type: Wrapper) {
    gradleVersion = '2.0'
}

Run the following command to download and initialize the wrapper scripts:

gradle wrapper

After this task completes, you will notice a few new files. The two scripts are in the root of the folder, while the wrapper jar and properties files have been added to a new gradle/wrapper folder.

└── initial
    └── gradlew
    └── gradlew.bat
    └── gradle
        └── wrapper
            └── gradle-wrapper.jar
            └── gradle-wrapper.properties

The Gradle Wrapper is now available for building your project. Add it to your version control system, and everyone that clones your project can build it just the same. It can be used in the exact same way as an installed version of Gradle. Run the wrapper script to perform the build task, just like you did previously:

./gradlew build

The first time you run the wrapper for a specified version of Gradle, it downloads and caches the Gradle binaries for that version. The Gradle Wrapper files are designed to be committed to source control so that anyone can build the project without having to first install and configure a specific version of Gradle.

