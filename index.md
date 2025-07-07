# Ball Tracking Robot
The ball tracking robot, is a motor driven robot that is able to track a ball. It is able to track a red ball and is able to make it's way to the ball.

 
<!--HTML You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Samvit K | Lynbrook | Electrical Engineering | Incoming Freshman

<!--```**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**```-->

<!--![Headstone Image](logo.svg)-->
  
# Final Milestone

<!--Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```-->

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```-->

<!--```For your final milestone, explain the outcome of your project. Key details to include are:```-->
<!--```- What you've accomplished since your previous milestone```-->
<!--```- What your biggest challenges and triumphs were at BSE```-->
<!--```- A summary of key topics you learned about```-->
<!--```- What you hope to learn in the future after everything you've learned at BSE ```-->



# Second Milestone
##Summary
For my second milestone, my objective was to create code that will allow my robot to track my red ball. This required many steps and a little code using libraries such as OpenCv. Unlike the first milestone that required barely any code, the second milestone was focused on coding. Here's how my code works: 
1. Import important libraries such as picamera2, for easy access to my camera, which is the picamera.
2. Second, I had to set up my camera's format, configure and start the camera.
3. Third, I had to convert the original BGR(Blue, Green, Red) to HSV(Hue, Saturation, Value) color space, because using a HSV color space will make isolating a certain color for ball tracking easier.
4. Fourth, I had to create a mask. A mask allows me to isolate a certain color, for example red. This is usefull for me because I need to isolate red to isolate my red ball. A mask blackens out everything that is not in a certain color range. Here's a picture of the mask in action:
<img width="1223" alt="Screenshot 2025-07-07 at 9 53 15 AM" src="https://github.com/user-attachments/assets/a3513fde-9e06-47e6-95a4-ef2e3dcf9b55" />
5. Fifth, I had to create contours, which are edges that are detected by the computer. These edges are detected by noticing the sudden change of color. For example, the computer can detect the contours around my ball that is on top of a black table, by noticing the sudden change from red to black. This sudden change informs the computer that there is a contour. This contour is useful to me because I can find the certain coordinates of the ball by finding the average of the countours points. Here's a picture of the contours being shown as green points:
   <img width="1256" alt="Screenshot 2025-07-07 at 9 55 16 AM" src="https://github.com/user-attachments/assets/52e43df9-cddf-472b-a6d8-092fc1434a11" />

<!--```**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```

<!--```For your second milestone, explain what you've worked on since your previous milestone. You can highlight:```
<!--```- Technical details of what you've accomplished and how they contribute to the final goal```
<!--```- What has been surprising about the project so far```
<!--```- Previous challenges you faced that you overcame```
v```- What needs to be completed before your final milestone ```
-->
# First Milestone
## Summary
For my first milestone, I used python to move the ball tracking robot, foward and back using motors. Reaching this goal took a couple of steps:

1. My first step was to set up my Raspberry Pi 4. The goal of this step, was to connect to the pi remotely without connecting it to my computers with a lot of wires. This step made me follow a lot of instructions which was given to me by Blue Stamp Engineering. I was sometimes confused about which wires go where, however it was relatively easy. 

2. My second step was to build the base of my robot, which came in a small kit including: a plastic base, two motors, two large wheels, one small rotating wheel, and a battery source. This also came with instructions, giving me small steps to build it.

3. My third step was to wire everything together. I had to wire the the L298N motor with the Raspberry pi 4, which allowed me to program instruction that get sent by the pi. I also had to connect the L298N driving motor with the two motors in my base. This required some soldering, which I had some unexpected difficulties with.

4. My final step was to write some simple code that tested the functionality of my motors. This code was mostly from viewing and understanding previous blue stamp engineering students, who had done the same project as me. After a few minor misteps, I succesfully made my motors run, thus finished my first milestone.


The Raspberry Pi 4 is a mini-computer which is powered by the USB-C source. Powering it, allows me to run code through the Raspberry Pi allowing me to control other components on the Ball Tracking Robot. The L298N is a driving motor powered by 5, 1.5 volt batteries. The driving motor gets it's power through the VS and ground pin, and outputs instructions to the motor from Output 1-4. The driving motor recieves instructions from the Raspberry Pi 4 from pins: ENA, ENB and IN 1-4. The inputs recieve code that controls direction of the motor, and the ENA and ENB pin recieve code that controll the speed of the motors. 

Another component in the L298N Driving Motor is the H-Bridge, which is a facinating system that allows the driving motor to control direction.

## Figure 2:
![image](https://github.com/user-attachments/assets/dde94b8d-169d-482e-b49f-104f02fe6358)

Source: Last Minute Engineers

As you can see in the diagram there are 4 switches, one GND and one VCC. The power comes from the VCC, and if the top right and bottom left switch are on, the power flows in a counter-clockwise direction, making the motors spin in the same  direction. However, if the top left and bottom right switch are on, the power flows in a clockwise direction, also making the motors spin in the same direction. This allows the L298N motor control the direction of the motor.

## Figure 1:

<img width="626" alt="Screenshot 2025-07-03 at 9 02 23 AM" src="https://github.com/user-attachments/assets/ead97e49-e20a-4c3e-aaf9-73279afef4f9" />


## Challenges:
Some challenges I faced were that my motor was not working because, I mistakenly put the L298N power source into the VSS instead of the VS, which limited the power supply recieved, resulting the motor not working. Another challenge I faced was that some of the wires that connected the L298N's outputs to the motors broke off, which required me to resolder some of the wires. One problem that stood out to me was my ssh(a way of remotely coding onto my raspberry pi 4, without wires) discconected many time. This stood out to me, because I could not find a solution to this.

## My Next Steps:
My next goal is to finish milestone 2. Completing this milestone will allow me to track the ball, which is essential in my ball tracking robot. To complete milestone 2, I will have to use picamera (a camera attachible to my raspberry pi), and the open cv software. I will have to create a mask, a mask allows me to only see objects in a certain range of colors. This will be able to track my ball, because the mask will be in the same color range as my ball, which make the ball one of the only objects visiable to my picamera.

<!--```**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**```

<!--```<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>```

<!--For your first milestone, describe what your project is and how you plan to build it. You can include:```
<!--```- An explanation about the different components of your project and how they will all integrate together```
<!--```- Technical progress you've made so far```
<!--```- Challenges you're facing and solving in your future milestones```
<!--```- What your plan is to complete your project```-->

# Schematics 
<!--```Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. ```-->

# Code
<!--``` Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. ```
****
```
c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```-->
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
The starter project I chose was the RGB sliders. I chose this because building these sliders will help me practice essential skills like soldering before I start my main project. There are three sliders in my project, one controlling red light, one controlling blue, and one controlling green. These LED lights are powered by a charger via the USB port located on the top right of the sliders. The three LEDs' lights blend together into one color allowing the sliders to emmit a spectrum of colors. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/COZAjiJK3ME?si=7rq4b5ZN2UaWGZ0Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Challenges:
A chalenge I faced was that sometimes the solder sometimes spilled into another spot, creating a connection between two pins, which is a problem. To deal with this problem, I had to remove the solder. Which led me to use the desoldering tool, which sucked the solder out when the solder was at a liquid state. I soon succesfully removed all the mistake, allowing me to re-solder and complete the project. This challenge helped me master desoldering, which is benificial if I make a mistake in any of my future projects. My next steps are to work on my main project, which is the ball tracking robot. I next few steps are to build the base of the robot, adding motors to allowing it to move. 




<!--
```
# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.-->
