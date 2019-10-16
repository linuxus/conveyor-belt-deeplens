# conveyor-belt-deeplens
A smart conveyor-belt with AWS DeepLens and IoT

The Industrial IoT demo is a comprehensive demo that combines several AWS technologies to show the art of the possible in how AWS can play a central role in industrial design & automation, fleet management, predictive maintenance, and technician training. It features a 3D printed conveyor belt that is connected to AWS IoT.

This repository contains lab instruction to build a demo in your class to that will leverage AWS DeepLens camera to simulate communicate with the AWS IoT device shadow, control a virtual conveyor's stepper motor, and publish telemetry data.

There will be a physical version of this lab running on an actual conveyor-belt to showcase the interaction between the DeepLens camera, conveyor-bet device and IoT Cloud.

## Learning Objectives of This lab
In this lab you will be achieving the following:
- Create and deploy object detection project to DeepLens.
- Modify the DeepLens object detection inference lambda function to detect persons and upload frame to S3.
- Create lambda function to identify persons who are not wearing safety hats.
- Analyze results using IoT and CloudWatch and Web Dashboard.
## Table of Contents
1. [Architecture](#Architecture)
2. [Modules](#Modules)
3. [LAB 1 - Register your DeepLens Device](#registerdl)
4. [LAB 2 - Create an *object-detection* project](#createmodel)
    - [Deploy your project](#deployproject)
    - [View your project output](#projectoutput)

5. [LAB 3 - Create Worker Safety Project](#workersafetyproject):
    - [Step 1: Setup IAM Role for Cloud Lambda](#cloudiamrole)
     - [Step 2: Setup IAM Role for DeepLens Lambda](#dliamrole)
     - [Step 3: Create S3 bucket](#s3create)
    - [Step 4: Create Cloud Lambda](#cloudlambda)
    - [Step 5: Create DeepLens Inference Lambda Function](#inferencelambda)
    - [Step 6: Create DeepLens Project](#createdlproject)
    - [Step 7: Deploy DeepLens Project](#deploydlproject)
     - [Step 8: View Output in IoT](#iotoutput)
     - [Step 9: View Output in CloudWatch](#cloudwatchoutput)
    - [Step 10: View Output in Web Dashboard](#dashboardoutput)
6. [Clean Up](#cleanup)

## Architecture

![](assets/AWS_Management_Console_1.png)