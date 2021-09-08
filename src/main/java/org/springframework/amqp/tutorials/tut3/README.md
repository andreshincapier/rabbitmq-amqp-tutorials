# Publish/Subscribe

See for more information
[Introduction](https://www.rabbitmq.com/tutorials/tutorial-three-spring-amqp.html)


The application uses Spring Profiles to control what tutorial it's running, and whether it's a sender or receiver. To run the receiver, execute the following command:

```shell
# consumer
java -jar target/rabbitmq-tutorials.jar --spring.profiles.active=pub-sub,receiver \
    --tutorial.client.duration=60000
```

Open another shell to run the sender:
```shell
# sender
java -jar target/rabbitmq-tutorials.jar --spring.profiles.active=pub-sub,sender \
    --tutorial.client.duration=60000
```