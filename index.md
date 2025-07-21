# Ball Tracking Robot
The ball-tracking robot is a motor-driven robot that can track a ball. It is controlled by the Raspberry Pi, which I can use to send instructions to other components. The robot can track any red objects using contour detection and masks to isolate the ball. Additionally, I made the robot capable of avoiding any obstacles in its path to the ball.
 
<!--HTML You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Samvit K | Lynbrook | Electrical Engineering | Incoming Freshman

<img width="610" height="531" alt="Screenshot 2025-07-17 at 9 35 22 AM" src="https://github.com/user-attachments/assets/0bdc167e-f54b-46a2-bde1-596707539152" />

# Modification 1 
## Summary
This modification allows my ball-tracking robot to avoid any obstacles in its path to the ball. This modification uses ultrasonic sensors to detect the distance of the closest object from the robot. Here's how my ultrasonic sensors work: they send out pulses of sound that we cannot hear, and detect the distance of the nearest object by measuring the time it takes for the echo to return and dividing it by the speed of sound. I use three of these ultrasonic sensors to find out if there are any objects other than the ball in the robot's path. If there is an object, I avoid it by using code to move around the obstacle.

Here is a schematic of how I connected the ultrasonic sensors to my Raspberry Pi 4:

<img width="911" height="589" alt="Screenshot 2025-07-18 at 12 15 44 PM" src="https://github.com/user-attachments/assets/84d66737-a6b7-42ab-8c5e-a8e993c1fae0" />

### Figure 7 Ultrasonic Sensors Schematic

In addition to the ultrasonic sensors, I added a breadboard, which allows me to organise my wiring and easily connect the ultrasonic sensors to the Raspberry Pi. I also added a case for my ball-tracking robot, so it looks cleaner. The case is shown covering the components in the final picture.

Here is the schematic of the case I built:

<img width="872" height="565" alt="Screenshot 2025-07-18 at 12 02 47 PM" src="https://github.com/user-attachments/assets/7cad591b-2d67-45ce-960c-2e50e94f8c45" />

### Figure 6: Drawing of the Case

## Challenges
In this modification, I faced many unexpected challenges. Out of them, two challenges stood out to me:

1. The first challenge was that the Ball Tracking Robot kept moving too far in one direction. To fix this problem, I had to juggle around with my code and ensure my robot stopped moving after it fulfilled a certain goal. This challenge took me the longest amount of time, but I fixed the code.

2. The second challenge that stood out to me was a bit of a setback. The setback was that my Raspberry Pi board stopped working. The reason is unknown, but I had to restart setting up the board. This required me to rewire many things and forced me to repeat the downloading process. The downloading took a long time, forcing me to waste a day at Bluestamp setting up my Pi.

## Here's a demo of my Ball Tracking Robot

## Here's my video explaining how it works.

# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/pGrgtaH59r0?si=6CvAePYxslzJZh-u" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!--Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```-->

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```-->

<!--```For your final milestone, explain the outcome of your project. Key details to include are:```-->
<!--```- What you've accomplished since your previous milestone```-->
<!--```- What your biggest challenges and triumphs were at BSE```-->
<!--```- A summary of key topics you learned about```-->
<!--```- What you hope to learn in the future after everything you've learned at BSE ```-->
## Summary
For my final milestone, my ball-tracking robot can now track and follow the ball. For this milestone, I had to write code using Python in Visual Studio Code that would be able to follow the ball. This code tracks whether the ball is to the left or right of the robot and then follows it. Here's how my code works:

<img width="872" height="492" alt="Screenshot 2025-07-10 at 11 58 31 AM" src="https://github.com/user-attachments/assets/324eb8c7-726c-4ed5-a1c0-e0e195f75dd8" />

### Figure 5: Diagram of How the Code Works

## Chalenges
A challenge I faced was that my robot kept turning left and right, which sometimes led to the ball-tracking robot hitting the ball off the table. I fixed this problem by making the code first turn left/right. Once it was in position, it would turn forward. However, other than that, there were no major setbacks, unlike my other milestones, and it was quick compared to the other two. This was because most of the code was from the other milestones, and the only code I wrote was for the ball-following system.

