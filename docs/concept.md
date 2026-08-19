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
    - In the zenith at the north pole (90 degrees latitude and 90 degrees altitude of Polaris)
    - On the horizon at the equator (0 degrees latitude and 0 degrees altitude of Polaris)
- Measurements (azimuth, altitude) of prominent celestial bodies (with a wide spread in azimuth) and with precise time (down to the second) of measurement
    - If measured by sextant, corrections must be applied for measurement error 
      - Height of eye - ***dip***
      - Index error
    - Total correction (in nautical almanac)
    - Additional refractive correction - ARC
      - Temperature, atmospheric pressure
      - Impacts stars near horizon more than one near zenith
      - In nautical almanac
    - Calculated altitude
      - Convert azimuth to sidereal hour angle (declination complement)

---
For the altitude:

$$sin(Hc) = \sin(Lat) \cdot \sin(Dec) + \cos(Lat) \cdot \cos(Dec) \cdot \cos(LHA) $$
Where:
- $Lat$ - latitude (North > 0, South < 0 )
- $Lon$ - longitude (East > 0, South < 0)
- $Dec$ - declination of the body observed
- $GHA$ - Greenwich hour angle of the body observed
- $LHA = GHA + Lon$ - the local angle of the body observed
- $Hc$ - Calculated altitude of the celestial body

And for the azimuth:

$$cos(\pm Zn)= \frac{\sin(Dec) - \sin(Lat) \cdot \sin(Hc)}{\cos(Lat) \cdot \cos(Hc)} $$
$$Z = \arccos(\cos(Z)) \in [0,180] $$
$$
Zn = \begin{cases}
+Z & \text{if} & LHA \in [180,360]\\
-Z & \text{if} & LHA \in [0,180]
\end{cases}
$$

Where:
- $Zn$ - Computed azimuth
- $Z$ - Preliminary result for Zn


Compare the calculated altitude and azimuth against measured altitude $Ho$ and measured azimuth $Zo$

# 

## 3. 

## 4. Nautical almanac



## 99999. Misc notes
- Use Stellarium for measurements
- "Golden reference testing"
  - Test the project against celnav by DaniilGalahov
- Investigate Declination and right ascension