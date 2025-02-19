# get_ip.xml
CircuitPython script to read and display IP and MAC address

There are two versions, one for a 128x64 oled and one for a 128x32 oled.

The idea behind this project is a device that I can plug into a medical device, driven by a Linux operating system,
to read the ip address and the MAC address to know which vlan it is on.

My colleagues used a memory stick with a blank file titled Get_ip.xml.  They would reboot the medical device and then wait for it to reconnect to the network. The device would see the file and populate it with various network information, including the ip and MAC addresses. They would then plug the memory stick into a laptop and read off the information they needed.  I felt this was too slow and cumbersome, so set about creating a "memory stick" sized device that would show the various network details.

I have a multiple of Seeeed Xiao Sam21 and RPi2040 devices and decided these should be used due to their very small footprint and their incredible processing power.  I also had various cheap 128x64 OLED displays laying around the home workshop.  My initial prototype was created usung a micro-board inside a mint tin, this restricted the size and gave a good deal of protection when not in use.

The project hinged on creating a device that appeared to be a memory stick. Reviewing the various operating systems that fit on these microcontrollers the Adafruit CircuitPython appeared to be the easiest to use, and it gave me an excuse to have a play with it.
While testing the first iteration it became apparent I needed to increase the complexity of the code to take into account the various errors that could occur, e.g. missing file, not connected to a network. 

I'm not a coder / programmer, just an old guy who likes to play with microcontrollers and a desire to build, so please forgive the randomness of the code. If you feel you could do something with it then please feel free to copy and improve, I'm not precious about what I create, I do it for fun.

The prototype worked well and did exactly what I wanted it to to; however, I started thinking about a more robust verson that was smaller and only displayed the information we needed, ip and MAC addresses.  I reduced the display to a 128x32 OLED and encased it all in an old memory stick. This worked well as the memory stick was the type that slides the usb connectror in and out. This means it has a large central cut out that perfectly fits a 128x32 OLED display.  

I found some Xiao Seeed Studio 2040's on line that were quite cheap so purchased them for the memory stick version. This has a type-c female usb connector so a cable is needed to connect to the medical device. I wanted to change this for the third incarnation of the project, however, after real world testing it appears the cable is the better option as it allows the user the ability to move the display to read the information. The devices I'm testing have downward slopping usb connectors, so to read the display you would need to incline your head to 30 degrees - not the best position to stand in while trying to read a display. 

All in all this project seems to work well, although it has a very limited use for me, it does exactly what I wanted it to do.

![ReadingIPMAC](https://github.com/stevegroves123/get_ip.xml/assets/10800904/8ac0deb9-86f9-4191-92ee-da98bc163f10)

