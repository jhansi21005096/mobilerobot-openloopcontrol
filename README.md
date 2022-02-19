# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Initiate the MobileRobot.
<br/>

Step2:
Connect your PC with the MobileRobot.
<br/>

Step3:
Open Python program.
<br/>

Step4:
Program the movements of the robot using python code.
<br/>

Step5:
Execute the python program.
<br/>

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=45, xy_speed=0.25).wait_for_completed()
    ep_chassis.move(x=0, y=-0.25, z=0, xy_speed=0.25).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.drive_speed(x=0.4,y=0,z=-20)
    time.sleep(12)
    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.drive_speed(x=0.4,y=0,z=-20)
    time.sleep(10)
    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here
![mobilerobot movement image](https://user-images.githubusercontent.com/94458641/154787427-ad863206-8794-42b5-b858-2da39b308861.jpeg)


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
https://youtube.com/shorts/VA9wJcm6lps?feature=share<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
