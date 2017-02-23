# OpenDS
Free Driving Task
OpenDS (Open-source Driving Simulator)
======================================

Version 4.0 - April 15th, 2016


OpenDS is an open source driving simulator for research. The software is 
programmed entirely in Java and is based on the jMonkeyEngine framework, 
a scene graph based game engine which is mainly used for rendering and 
physics computation. OpenDS is distributed under the terms of GNU General 
Public License (GPL).



1. What is contained in this folder
-----------------------------------
The folder you downloaded contains sources and an already built version of OpenDS 
including the Drive Analyzer tool to replay a drive. Furthermore, library files 
needed to run OpenDS - from sources and binaries - as well as the assets folder
(containing scenes, models and tasks) is included. More details about the available 
tasks can be found in paragraph 7. In addition, you will also find the JavaDoc 
files, the license text, the multi-driver server and a client to receive data from 
the running simulator (settings controller server). 



2. Getting started
------------------
Binaries for Windows, Mac OS and Linux are contained in this folder. 

1. Make sure you have installed the Java Runtime Environment (JRE) version 8 
   or higher. If not, download it from http://www.java.com
2. Run 'OpenDS.jar' either by double clicking or using console (type: 
   'java -jar OpenDS.jar'). Windows users could also run "start.bat"
3. Select resolution and proceed with clicking 'OK'.
4. Specify driver’s name (optional).
5. Select which task to load and click 'Start'.

To stop the application, hit the ESC key or close the window.
Press F1 during simulation for default key assignment.

NOTICE: File 'startProperties.properties' might help you to start pre-defined
        tasks even faster. You can set up the display settings and skip the 
        selection screen by uncommenting 'showsettingsscreen=false'. Furthermore,
        you can set the name of the driver and the task to start when executing 
        OpenDS. 



3. Building OpenDS
------------------
Sources for Windows, Mac OS and Linux are contained in the "src" folder. The 
following steps show how to setup the source code for Eclipse. Of course, you
can use your favored IDE.

1. Make sure you have installed the Java Development Kit (JDK) version 1.8 
   or higher. If not, download it from 
   http://www.oracle.com/technetwork/java/javase/downloads/index.html
2. Start Eclipse and import an existing Project (File -> Import...). 
   Select 'General' -> 'Existing Projects into Workspace' and click 'Next'.
3. Select this folder as root directory and click 'Finish'.
4. Make sure the 'assets' folder has been added to your project.

You can skip the next two instructions if there are no Build Path errors.
5. Make sure that all jar files (counting 152) that can be found in 'lib' or 
   any of its sub-folders have been added to the Build Path.
6. Right-click the project and select 'Build Path' -> 'Configure Build 
   Path...' to open the 'Properties'-dialog. Go to tab 'Libraries' and 
   click 'Add Class Folder'. Select the check box of folder 'Logo' which 
   can be found at 'assets/Textures' as well as the check box of folder 
   'log4j' which can be found at 'assets/JasperReports'. Click 'OK' to close 
   both dialog windows.

7. Run OpenDS by right-clicking eu.opends.main.Simulator in Eclipse's Package 
   Explorer and selecting 'Run As' -> 'Java Application'.
8. Select resolution and proceed with clicking 'OK'.
9. Specify driver’s name (optional).
10.Select which task to load and click 'Start'.

To stop the application, hit the ESC key or close the window.
Press F1 during simulation for default key assignment.



4. Where to find documentation
------------------------------
More information can be found in the download area of the project website.
http://www.opends.eu


5. Contributors
---------------
a) Concept: Christian Müller
b) Architecture and development: Rafael Math
c) Other contributions:
	Saied Tehrani
	Michael Feld
	Otávio Biasutti
	Daniel Braun
	Gleb Banas
	Till Maurer
	Dastin Rosemann
	Paul Jacob Hoepner
	Malvin Danhof
	Tarek Schneider
	Michael Walz
	Eric Audehm
