# docker-aojdk-gradle

AdoptOpenJDK containers with gradle inside ready to build your apps. This image is putting gradle dependency cache into your project directory inside `.gradle_home`.

## Usage

To run gradle build task simply run:

`$ docker run --rm -it -v $PWD:/opt/project -w /opt/project auxx/aojdk-gradle:5.3.0-jdk11-alpine gradle build`

Create a Bash alias to make it shorter.

`alias dgradle="docker run --rm -it -v $PWD:/opt/project -w /opt/project auxx/aojdk-gradle:5.3.0-jdk11-alpine gradle"`

Usage:

`$ dgradle build`
