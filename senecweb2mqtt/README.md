# Senec Web2MQTT
Reads stats from Senec Web API and publishes them as MQTT device to home assistant. Works with Senec Home V2 / V3 / V4.


### Requirements
- An MQTT Broker, e.g. mosquitto. Can be installed by going to Settings -> Addons -> Addon Store -> Mosquitto
- The HA MQTT Integration. Can be installed by going to Settings -> Devices and Services -> Add Integration -> MQTT. 
When setting up the MQTT integration, use "core-mosquitto" as MQTT broker when you are using the Mosquitto-Addon. Else use the IP adress of your own MQTT broker

### Configuration 
The configuration is done in the configuration tab of the addon. All available options are described below:

```
# Credentials for Senec Website (mein-senec.de)
SENEC_USERNAME='mail@example.com'
SENEC_PASSWORD='supersafepassword'

# Number of the unit you want to fetch data for. Default is unit 0.
SENEC_ANLAGENUMMER='0'

# MQTT parameters for connection with broker
MQTT_USERNAME='exampleuser'
MQTT_PASSWORD='anotherpassword'
MQTT_HOST='core-mosquitto'
MQTT_PORT=1883

# Default HA MQTT topic, only change when you know what you are doing
MQTT_TOPIC_PREFIX='homeassistant/sensor/'

# An arbitrary sensor name prefix, results in e.g. "senec_acculevel_now" as sensorname in HA
MQTT_SENSOR_NAME_PREFIX='senec' 
# An arbitrary name for the MQTT device in home assistant
MQTT_DEVICE_NAME='Senec Home V4' 
# Serial number of your Senec Device, needed for unique entity ids
MQTT_DEVICE_IDENTIFIER='xx-xxxxxxxx'
# An arbitrary name of the device Manufacturer (MQTT device info)
MQTT_DEVICE_MANUFACTURER='Senec' 
# An arbitrary name of the device Model (MQTT device info)
MQTT_DEVICE_MODEL='Home V4'
```


![grafik](https://github.com/mstuettgen/homeassistant-addons/assets/10927858/a0d2c28b-7ee6-4267-847b-80b5509108c0)


