Below you will find an example of how to send and receive HTTPS in NodeRed. Please refer to the [wiki](https://github.com/iotacademy/NodeRed_KPN_LoRa/wiki/1.-Receive-with-HTTPS-nodes) to get more explanation.

Copy the below code, and import through the clipboard in NodeRed
```json
[{"id":"e0e4fb1f.e20908","type":"http in","z":"65bb5a5b.a49fc4","name":"LoRa Post Catcher","url":"/lorapost","method":"post","swaggerDoc":"","x":194.6145782470703,"y":305.0035400390625,"wires":[["40bca731.7a2f48","4ab9cfaa.2f78e"]]},{"id":"40bca731.7a2f48","type":"debug","z":"65bb5a5b.a49fc4","name":"","active":true,"console":"false","complete":"false","x":439.6111297607422,"y":304.3263854980469,"wires":[]},{"id":"4ab9cfaa.2f78e","type":"function","z":"65bb5a5b.a49fc4","name":"Create Post Resp","func":"msg.payload = \"I have received something!\";\nreturn msg;","outputs":1,"noerr":0,"x":475.8957977294922,"y":223,"wires":[["c4e87a33.a564f8"]]},{"id":"c4e87a33.a564f8","type":"http response","z":"65bb5a5b.a49fc4","name":"LoRa Post Catcher","x":734.8958587646484,"y":222,"wires":[]}]
```
