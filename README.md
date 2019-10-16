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

## Lab 1
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
#### Create Your Project

1. Using your browser, open a **new tab** for AWS DeepLens console at https://console.aws.amazon.com/deeplens/.
2. Choose Projects, then choose Create new project.
3. On the Choose project type screen
- Choose Use a project template, then choose Object detection.

![](assets/projecttemplate.png)

- Scroll to the bottom of the screen, then choose Next.
4. On the Specify project details screen
   - In the Project information section:
      - Either accept the default name for the project, or type a name you prefer.
      - Either accept the default description for the project, or type a description you prefer.

  - Choose Create.

This returns you to the Projects screen where the project you just created is listed with your other projects.

#### Deploy your project <a id="deployproject"></a>

Next you will deploy the Object Detection project you just created.

1. From Deeplens console, On the Projects screen, choose the radio button to the left of your project name, then choose Deploy to device.

![](assets/projecthome.png)

2. On the Target device screen, from the list of AWS DeepLens devices, choose the radio button to the left of the device that you want to deploy this project to. An AWS DeepLens device can have only one project deployed to it at a time.

![](assets/targetdevice.png)

3. Choose Review.

   This will take you to the Review and deploy screen.

   If a project is already deployed to the device, you will see an error message
   "There is an existing project on this device. Do you want to replace it?
   If you Deploy, AWS DeepLens will remove the current project before deploying the new project."

   If you receive an error message stating "Cloud not find a project" please omit and proceed.

4. On the Review and deploy screen, review your project and choose Deploy to deploy the project.

   This will take you to to device screen, which shows the progress of your project deployment.

#### View your project log messages in IoT:

You can also view the log messages that your project's Lambda function running on DeepLens device sends to IoT topic.

1. Once the deployment has been successful (Green message at the top), click on *Devices* the left menu.
2. Click on the name of your DeepLens device and on the next screen click on Copy button on the IoT topic under Project ouput.

![](assets/dliottopic.png)

3. On a new browser tap open the AWS IoT Console at https://console.aws.amazon.com/iot/home?region=us-east-1#/dashboard
4. Click on Test in the left navigation.
5. Paste the IoT topic in the textbox under Subscription topic and click Subscribe to topic
6. You should now see log messages published from DeepLens device to IoT.

![](assets/dlmessages.png)

### Completion:
You have created and deployed object detection project to your Deeplens device.

