# optbv-intl
Internationalized style for optbv by Geospatial Information Authority of Japan (GSI)

# Demo
[![gif](https://user-images.githubusercontent.com/18297/192099806-bc10d2cf-5b7a-4c2b-95ae-f6212f69b058.gif)](https://optgeo.github.io/optbv-intl)

https://optgeo.github.io/optbv-intl

# How to use
```html
<!doctype html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<link rel="stylesheet" href="https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.css"/>
<script src="https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.js"></script>
</head>
<body>
<style>
body { margin:0; padding:0; font-family: 'Roboto', sans-serif; color: #333333}
#map { top:0; height: 100vh; width: 100vw; position: fixed; z-index: 0; }
</style>
<div id="map"></div>
<script>
const map = new maplibregl.Map({
  container: "map",
  style: "https://optgeo.github.io/optbv-intl/optbv-intl-dev.json",
  hash: true, 
  center: [135, 35],
  zoom: 4,
  maxZoom: 22
})
map.addControl(new maplibregl.NavigationControl())
map.addControl(new maplibregl.ScaleControl({
  maxWidth: 200, unit: "metric"
}))
</script>
</body>
```

# About this repository
This repository was originally developed to contribute to achieving Objective #4 (demonstrate a distributed map hosting environment for equitable smart campus solutions) of the WG4 (Fast and Smart Maps) of the United Nations Open GIS Initiative.

# See also
- https://github.com/optgeo/optbv-charites
- https://github.com/optgeo/optbv-spec
