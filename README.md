# Condompult - The Instructions to build the launcher that gets you laid (maybe)
Instructions for making a google powered condom launcher for the ultimate nerd rizz that may or may not get you laid *USE WITH CAUTION*

As seen in the reel on my Instagram:
https://www.instagram.com/reel/DGL-qspOhVT/?utm_source=ig_web_copy_link&igsh=MzRlODBiNWFlZA==

The whole setup is pretty Janky but here are the things you need:

# Shopping List 
- 1 x ESP32 MicroController https://amzn.to/4i5w1lD
(in theory you can also use an ESP8266 but the code I've written for it is for an ESP32)
- 1 x 9g Servo Motor https://amzn.to/3EUyrVQ
- 1 x Male to Female Jumper Wires: https://amzn.to/436ySGL
- 1 x USB Power Bank (You need to power it without cables running into your cupboard) https://amzn.to/4k788w0
- 1 x USB A to USB Micro (For powering the ESP32) https://amzn.to/3QlZcFo
- 1 x Breadboard (Optional - I used it in the video for dramatic effect but its not really neccesary) https://amzn.to/4i2qGvs

# 3D Printing Files
if you don't have a 3D Printer you're going to need to make contact with that one weird friend of yours that you don't talk to very often who has one, to ask him to print you this file out of PLA.
Don't let him bullshit you though, it's not a lot of filament so he shouldn't charge you much for it.

![image](https://github.com/user-attachments/assets/6230cfce-d5ce-48e1-bf3d-6a7540c54d84)
![image](https://github.com/user-attachments/assets/b98b79fd-a050-4403-8967-61171b6629ce)
![image](https://github.com/user-attachments/assets/5bf0ee60-52b5-4645-aaf1-83461b11eadf)

The Catapult part is just glued to a peice of perspex but you don't really need to do this. It's just for the video.

I've put the files for the 3D Print inside this Repo. Its literally just one file that is printed in two parts and an elastic is used to hold it back.
I am going to admit, this model is a bit janky and it took a few tries to launch the condom correctly. 
If ANYONE can design a better file for this project, I will 100% add it to this repo as an upgrade with full credits to you!


# Wiring
Pretty Simple stuff.
On the servo you will have Red Orange and Brown
Red - 5v
Orange - PWM (Pin 12)
Brown - GND

![image](https://github.com/user-attachments/assets/9be77aa0-2c3a-4ce6-83aa-708984de0521)

# Adding Code - Google Assistant Integration

If you know nothing about programming, you're in luck because we won't touch any written code as its controlled using AdafruitIO, an online service that allows you to wirelessly interface with micro-controllers without having to touch any code at all, neat right?

We do this in two parts, There is probably and easier way and if there is please fork this so we can help others set up easier:

1) Adafruit IO Setup.
- Create An account here: https://io.adafruit.com/
- Select New Device:
![image](https://github.com/user-attachments/assets/72e454cd-b160-4243-b33a-695a2a23e913)
- Run through the setup for the board and skip the Optional CircuitPython Backup
![image](https://github.com/user-attachments/assets/591defc0-cf0c-4f7e-a83b-68becc7d42f8)

After you've followed the steps and connected the board to your WiFi. Select Your new Board from your Device list and Select "New Component"
- Search for generic servo and add this new component. Use the following settings:
![image](https://github.com/user-attachments/assets/286e9b48-5221-4b52-9256-46a9e392f570)

![image](https://github.com/user-attachments/assets/b7a45961-e6d6-470c-9a68-9827eb1f6de6)

If we've done everything correctly you will now see the following screen with a slider on the right. 
If your servo is plugged into the correct pins, moving the slider left and right should move the servo on your table.
![image](https://github.com/user-attachments/assets/504ebc83-0e29-410e-89ed-c80f18ae20a9)

All we need to do now is tell Google to move from 500us to 2500us when we ask it via Google Assistant.
To do this, we need to connect our AdafruitIO Account to our Google Account using the last part of the equation called [IFFF](https://ifttt.com/)

2) IFTTT Account Setup

Once you create an account you're going to use this [Applet](https://ifttt.com/applets/r7T3ALxN-if-you-say-okay-google-activate-trst-then-send-data-to-condompult-generic-servo-feed):

![image](https://github.com/user-attachments/assets/890dabd8-88d9-4b63-8a0e-fc574248fd44)


Applets are little trigger scenes inside IFTTT that connects two services. In this case we're going to connect our Google Account with our AdafruitIO Account so we can control the servo from Google.
IFFF Will ask you to link both your Google and your AdafruitIO Account. If you are asked for your AdafruitIO KEY: It is located here:
![image](https://github.com/user-attachments/assets/dd75adfd-e46f-4a14-b470-f2eb722286f4)


Once your Applet is connected it should look like this and everything is ready to go.
![image](https://github.com/user-attachments/assets/3e723862-8eaf-430e-9fe6-8809a578aab1)



You can test if everything works by asking your google "Hey Google, Acitivate Shields" and it should trigger the servo to move from closed to open. If you want to move it back to the closed position. You can run the command again via Google Assistant and it will go back to where it originally started from.

# Changing the Activation name to a custom name

- If you want to use another phrase such as "Activate Forcefield" etc - You can change the scene name to whatever you want that phrase to be. 

![image](https://github.com/user-attachments/assets/58a97ec6-cad3-4cb4-9386-e4df538dec91)

- Change the Trigger name here:

![image](https://github.com/user-attachments/assets/4021bf4a-aeab-4e82-b94d-4aecf5a2363c)

Remember Google Actually thinks its some kind of Smart Device such as a swtich or a Light or something. So you can use other words that Google understands such as "Turn on *shields* ", "Switch on *shields*" etc etc


Have Fun building this and if you get laid. You owe me! Enjoy boys!

Follow me on YouTube or Instagram for more Stupid Electronic Content!

-www.youtube.com/BrenMaartens
-www.instagram.com/BrenMaartens












