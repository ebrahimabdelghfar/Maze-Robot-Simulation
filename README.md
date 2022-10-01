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
   
  # Sensors
   ## Robot sensors
   * Velodyne VLP-16  
   * GPS **robot C.G Position "x,y,z" ** 
   * Gyro **robot C.G Orientation "alpha,beta,gamma"**  
   ## Arm Sensors
   * Accelerometer 
   * Gyro
  # Topics and Messages
  ## Acutation topics
  ```
  /rear/left_motor       #this topic is used to publish joint velocity for rear left motor "std_msgs/Float64" 
  /rear/right_motor      #this topic is used to publish joint velocity for rear right motor "std_msgs/Float64"
  /front/right_motor     #this topic is used to publish joint velocity for front right motor "std_msgs/Float64"
  /front/left_motor      #this topic is used to publish joint velocity for front left motor "std_msgs/Float64"
  ```
  ## Sensors Topics
  ```
  /velodyne_points #this topic published lidar pointclouds ""

   
   
   
  
