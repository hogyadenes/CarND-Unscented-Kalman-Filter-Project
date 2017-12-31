# Unscented Kalman Filter Project 
Self-Driving Car Engineer Nanodegree Program

In this project I utilize an Unscented Kalman Filter to estimate the state of a moving object of interest with noisy lidar and radar measurements. Passing the project required obtaining RMSE values that are lower that the tolerance outlined in the project rubric (RMSE <= [.09, .10, .40, .30]) 

# Tuning the parameters
Before implementing NIS I tuned the two process noise parameters by hand. I found that by setting the standard deviation for the longitudinal acceleration to 2 m/s^2 and for the yaw acceleration to 0.4 rad/s^2 the filter can pass the RMSE requirements.

The NIS-test also confirmed these parameters - the following NIS values are calculated after each update step (laser and radar). They are below 7.83 most of the time which seems just about right.
 7.96866
 2.16449
 0.435831
 0.230976
 4.32185
 1.56521
 1.53546
 0.695062
 2.40115
 2.76545
 0.669788
 8.79073
 2.68135
 0.240752
 1.03491
 6.56525
 2.288
 3.76084
 0.903464
 2.47296
 1.31782
 6.12601
 4.02207
 1.6094
 6.77319
 2.2759
 0.75624

# Results

## Using only radar measurements
![Radar only](radar_only.jpg)

## Using only laser measurements
![Laser only](laser_only.jpg)

## Fusing both sensor measurements
![Fused](sensor_fusion.jpg)

So radar is better than laser but it is best to use both measurements.

# Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF` Previous versions use i/o from text files.  The current state uses i/o
from the simulator.

