+++
title = "Json"
date =  2022-04-18T19:03:00+02:00
weight = 110
+++

Le JSON est simplement une déclaration en javascript d'un objet.

On l'utilise très régulièrement pour faire communiquer des programmes ensemble (API) ou comme configuration pour des scripts javascript.

```js
{
    "coord": {"lon": -122.08,"lat": 37.39},
    "weather": [
        {"id": 800,"main": "Clear","description": "clear sky","icon": "01d"}
        ],
    "base": "stations",
    "main": {
        "temp": 282.55,
        "feels_like": 281.86,
        "temp_min": 280.37,
        "temp_max": 284.26,
        "pressure": 1023,
        "humidity": 100
        },
    "visibility": 16093,
    "wind": {
        "speed": 1.5,
        "deg": 350
        }
}
```