# Pi Roboter Workshop
Hier findest du die Worksheets und den Programmcode vom [CamJam EduKit 3](http://camjam.me/?page_id=1035). 

Sollte das Cam Jam Kit ausverkauft sein verwenden wir auch ein Motor Board und ein Lasercut Chassis von Ryanteck. Eine Anleitung für den Zusammenbau findest [hier] (http://wiki.ryanteck.uk/RTK-000-003-Robot-Assembly). Der einzige Unterschied ist, dass die Motoren mit anderen Pins angesteuert werden. Python Code Examples findest du [hier] (https://github.com/RyanteckLTD/RTK-000-003/blob/master/basicPython/codeSamples/pythonBasis.py). Unter `code` findest du code examples für jedes Board. 

Solltest du ein RaspiRobotBoard V2 oder V3 von Simon Monk haben dann findest du den code [hier] (https://github.com/simonmonk/raspirobotboard2/tree/master/python/examples) und die Anleitung zum Zusammenbau hier.



## Kursinhalt
### Aufbau und Motortest
In den PDFs im Ordner `worksheets` ist der Zusammenbau des Robots und der Motortest beschrieben. Da wir als Distribution Kano verwenden, haben wir das erste Worksheet auf Deutsch neu geschrieben. 

### Einführung in GPIO Zero

Um dir den Einstieg in die Roboterprogrammierung zu vereinfachen verwenden wir die [gpiozero library](https://gpiozero.readthedocs.org/en/v1.1.0/). 


#### Installation 

Mit diesen Kommandos kannst du pizero installieren. 

```
sudo apt-get install python-dev

```

``` 
sudo pip install gpiozero

```

### Kontrollieren des CamJam #3 Kit Robot mit pizero

Mittlerweile gibt es eine eigene Klasse für den CamJam Robot. Du musst so gar nicht mehr die Pins definieren. So kannst du etwa deinen Roboter Links fahren lassen.

```
from gpiozero import CamJamKitRobot

robot = CamJamKitRobot()
robot.left()

```
Folgende Kommandos stehen dir zur Verfügung:  


> `backward(speed=1)`

Fahre den Roboter rückwärts indem du beide Motoren rückwarts drehen läßt.
 
>  close()

Shut down the device and release all associated resources.
 
> forward(speed=1)

Fahre vorwärts indem du beide Motoren vorwärts drehen läßt. 
 
>  left(speed=1)

Fahre eine enge Links Kurve indem du den rechten Motor vorwärts drehen läßt und den linken Motor rückwärts drehen läßt. 
 
>  reverse()

Reverse the robot’s current motor directions. If the robot is currently running full speed forward, it will run full speed backward. If the robot is turning left at half-speed, it will turn right at half-speed. If the robot is currently stopped it will remain stoppe
 
>  right(speed=1)

Fahre eine enge rechts Kurve indem du den linken Motor vorwärts und den rechten Motor rückwärts fahren läßt. 
 
>  stop() 
 
Stoppe alle Motoren. 


### Autostart Python Programm
Wie Du dein Programm automatisch beim Hochfahren des Raspberrys starten kannst, steht in [dieser Anleitung](Autostart.md).

###Programmierung mit Scratch
Nachdem wir das Python Sript geschrieben haben, werden wir das Programm in Scratch nachbauen. 


##Extras

Zu Hause oder im wöchentlichen Pi Club kannst du weiter an deinem Roboter arbeiten. 

###Ultraschallsensor
Eine englische Anleitung findest du dazu `worksheets` 
.

###Line Follower Sensor
Eine englische Anleitung findest du dazu `worksheets` 
.

###Feinjustierung der Motoren
Eine englische Anleitung findest du dazu `worksheets` 
.

### Fernsteuerung mit Blynk
Hier findest du eine Anleitung, wie du den Roboter mit dem iphone/Android Blynk fernsteuern kannst: [blynk/README.md](blynk/README.md)

### eigenes Chassis
In einem weiteren Workshop werden wir zusammen ein Chasis designen und 3D Drucken. Ein Beispiel findest du hier auf [thingiverse](http://www.thingiverse.com/thing:1113796/#files). 

## Download 
* den ganzen order über "Download ZIP" rechts oben
* Oder klicke auf RAW und copy paste den code in deinen geany editor, achte darauf, dass du alle Identications mitnimmst
* Oder direkt über git, ein gutes Tutorial dazu findest du hier: [try.github.io](https://try.github.io)

##LIZENZ
Dieses Repository ist unter der Creative Commons Lizenz [CC-BY-SA] (http://creativecommons.org/licenses/by-sa/4.0/) lizensiert. 


## Kontakt
* Web: [www.erfindergarden.de](http://www.erfindergarden.de)
* Email: [play@erfindergarden.de](mailto:play@erfindergarden.de)