# MOBILE ROBOTICS - OPEN LOOP CONTROL
## Developed by : G.SINDHU PRIYA REDDY
## Register No. : 212224040319


## Aim:
To develop a python control code to move the mobilerobot along the predefined path.



## Equipments Required:
1. RoboMaster EP core
2. Python 3.7
 
## Procedure
### STEP 1 :
Use from robomaster import robot
### STEP 2 :
Choose the x,y,z - axis movement distance(meters).
### STEP 3 :
Give ep_chassis.move to move straight.
### STEP 4:
Give time.sleep() for a break.
### STEP 5:
Give ep_chassis.drive_speed to have a circular movement.




## Program

```

## Developed by : G.SINDHU PRIYA REDDY
## Register No. : 212224040319

from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

   from robomaster import robot
from robomaster import camera
import time

if _name_ == '_main_':
    # Initialize robot connection
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    # Get robot modules
    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started...")
    ep_camera.start_video_stream(display=True, resolution=camera.STREAM_360P)

    # Movement and LED sequence
    sequence = [
        (0.7, 0, 0),
        (0, 0, 30),
        (0.5, 0, 0),
        (0, 0, 30),
        (0.3, 0, 0),
        (0, 0, 15),
        (0.3, 0, 0),
        (0, 0, 12),
        (0.8, 0, 0),
        (0, 0, 12),
        (0.2, 0, -10),
        (0,0,-30),
        (1.4,0,0),
        (0,0,35),
        (0.6,0,0),
        (0, 0, 35),
        (0.8,0,0),
        (0,0,5),
        (0.9,0,0),
        (0,0,10),
        (0.7,0,0),
        (0,0,20),
        (0.8,0,0),
        (0,0,10),
        (0.8,0,0),
        (0,0,45),
        (0.5,0,0),
        (0,0,30),
        (0.6,0,0),
        (0,0,28),
        (1.1,0,0),
        (0,0,25),
        (0.5,0,0),
        (0,0,20),
        (0.8,0,0),
        (0,0,-25),
        (0.4,0,0),
        (0,0,-30),
        (0.6,0,0),
        (0,0,-20),

        (0.7,0,0),

        (0,0,30),
        (0.4,0,0),
        (0,0,40),
        (0.4,0,0),
        (0,0,10),
        (0.4,0,0),

    ]

    for (x, y, z) in sequence:
        ep_chassis.move(x=x, y=y, z=z, xy_speed=1.1).wait_for_completed()
        ep_led.set_led(comp="all", r=255, g=100, b=0, effect="on")

    # Stop camera and close connection
    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming...")

    ep_robot.close()



    
    ep_robot.close()


```


## MobileRobot Movement Image:
<img width="827" alt="image" src="https://github.com/gauthamkrishna7/mobilerobot-openloopcontrol/assets/141175025/886ad367-4566-495a-86d2-702ace7b8c2d">

## MobileRobot Movement Video:
https://youtu.be/hciCJp1ADlU?si=WU_N21qmroxDc_ey
## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
