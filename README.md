# Homeassistant component to control Openhab
Enable while you port your config over to homeassistant

## Installation

```bash
git clone https://github.com/Br3nda/homeassistant-openhab-component
cd homeassistant-openhab-component
cp sensor/openhab.py ~/.homeassistant/custom_components/sensor/
cp switch/openhab.py ~/.homeassistant/custom_components/switch/
```

## Example configuration:

Control openhab switches (on/off) from homeassistant
```yml
switch openhab:
  platform: openhab
  host: http://127.0.0.1:8080
```

Control openhab dimmers as lights in homeassistant
```yml
light openhab:
  platform: openhab
  host: http://127.0.0.1:8080
```

Read everything else
```yml
sensor openhab:
  platform: openhab
  host: http://127.0.0.1:8080
```

## Limitations
* Openhab only gives us the name, not the friendly string you see in openhab sitemaps (you can use customize friendly_name to override once you know the device names).
* Openhab doesn't have "units", so the items don't appear with degrees or percentage humidity etc.