## What I learned through the milestones:
I learned a lot from BSE, including the basics of circuits, to setting up masks and contours for ball tracking. Here's a list of the few things I learned from BSE:
1. I learned the basics of circuits, such as the power source and ground. I learned the different types of wires and how to solder them to the circuit board. I also learned Ohm's Law, which states that Current is equal to Voltage over Resistance.
2. I learned about how to control DC motors with the L298N motor driver and how to control pins using the Raspberry Pi 4.
3. I learned how to use the Picam and software like OpenCV to complete tasks like ball detection.
4. I also learned about ultrasonic sensors, which I use in modification 1. I learned how to connect the ultrasonic sensor to breadboards, which are used to organize circuits.
5. At Bluestamp, I learned how to find code, how to connect it to physical components, and how to make a lot of components work together to accomplish a task.
   
## Next Steps
My next steps would be to add a modification to my Ball Tracking Robot. This modification would involve adding obstacle-avoiding code. I plan to use ultrasonic sensors to achieve this goal by measuring the distance between any obstacles and the robot. One challenge I may face is confusing the ball with an obstacle. After BlueStamp Engineering, I plan to join the robotics team and hope to learn more and gain more experience in all aspects of engineering.

# Second Milestone
## Summary
For my second milestone, my objective was to create code that would allow my robot to track my red ball. This required many steps and some code using libraries such as OpenCV. Unlike the first milestone, which required barely any code, the second milestone was focused on coding. Here's how my code works:
1. Import important libraries such as picamera2 for easy access to my camera, which is the picamera.
2. Second, I had to set up my camera's format, configure it, and start the camera.
3. Third, I had to convert the original BGR (Blue, Green, Red) to HSV (Hue, Saturation, Value) colour space because using an HSV colour space makes isolating a certain colour for ball tracking easier.
4. Fourth, I had to create a mask. A mask allows me to isolate a certain colour, for example, red. This is useful for me because I need to isolate red to track my red ball. A mask blackens out everything that is not within a certain colour range. Here's a picture of the mask in action:

<img width="1223" alt="Screenshot 2025-07-07 at 9 53 15 AM" src="https://github.com/user-attachments/assets/a3513fde-9e06-47e6-95a4-ef2e3dcf9b55" />

### Figure 4 Picture of the Picam Using A Mask

5. Fifth, I had to create contours, which are edges that are detected by the computer. These edges are identified by noticing the sudden colour change. For example, the computer can detect the contours around my ball that is on top of a black table by noticing the sudden change from red to black. This sudden change informs the computer that there is a contour. This contour is useful to me because I can find the specific coordinates of the ball by averaging the contour points. Here's a picture of the contours shown as green points:

   <img width="1256" alt="Screenshot 2025-07-07 at 9 55 16 AM" src="https://github.com/user-attachments/assets/52e43df9-cddf-472b-a6d8-092fc1434a11" />

### Figure 3 Picture of the Picam Using Contour Detection
## Milestone 2 Video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/h3WfutsooX8?si=DJW7ErF61s7oUL5d" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Next Steps:
For my next steps, I will need to work on my third milestone, which allows the ball-tracking robot to move towards the ball while avoiding any obstacles in its way. This will be my last milestone unless I add any modifications. I will achieve this goal by using the coordinates I obtained from the second milestone to determine if the ball is to the right or left of the robot.

## Challenges:
A major challenge I faced was getting the code to work. I had to change the code a lot because sometimes the colour space wasn't being changed, and sometimes the colour range was not quite right. However, I was able to create code that works, as shown below.
<!--
```**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```

<!--```For your second milestone, explain what you've worked on since your previous milestone. You can highlight:```
<!--```- Technical details of what you've accomplished and how they contribute to the final goal```
<!--```- What has been surprising about the project so far```
<!--```- Previous challenges you faced that you overcame```
v```- What needs to be completed before your final milestone ```
-->
# First Milestone
## Summary
For my first milestone, I used Python to move the Ball Tracking Robot forward and backwards using motors. Reaching this goal took a couple of steps:

