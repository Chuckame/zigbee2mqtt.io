---
title: "AUBESS ZXZIR-02 control via MQTT"
description: "Integrate your AUBESS ZXZIR-02 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-05-28T16:23:11Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# AUBESS ZXZIR-02

|     |     |
|-----|-----|
| Model | ZXZIR-02  |
| Vendor  | AUBESS  |
| Description | Universal smart IR remote control |
| Exposes | switch (state), learned_ir_code, ir_code_to_send, linkquality |
| Picture | ![AUBESS ZXZIR-02](https://www.zigbee2mqtt.io/images/devices/ZXZIR-02.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


Device can learn IR codes and send already known IR codes.

### Control
By publishing to `zigbee2mqtt/FRIENDLY_NAME/set` various device attributes can control the device:

#### Switch to a learning mode

Request:
```json
{
    "learn_ir_code":"ON"
}
```

The command activates the orange light on the device. You have several seconds to take source IR remote, move it closer to the device and press a button. The learned IR code will be exposed as `learned_ir_code`.

#### Send already learned IR code

Request:
```json
{
    "ir_code_to_send": "<previously learned IR code>"
}
```
<!-- Notes END: Do not edit below this line -->



## Exposes

### Switch 
The current state of this switch is in the published state under the `learn_ir_code` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"learn_ir_code": "ON"}`, `{"learn_ir_code": "OFF"}` or `{"learn_ir_code": "undefined"}`.
It's not possible to read (`/get`) this value.

### Learned_ir_code (text)
The IR code learned by device.
Value can be found in the published state on the `learned_ir_code` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Ir_code_to_send (text)
The IR code to send by device.
Value will **not** be published in the state.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"ir_code_to_send": NEW_VALUE}`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

