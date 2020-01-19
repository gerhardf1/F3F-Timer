# F3F-Timer

This App is running on Android mobilephones and acts as a simple Timer for the piCAMTracker (see https://github.com/barney-NG/piCAMTracker).
Starting with V0.5 the piCAMTracker sends UDP broadcasts when it is powered and in case a "Turn" is detected.
The App receives the UDP broadcasts and handles a single or continuous F3F runs (starting, 30s countdown, Base A crossing off course, Base A crossing in course in course, 10 laps, running time).

# News
2019-09-16: V0.2 released: bugfix BaseA-Counter of 3 leads to lap 1)
2019-09-16: V0.1 released

# Prerequisite:

* piCAMTracker and the mobilephone has to be in the same IP network.
* The simplest solution is to use the mobilephone as a hotspot and connect both piCAMTracker to it.
* Be sure that the following lines are included in config.json:
  * "IPUDPBEEP": "255.255.255.255",
  * "accessPoint": false,

# Usage:

* First of all the App has to be started.
* It shows the own IP address.
* After pressing button "Connect" it waits for Base A.
* Now piCAMTracker of Base A should be powered.
* After booting the App will show the IP address of Base A.
* Now piCAMTracker of Base B should be powered.
* After booting the App will show the IP address of Base B and is now ready for start.
* you can select between 3 modes:
  * single: the time for one round is measured.
  * continuous: the time for more rounds is measured, countdown starts 30s after last lap.
  * beeper: at every Turn signal the beeper is activated, no time measurement.

* To start the 30s countdown the button "Start" has to be pressed.
* Now the App is ready for Turn signals from Base A and B.
* After 10 laps the flight time will be announced and recorded.
* With pressing button "Reset" the time and counters will be resetted.
* With pressing button "List Rounds" the time for the last rounds are shown.
