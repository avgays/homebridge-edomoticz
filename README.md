# homebridge-eDomoticz
A fully-fledged up-to-date Homebridge-Plugin
for use with [Homebridge](https://github.com/nfarina/homebridge) v0.2.1x
and [Domoticz](https://github.com/domoticz/domoticz)

##Supports:
- Switches (Light / Socket On & Off, & reflected status)
- Temperature Sensors (Current Temperature, deg C)
- Temperature & Humidity Sensors (as above + Humidity, %)
- Temperature & Humidity & Pressure Sensors (as above + Pressure, hPa)
- Power Meters (General / YouLess Meter, kWh / YouLess counter - Current Consumption, Total Consumption, [Today Consumption - YouLess])
- General Usage Sensors (eg: CPU%, Mem%, HDD% from Motherboard Sensors Hardware Device)

###Todo:
- [ ] homebridge [plugin 2.0](https://github.com/nfarina/homebridge/pull/497) support
- [x] Respect Room setting if defined in config.json
- [x] kWh (electricity usage)
- [x] General % usage
- [ ] Improve val types with val type (int) and unit rather than relying on string
- [ ] Brightness
- [ ] Hue
- [ ] m3 (gas usage)
- [x] Humidity
- [x] Pressure
- [x] YouLess Meter
- [ ] ...more sensors (ongoing)!

## Installation
```
sudo npm install -g patchworkboy/homebridge-eDomoticz
```

## Configuration

~/.homebridge/config.json example:
```
{
    "bridge": {
        "name": "Homebridge",
        "username": "CC:21:3E:E4:DE:33",
        "port": 51826,
        "pin": "031-45-154"
    },
    "description": "Configuration file for (e)xtended Domoticz platform.",
    "platforms": [
        {
            "platform": "eDomoticz",
            "name": "eDomoticz",
            "server": "127.0.0.1",
            "port": "8080",
            "roomid": 0
        }
    ],
    "accessories": []
}
```
