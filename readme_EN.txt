/*****************************************************************************
* | File      	:   Readme_CN.txt
* | Author      :   Waveshare team
* | Function    :   Help with use
* | Info        :
*----------------
* |	This version:   V1.0
* | Date        :   2019-09-24
* | Info        :   Here is an English version of the documentation for your quick use.
******************************************************************************/
This file is to help you use this Demo.
A brief description of the use of this project is here:

1. Basic information:
This Demo has been verified on the Raspberry Pi 3B+ and Jetson Nano;
This Demo has been verified using the e-paper Driver HAT module. 
You can view the corresponding test routines in the examples\ of the project;

2. Pin connection:
Pin connections can be viewed in \lib\waveshare_TSL2591\TSL2591.py and will be repeated here:
TSL25911    =>    Jetson Nano/RPI(BCM)
VCC         ->    3.3V
GND         ->    GND
SDA         ->    SDA
SCL         ->    SCL
INT         ->    4

3.Installation library
Raspberry Pi
    
    Installation wiringPi
        2.	#For Raspberry Pi 4B you may need to upgrade:
        3.	cd /tmp
        4.	wget https://project-downloads.drogon.net/wiringpi-latest.deb
        5.	sudo dpkg -i wiringpi-latest.deb
        6.	gpio -v
        7.	# Running gpio -v will appear version 2.52, if there is no error, the installation is wrong.
        

4. Basic use:
Test the program in the examples\ directory:
    make clean 
    make
    sudo ./main
    
5 install as service
    sudo cp poe-hat-b.service /lib/systemd/system
    sudo systemctl daemon-reload
    sudo systemctl enable poe-hat-b.service 
    sudo cp poe-hat-b /usr/bin/
    sudo service poe-hat-b start
