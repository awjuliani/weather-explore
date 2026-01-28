# City Weather Explorer

A web-based tool for comparing average monthly weather patterns between cities using interactive 3D visualizations.

![City Weather Explorer](https://img.shields.io/badge/version-1.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Features

- **3D Carousel Visualization**: Compare up to 3 cities simultaneously on a rotating 3D radar chart
- **Multiple Data Types**: View temperature, rainfall, or sunlight hours
- **Historical Data**: Select data from any decade from the 1940s to present
- **Temperature Options**: Toggle between actual and "feels like" temperatures, and between high/mean/low
- **Unit Conversion**: Switch between Fahrenheit and Celsius
- **Shareable URLs**: Share specific comparisons via URL with all settings preserved
- **Responsive Design**: Works on both desktop and mobile devices
- **Dark Mode**: Supports system preference with manual override

## How It Works

### Data Source
Weather data is fetched from the [Open-Meteo API](https://open-meteo.com/), which provides historical weather data including:
- Daily high, low, and mean temperatures
- Apparent (feels like) temperatures
- Precipitation totals
- Sunshine duration

### Visualization
The 3D visualization is built with [Three.js](https://threejs.org/). Each city's data is displayed as a ring of connected points around a circular calendar, where:
- The 12 months are arranged around the circle
- Bar height represents the data value (temperature, rainfall, or sunlight hours)
- Different colors distinguish between cities

### Caching
API responses are cached in localStorage to reduce API calls and improve load times for previously viewed city/decade combinations.

## Usage

1. Search for a city using the search box
2. Select a decade for historical data
3. Add up to 2 more cities to compare
4. Use the toggles to switch between data types and temperature metrics
5. Drag the visualization to rotate and explore the data
6. Click "Share" to copy a URL with your current comparison

## Development

This is a single-page application contained entirely in `index.html` with no build process required. Simply open the file in a browser or serve it from any static file server.

## Author

Developed by [Arthur Juliani](https://awjuliani.github.io/)
