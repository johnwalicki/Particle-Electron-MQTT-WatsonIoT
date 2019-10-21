# A MQTT primer

``` text
 MQTT is a M2M or Machine to Machine binary protocol, that is especially well suited to connecting
IoT/sensors via Unreliable Networks ( e.g. 2G, intermittent SattComm like Iridium etc )
```


## The Central Broker / server
This is a hub and spoke network topology, i.e. many Sources ( Sensors for example )
can Publish to a well known MQTT Broker IP address or Hostname ( port 1833 or for ssl 8883 ).
Sinks or consumers can then Subscribe to the Broker to receive the messages

## Quality of service
Although it uses TCP/IP there is still the chance of messages been lost. 

at least once ...

at most once ...

Ephemeral msg typically ( QOS possible with some Broker configuration that use a persistent storage mechanism like a DB / file)

## Topics
Pub/Sub is coordinated and effected by the use of Topics.  These are akin to say a person tuning into a radio channel.
....

It's binary so message packets are small! ( vs say STOMP ) and do not work over well known HTTP/S ports - so if you need firewall less headaches use Web-sockets to channel MQTT.  STOMP is text based so easier to work with and may be a good alternative for the beginner pub/sub/MQTT technologist.






### Useful Resources
An Introduction to MQTT for Beginners - Steve Cope - 6 September 2017 - Video
https://www.youtube.com/watch?v=2aHV2Fn0I60

RabbitMQ extensions for STOMP / AMQP / MQTT from Pivotal Labs