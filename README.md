# uav-forest

Task: Build and experiment with an open source platform for UAV mounted LIDARs

### LIDAR SELECTION:

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

### TESTED MID-40 ROS BAGS
ROSBAGs and ROS packages taken from [here](https://github.com/hku-mars/loam_livox)

Note: Check Ceres-solver and PCL dependencies
![ROS BAG](/MID-40%20%20ROS%20BAG.png)


### UAV SELECTION

UAV's considered

- DJI Matrice 100, 200 and 600
- Custom Drone

### PARTS FOR DRONE

//TODO
