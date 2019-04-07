# Connecting ESP8266 with AWS IoT
Learning to connect ESP8266 with AWS IoT using Arduino Sketch

## Pre-requisites
* ESP8266 NodeMCU 1.0 Lua V3
* Arduino IDE with ESP8266 board manager v2.5

## Steps to achieve successful AWS IoT connection using ESP8266
* Create an IoT device in AWS IoT core (https://github.com/debsahu/ESP-MQTT-AWS-IoT-Core/blob/master/doc/README.md)
* Practice pub and sub to the newly created IoT thing using web based MQTT client (https://docs.aws.amazon.com/iot/latest/developerguide/view-mqtt-messages.html)
* Import JSON library to Arduino IDE (https://www.ardu-badge.com/ArduinoJson/6.10.0)
* Import MQTT library to Arduino IDE (https://github.com/256dpi/arduino-mqtt)
* Use the example sketch (https://github.com/debsahu/ESP-MQTT-AWS-IoT-Core/tree/master/Arduino/MQTT)
  - Learn the fundamentals of connection to AWS IoT and the certificate TLS1.2 requirements (https://raphberube.com/blog/2019/02/18/Making-the-ESP8266-work-with-AWS-IoT.html)
* You should be in a position to successfully connect your device to AWS IoT and see the shadow status updates

## Next steps
* Create a new topic, push messages to that topic using web MQTTclient, read the messages sent to that topic in device and do some actions like turning device built-in LED ON / OFF
* Create AWS IoT rules to trigger AWS Lambda functions based on certain message values
* Create AWS IoT rules to make use of Twilio notifications / AWS SNS
