# Unscented Kalman Filter Project 
Self-Driving Car Engineer Nanodegree Program

In this project I utilize an Unscented Kalman Filter to estimate the state of a moving object of interest with noisy lidar and radar measurements. Passing the project required obtaining RMSE values that are lower that the tolerance outlined in the project rubric (RMSE <= [.09, .10, .40, .30]) 

# Tuning the parameters
Before implementing NIS I tuned the two process noise parameters by hand. I found that by setting the standard deviation for the longitudinal acceleration to 2 m/s^2 and for the yaw acceleration to 0.4 rad/s^2 the filter can pass the RMSE requirements.

# Results

## Using only radar measurements
![Radar only](radar_only.jpg)

## Using only laser measurements
![Laser only](laser_only.jpg)

## Fusing both sensor measurements
![Fused](sensor_fusion.jpg)

# Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF` Previous versions use i/o from text files.  The current state uses i/o
from the simulator.

