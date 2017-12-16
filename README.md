# chili-environment
Chili growing environment control

*Under active development*. Currently, only toggling a Lightify plug is supported.

## Requirements

- [Lightify gateway](https://www.amazon.de/Osram-Controller-Fernsteuerung-Schnittstelle-Kompatibel/dp/B00JDJC1RY/ref=sr_1_1?s=lighting&ie=UTF8&qid=1513423858&sr=1-1&keywords=lightify+gateway)
- [Lightify plug](https://www.amazon.de/Osram-Schaltbare-Steckdose-Schnittstelle-Erweiterung/dp/B074PZLX2P/ref=pd_lpo_vtph_201_bs_t_1?_encoding=UTF8&psc=1&refRID=EYBF93SNDHEWSG60EYK5)
- node version 8

## Setup

1. configure your Lightify gateway and plug according to the manufacturer's manuals.
2. get the local IP of your Lightify gateway (you should assign it a static IP in your router/DHCP server)
3. create a config file from sample
    ```shell
    cp config.example.json config.json
    ```
4. replace `LOCAL_IP_OF_LIGHTIFY_GATEWAY` in `config.json` with the IP of your Lightify gateway
5. run `npm install` and then `./discover` to show all Lightify products connected to your gateway.
6. get the `friendlyMac` value of the plug connected to your heating unit and put it into your `config.json` (replace `FRIENDLY_MAC_OF_HEATING_UNIT_PLUG` with it).
7. running `./toggle_heat` should now toggle the plug's status.
