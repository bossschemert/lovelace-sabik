# Homeassistant Lovelace Sabik card

![Image](https://raw.githubusercontent.com/Arie/lovelace-sabik/master/result.png)

# Installation

* Clone this repo into your `www` folder inside your configuration. So it will be: `config_folder/www/lovelace-sabik`.
* Edit your lovelace-ui.yaml or use the flat configuration mode in lovelace and add to the top:
```yaml
resources:
  - type: module
    url: /local/lovelace-sabik/sabik-card.js
```
* Add a card with `type: 'custom:sabik-card'` to your UI:
```yaml
type: 'custom:sabik-card'
```
* Restart home assistant
* ???
* Profit!

## Required Entities

The card expects the following entities to be available:

```yaml
sensor.sabik_outdoor_air_temperature
sensor.sabik_rh_outdoor_air
sensor.sabik_rpm_supply_motor
sensor.sabik_exhaust_air_temperature
sensor.sabik_rh_exhaust_air
sensor.sabik_rpm_extract_motor
sensor.itho_wpu_current_room_temp (replace with your own room temperature sensor)
sensor.sabik_selected_air_volume
binary_sensor.sabik_boost_status
sensor.sabik_extract_air_temperature
sensor.sabik_rh_extract_air
sensor.sabik_voltage_extract_motor
sensor.sabik_supply_air_temperature
sensor.sabik_rh_supply_air
sensor.sabik_voltage_supply_motor
binary_sensor.sabik_extract_fan_alarm
binary_sensor.sabik_filter_alarm
sensor.sabik_bypass_valve_position
sensor.sabik_defrost_status
binary_sensor.sabik_summer_mode
sensor.sabik_current_work_mode
```

## MQTT Topics

The card publishes commands to the following MQTT topics:

```yaml
homeassistant/climate/sabik/fan_mode/set     # For fan speed control
homeassistant/climate/sabik/mode/set         # For snooze mode
homeassistant/climate/sabik/boost/set        # For boost mode
homeassistant/climate/sabik/bypass/set       # For bypass control
homeassistant/climate/sabik/summer_mode/set  # For summer mode
```

## Features

* Display temperatures and humidity levels throughout the system
* Control fan speeds (low/medium/high/auto)
* Toggle boost mode
* Toggle snooze mode
* Control bypass and summer mode with temperature condition feedback
* Monitor filter and fan alarms
* Visual feedback for all system states