1. My first step was to set up my Raspberry Pi 4. The goal of this step was to connect to the Pi remotely without connecting it to my computer with a lot of wires. This step made me follow a lot of the instructions provided by Blue Stamp Engineering. I was sometimes confused about which wires went where; however, it was relatively easy.
2. My second step was to build the base of my robot, which came in a small kit including a plastic base, two motors, two large wheels, one small rotating wheel, and a battery source. This also came with instructions, giving me small steps to build it.
3. My third step was to wire everything together. I had to wire the L298N motor with the Raspberry Pi 4, which allowed me to program instructions that get sent by the Pi. I also had to connect the L298N driving motor to the two motors in my base. This required some soldering, which I had some unexpected difficulties with.
4. My final step was to write some simple code that tested the functionality of my motors. This code was mostly from viewing and understanding previous Blue Stamp Engineering students who had done the same project as I. After a few minor mistakes, I successfully made my motors run, thus finishing my first milestone.

The Raspberry Pi 4 is a mini-computer that is powered by a USB-C source. Powering it allows me to run code through the Raspberry Pi, enabling me to control other components on the Ball Tracking Robot. The L298N is a driving motor powered by five 1.5-volt batteries. The driving motor gets its power through the VS and ground pin and outputs instructions to the motor from Output 1-4. The driving motor receives instructions from the Raspberry Pi 4 from pins: ENA, ENB, and IN 1-4. The inputs receive code that controls the direction of the motor, and the ENA and ENB pins receive code that controls the speed of the motors.

Another component in the L298N Driving Motor is the H-Bridge, which is a fascinating system that allows the driving motor to control direction.

<img width="652" height="352" alt="Screenshot 2025-07-17 at 10 20 10 AM" src="https://github.com/user-attachments/assets/62b3cb7c-24a1-4029-be90-299fa89fb447" />
### Figure 2: Diagram of the L298N Driving Motor

As you can see in the diagram, there are 4 switches, one GND, and one VCC. The power comes from the VCC, and if the top right and bottom left switches are on, the power flows in a counter-clockwise direction, making the motors spin in the same direction. However, if the top left and bottom right switches are on, the power flows in a clockwise direction, also making the motors spin in the same direction. This allows the L298N motor to control the direction of the motor.

<img width="942" alt="Screenshot 2025-07-07 at 11 58 07 AM" src="https://github.com/user-attachments/assets/7599743f-4bbe-407f-a6cb-58e955000324" />
### Figure 1 Schematic of the Motors

## Challenges:
Some challenges I faced were that my motor was not working because I mistakenly put the L298N power source into the VSS instead of the VS, which limited the power supply received, resulting in the motor not working. Another challenge I faced was that some of the wires that connected the L298N outputs to the motors broke off, which required me to resolder some of the wires. One problem that stood out to me was my SSH (a way of remotely coding onto my Raspberry Pi 4 without wires) disconnected many times. This stood out to me because I could not find a solution to this.

## My Next Steps:
My next goal is to finish milestone 2. Completing this milestone will allow me to track the ball, which is essential for my Ball Tracking Robot. To complete milestone 2, I will have to use a PiCamera (a camera attachable to my Raspberry Pi) and OpenCV software. I will need to create a mask; a mask allows me to only see objects in a certain range of colours. This will enable me to track my ball because the mask will be in the same colour range as my ball, which makes the ball one of the only objects visible to my PiCamera.

<!--```**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```

<!--For your first milestone, describe what your project is and how you plan to build it. You can include:```
<!--```- An explanation about the different components of your project and how they will all integrate together```
<!--```- Technical progress you've made so far```
<!--```- Challenges you're facing and solving in your future milestones```
<!--- What your plan is to complete your project```-->

# Schematics 
## Schematic for Ultrasonic Sensors:
<img width="911" height="589" alt="Screenshot 2025-07-18 at 12 15 44 PM" src="https://github.com/user-attachments/assets/84d66737-a6b7-42ab-8c5e-a8e993c1fae0" />

## Schematic for L298N Driving Motor:
<img width="942" alt="Screenshot 2025-07-07 at 11 58 07 AM" src="https://github.com/user-attachments/assets/7599743f-4bbe-407f-a6cb-58e955000324" />

# Code
## Final Code (For Modification 1)
```
# Importing Necessary Software
import picamera2
from time import sleep
import os
import cv2
import numpy as np
from picamera2 import Picamera2
import  RPi.GPIO as GPIO
import time
from gpiozero import DistanceSensor, Motor
GPIO.setmode(GPIO.BOARD)

