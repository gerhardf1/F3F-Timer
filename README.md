# F3FTimer
The App "F3FTimer" is running on Android mobilephones and acts as a simple Timer for the [piCAMTracker](https://github.com/barney-NG/piCAMTracker).
Starting with V0.5 the piCAMTracker sends UDP broadcasts when it is powered and in case a "Turn" is detected.
The App receives the UDP broadcasts and handles a single or continuous F3F runs (starting, 30s countdown, Base A crossing off course, Base A crossing in course, 10 laps, running time).

# F3FTimerRemoteSwitch
The App "F3FTimerRemoteSwitch" is running on Android mobilephones and can be used instead of piCAMTracker to manually produce "Turn" signals on Base A or B.

# News
* 2024-06-30: F3FTimer V0.11 released:
  * number of laps selectable (default: 10)
* 2024-06-01: added some informations in case of range problems
* 2024-01-14: F3FTimer V0.10 released:
  * mode "F3B-Speed" removed because of new [F3B-Timer](https://github.com/gerhardf1/F3B-Timer)
* 2023-03-12: F3FTimer V0.9 released:
  * IP addresses are now stored
* 2022-08-19: F3FTimer V0.8 released:
  * new mode "F3B-Speed"
  * prevent the mobilephone from sleeping
* 2021-10-07: F3FTimer V0.7 released:
  * mode "beeper" is working again
* 2021-05-01: F3FTimer V0.6 and F3FTimerRemoteSwitch V0.2 released:
  * communication between Timer and RemoteSwitch is now bi-directional
  * Lapcounter and endtime are announced at RemoteSwitch
* 2021-04-20: F3FTimer V0.5 released:
  * tighten the User Interface of "F3FTimer"
  * Button "Start" and "Reset" can now be controlled by UDP Broadcasts, an additional device will follow
* 2021-03-28: added a new app F3FTimerRemoteSwitch
  * can be used instead of piCAMTracker
  * connects to F3FTimer via WiFi (similar to piCAMTracker)
* 2020-12-08: V0.4 released:
  * Button "STEP" heightened
  * after entering course "Time" is showing previous seconds
  * Screenorientation fixed to portrait
* 2020-11-23: V0.3 released: new Button "STEP": manual step through a F3F round
* 2020-01-19: V0.2 released: bugfix BaseA-Counter = 3 leads to lap 1
* 2019-09-16: V0.1 released

# Prerequisite:

* piCAMTracker and the mobilephone has to be in the same IP network.
* The simplest solution is to use the mobilephone as a hotspot and connect both piCAMTracker to it.
* Be sure that the following lines are included in config.json:
  * "IPUDPBEEP": "255.255.255.255",
  * "accessPoint": false,

# Usage:

* First of all the App "F3FTimer" has to be started.
* It shows the own IP address.
* After pressing button "Connect" it waits for Base A.
* Now piCAMTracker of Base A should be powered or button "Connect" shoud be pressed on App "F3FTimerRemoteSwitch"
* After booting the App will show the IP address of Base A.
* Now piCAMTracker of Base B should be powered or button "Connect" shoud be pressed on App "F3FTimerRemoteSwitch".
* After booting the App "F3FTimer" will show the IP address of Base B and is now ready for start (from version V0.9 onwards the IP addresses are stored and you have to do this procedure only at the first connection).
* you can select between 3 modes:
  * single: the time for one round is measured.
  * continuous: the time for more rounds is measured, countdown starts 30s after last lap.
  * beeper: at every Turn signal the beeper is activated, no time measurement.

* To start the 30s countdown the button "Start" has to be pressed.
* Now the App is ready for Turn signals from Base A and B.
* After 10/4 laps the flight time will be announced and recorded.
* With pressing button "Reset" the time and counters will be resetted.
* With pressing button "List Rounds" the time for the last rounds are shown.

# range problems
In case of having range problems the the following items can be used:
* using a WiFi access point as a hotspot, e.g. Mikrotik wAP, which has several advantages
  * is suitable for outdoor use
  * can be powered by a 3s or 4s LiPo battery
* using a Raspberry Pi with an external WiFi antenna:
  * informations how to update the Pi can be found [here](https://geeks-r-us.de/2019/08/31/wlan-bluetooth-upgrade-fuer-den-rpi-4/)
  * already updated Pi can be bought [here](https://geeks-r-us.de/produkt/raspberry-pi-4-mit-u-fl-buchse/)
