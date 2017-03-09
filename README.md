### alpine-rabbitmq-standalone

Small RabbitMQ image of standalone.

***

#### Get image from DockerHub

```
$ docker pull leafney/alpine-rabbitmq-standalone
```

#### Create a default rabbitmq container

```
$ docker run --name rmq -d -p 5672:5672 -p 15672:15672 leafney/alpine-rabbitmq-standalone
```

With browser for `http://localhost:15672` by default `user` and `123456` .

***

#### Custom container

Set Login User and Password by yourself and Mount the rabbitmq log and data from container.

```
$ docker run --name rmq -d -p 5672:5672 -p 15672:15672 -v /home/tiger/rmqfiles:/rabbitmq/var -e RMQ_USER=tom -e RMQ_PWD=123123 leafney/alpine-rabbitmq-standalone
```
