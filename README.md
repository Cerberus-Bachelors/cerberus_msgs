# Custom messages for Cerberus
This Repository contains the custom messages for cerberus.

## Messages
The messages included:
* CerberusObservationTensor - Contains data needed for the inference model [cerberus_controller](https://github.com/Cerberus-Bachelors/Control)
    - geometry_msgs/Vector3 lin_acc ---- Linear acceleration
    - geometry_msgs/Vector3 ang_vel ---- Angular velocity
    - geometry_msgs/Vector3 proj_grav ---- Projected Gravity
    - geometry_msgs/Vector3 command ---- Command input
    - float64[] joint_pos ---- Current joint positions
    - float64[] joint_vel ---- Current joint positions
    - float64[] actions ---- Previous Actions
* SensorData - Contains the sensor data supplied by the ESP32
    - float32 accel_x ---- Acceleration along x
    - float32 accel_y ---- Acceleration along y
    - float32 accel_z ---- Acceleration along z
    - float32 gyro_x ---- Angular velocity around x
    - float32 gyro_y ---- Angular velocity around y
    - float32 gyro_z ---- Angular velocity around z
    - float32 heading ---- Heading angle
    - float32 latitude ---- current latitude
    - float32 longitude ---- current longitude
    - float32 altitude ---- current altitude
* EspCommands - Contains the command values for the ESP32
    - bool calibrate ---- Calibration flag
    - bool startup ---- Startup flag
    - bool shutdown ---- Shutdown flag
* JogCommand - Contains the group name and position to set groups of joints at a time.
    - string group_name ---- Group to be controlled e.g: "Hip"
    - float32 position ---- position the group should move to