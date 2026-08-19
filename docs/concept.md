# Desired functionalities of the project

## 1. Longitude determination
Can be determined by:
- Difference in local time from Greenwich (UTC). +1h = +15 deg
- Use time reference points such as:
  - Noon
  - Civil twilight
  - Civil sunset
  - etc

## 2. Latitude determination
Latitude can be determined in multiple ways:
- By using Polaris (North Star)
    - In the zenith north pole (90 degrees latitude and 90 degrees elevation of Polaris)
    - On the horizon at the equator (0 degrees latitude and 0 degrees elevation of Polaris)
- Measurements (azimuth, elevation) of prominent celestial bodies (with a wide spread in azimuth) and with precise time (down to the second) of measurement
    - If measured by sextant, corrections must be applied for measurement error 
      - Height of eye - **DIP**
      - Index error
    - Total correction (in nautical almanac)
    - Additional refractive correction - ARC
      - Temperature, atmospheric pressure
      - Impacts stars near horizon more than one near zenith
      - In nautical almanac
    - Calculated altitude
      - Convert azimuth to sidereal hour angle (declination complement)
## 3. Declination and right ascension

## 4. Nautical almanac



## 99999. Misc notes
Use Stellarium for measurements