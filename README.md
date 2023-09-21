# EmbodiedExercise-Kyle

Original by Kyle Xu , with code from Amos (?)

---

# Instructions


TODO: Need to replicate (Docker?)
TODO: Need to clean-up

# Materials
1. USB webcam
2. A external monitor must be plugged in
3. The POLAR varity sensor, worn by the user. It must be worn, added on Bluetooth devices and turned on.
	- If changed, we need to change the mac adress test.py, can be found in bluetooth settings.
4. The Pepper robot, connected **only** via WiFi. Say "Open settings" to check for connected network. 

# Running

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

## Libraries

List included now in scripts

pip install requests requests-unixsocket bluepy flask mediapipe

%numpy 
%cv2




 
