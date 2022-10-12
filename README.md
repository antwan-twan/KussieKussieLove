# Kussie Kussie Love

Anthonie Meijers - 500827558

12-10-2022

## Introduction

This time, we are going to make a receiving and sending NodeMCU  board. It's a simple concept with just 2 boards and a single button. Also you need a partner for this one. Or just do it yourself with 2 boards. You can decide which is more fun.

This allows you to send simple messages to another board. 



## Step 1 - Skip the normal explanation

Unlike the normal explanation the teacher gave, just skip the steps and go straight to this example:

files > examples > Adafruit IO Arduino and choose either **adafruitio_21_feed_read** or **adafruitio_20_shared_feed_write**. 

The file you choose depends on if you want to receive or send a message to the other board. 





## Step 2 - Credentials and feed

The example files are already stocked with information. All of the details you need to fill in are provided. 

In both files go to the *config.h* file and fill in your Adafruit IO username and key.

<img src="img\image-20221012132253210.png" width="375px" alt="error overload">

Do the same for your WiFi network.

> It's best if you use your mobile hotspot. On Android, select a 2,4 gHz network and for iPhone, make sure to turn on 'Maximise Compatability'.

<img src="img\image-20221012132809908.png" width="375px" alt="error overload">



The next step is making a feed on Adafruit IO. Create one and set the privacy to 'Public'. 

<img src="img\image-20221012134427217.png" width="375px" alt="error overload">



## Step 3 - Change the code

There are a few things inside the code you need to adjust. 



Connect your button to your board at D0. Connect the red wire to 3v3, black to gnd and the yellow one to D0. It's important that you change this in your code. 

> Adjust #define BUTTON_PIN to D0. 



Then change #define FEED_OWNER. Between the brackets change the text to your Adafruit IO username. 



On line 33, change FEED_NAME to the feed you or your partner just created. 

<img src="img\image-20221012133128683.png" width="375px" alt="error overload">


Then upload to your board. Make sure the boards are connected to WiFi or your hotspot. Then try sending a message by pressing the button. 

Great success!



## Sources

- https://learn.adafruit.com/adafruit-io-basics-feeds/sharing-a-feed