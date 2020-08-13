# vocbenc-semanticturkey

Docker setup for running VocBench3 and SemanticTurkey via two separate docker services

Once you clone this repository execute command, make two docker networks (web and backend):

```
docker network create $network_name
```

afterwards execute command:

```
docker-compose up
```

To access Tomcat dashboard enter `127.0.0.1:8080` in browser of choice, user/pass are admin/admin.
To access VocBench enter `127.0.0.1:8080/vocbench` in browser of choice.
