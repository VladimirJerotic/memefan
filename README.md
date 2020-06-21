# Memefan

![Screenshot](https://i.ibb.co/BgRJx06/Screenshot-from-2020-06-21-07-13-44.png)

This is an application for controlling fan speed on IBM/Lenovo ThinkPads.

It can also monitor CPU temp and fan RPM.

It is written for Linux only. For windows, see http://www.almico.com/speedfan.php   

## How it Works?
 + Parses `sensors` command to show CPU temp and fan RPM
 + Modifies `/proc/acpi/ibm/fan` to change fan speed

## Dependenciesls
`sudo apt install lm-sensors python3 python3-tk`

## Setup 1
+ Open this file, using command -- `sudo nano /etc/modprobe.d/thinkpad_acpi.conf` 
+ Add line `options thinkpad_acpi fan_control=1`
+ Reboot. 
+ `python3 fan.py`

( Add `sudo` to modify speed )

## Setup 2
+ Download memefanBIN.7z
+ Extract and navigate to /dist/memefan
+ Run memefan (make sure you have right premissions)

---

Note: You are required to have the Linux kernel with `thinkpad-acpi` patch. (Ubuntu, Solus and a few others already seem to have this)
