# Nexe Docker

Builds a [Docker](http://docker.io) image for building static  [nodejs](http://nodejs.org) executable application using
[nexe](https://github.com/crcn/nexe).

## Example usage:

### No argument (I'm feeling lucky...)

Build static binary from executable file in `./bin` directory and put it in
the `./dist` directory.

	  docker run --rm -v $PWD:/app cogniteev/nexe

### Pass script in argument

Build static binary from executable file specified in parameter and put it in
the `./dist` directory.

	  docker run --rm -v $PWD:/app /app cogniteev/nexe

### Execute arbitrary command

Prefix your command with a dash character.

		docker run --rm -ti cogniteev/bexe - bash

## Environment variables

Variable       | Default value | Description
---------------|---------------|---------------
NEXE_VERSION   | 0.4.1         | nexe package version
NODEJS_VERSION | latest        | static executable NodeJS runtime
LDFLAGS        | -static-libgcc -static-libstdc++ | NodeJS build flags