d) How to contribute?
   Please write us using the contact form on the project website 
   (http://www.opends.eu).



6. Credits
----------
Digital media assets have been taken from jMonkeyEngine (http://www.jmonkeyengine.org)
if no other reference can be found in the corresponding folder.

The "BigCity" model has been provided by Paul Jacob Hoepner from the Technical 
University of Berlin, Germany

The Oculus Rift Extension has been provided by Malvin Danhof, Tarek Schneider, Michael 
Walz, and Eric Audehm from Hochschule Konstanz (University of Applied Sciences), Constance, Germany



7. Available tasks
------------------

BigCity/bigCity.xml  (Very powerful computer required!)

Drive through a large city model provided by Paul Jacob Hoepner from the Technical 
University of Berlin, Germany. This task needs high performance computer.


ConTReTask/conTReTask.xml (OpenDS Premium only!)

The Continuous Tracking and Reaction Task (ConTRe Task) is a highly controlled 
driving task that allows fine-grained measurement of steering and event detection 
performance through very few dependent variables. Also, it is a rather artificial 
task that only resembles to realistic driving.
NOTE: This driving task is only available in the Pro Complete version of OpenDS


Countryside/countryside.xml

This model has been created with CityEngine and shows the ability to model roads in 
hilly terrain. Furthermore, some vehicles will be driving around. By pressing 
the U key a top-down view will be shown. Screen capturing is switched on by default.


Countryside2/countryside2.xml (Powerful computer required!)

Slightly larger remake of "Countryside" with a lot more traffic on the road. This 
task needs high performance computer.


Idealtest2/idealtest2.xml

In this model the traffic light control will be demonstrated by the help of a few
simple intersections. At the beginning, trigger mode is active, i.e. approaching 
vehicles will be detected and the related traffic light will turn green. By 
pressing the "A"-key, you can toggle all traffic light modes: 
TRIGGER -> PROGRAM -> EXTERNAL INPUT -> BLINKING -> OFF. In program mode, all 
traffic lights will obey to a pre-defined list of traffic light rules and in 
external mode traffic lights can be interactively controlled by the experiment 
leader. When you reached modes blinking and off you can go back to trigger mode 
by pressing the "A"-key once more. The trip will be recorded for later analysis 
and in the "data analyzer" folder. Furthermore, a traffic vehicle obeying to traffic
lights will be available. 
Also used as test track for OpenDS HMI (OpenDS Premium only!)


Paris/paris.xml

This CityEngine model includes photo-realistic textures of Paris and was equipped 
with a bus stop and a roundabout. This model shows how to use the Object Locator tool
to place further objects (cf. ParisTraffic as potential result).


ParisTraffic/parisTraffic.xml (Powerful computer required!)

This is the extended model (road signs, traffic, sky texture, triggers, etc.) of the 
aforementioned Paris model. This model can be used for eye-gaze analysis (OpenDS
Premium only!).


ReactionTest/reactionTest.xml (Powerful computer required!)

This task contains a reaction experiment with instruction screen. The driver has to 
drive in the center lane at full speed and react to suddenly appearing signs. On red X 
signs the driver has to decelerate while keeping the center lane. On green arrow signs 
the driver has to change to the indicated lane at full speed. After a confirmation 
sound is played, the car is advised to go back to driving in the center lane at full 
speed. After the drive, a PDF file showing the driver's performance will be presented.


Terrain/terrain.xml

Test track for simple terrain generation from hight map and alpha map. This model can 
be used for the multi-driver demo by running multiple OpenDS instances on that track.
The multi-driver server which can be found in the "tools" folder must be running first 
(default port 4510).


ThreeVehiclePlatooningTask/threeVehiclePlatooningTask.xml (OpenDS Premium only!)

The Three Vehicle Platooning Task (3VPT) is a more realistic driving task and allows 
measuring many different dependent variables, but is still controlled. It demands 
the driver to control his lateral as well as longitudinal position and additionally 
to detect and respond to several events. 
NOTE: This driving task is only available in the Pro Complete version of OpenDS


Village/village.xml

Another CityEngine model showing snow and fog effects. This model can be used for the
settings controller demo. Running the test client in the "tools" folder will show live
simulation data. Connect to server (default port 5678) and open 
"examples/EstablishConnection.xml"


Village2/village2.xml (Powerful computer required!)

Another CityEngine model showing traffic and pedestrians.
