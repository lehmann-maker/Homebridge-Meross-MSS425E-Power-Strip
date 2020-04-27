<span align="center">

<a href="https://github.com/homebridge/verified/blob/master/verified-plugins.json"><img alt="homebridge-verified" src="https://raw.githubusercontent.com/donavanbecker/homebridge-meross/master/meross/Meross_x_Homebridge.svg" width="500px"></a>

# Homebridge Meross

<a href="https://www.npmjs.com/package/homebridge-meross"><img title="npm version" src="https://badgen.net/npm/v/homebridge-meross?icon=npm" ></a>
<a href="https://www.npmjs.com/package/homebridge-meross"><img title="npm downloads" src="https://badgen.net/npm/dt/homebridge-meross?icon=npm" ></a>

<p>The <a href="https://www.meross.com">Meross</a> plugin for
  <a href="https://homebridge.io">Homebridge</a>.

  This Plugin allows you to control your Meross Devices from HomeKit.
</p>

</span>

## Origin
The original work was done by [donavanbecker](https://github.com/donavanbecker). This is only refinement information for Meross-MSS425E-Power-Strip, given in script below. Thanks to [donavanbecker](https://github.com/donavanbecker) for the plugin.

## Installation
* Install [config-ui-x](https://github.com/oznu/homebridge-config-ui-x).
* Search for "Meross" on the Plugin Screen of [config-ui-x](https://github.com/oznu/homebridge-config-ui-x) .
* Click Install on Homebridge Meross.

## Authorization & Configuration
If you're setting this plug up fresh, make sure you go through the
typical Meross app for initial setup.

You will also have to obtain some information that the Meross mobile
app uses in its HTTP request headers. The [Charles](https://www.charlesproxy.com)
proxy application can be used to sniff the network requests sent from the iOS app.
A detailed tutorial on how to set up Charles with your iOS device can be found
[here](https://www.raywenderlich.com/641-charles-proxy-tutorial-for-ios).

Please rewrite your script for use of Meross-MSS425E-Power-Strip as following:

```

"accessories": [
{
            "name": "Plug1",
            "deviceUrl": "http://xxx.xxx.xxx.xxx",
            "hardwareVersion": 2,
            "channel": 1,
            "messageId": "xxxxxxx",
            "timestamp": xxxxxx,
            "sign": "xxxxxx",
            "accessory": "Meross"
        },
        {
            "name": "Plug2",
            "deviceUrl": "http://xxx.xxx.xxx.xxx",
            "hardwareVersion": 2,
            "channel": 2,
            "messageId": "xxxxxxx",
            "timestamp": xxxxxx,
            "sign": "xxxxxx",
            "accessory": "Meross"
        },
        {
            "name": "Plug3",
            "deviceUrl": "http://xxx.xxx.xxx.xxx",
            "hardwareVersion": 2,
            "channel": 3,
            "messageId": "xxxxxxx",
            "timestamp": xxxxxx,
            "sign": "xxxxxx",
            "accessory": "Meross"
        },
        {
            "name": "USB",
            "deviceUrl": "http://xxx.xxx.xxx.xxx",
            "hardwareVersion": 2,
            "channel": 4,
            "messageId": "xxxxxxx",
            "timestamp": xxxxxx,
            "sign": "xxxxxx",
            "accessory": "Meross"
        }
    ]
    
```
