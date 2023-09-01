# EmbodiedExercise-Kyle

Original by Kyle Xu , with code from Amos (?)

---

# Instructions


TODO: Need to replicate (Docker?)
TODO: Need to clean-up

## Materials
1. Need usb webcam
2. External monitor
3. Give sensor POLAR varity sensor to user, turn on.
	- If changed, we need to change the mac adress test.py, can be found in bluetooth settings. 

## Running
4 files on github

1. Initiate the one with flasks (acts as a server)
2. Run choreographe, connect to Pepper
3. Make sure that Pepper and computer are connected to the same network (i.e. wifi)
4. In a terminal window, run `Python3.8 app.py`
	1. Copy internet address (IP to test.py) and paste to replace all mentions to url
	2. Copy also to `Arm_angle3.py`
	3. Adjust age of user in test.py
	4. Adjust data directory to record data to and csv filename.
5. In a separate terminal, run  `test.py` -> This records everything, but starts with the heartrate.
	1. Check port of the usb camera. 

Closing app.py will stop everything.

To start a new session, start from fresh terminals


## Libraries

List included now in scripts

Flask
Bluepy

cv2
mediapipe
numpy




 
