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
### Tarot 650 Sport Quadcopter with following Config
This config will give approx 2.0kg thrust per arm (not full throttle). Comes around to almost 8kg AUW.
 - 690 mm
 - 4 x Tarot 4114-320kV brushless motor
 - 4 x Tarot 1555 Propellers 
 - 4 x Hobbywing XRotor 40A-OPTO ESC
 - Pixhawk 2 (Cube)
 - Herelink HD Video Transission System
 - GPS/RTK CUAV C-RTK (Support for PX4)
 - ~20000mAh 6S LiPo Battery Pack
 
 Calculation for weight
 - Battery 2.5kg
 - Frame 0.75kg
 - Motors 0.592kg
 - Horizon 0.950kg
 - Pixhawk, GPS, Herelink, ESC, Wiring etc upperbound ~1kg
 
 Total ~ 5.79kg
 
 Cost estimate for 650 Sport Quadcopter
  - Frame $270
  - Motors $200
  - Propellers $60
  - ESCs $60
  - Pixhawk cube $240
  - Herelink $800
  - RTK module $1900
  - Battery $190
 
Total $3720
 
 ### Tarot X4 Quadcopter with following Config
This config will give approx 2.25kg thrust per arm(not full throttle). Comes around to almost 9kg AUW.
Bigger props -> Slower motors -> longer flight
 - 960 mm
 - 4 x Tarot 6115-320kV brushless motor
 - 4 x Tarot 2455 Propeller
 - 4 x Hobbywing XRotor 50A Pro ESC
 - Pixhawk 2 (Cube)
 - Herelink HD Video Transission System
 - GPS/RTK CUAV C-RTK (Support for PX4)
 - ~20000mAh 6S LiPo Battery Pack
 
Calculation for weight
 - Battery 2.5kg
 - Frame 2.0kg
 - Motors 1.2kg
 - Horizon 0.950kg
 - Pixhawk, GPS, Herelink, ESC, Wiring etc upperbound ~1kg
 
Total ~ 7.65kg

Cost estimate for X4
  - Frame $450
  - Motors $400
  - Propellers $120
  - ESCs $120
  - Pixhawk cube $240
  - Herelink $800
  - RTK module $1900
  - Battery $190
 
Total $4220
 
 Tarot X4 estimated flight time with AUW 7.85kg is 27 min. ![Refer](/tarot-x4-estimate-time-6115.jpg)
 
 Payload if we use commercial drone: 0.95kg horizon + ~100g (raspberry pi or gps/rtk etc) = ~1.15kg. 

## PARTS FOR DRONE

- Designed LIDAR mount for drone using Autodesk
 Fusion 360
- Mount designed specifically for the LIVOX Horizon
STL file  [here](/https://github.com/ameykasar/uav-forest/blob/master/LIDAR%20mount.stl)
![LIDAR MOUNT](/lidarmount.png)