# Giving Names to each of the Ultrasonic Sensors
ultrasonic_left = DistanceSensor(echo=17, trigger=4)
ultrasonic_front = DistanceSensor(echo=9, trigger=10)
ultrasonic_right = DistanceSensor(echo=22, trigger=27)

# Giving Names to the motors, and the numbers are the pins on the Raspberry Pi
# that the motors are connected to
motor_left = Motor(forward=23,backward=24)
motor_right = Motor(forward=26,backward=16)

# Allowing the Ultrasonic Sensors to get more distance
ultrasonic_front.max_distance = 10000000
ultrasonic_front.threshold_distance = 20
ultrasonic_left.max_distance = 10000000
ultrasonic_left.threshold_distance = 20
ultrasonic_right.max_distance = 10000000
ultrasonic_right.threshold_distance = 20 
last_x = 0

# Writing functions for moving the robot, so I do not need to rewrite everything
def move_backward():
   motor_left.forward(0.5)
   motor_right.forward(0.5)
def stop_move():
   motor_left.stop()
   motor_right.stop()
def move_right():
   motor_left.backward(0.5)
   motor_right.forward(0.5)
def move_left():
   motor_left.forward(0.5)
   motor_right.backward(0.5)
def move_forward():
   motor_left.backward(0.5)
   motor_right.backward(0.5)

