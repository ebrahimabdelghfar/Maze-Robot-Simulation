# Maze-Robot-Simulation
# Dependencies 
 * ROS noetic
 * git tools
 ``` sudo apt install git-all```
# Requirments
  * Create workspace <br>
    ```
       mkdir <name_of_folder>
       cd <name_of_folder> && git clone https://github.com/ebrahimabdelghfar/Maze-Robot-Simulation.git
       catkin_make
    ```
  * install Coppeliasim </br>
    1- Download the simulator from this link https://www.coppeliarobotics.com/downloads **download the edu version** </br>
    2- Extract the simulator </br>
     ```
       cd /<download_location> 
       tar -xvf <name_of_file>.tar.xz
     ```
     3- copy the file **libv_repExtRosVelodyne.so** to the coppeliasim extracted folder </br>
   * Run Coppeliasim
     ```
     roscore # wait untill become stable *In first terminal*
     cd <coppeliasim_folder> #In second terminal
     ./coppeliaSim.sh
     ``` 
   * Open open scene
   1. Click on file in coppeliasim window
   2. Click **open scene**
   3. Go to your workspace
   4. Open src/Vrep_model/models
   5. Click on simulation_environment.ttt
   * Run simulation
   1. click on play icon
  # Sensors
   ## Robot sensors
   * Velodyne VLP-16  
   * GPS **robot C.G Position "x,y,z"** 
   * Gyro **robot C.G Orientation "alpha,beta,gamma"**  
   ## Arm Sensors
   * Accelerometer 
   * Gyro
  # Topics and Messages
  ## Acutation topics
  ```
  # all in **degree/sec**
  /rear/left_motor       #this topic is used to publish joint velocity for rear left motor "std_msgs/Float64" 
  /rear/right_motor      #this topic is used to publish joint velocity for rear right motor "std_msgs/Float64"
  /front/right_motor     #this topic is used to publish joint velocity for front right motor "std_msgs/Float64"
  /front/left_motor      #this topic is used to publish joint velocity for front left motor "std_msgs/Float64"
  ```
  ## Sensors Topics
  ```
  # Robot sensors 
  /velodyne_points #this topic published lidar pointclouds "sensor_msgs/PointCloud2"
  /gps  #this topic position of robot's CG publish list [x,y,z] in **meter** with message type "std_msgs/Float64MultiArray"
  /gyro #this topic orientation of robot's CG in euler angles publish list [alpha,beta,gamma] in **rad** with message type "std_msgs/Float64MultiArray" 
  /camera/rgb_image #this topic publish Image from monocular camera with message type "sensor_msgs/Image"
  # Arm sensor 
  /arm/gyro #this topic orientation of arms's CG in euler angles publish list [alpha,beta,gamma] in **rad** with message type "std_msgs/Float64MultiArray" 
  ```
  # Paltform used
  ![image](https://user-images.githubusercontent.com/81301684/193398603-c2f7f773-95bc-49f3-a321-3390dd1755c1.png)![image](https://user-images.githubusercontent.com/81301684/193398736-8fa86e1d-3fd1-4f9d-97d8-942e489f7c8c.png) 
  # Simulation screenshots
  ![Screenshot from 2022-10-01 09-48-32](https://user-images.githubusercontent.com/81301684/193399863-19ef6df9-b6a0-4ac1-9cd4-5b4a87091802.png)
![Screenshot from 2022-10-01 09-48-13](https://user-images.githubusercontent.com/81301684/193399868-14c288dd-bdd6-4931-b612-97c53775ecc3.png)
![Screenshot from 2022-10-01 12-02-43](https://user-images.githubusercontent.com/81301684/193404090-0d2ae2e7-89fd-44c2-9551-ba8e58cd4a88.png)

