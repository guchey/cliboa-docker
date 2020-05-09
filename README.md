# cliboa-docker

## Run scenario with file redirect

```
docker run -i taguchi8s/cliboa-docker cliboa < scenario.yml
```

## Run scenario on pipe

```
cat scenario.yml | docker run -i taguchi8s/cliboa-docker cliboa
```

## Run project from local

```
docker run -v /path/to/<project_name>:/cliboa/project/<project_name> taguchi8s/cliboa-docker cliboa <project_name>
```