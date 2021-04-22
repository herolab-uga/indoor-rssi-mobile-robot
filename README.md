# Overview

This repository contains the datasets used in particle filter localization of a fixed Wi-Fi Access Point (AP). The datasets contain robot path locations, odometry data, and RSSI measurements captured from a mobile robot with multiple receivers onboard moving in an indoor office environment. The datasets have the same structure and the data is all obtained from within the same environment. 

# Experimental setup

All data in the datasets is obtained from a 20-meter x 26-meter indoor office hall with multiple rooms. The path taken by the robot, however, is different in the datasets. The robot begins at (0, 0) in all of the datasets and the Wi-Fi AP is located at (9, 0) in every dataset. The robot obtains RSSI measurements using multiple receivers (located at the upper left, upper right, lower left, and lower right corners of the robot and the center of the robot) with directional antennae. The distance from the lower antennae to the upper antennae is 1.2 m and the distance from the right antennae to the left antennae is 1 m.  Figure 1 and 2(b) in Ref. [1] will provide an idea of how the Wi-Fi devices are setup onboard the mobile robot.
  
Below are figures displaying the paths the robot takes in the environment in datasets 1-5, sequentially. The paths for datasets 6 and 7 are not shown as the robot does not move in the x-y plane but instead spins on its axis for a period of time. The red square indicates the starting position of the robot and the green star indicates the position of the Wi-Fi AP. All axis markers are in meters.  
![dataset1 robot path](./robot_paths/dataset1.png)
![dataset2 robot path](./robot_paths/dataset2.png)
![dataset3 robot path](./robot_paths/dataset3.png)
![dataset4 robot path](./robot_paths/dataset4.png)
![dataset5 robot path](./robot_paths/dataset5.png)  

# Dataset structure

The dataset structure is similar to Ref. [2] In fact, the dataset1 in this repository is the same as in the dataset in Ref. [2].

| attribute #   | attribute name | attribute description                                     |
| ------------- | -------------  | --------------------------------------------------------- |
| 0             | temp_step      | irregular sequence count                                  |
| 1             | temp_sec       | time stamp in sec.                                        |
| 2             | temp_nsec      | time stamp in nanosec.                                    |
| 3             | robot_pos_x    | robot position (m.) on x-axis with 0 as starting position |
| 4             | robot_pos_y    | robot position (m.) on y-axis with 0 as starting position |
| 5             | robot_w_x      | part of orientation of robot in quaternion format         |
| 6             | robot_w_y      | part of orientation of robot in quaternion format         |
| 7             | robot_w_z      | part of orientation of robot in quaternion format         |
| 8             | robot_w_w      | part of orientation of robot in quaternion format         |
| 9             | theta_p        | direction (degrees) of onboard camera                     |
| 10            | UL_level*      | filtered RSSI value obtained from upper left (FL) antenna      |
| 11            | UR_level*      | filtered RSSI value obtained from upper right (FR) antenna     |
| 12            | LL_level*      | filtered RSSI value obtained from lower left (BL) antenna      |
| 13            | LR_level*      | filtered RSSI value obtained from lower right (BR) antenna     |
| 14            | C_level*       | filtered RSSI value obtained from center antenna          |
| 15            | UL_level_a     | RSSI value obtained from upper left (FL) antenna              |
| 16            | UR_level_a     | RSSI value obtained from upper right (FR) antenna              |
| 17            | LL_level_a     | RSSI value obtained from lower left (BL) antenna              |
| 18            | LR_level_a     | RSSI value obtained from lower right (BR) antenna              |
| 19            | C_level_a      | RSSI value obtained from center antenna                   |
| 20            | Feedback       | reserved for future use                                   |

*filtered RSSI values are calculated from RSSI values as described in eq. (8) of Ref. [1]:  

# Related publication

This dataset is used in the below paper. Please cite the below paper when you use this dataset repository.
**R. Parashar and R. Parasuraman, "Particle Filter Based Localization of Access Points Using Direction of Arrival on Mobile Robots". In Vehicular Technology Conference VTC-Fall 2020.** CAVVTC Workshop: https://cavvtc.weebly.com/program.html

# References

[1] S. Caccamo, R. Parasuraman, F. Båberg and P. Ögren, "Extending a UGV teleoperation FLC interface with wireless network connectivity information," 2015 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), Hamburg, 2015, pp. 4305-4312, doi: 10.1109/IROS.2015.7353987. https://ieeexplore.ieee.org/abstract/document/7353987/

[2] Parasuraman R, Caccamo S, Baberg F, Ogren P. CRAWDAD dataset kth/rss (v. 2016-01-05). https://crawdad.org/kth/rss/20160105/indoor/

# Contact

For further information, contact Ravi Parashar ravi.parashar25@uga.edu or Prof. Ramviyas Parasuraman ramviyas@uga.edu

**Heterogeneous Robotics Lab (HeRoLab), Department of Computer Science, University of Georgia.** http://hero.uga.edu 

<p align="center">
<img src="http://hero.uga.edu/wp-content/uploads/2021/04/herolab_newlogo_whitebg.png" width="300">
</p>

