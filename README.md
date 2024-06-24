# Embodied Exercise with Socially Assistive Robots

# Overview
This project is based on our research paper titled `Embodied Exercise with Socially Assistive Robots`. The project aims to enhance physical exercise adherence and performance among older adults using a feedback system composed of wearable sensors, a socially assistive robot, a camera, and a screen-based graphical user interface.

---
# System Architecture
The feedback system is composed of four hardware modules:

- **Wearable Sensor**: The Polar Verity Sense sensor is attached to the participant’s lower arm, connected wirelessly to the server via Bluetooth to monitor the user's heart rate in real-time.
- **Socially Assistive Robot**: The NAO and PEPPER robots serve as exercise instructors, providing verbal feedback and demonstrating exercises.
- **Camera**: A Logitech BCC950 ConferenceCam is used to track the user's body kinematics, providing real-time joint angle data.
- **Screen and GUI**: Displays real-time information including the number of completed movements, heart rate, and a mirror image of the participant with emphasized joints.

---
# How to Use the System

## Materials
1. USB webcam
2. A external monitor must be plugged in
3. The POLAR varity sensor, worn by the user. It must be worn, added on Bluetooth devices and turned on.
	- If changed, we need to change the mac adress test.py, can be found in bluetooth settings.
4. The Pepper robot, connected **only** via WiFi. Say "Open settings" to check for connected network. 

## Running

1. **Connection**
	- Run ```Python3.8 01_flask_server.py```. This will start the flask server. Make note of the *IP address for mediapipe communication* (Final "Running on http://**IP**:5000"). If the Pepper its connected, it will also output its IP address
	- Run choreographe, connect to only Pepper via WiFi, make note of the _IP to Pepper_.

2. **Update IP addresses**
	- Open the file "02_kinematics_visuals.py" and update ```mediapipe_url``` with the above value. ```Video_port``` corresponds to the webcam, with 0 being the laptop default one. This might need to be changed if multiple cams are connected, but 1 or 2 are usually correct.
 	- On Choreographe, open the file PepperExerciseRoutine.pml and double click the only block (testpepper) to open the code editor. Update ```pepper_url``` and ```mediapipe_url```.
	- If testing, adjust data of user in "03_record_user.py".  Adjust data directory to record data to and csv filename.
	
3. **Running**
 	- Run `Python3.8 02_kinematics_visuals.py`. A blue window should open.
 	- On Choreographe, press the play button. This will start the activity and video on the window.   
	- Run `Python3.8 03_record_user.py`
	- Stopping The terminal runnin ```01_flask_server.py``` will stop everything.

To start a new session, start from fresh terminals

### Performing Exercises:

Follow the verbal instructions provided by the robot.
Perform the exercises as demonstrated.
You can say "Stop" to end the session, or "Pause" and "Continue" to interrupt and resume the exercises.

- Single Arm Forward Fold: Flex one arm at the shoulder and elbow until parallel to the ground, then return to the original position.
- Both Arms Forward Fold: Flex both arms at the shoulder and elbow simultaneously until parallel to the ground, then return.
- Arms Raised: Lift both arms from the sides until fully perpendicular to the ground, then return to the rest position.




---


## Requisites

List included now in scripts

```
pip install requests requests-unixsocket bluepy flask mediapipe numpy cv2
```


# Citing this work

If you use this repository in your research, please cite the following:

```
@software{KyleXu2024_ExerciseFeedback,
author = {Kyle Xu and Emanuel, Nunez Sardinha and Mohammadhadi Sarajchi and Maria Paula, Insuasty Pineda and Marcela, Munera and Carlos Cifuentes },
doi = {pending},
month = june,
title = {{Real-Time Feedback on Older Adults Exercise: A Socially Assistive Robot Coaching System}},
url = {https://github.com/Assistive-Robotics-Lab/EmbodiedExercise-Kyle},
version = {1.0},
year = {2024}
}
```

# EmbodiedExercise-Kyle

Original by Kyle Xu , cleaned up by Emanuel Nunez



 
