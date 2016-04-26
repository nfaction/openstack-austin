# How to Troubleshoot OpenStack Without Losing Sleep

## RabbitMQ

Too few RMQ file descriptors is a recipe for disaster

Set `rabbitmq-server` to `NOFILE limit to 65436*`

## Knowledge-Centered Support (KCS)

Random failure when spawning large amount of instances

100+ tasks, 1 or 2 failures per bulk deploy