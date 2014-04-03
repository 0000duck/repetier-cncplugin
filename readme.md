# CncControl plugin to Repetier-host

## Abstract
This is a Repetier Host plugin focused on CNC machines. 
When working with CNC machines there are slightly different demands on user interface for frequent tasks such as jogging and height probing as the machined objects can be clamped at different positions on the bed. 

##Screenshot
<img src="/CncPlugin/Screenshots/screenshot-2014-03-31.png">

## Install
(Only windows tested so far but plugins are supposed to work in linux too)
* Create the directory C:\Program Files\Repetier-Host\plugins\CncPlugin
* Change privileges to write access for the folder if required.
* Download plugin dll (https://github.com/ahd71/repetier-cncplugin/raw/master/CncPlugin/Binaries/CncPlugin.dll)
* Copy dll file (CncPlugin.dll) into the new directory (note that Repetier host is case sensitive)
* Unblock windows security for the file if required (right click on file and click UNBLOCK https://github.com/ahd71/repetier-cncplugin/blob/master/CncPlugin/Screenshots/security_unblock.PNG)
* Restart Repetier Host.
* Done :-)

## Feature list
* Jog with keyboard (instead of mouse + click) - enabled only when the plugin panel is opened. Right now, arrow keys moves X and Y axis, PgUp/PgDn Z axis and numerical keyboard keys /*- keys sets step interval.
* Easy access to Z-Probe (G30, G31) and one-click-action to set height (G92 Zn.nn) based on the probing.
* Spindle on/off and PWM 
* G1 assist mode (just three textboxes for coordinates to move to, leave empty to not move one or several axis)
* G92 assist mode  (just three textboxes for redefining coordinates, leave empty to not redefine one or several axis)

## Planned features / To-do
(Moved to the [issue tracker](https://github.com/ahd71/repetier-cncplugin/issues)., but most important at this time is a Preferences dialog to host all configurable options to be saved in the host register structure like keyboard short cuts and step distances and spindle commands)

## Releases
* 0.11 / 2014-03-31 - Bug fix: 0.1mm jog fixed (invalid decimal point), Added Connect/Disconnect short cut and graphics
* 0.10 / 2014-03-31 - Added spindle control and gcode sender for move/setref/manual. Controls properly disabled when machine is disconnected. Gcode info next to buttons.
* 0.01 / 2014-03-30 - Prototype with working keyboard jog + height probe aid

(c) Hellstrand 2014
