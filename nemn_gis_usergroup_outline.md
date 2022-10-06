# NE MN GIS User Group Talk - geotiff.js
March 16th, 2022  
Kris Johnson, NRRI/UMD

## Outline
  - [What is geotiff.js](#what-is-geotiffjs)
  - [Why use it?](#why-use-it)
  - [Examples](#examples)
  - [My use case](#my-use-case)

## What is [geotiff.js](https://geotiffjs.github.io/)

GeoTIFF in the browser

[Cloud Optmized GeoTIFFs](https://www.cogeo.org/)

How to use it:
- [COGs how-to for data providers](https://www.cogeo.org/providers-guide.html)
- [GDAL](https://github.com/GeoTIFF/georaster-layer-for-leaflet/blob/master/FAQs.md#how-do-i-convert-my-geotiff-into-a-cloud-optimized-geotiff)

Who is using it:
- [Planet](https://www.planet.com/explorer/)
- [USGS LandsatLook](https://landsatlook.usgs.gov/explore)

[HTTP GET range requests](https://www.cogeo.org/in-depth.html)

## Why use it?

Server-side (the traditional approach)
- WMS (for rendering)
- WCS (for analyzing)

Client-side (raster rendering and analysis in your browser)
 - parse multiple formats (remote, local, via ArrayBuffer)
 - compression
 - resampling
 - bounding box

 Essentially, the raster equivalent of GeoJSON

## Complimentary Technologies

_I'm not an expert so I need to rely on these_

[Georaster](https://github.com/GeoTIFF/georaster) - simplifies the JavaScript interface to geotiff.js

[Georaster Layer for Leaflet](https://github.com/GeoTIFF/georaster-layer-for-leaflet) - Leaflet plugin for georasters

## Examples

[COG-Explorer](https://geotiffjs.github.io/cog-explorer/) - explore the capabilities of multispectral imagery in the browser

[GeoTIFF.io](https://app.geotiff.io/) - add your own GeoTIFF and play around

[List of examples using georaster-layer-for-leaflet](https://github.com/GeoTIFF/georaster-layer-for-leaflet-example#other-examples)
- [color scale example](https://geotiff.github.io/georaster-layer-for-leaflet-example/examples/color-scale.html)
- [YCbCr Photometric Interpretation](https://geotiff.github.io/georaster-layer-for-leaflet-example/examples/ycbcr.html)
- [custom icon symbology](https://geotiff.github.io/georaster-layer-for-leaflet-example/examples/wind-direction-arrows.html)

## My use case

NRRI's ForCAST Tool
- I can't share the link yet. Look for our presentation at the annual conference in the Fall. It should be available to the public at that point.

