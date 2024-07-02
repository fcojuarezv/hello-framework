# Weather report
```js
const forecast = FileAttachment("./data/forecast.json").json();

```

```js
import * as L from "npm:leaflet";

const div = display(document.createElement("div"));
div.style = "height: 400px;";

const map = L.map(div)
  .setView([37.80, -122.47], 13);

L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
  attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>'
})
  .addTo(map);

L.marker([37.80, -122.47])
  .addTo(map)
  .bindPopup("A nice popup<br> indicating a point of interest.")
  .openPopup();

//L.circle([51.508, -0.11], {
//    color: 'red',
//    fillColor: '#f03',
//    fillOpacity: 0.5,
//    radius: 500
//}).addTo(map);

var polygon = L.polygon([
    [37.8158863, -122.4928863],
    [37.794076000000004, -122.487211],
    [37.7985504, -122.4596518],
     [37.8203613, -122.4653217],
     [37.8158863, -122.4928863]
]).addTo(map);

```

```js
display(forecast);
```