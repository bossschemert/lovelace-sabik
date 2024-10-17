# Homeassistant Lovelace Sabik card

![Image](https://raw.githubusercontent.com/Arie/lovelace-sabik/master/result.png)

# Installation

* Clone this repo into your `www` folder inside your configuration. So it will be: `config_folder/www/lovelace-sabik`.
* Edit your lovelace-ui.yaml or use the flat configuration mode in lovelace and add to the top:
```
resources:
  - type: module
    url: /local/lovelace-sabik/sabik-card.js
```
* Add a card with `type: 'custom:sabik-card'` and `entity: 'climate.put-your-sabik-name-here'` to your UI:
```
type: 'custom:sabik-card'
entity: 'climate.put-your-sabik-name-here'
```
* Restart home assistant
* ???
* Profit!

