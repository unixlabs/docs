<!--

********************************************************************************

WARNING:

    DO NOT EDIT "gradle/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "gradle/" combined with a set of templates)

********************************************************************************

-->

# Quick reference

-	**Maintained by**:  
	[Keegan Witt (of the Groovy Project)](https://github.com/keeganwitt/docker-gradle), [with the Gradle Project's approval](https://discuss.gradle.org/t/official-docker-images/21159/8)

-	**Where to get help**:  
	[the Docker Community Forums](https://forums.docker.com/), [the Docker Community Slack](https://dockr.ly/slack), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

# Supported tags and respective `Dockerfile` links

-	[`7.2.0-jdk8`, `7.2-jdk8`, `7-jdk8`, `jdk8`](https://github.com/keeganwitt/docker-gradle/blob/12de35caaf73bc28651fa6fa00c7dd4078695de9/jdk8/Dockerfile)
-	[`7.2.0-jdk11`, `7.2-jdk11`, `7-jdk11`, `jdk11`](https://github.com/keeganwitt/docker-gradle/blob/12de35caaf73bc28651fa6fa00c7dd4078695de9/jdk11/Dockerfile)
-	[`7.2.0-jdk17`, `7.2-jdk17`, `7-jdk17`, `jdk17`, `7.2.0-jdk`, `7.2-jdk`, `7-jdk`, `jdk`, `7.2.0`, `7.2`, `7`, `latest`](https://github.com/keeganwitt/docker-gradle/blob/12de35caaf73bc28651fa6fa00c7dd4078695de9/jdk17/Dockerfile)
-	[`6.9.1-jdk8`, `6.9-jdk8`, `6-jdk8`](https://github.com/keeganwitt/docker-gradle/blob/c1589fa3ca8eca327c505c1a088902e83cac9b3e/jdk8/Dockerfile)
-	[`6.9.1-jdk11`, `6.9-jdk11`, `6-jdk11`](https://github.com/keeganwitt/docker-gradle/blob/c1589fa3ca8eca327c505c1a088902e83cac9b3e/jdk11/Dockerfile)
-	[`6.9.1-jdk17`, `6.9-jdk17`, `6-jdk17`, `6.9.1-jdk`, `6.9-jdk`, `6-jdk`, `6.9.1`, `6.9`, `6`](https://github.com/keeganwitt/docker-gradle/blob/c1589fa3ca8eca327c505c1a088902e83cac9b3e/jdk17/Dockerfile)

# Quick reference (cont.)

-	**Where to file issues**:  
	[https://github.com/keeganwitt/docker-gradle/issues](https://github.com/keeganwitt/docker-gradle/issues)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/gradle/), [`arm32v7`](https://hub.docker.com/r/arm32v7/gradle/), [`arm64v8`](https://hub.docker.com/r/arm64v8/gradle/), [`ppc64le`](https://hub.docker.com/r/ppc64le/gradle/), [`s390x`](https://hub.docker.com/r/s390x/gradle/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/gradle/` directory](https://github.com/docker-library/repo-info/blob/master/repos/gradle) ([history](https://github.com/docker-library/repo-info/commits/master/repos/gradle))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images repo's `library/gradle` label](https://github.com/docker-library/official-images/issues?q=label%3Alibrary%2Fgradle)  
	[official-images repo's `library/gradle` file](https://github.com/docker-library/official-images/blob/master/library/gradle) ([history](https://github.com/docker-library/official-images/commits/master/library/gradle))

-	**Source of this description**:  
	[docs repo's `gradle/` directory](https://github.com/docker-library/docs/tree/master/gradle) ([history](https://github.com/docker-library/docs/commits/master/gradle))

# What is Gradle?

[Gradle](https://gradle.org/) is a build tool with a focus on build automation and support for multi-language development. If you are building, testing, publishing, and deploying software on any platform, Gradle offers a flexible model that can support the entire development lifecycle from compiling and packaging code to publishing web sites. Gradle has been designed to support build automation across multiple languages and platforms including Java, Scala, Android, C/C++, and Groovy, and is closely integrated with development tools and continuous integration servers including Eclipse, IntelliJ, and Jenkins.

![logo](https://raw.githubusercontent.com/docker-library/docs/c3d3ca6beed000f9ba6eabc98f3399158f520256/gradle/logo.png)

# How to use this image

## Building a Gradle project

Run this from the directory of the Gradle project you want to build.

`docker run --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle <gradle-task>`

Note the above command runs using uid/gid 1000 (user *gradle*) to avoid running as root.

If you are mounting a volume and the uid/gid running Docker is not *1000*, you should run as user *root* (`-u root`). *root* is also the default, so you can also simply not specify a user.

# License

View [license information](https://gradle.org/license/) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `gradle/` directory](https://github.com/docker-library/repo-info/tree/master/repos/gradle).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
