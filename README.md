# node-red-contrib-meo-hutech-olp

This module provices a set of nodes in Node-RED to quickly receive data from ESP8266 or ESP32 board with MEO ESP firmware flashed.

There are 2 nodes available at the moment:
- An input node is to receive data from ESP Board, bellow is a sample of output format:
```json
{
  "deviceId": "DEVICE_ID",
  "payload": {
    "D5": 0,
    "D6": 1,
    "D7": 1,
    "D8": 0,
    "A0": 129,
    "V1": "VALUE FROM V1 (Ax)",
    "V2": "VALUE FROM V2 (Ay)",
    "V3": "VALUE FROM V3 (Az)",
    "V4": "VALUE FROM V4 (Gx)",
    "V5": "VALUE FROM V5 (Gy)",
    "V6": "VALUE FROM V6 (Gz)"
  }
}
```

- An ouput node is to send configuration to target ESP Board, users can set the value from pin D0 to D5 (HIGH, LOW or PWM)

## Pre-requisites

Node-RED-MEO-ESP requires Node-RED version 0.14 or more recent.

## Install

To install the stable version run the following command in your Node-RED user directory (typically `~/.node-red`):

    npm i node-red-contrib-meo-hutech-olp

Open your Node-RED instance and you should have one new node in input category and one new node in output category.
