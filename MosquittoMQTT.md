Using mosquitto MQTT broker on MacOS:

Installation and setup:


Installation via brew:
```
brew install mosquitto
```

Get additional information:
```
brew info mosquitto
```
This will also show you the location of the brokers config file. Advised is to
set the port to 1883

Start your mosquitto MQTT broker through brew services:
```
brew services start mosquitto
```

Examples:

Subscriber (first terminal):
```
mosquitto_sub --url mqtt://<HOST-IP>:<HOST-PORT>/<TOPIC-NAME>

example: "mosquitto_sub --url mqtt://10.3.48.18:1883/topic/state"
```

Publisher (second terminal)
```
mosquitto_pub --url mqtt://<HOST-IP>:<HOST-PORT>/<TOPIC-NAME> -m "<MESSAGE>"

example: "mosquitto_pub --url mqtt://10.3.48.18:1883/topic/state -m "To app and internal broker""
```
