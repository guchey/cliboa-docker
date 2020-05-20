# Sample

You can easily try cliboa with Docker containers.

## Up test server

```
$ cd ./docker-compose
$ docker-compose up -d
```

## Execute scenario

```
$ ls docker-compose/sftp/foo # no output
$ docker run --rm -i --net=cliboa_sample_network taguchi8s/cliboa-docker cliboa < ./scenario/ftp_to_sftp.yml
$ ls docker-compose/sftp/foo
test.csv.gz
```