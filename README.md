# conveyor-belt-deeplens
A smart conveyor-belt with AWS DeepLens and IoT

The Industrial IoT demo is a comprehensive demo that combines several AWS technologies to show the art of the possible in how AWS can play a central role in industrial design & automation, fleet management, predictive maintenance, and technician training. It features a 3D printed conveyor belt that is connected to AWS IoT.

This repository contains lab instruction to build a demo in your class to that will leverage AWS DeepLens camera to simulate communicate with the AWS IoT device shadow, control a virtual conveyor's stepper motor, and publish telemetry data.

There will be a physical version of this lab running on an actual conveyor-belt to showcase the interaction between the DeepLens camera, conveyor-bet device and IoT Cloud.

## Learning Objectives of the lab
In this lab you will be achieving the following:
- Create and deploy object detection project to DeepLens.
- View DeepLens camera inference output via AWS IoT Core.
- Create new DeepLens project to detect specific object and communicate with digital twin conveyor belt.
- Analyze results using IoT and CloudWatch.

## Table of Contents
1. [Architecture](#Architecture)
2. [LAB 1 - Create an *object-detection* project](#createmodel)
    - [Deploy your project](#deployproject)
    - [View your project output](#projectoutput)
3. [LAB 2 - Create Conveyor-belt Project](#conveyorbeltproject):

## Architecture
Lab Architecture
![](assets/Conveyor_Lab_Architecture_1.png)

1. Login into your AWS Lab account. Please consult the presenter's slide for detailed instructions:

2. Make sure you are using the N. Virginia region when you login into the console.
![](assets/AWS_Management_Console_1.png)

3. Go to the DeepLens service by searching "DeepLens" in the *find services* search menu
![](assets/AWS_Management_Console_2.png)
click on the name and the DeepLens service console page will open.

4. Make sure that there is a DeepLens device registered:
![](assets/AWS_DeepLens_1.png)

5. Click on the device name and make sure that it shows *online* before proceeding the rest of the lab. *NOTE*: if the device does not show online please notify the instructore.
![](assets/AWS_DeepLens_2.png)

