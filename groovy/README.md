<!--

********************************************************************************

WARNING:

    DO NOT EDIT "groovy/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "groovy/" combined with a set of templates)

********************************************************************************

-->

# Quick reference

-	**Maintained by**:  
	[the Apache Groovy project](https://github.com/groovy/docker-groovy)

-	**Where to get help**:  
	[the Docker Community Forums](https://forums.docker.com/), [the Docker Community Slack](https://dockr.ly/slack), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

# Supported tags and respective `Dockerfile` links

-	[`3.0.9-jdk8`, `3.0-jdk8`, `jdk8`](https://github.com/groovy/docker-groovy/blob/e46b8fbd268e1b4559178b87358aac7385f694d2/jdk8/Dockerfile)
-	[`3.0.9-jdk11`, `3.0-jdk11`, `jdk11`](https://github.com/groovy/docker-groovy/blob/e46b8fbd268e1b4559178b87358aac7385f694d2/jdk11/Dockerfile)
-	[`3.0.9-jdk17`, `3.0-jdk17`, `jdk17`, `3.0.9-jdk`, `3.0-jdk`, `3.0.9`, `3.0`, `3`, `jdk`, `latest`](https://github.com/groovy/docker-groovy/blob/e46b8fbd268e1b4559178b87358aac7385f694d2/jdk17/Dockerfile)
-	[`4.0.0-beta-1-jdk8`, `4.0.0-jdk8`, `4.0-jdk8`](https://github.com/groovy/docker-groovy/blob/86f6ece313350fad2a27d2ce89e127804bb098f6/jdk8/Dockerfile)
-	[`4.0.0-beta-1-jdk11`, `4.0.0-jdk11`, `4.0-jdk11`](https://github.com/groovy/docker-groovy/blob/86f6ece313350fad2a27d2ce89e127804bb098f6/jdk11/Dockerfile)
-	[`4.0.0-beta-1-jdk17`, `4.0.0-jdk17`, `4.0-jdk17`, `4.0.0-beta-1-jdk`, `4.0.0-jdk`, `4.0.0-beta-1`, `4.0.0`, `4.0`, `4`](https://github.com/groovy/docker-groovy/blob/86f6ece313350fad2a27d2ce89e127804bb098f6/jdk17/Dockerfile)

# Quick reference (cont.)

-	**Where to file issues**:  
	[https://github.com/groovy/docker-groovy/issues](https://github.com/groovy/docker-groovy/issues)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/groovy/), [`arm32v7`](https://hub.docker.com/r/arm32v7/groovy/), [`arm64v8`](https://hub.docker.com/r/arm64v8/groovy/), [`ppc64le`](https://hub.docker.com/r/ppc64le/groovy/), [`s390x`](https://hub.docker.com/r/s390x/groovy/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/groovy/` directory](https://github.com/docker-library/repo-info/blob/master/repos/groovy) ([history](https://github.com/docker-library/repo-info/commits/master/repos/groovy))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images repo's `library/groovy` label](https://github.com/docker-library/official-images/issues?q=label%3Alibrary%2Fgroovy)  
	[official-images repo's `library/groovy` file](https://github.com/docker-library/official-images/blob/master/library/groovy) ([history](https://github.com/docker-library/official-images/commits/master/library/groovy))

-	**Source of this description**:  
	[docs repo's `groovy/` directory](https://github.com/docker-library/docs/tree/master/groovy) ([history](https://github.com/docker-library/docs/commits/master/groovy))

# What is Groovy?

[Apache Groovy](http://groovy-lang.org/) is a powerful, optionally typed and dynamic language, with static-typing and static compilation capabilities, for the Java platform aimed at improving developer productivity thanks to a concise, familiar and easy to learn syntax. It integrates smoothly with any Java program, and immediately delivers to your application powerful features, including scripting capabilities, Domain-Specific Language authoring, runtime and compile-time meta-programming and functional programming.

![logo](https://raw.githubusercontent.com/docker-library/docs/bb5fc730ed18c45d86425f9fa4265d50cb795ec8/groovy/logo.png)

# How to use this image

Note that if you are mounting a volume and the uid running Docker is not `1000`, you should run as user `root` (`-u root`).

## Starting Groovysh

`docker run -it --rm groovy`

## Running a Groovy script

`docker run --rm -v "$PWD":/home/groovy/scripts -w /home/groovy/scripts groovy groovy <script> <script-args>`

## Reusing the Grapes cache

The local Grapes cache can be reused across containers by creating a volume and mounting it in `/home/groovy/.groovy/grapes`.

```console
docker volume create --name grapes-cache
docker run --rm -it -v grapes-cache:/home/groovy/.groovy/grapes groovy
```

# License

View [license information](http://www.apache.org/licenses/LICENSE-2.0.html) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `groovy/` directory](https://github.com/docker-library/repo-info/tree/master/repos/groovy).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
