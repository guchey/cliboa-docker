[![CircleCI](https://circleci.com/gh/taguchi8s/cliboa-docker.svg?style=svg)](https://circleci.com/gh/taguchi8s/cliboa-docker)

# What is cliboa-docker?

Image for easy use of [cliboa](https://github.com/BrainPad/cliboa).

# How to use this image

## Create your scenario.yml

[YAML Configuration](https://github.com/BrainPad/cliboa/blob/master/docs/yaml_configuration.md)

## Run scenario with file redirect

```
$ docker run -i taguchi8s/cliboa-docker cliboa < scenario.yml
```

## Run scenario on pipe

```
$ cat scenario.yml | docker run -i taguchi8s/cliboa-docker cliboa
```

## Run project from local

```
$ docker run -v /path/to/<project_name>:/cliboa/project/<project_name> taguchi8s/cliboa-docker cliboa <project_name>
```
