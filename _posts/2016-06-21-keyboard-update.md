---
layout: inner
title: 'Keyboard Scratchbuild Update'
date: 2016-06-21 15:53:00
categories: Projects
featured_image: 'http://imgur.com/X2kRB2r.png'
excerpt: 'An update to my previous post on my mechanical keyboard scratch build'
tags: Mechanical Keyboard scratch build 
---
You can view the previous post about my scratch build [here](/ECE-561-keyboard.html)

# Progress

In addition to everything that was already completed, I have began to work on a PCB for the keyboards. PCB's make this keyboard much easier to put together than hand-wiring as I have done so far. To make the PCB I am using KiCad, and footprint libraries from [stormbard](https://github.com/stormbard/Keyboard.pretty). I created my own schematic for the switches because I wanted them to align properly with the grid. 

## Layout: 

The layout above is what was cut into the aluminum top plate. I have been asked by my roommate to change the backspace key into two keys. We tested this, and it will work properly with the existing plate. There are other problems though. Row 4 and row 3 both have 15 keys; rows 2 and 1 have 14; row 0 has 12 (Keyboard rows are denoted from bottom up, so space bar row is row 0). This means that if I were to change backspace to two keys I would have 16 columns in row 4, which would require an extra pin on the microcontroller. This is not a huge deal, but I have not made the changes yet because I am not sure if I will have enough pins to spare.   

<a href="http://i.imgur.com/a5uDPmo.png">
  <img src="http://imgur.com/a5uDPmol.png" />
  <b>Click Me!</b>
</a>

## Schematic:

In the schematic below you can see how the keyboard will be wired together. There are diodes connecting the switches to the rows to prevent ghosting. This schematic is carried over into the PCB Footprint below. It is basically a template before adding the traces and figuring out what layer to put everything on. I have never worked with KiCad before, and my only experience with anything similar is with Cadnce in school. It has been quite a journey 

<a href="http://i.imgur.com/X2kRB2r.png">
  <img src="http://imgur.com/X2kRB2rl.png" />
  <b>Click Me!</b>
</a>



## PCB Footprint

The footprint is coming along nicely. This is the keyboard layer, you can see the tags on the right and bottom which connect to the Backlight layer (below).

<a href="http://i.imgur.com/WycN2Wa.png">
  <img src="http://imgur.com/WycN2Wal.png" />
  <b>Click Me!</b>
</a>

## Backlighting Schematic

This has been the hardest part of the project. Controlling LED's individually with a very small number of pins is pretty easy with an LED Matrix, but I needed to modify it to work with the teensy instead of the Arduino. This part of the project is still a work in progress, and hooking up 5 rows and 15 columns of LED's on a breadboard is quite tricky. Honestly, the breadboard might be a bottleneck for the whole project at this point. If I had a PCB with the rows and columns properly connected I could try my design faster, but I am scared to make a PCB before I know the design works. It is a tough situation. I might just build a single sided test PCB with a CNC Machine where only a few random rows and columns are connected, and the rest are just open. If each row works, and several of the columns work I will go ahead and get the full sized PCB built and try it out.  

<a href="http://i.imgur.com/OfUadOv.png">
  <img src="http://imgur.com/OfUadOvl.png" />
  <b>Click Me Too!</b>
</a>

## Other Problems

I really do not want to use the whole Teensy 2.0 board and attach it to the PCB, so I will have to get the microconroller separate. I have never worked with a Microcontroller outside of the microcontroller board. It will be an interesting experience to try it out and find out how much of the teensy board is necessary or unnecessary. It has been an expensive and exciting journey so far, and I am only half way there. I do have a working keyboard prototype (see the scratch build post), but that may have been the easy part. I will keep updating you (my dearest google web crawler, and people from the UK who found my blog somehow and visit a surprising amount) of any progress that I make on this project.
