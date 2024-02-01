# Asteroid Orbit Determination

## Overview

This program is designed for orbit determination of an asteroid, aiming to calculate the six crucial orbital elements based on observational data obtained from three separate observations. The orbital elements include:

1. Semi-major axis of the orbit.
2. Eccentricity of the orbit.
3. Inclination of the orbit.
4. Longitude of the ascending node.
5. Argument of perihelion.
6. True anomaly.

## Input

The input data consists of:
- Time of each observation.
- Right ascension.
- Declination of the asteroid.
- Position and velocity vectors relative to Earth.

The data is read from a CSV file named 'data.csv'.

```python
import csv

with open('data.csv', newline='') as f:
    reader = csv.reader(f)
    data = list(reader)
```

## Observations

The program organizes the data into three different observations: `obs1`, `obs2`, and `obs3`.

## Time and Position Calculations

The program calculates time intervals between observations and utilizes various functions to extract necessary parameters, including right ascension, declination, position vectors, and velocity vectors.

## Lagrange Coefficients and Scalar Triple Product

Lagrange coefficients are computed to further calculate the scalar triple product. Cross products and dot products of observational unit direction vectors are also determined.

## Scalar Distance Polynomial and Newton-Raphson Method

The program uses the scalar distance polynomial coefficients and applies the Newton-Raphson method to find the value of `r2`, a key parameter in the calculations.

## Orbiting Body Position and Velocity

The slant range, position vectors, and velocity vectors are computed based on the calculated parameters.

## Orbital Elements

The six orbital elements are determined, including the type of the orbit (circle, ellipse, parabola, or hyperbola). The calculations are demonstrated for two different values of `r2`.

```python
# when r2 = 14.388
elements(r[2],v2)
# when r2 = -14.388
elements(r[2],v2)
```

## Results

The program provides valuable insights into the orbit of the asteroid, offering information about its trajectory in space.
For more details check out our presentation: https://www.canva.com/design/DAFUFEJcrU8/nUCFLJw92gY8-XuoPJNKsQ/edit?utm_content=DAFUFEJcrU8&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
Feel free to explore and contribute to this project for further enhancements and understanding of orbital mechanics.