# Function that takes a picture, and find the coordinates of the ball
def find_ball():
   global last_x
   # Take each frame
   frame_old = cam.capture_array()
   frame = cv2.cvtColor(frame_old, cv2.COLOR_RGB2BGR)


   # Convert BGR to HSV
   hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
   # define range of red color in HSV
   lower_red = np.array([155,80,200])
   upper_red = np.array([179,255,255])
   # Threshold the HSV image to get only red    colors
   mask = cv2.inRange(hsv, lower_red, upper_red)
   kern_dilate = np.ones((8,8),np.uint8)
   kern_erode  = np.ones((3,3),np.uint8)
    
   mask = cv2.resize(mask, (320, 240)) # resize to reduce resolution/improve performance
   mask= cv2.erode(mask,kern_erode)      # erode to approximate color
   mask=cv2.dilate(mask,kern_dilate)     # dilate to blur


   #The Following Code finds the contours, or the points that surround the ball,
   #and finding the average of those, to find the center of the ball
   contours, hierarchy = cv2.findContours(mask, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
   if len(contours) != 0:
       shape = max(contours, key=cv2.contourArea)
       area = cv2.contourArea(shape)
       average_x = 0
       average_y = 0
       for n in shape:
           x= n[0][0]
           average_x += x
           y = n[0][1]
           average_y += y
       number_points = len(shape)
       x_cord = average_x/number_points
       y_cord = average_y/number_points
       #The Following Code shows what the picam is seeing
       cv2.imshow('frame',frame)
       cv2.imshow('mask',mask)
       last_x = x_cord
       return (x_cord, area)
   else:
       return (last_x, 0)
   
#setting up the camera
cam = Picamera2()
config = cam.create_video_configuration(main = {'format': 'BGR888'})
cam.configure(config)
cam.start()


# Code for obstacle avoidance modification 1
def obstacle_avoidance():
    x_cord, area = find_ball()
# I believe there are only two possible obstacles, one toward the right, or left,
    if area < 7500:
        if ultrasonic_left.distance < 0.1 or ultrasonic_right.distance < 0.1:
        
           if ultrasonic_left.distance < 0.1:
               move_right()
               while ultrasonic_front.distance < 0.125 and ultrasonic_left.distance < 0.1:
                   move_right()
               while ultrasonic_left.distance < 0.1:
                   move_right()
           if ultrasonic_right.distance < 0.1:
               move_left()
               while ultrasonic_front.distance < 0.125 and ultrasonic_right.distance < 0.1:
                   move_left()
               while ultrasonic_right.distance < 0.1:
                   move_left()
           stop_move()
        else:
            while ultrasonic_right.distance > 0.1 and ultrasonic_left.distance > 0.1:
                move()
    else:
        stop_move()

# Function for moving
def move():
       x_cord, area = find_ball()
       print(area)
       if area < 7500:
           if area == 0:
               if x_cord > 160:
                   move_left()
               else:
                   move_right()
           elif x_cord > 260 or x_cord < 60:
               print(x_cord)
               if x_cord > 260:
                   move_left()
               else:
                   move_right()
           else:
               move_forward()
       else:
           stop_move()
       return area 

while(1):
   #The follow code allows the robot to move towards the ball
    obstacle_avoidance()
cv2.destroyAllWindows()



 ```

## Ball Tracking Code for Milestone 3:

```
import picamera2 
from time import sleep
import os
import cv2
import numpy as np
from picamera2 import Picamera2
import  RPi.GPIO as GPIO
import time
from gpiozero import DistanceSensor, Motor
GPIO.setmode(GPIO.BOARD)
ultrasonic_left = DistanceSensor(echo=17, trigger=4)

ultrasonic_front = DistanceSensor(echo=9, trigger=10)

ultrasonic_right = DistanceSensor(echo=22, trigger=27)
#from gpiozero import DistanceSensor
# The following are the names of the raspberry-pi pins that control each of them
motor_left = Motor(forward=23,backward=24)
motor_right = Motor(forward=26,backward=16)

ultrasonic_front.max_distance = 10000000
ultrasonic_front.threshold_distance = 20
ultrasonic_left.max_distance = 10000000
ultrasonic_left.threshold_distance = 20
ultrasonic_right.max_distance = 10000000
ultrasonic_right.threshold_distance = 20  


def move_forward():
    motor_left.forward(0.5)
    motor_right.forward(0.5)
def stop_move():
    motor_left.stop()
    motor_right.stop()
def move_left():
    motor_left.backward(0.4)
    motor_right.forward(0.4)
def move_right():
    motor_left.forward(0.4)
    motor_right.backward(0.4)
def move_backward():
    motor_left.backward(0.75)
    motor_right.backward(0.75)


def find_ball():
    # Take each frame
    frame_old = cam.capture_array()
    frame = cv2.cvtColor(frame_old, cv2.COLOR_RGB2BGR)

    # Convert BGR to HSV
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
 
    # define range of red color in HSV
    lower_red = np.array([155,80,80])
    upper_red = np.array([179,255,255])
 
    # Threshold the HSV image to get only red    colors
    mask = cv2.inRange(hsv, lower_red, upper_red)
 
    # Bitwise-AND mask and original image
    res = cv2.bitwise_and(frame,frame, mask= mask)

    #The Following Code finds the contours, or the points that surround the ball,
    #and finding the average of those, to find the center of the ball
    contours, hierarchy = cv2.findContours(mask, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
    cv2.drawContours(frame, contours, -1, (0,255,0), 3)
    if len(contours) != 0:
        shape = max(contours, key=cv2.contourArea)
        area = cv2.contourArea(shape)
        average_x = 0
        average_y = 0
        for n in shape: 
            x= n[0][0]
            average_x += x
            y = n[0][1]
            average_y += y
        number_points = len(shape) 
        x_cord = average_x/number_points
        y_cord = average_y/number_points
        #The Following Code shows what the picam is seeing
        cv2.imshow('frame',frame)
        cv2.imshow('mask',mask)
        return (x_cord, area)
    else:
        return (0, 0)
#setting up the camera
cam = Picamera2()

config = cam.create_video_configuration(main = {'format': 'BGR888'})
cam.configure(config)
cam.start()
while(1):
    

        #The follow code allows the robot to move towards the ball
    def move():
        x_cord, area = find_ball()
        print(x_cord ,area)
        if area < 250000 and area > 0:
            if x_cord > 900 or x_cord < 400:
                print(x_cord)
                if x_cord > 840:
                    move_left()
                else:
                    move_right()
            else:
                move_forward()
        else:
            stop_move()


      
    move()

cv2.destroyAllWindows()
```
## Ball Tracking Code for Milestone 2:
```
#import important libraries
import picamera2 
from time import sleep
import os
import cv2
import numpy as np
from picamera2 import Picamera2

#setting up the camera
cam = Picamera2()

config = cam.create_video_configuration(main = {'format': 'BGR888'})
cam.configure(config)
cam.start()
while(1):
    # Take each frame
    frame_old = cam.capture_array()
    frame = cv2.cvtColor(frame_old, cv2.COLOR_RGB2BGR)

    # Convert BGR to HSV
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
 
    # define range of red color in HSV
    lower_red = np.array([155,80,80])
    upper_red = np.array([179,255,255])
 
    # Threshold the HSV image to get only red    colors
    mask = cv2.inRange(hsv, lower_red, upper_red)
 
    # Bitwise-AND mask and original image
    res = cv2.bitwise_and(frame,frame, mask= mask)
    contours, hierarchy = cv2.findContours(mask, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
    cv2.drawContours(frame, contours, -1, (0,255,0), 3)
    if len(contours) != 0:
        shape = max(contours, key=cv2.contourArea)
        average_x = 0
        average_y = 0
        for n in shape: 
            x= n[0][0]
            average_x += x
            y = n[0][1]
            average_y += y
        number_points = len(shape) 
        x_cord = average_x/number_points
        y_cord = average_y/number_points
        print(x_cord, y_cord)
    cv2.imshow('frame',frame)
    cv2.imshow('mask',mask)
    k = cv2.waitKey(5) & 0xFF
    if k == 27:
        break

cv2.destroyAllWindows()
```
## Motor Testing Code for Milestone 1:
```
#Basic Python Motor Code

import  RPi.GPIO as GPIO
import time

GPIO.setmode(GPIO.BCM) 


# The following are the names of the raspberry-pi pins that control each of them
MOTOR1B = 23
MOTOR1E = 24
MOTOR2B = 16
MOTOR2E = 26
ena = 25
enb = 12

GPIO.setup(MOTOR1B, GPIO.OUT)
GPIO.setup(MOTOR1E, GPIO.OUT)
GPIO.setup(ena, GPIO.OUT)
GPIO.setup(MOTOR2B, GPIO.OUT)
GPIO.setup(MOTOR2E, GPIO.OUT)
GPIO.setup(enb, GPIO.OUT)

pwmA = GPIO.PWM(ena, 100)
pwmB = GPIO.PWM(enb, 100)
pwmA.start(60)
pwmB.start(60)
#These move the wheels Backwards
GPIO.output(MOTOR1B,GPIO.HIGH)
GPIO.output(MOTOR1E, GPIO.LOW)
GPIO.output(MOTOR2E, GPIO.HIGH)
GPIO.output(MOTOR2B, GPIO.LOW)

time.sleep(5)


GPIO.output(MOTOR1B, GPIO.LOW)
GPIO.output(MOTOR1E, GPIO.LOW)

GPIO.output(MOTOR2B, GPIO.LOW)
GPIO.output(MOTOR2E, GPIO.LOW)
```
# Bill of Materials
<!--```Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.```
```Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. ```-->

<!--| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
-->
# Starter Project: RGB Sliders
The starter project I chose was the RGB sliders. I chose this because building these sliders will help me practice essential skills like soldering before I start my main project. There are three sliders in my project: one controlling red light, one controlling blue, and one controlling green. These LED lights are powered by a charger via the USB port located on the top right of the sliders. The three LEDs' lights blend together into one color, allowing the sliders to emit a spectrum of colors.
<iframe width="560" height="315" src="https://www.youtube.com/embed/COZAjiJK3ME?si=7rq4b5ZN2UaWGZ0Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Challenges:
A challenge I faced was that sometimes the solder spilled into another spot, creating a connection between two pins, which is a problem. To deal with this problem, I had to remove the solder, which led me to use the desoldering tool that sucked the solder out when it was in a liquid state. I soon successfully removed all the mistakes, allowing me to re-solder and complete the project. This challenge helped me master desoldering, which is beneficial if I make a mistake in any of my future projects. My next steps are to work on my main project, which is the Ball Tracking Robot. The next few steps are to build the base of the robot and add motors to allow it to move.



<!--
```
# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.-->
