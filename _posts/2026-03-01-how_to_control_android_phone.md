---
title: "How to control phone airplane mode from linux laptop"
date: 2026-03-01
categories: [Academic, Career]
tags: [Job Application, Research Statement, Teaching Statement]
excerpt: "Key points and structure ideas for preparing an academic job application."
---


## How to control android phone from linux  

### 1 set phone to be dev and debug mode


### 2 Install adb on pc
sudo apt install android-tools-adb android-tools-fastboot -y

### 3 add rules
sudo vim /etc/udev/rules.d/51-android.rules
add
      SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", MODE="0666"

### apply rules
sudo udevadm control --reload-rules
sudo udevadm trigger

### check device status
adb devices

### enable airplane mode
adb shell settings put global airplane_mode_on 1
adb shell am broadcast -a android.intent.action.AIRPLANE_MODE --ez state true

### disable airplane mode 
adb shell settings put global airplane_mode_on 0
adb shell am broadcast -a android.intent.action.AIRPLANE_MODE --ez state false
 

