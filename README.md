# F3F-Timer

This App is running on Android mobilephones and acts as a simple Timer for the piCAMTracker (see https://github.com/barney-NG/piCAMTracker). 
With the last commit to the github repository (End of July 2019) the piCAMTracker sends UDP broadcasts when it is powered and in case a "Turn" is detected.
The App receives the UDP broadcasts and handles a single F3F run (starting, 30s countdown, Base A crossing off course, Base A crossing in course in course, 10 laps, running time).

Prerequisite:
piCAMTracker and the mobilephone has to be in the same IP network.
The simplest solution is to use the mobilephone as a hotspot and connect both piCAMTracker to it.

Usage:
First of all the App has to be started.
It shows the own IP address.
After pressing button "Connect" it waits for Base A.
Now piCAMTracker of Base A should be powerred.
After booting the App will show the IP address of Base A.
Now piCAMTracker of Base B should be powerred.
After booting the App will show the IP address of Base B and is now ready for start.
To start the 30s countdown the button "Start" has to be pressed.
Now the App is ready for Turn signals from Base A and B.
After 10 rounds the flight time will be announced.
With pressing button "Reset" the time and counters will be resetted.
