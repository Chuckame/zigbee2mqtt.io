---
title: "TuYa TS0601_gas_sensor control via MQTT"
description: "Integrate your TuYa TS0601_gas_sensor via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-05-01T14:47:09Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa TS0601_gas_sensor

|     |     |
|-----|-----|
| Model | TS0601_gas_sensor  |
| Vendor  | TuYa  |
| Description | gas sensor |
| Exposes | gas, self_test, self_test_result, fault_alarm, silence, linkquality |
| Picture | ![TuYa TS0601_gas_sensor](https://www.zigbee2mqtt.io/images/devices/TS0601_gas_sensor.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Gas (binary)
Indicates whether the device detected gas.
Value can be found in the published state on the `gas` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` gas is ON, if `false` OFF.

### Self_test (binary)
Indicates whether the device is being self-tested.
Value can be found in the published state on the `self_test` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"self_test": NEW_VALUE}`.
If value equals `true` self_test is ON, if `false` OFF.

### Self_test_result (enum)
Result of the self-test.
Value can be found in the published state on the `self_test_result` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `checking`, `success`, `failure`, `others`.

### Fault_alarm (binary)
Indicates whether a fault was detected.
Value can be found in the published state on the `fault_alarm` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` fault_alarm is ON, if `false` OFF.

### Silence (binary)
Silence the alarm.
Value can be found in the published state on the `silence` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"silence": NEW_VALUE}`.
If value equals `true` silence is ON, if `false` OFF.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

