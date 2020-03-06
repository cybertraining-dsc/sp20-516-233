# Environmental Robot Boat sp20-516-233 Holly Zhang

## Abstract

We introduce a network architecture using MQTT services to send sensor data from 
an environmental robot boat to various cloud AI services. 

## Evaluating Messaging Protocols

### MQTT

This messaging protocol was specifically made for devices with low capacities 
and requires low energy to execute [@rabbit]. Since a large amount of energy is 
consumed from the the boat's battery by the motors, we want the program to use 
as little energy as possible. Furthermore, the emphasis on low end devices 
means that it executing the code on a Raspberry Pi 3B+ should be possible with 
this protocol. 

### STOMP

STOMP is a protocol that utilizes text-based messaging [@rabbit]. Its 

### AMQP

This will most likely not be used in the project since the Python library for 
AMQP does not support Python 3.8 [@amqp]. Furthermore, it is mostly used in 
industrial settings.  

## Evaluating Messaging Toolkits

### MQTT Toolkits

#### Paho Python Client

Will most likely use this since MQTT uses low energy.
[@eclipse-paho]

#### Mosquitto Python Client

The Mosquitto Python library is now depreciated so it will not be used. Instead, 
it has been added into the Eclipse Paho project [@eclipse-mosquitto].

### STOMP Toolkits


### Other Toolkits

#### RabbitMQ

RabbitMQ supports multiple messaging protocols such as MQTT, STOMP, and a few 
versions of AMQP. However, it has AMQP 0-9-1 as its main messaging protocol, 
while other messaging protocols must be downloaded as plugins from the website 
[@rabbit]. The appropriate plugins can be found through the following link:

<https://www.rabbitmq.com/protocols.html>  

## Network Architecture



### MQTT Client

>* Server: mqtt.eclipse.org
>* Port: (default) 1883
>* Subscribe to messages: OpenAgBloom/#
>* The two messages are: OpenAgBloom/Air/BME, OpenAgBloom/GPS/Loc

```

```