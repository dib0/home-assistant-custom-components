# Home-Assistant Custom Components

Here are my custom components for home-assistant. (http://www.home-assistant.io)

# Blink4Home support

The [Blink4Home](https://blinkforhome.com/) platform allows you to arm and disarm your Blink4Home camera network (as configured through the app) in  Home Assistant. Besides providing these two services, it also allows you to add a binary sensor that will indicate if the camera network is armed or not.

To enable your Blink4Home camera network in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
blink4home:
    username: "<your e-mailadress>"
    password: "<your Blink4Home password>"
```

Configuration variables:

- **username** (*Required*): The emailadress that you use for the Blink4Home camera's.
- **password** (*Required*): The password that you use for the Blink4Home camera's.
- **network_id** (*Optional*): The id of the network you wan't to control (in case you have more than one network).

# Blink4Home sensor
The [Blink4Home](https://blinkforhome.com/) indicates if the blink camera network (configured with the [Blink4Home camera platform](/components/camera.blink4home/) is armed or not.

To enable the Blink4Home sensor in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
binary_sensor:
   - platform: blink4home
```

**Note:** *The binary sensor depends on the configuration of the Blink4Home camera platform, so you also need to add the camera plaform to your installation.*
