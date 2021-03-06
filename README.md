# NHL Goal Light

[![GitHub release](https://img.shields.io/github/release/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/releases)
[![GitHub commits](https://img.shields.io/github/commits-since/arim215/nhl_goal_light/v3.0.svg)](https://github.com/arim215/nhl_goal_light/commits/master)
[![closed pull requests](https://img.shields.io/github/issues-pr-closed/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/pulls?q=is%3Apr+is%3Aclosed)
[![Libraries.io for GitHub](https://img.shields.io/librariesio/github/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/blob/master/requirements.txt)
[![Code Issues](https://www.quantifiedcode.com/api/v1/project/c0f4d36de7234c45bb7689af5a35c7ec/badge.svg)](https://www.quantifiedcode.com/app/project/c0f4d36de7234c45bb7689af5a35c7ec)
[![license](https://img.shields.io/github/license/arim215/nhl_goal_light.svg)](https://github.com/arim215/nhl_goal_light/blob/master/LICENSE)

##Overview

Nhl goal light python3 for raspberry pi GPIO. Works with any team, just enter team **name without city** when prompted.

Before use, make sure you have:

Python3, python3-pip, mpg123, git

Run the following commands manually to install requirements

run:

  	$ sudo apt-get install git mpg123 python3 python3-pip
    $ sudo git clone https://github.com/arim215/nhl_goal_light.git 
  	$ sudo pip3 install -r requirements.txt
        
**Always pass through code to read comments and see necessary inputs for your setup!!**

You can prepare a "settings.txt" file to auto-config the nhl_goal_light.py code, or the code will ask for your input everytime. You can run the flask API ($ sudo python3 flask_api.py) to find your team_id (Ex: FLASK_API_IP/api/v1/team/Canadiens/id will return "id : 8").

To start application, use following commands:
	
    $ sudo python3 flask_api.py &
    $ sudo python3 nhl_goal_light.py

***
###Materials

For documentation on how to wire the GPIOs with the lights and the button, pleaser refer to the "docs" folder.

* Raspberry Pi (currently using raspberry pi A model, but any model will work)
* Red Rotating Beacon Warning Light from ebay
* 5V 2 Channel Relay Module from ebay
* Momentary OFF ON Push Round Button
* 12V to 5V 1A adapter (used a car usb adapter) would be good to have a dual usb adapter in case you need to plug something else like a usb speaker.
* 3.5mm audio extension cable

***
###Audio
If you wish to change the audio clips to sounds with your teams goal horn and music, just download them, rename them (goal_horn_#.mp3) and save them in the "audio" folder.

***
##Delay

I've teste my code while watching Rogers Gamecenter Live and the stream seems to be a bit delayed, so I added a delay to my code to make the goal horn start later. You will be prompted to enter a delay that works with your stream.  

***
## TODO
* Test response time after a goal is scored
* Add option to select team thru webpage
* Make code pause between periods
* Allow the addition of a I2C display
* Add a text message service to notify goals and more
