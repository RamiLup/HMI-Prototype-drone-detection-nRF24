# Efficient, low-cost prototype for a fast-scanning drone detection system 
# based on 2.4GHz channel power analysis, utilizing three nRF24 modules and an ESP32
<br>
<p align="center">
 
![InHousePatrol](https://github.com/user-attachments/assets/44355cbc-a66c-48aa-9ca1-b6daf258144a)
</p>
</br>

## TL;DR:

Rombi is an innovative mobile scarecrow using an old iRobot 

## How it started ?
While organizing the storage room, I came across an old Roomba 

The experiment was a success, and I moved on to the improvement 

<br>

<p align="center">


<p align="center">
  <img src="/media/testing the protocl.jpg" alt="web_server" width="300" height="500"/>
</p>

 </p>

<br>


I assembled an ESP32 on a breadboard, along with some voltage 
converters, and prepared a set of HEX commands in Roomba’s 


[The full protocol is here](media/iRobot_Roomba_500_Open_Interface_Spec.pdf)

<br>

And it worked.
<br>



<br>
It’s possible to execute dozens of commands, from starting and 

<p align="center">
  <img src="/media/web_server_with_video.png" alt="web_server" width="300" height="500"/>
</p>

It works excellently when connected to the same Wi-Fi network. 

<p align="center">
  <img src="/media/vlcsnap-2024-08-27-21h21m46s777.png" alt="Rombi" width="700" height="300"/>
</p>


I can even get a real time video from the Roomba's patrol.
The current version supports the following commands via the Web Server and Telegram:
- Start patrol


The sensors are Arduino-based and communicate directly with the web 
server within the Roomba, all connected to the same Wi-Fi network.


## Summary:

<p align="center">
 
 https://github.com/user-attachments/assets/44740bdd-6202-4ac6-9fad-2e479e566b7c

</p>
<br>

And, of course, there’s a bonus. Implementing this idea allows me 
to learn more about Arduino hardware and software, image processing,
PCB design, CAD software,  sensor design and much more. 
It’s pure enjoyment.


## Notes:

1. Virtu
3. Smag t
source.
4. The comoar


## Planned Improvements for the Next Versions:

1. A hollow body (e.g., made of metal mesh) for the scarecrow boady
to make it less sensitive to strong winds.
2. Sending the Roomba directly to the sensor area from which the 
alert was triggered.
3. Adjusting the Roomba's travel path based on the shape and size 
of the balcony.
