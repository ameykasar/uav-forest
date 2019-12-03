# uav-forest

Task: Build and experiment with an open source platform for UAV mounted LIDARs

## LIDAR SELECTION:

Following LIDARs were considered
- LIVOX MID-40
  - $600
  - Good range (130 m @ 20% reflectivity)
  - Small circular FOV (38.4° Circular (Mid-40))
  - High integration time (around 1s to cover 93% FOV)
  - 100,000 points/s
  - Weight 760g
  
- LIVOX MID-100
  - Just three MID-40s attached to each other
  - $1600
  - Good range (130 m @ 20% reflectivity)
  - Wide FOV 98.4° (Horizontal) × 38.4° (Vertical) (Mid-100)
  - High integration time (1s to cover 93% FOV)
  - 300,000 points/s
  - Weight 2200 g

- LIVOX HORIZON
  - In prototype. Not for sale right now
  - Good range 130 m @ 20% reflectivity
  - FOV 81.7° (Horizontal) ×25.1° (Vertical)
  - Lower integration time(0.2s to cover 85% FOV)
  - 240,000 points/s
  - Weight 950g

### Chose LIVOX Horizon for low integration time and better FOV/weight

## TESTED MID-40 ROS BAGS
ROSBAGs and ROS packages taken from [here](https://github.com/hku-mars/loam_livox)

These do not include any external odometry data. It uses [LOAM](http://www.roboticsproceedings.org/rss10/p07.pdf) (LIDAR Odometry And Mapping) to compute odometry using feature extraction from real time LIDAR data.

Note: Check Ceres-solver and PCL dependencies before running packages.
![ROS BAG](/MID-40%20%20ROS%20BAG.png)


## UAV SELECTION

UAV's considered

- DJI Matrice 100, 200 and 600
## Custom Drone
Requirements:
 - Thrust to weight ratio of 2:1
 - 30 min flight time
### Drone Frames Considered
 - Tarot 650 Sport Quadcopter
 - Tarot X4 Quadcopter
 - Tarot T960
 - LynxMotion HQuad500
### Choose Tarot 650 Sport Quadcopter with following Config
This config will give approx 3kg thrust per arm. Comes around to almost 12kg AUW.
 - 4 x Tarot 5008-340kV brushless motor
 - 2 x Tarot 1855 Propellers set
 - 4 x Hobbywing XRotor 40A-OPTO ESC
 - Pixhawk 2 (Cube)
 - Herelink HD Video Transission System
 - GPS/RTK CUAV C-RTK (Support for PX4)
 - ~20000mAh 6S LiPo Battery Pack
 
Calculation for weight
 - Battery 2.5kg
 - Frame 0.75kg
 - Motors 0.88kg
 - Horizon 0.950kg
 - Pixhawk, GPS, Herelink, ESC, Wiring etc upperbound ~1kg
 Total ~ 6kg
 Payload if we use commercial drone: 0.95kg horizon + ~100g (raspberry pi or gps/rtk etc) = ~1.15kg. 

## PARTS FOR DRONE

- Designed LIDAR mount for drone using Autodesk
 Fusion 360
- Mount designed specifically for the LIVOX Horizon
STL file  [here](https://drive.google.com/file/d/1VtJUtXA3kpb0fzF0VgNHmB1ww9s7paSR/view?usp=sharing)
![LIDAR MOUNT](/lidarmount.png)
