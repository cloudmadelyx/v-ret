# v-ret
# Open-Meteo Weather Data Client

**Important Notice:**  
This code and its outputs are provided for personal or educational use only. You **may NOT use this code to earn money or for any commercial purposes** without explicit permission from the original author.

---

This repository contains a project based on the idea from the website:
https://roadmap.sh/projects/weather-api-wrapper-service https://roadmap.sh/projects/weather-api-wrapper-service

---

## Project Description

The goal of this project is to create a wrapper service for weather APIs that fetches, processes, and caches weather data in a user-friendly way.

This implementation uses the Open-Meteo API with caching and automatic retries, providing current and hourly weather data for given locations.

---

## Acknowledgment

This project was inspired by the roadmap.sh project idea to help learners build practical API wrapper services.

## What This Code Does

This script fetches weather data from the Open-Meteo API for a specified geographic location (latitude and longitude). It includes the following features:

- Uses caching (`requests_cache`) to avoid redundant API calls and speed up repeated requests.
- Implements automatic retries with exponential backoff on API request failures (`retry_requests`).
- Retrieves current weather conditions such as temperature, humidity, wind speed/direction, rain, and precipitation.
- Retrieves hourly weather forecast data for the next 24 hours, including temperature, humidity, rain, snowfall, wind speed, weather codes, sunshine duration, and shortwave radiation.
- Processes and organizes this data into a pandas DataFrame for easy analysis or further processing.
- Prints summary information including location coordinates, elevation, timezone, current weather variables, and the hourly forecast.

---

## How to Use

1. **Set the location coordinates:**  
   Replace the `x` placeholders in the `params` dictionary with your desired latitude and longitude.

2. **Run the script:**  
   The script will output current weather details and a pandas DataFrame containing hourly forecast data.

3. **Modify as needed:**  
   - You can extend the script to handle multiple locations or weather models by adding loops.
   - Adjust which weather variables to fetch by modifying the lists in the `params`.

---

## Requirements

- Python 3.x
- `openmeteo_requests` package
- `pandas`
- `requests_cache`
- `retry_requests`

Install missing packages via pip, for example:

```bash
pip install openmeteo_requests pandas requests_cache retry_requests
# Project Information

