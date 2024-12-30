# Venezuela GeoJSON

This repository contains GeoJSON data for Venezuela. The data can be used for mapping and spatial analysis purposes.

## Files

- `municipalities.geojson`: GeoJSON data for municipalities.

## Usage

To use the GeoJSON data, you can load it into your preferred mapping library or GIS software. Here is an example of how to load the data using Leaflet.js:

```javascript
var map = L.map('map').setView([6.4238, -66.5897], 6);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; OpenStreetMap contributors'
}).addTo(map);

fetch('venezuela.geojson')
    .then(response => response.json())
    .then(data => {
        L.geoJSON(data).addTo(map);
    });
```

## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

