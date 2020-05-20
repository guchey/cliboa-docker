[![CircleCI](https://circleci.com/gh/taguchi8s/cliboa-docker.svg?style=svg)](https://circleci.com/gh/taguchi8s/cliboa-docker)

# What is cliboa-docker?

This Docker container implements a [cliboa](https://github.com/BrainPad/cliboa) runner, execution environment and can easily perform container-based ETL processing.

# How to use this image

## You can try it out quickly

[Sample ETL processing](https://github.com/taguchi8s/cliboa-docker/blob/master/sample/README.md)

## You are free to create your own scenario

[YAML Configuration](https://github.com/BrainPad/cliboa/blob/master/docs/yaml_configuration.md)

# There are several ways to do it

## Run scenario with file redirect

```
$ docker run -i taguchi8s/cliboa-docker cliboa < scenario.yml
```

## Run scenario on pipe

```
$ cat scenario.yml | docker run -i taguchi8s/cliboa-docker cliboa
```

## Run local project

```
$ docker run -v /path/to/<project_name>:/cliboa/project/<project_name> taguchi8s/cliboa-docker cliboa <project_name>
```
