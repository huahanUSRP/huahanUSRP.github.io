---
title: "How to use tailscale to make small network"
date: 2026-03-01
categories: [Academic, Career]
tags: [Job Application, Research Statement, Teaching Statement]
excerpt: "Key points and structure ideas for preparing an academic job application."
---


## Windows PC/laptop

### Install tailscale
Open website: https://tailscale.com/download
Choose windows and download setup file
Install the software
Login with github account and click "connect"
The PC/laptop has been added to the network

### How to use tailscale
control other laptop/PC with powershell, input "powershell" from WIN+R

## Linux PC/laptop

### Install tailscale
Open website: https://tailscale.com/download
Choose linux and use the command to install tailscale
    
    curl -fsSL https://tailscale.com/install.sh | sh

### Start tailscale
Start the tailscale
         
         sudo tailscale up
         Permenant tailscale enable
         sudo systemctl enable tailscaled

### Install ssh
         sudo apt update
         sudo apt install openssh-server

## How to acces another laptop/PC
### check ip address
         tailscale status
### ssh target PC/laptop
         ssh username@ipaddress
Example:
         
         ssh otfs1@100.77.195.126
The terminal will show the target PC/laptop home folder

 
