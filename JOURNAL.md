---
title: "BuzzerBox"
author: "@dld"
description: "Physical Minecraft Jukebox that plays discs!"
created_at: "2025-06-14"
---
Just gonna copy and paste the README for now, until I start working on it:

This project is game-show style buzzers, powered by Arduino and a Raspberry Pi Zero 2 W. Here's the rundown of how it'll work:

- There'll be 4 buzzer boxes and a central box.
  - The buzzer boxes will be powered by some sort of Arduino-based device, possibly an ESP8266 or ESP32, but might use a different method of transmitting depending on how it ends up working. They'll have a big red button on the top and a 7 segment display on the front. They'll likely have small speakers in them as well.
  - The central box will be powered by a Raspberry Pi Zero 2. All the real magic will happen here. It'll have a bunch of different buttons and lights and displays to show different things, not exactly sure what yet! It'll also have a speaker to play sounds.
- The main function of the project will be game show mode. In that mode, it'll function like game show buzzers, where a question is asked, and then when someone presses the buzzer, it'll transmit a signal to the central hub. It'll then check which signal it received first, then send a signal back to all of the other boxes saying which one was first, cueing that box to light up. You'll be able to give or subtract points from the central box.

### June 14, 2025

1:15 PM: Starting research on this now. Gonna just jot down the feature list, then I'll start researching.

- Buzzer Boxes (4 of them)
  - Arduino inside, probably hooked up to an NRF24L01
  - Big red button on top (might be hard to find, preferably not AliExpress, I have a strong desire to avoid it at all costs, but I can't find it for a good price anywhere else, after a very brief look though)
  - 4 digit 7 segment display to show points (possible link [here](https://www.amazon.com/dp/B0BFQNFX6D))
  - Small speaker to play buzzing noises
  - If possible, a 16x2 LCD display for displaying names and potentially error messages? Found a 5 pack [here](https://www.amazon.com/dp/B07T8ZG5D1)
  - Battery pack
  - On/Off Switch (might come with battery pack)
- Central box
  - Raspberry Pi Zero 2 W as a control hub, also with an NRF24L01
  - Button array to add points, will elaborate on this after I finish the list out
  - Speaker, probably same system I used as the Jukebox
  - The leftover 7 segment display and 16x2 LCD
  - Maybe a big button too, because I'll likely find it it a 5 pack as well and might as well use it
 
For the button, I found a couple Amazon listings, but they're more of a color variety pack. Wanted them to all be red, but it could work still. They have [6cm](https://www.amazon.com/dp/B01M7PNCO9) and [10cm](https://www.amazon.com/dp/B086ZNTZ8H) diameter buttons. The one issue I see with this is that they use 12V LED lights. Hopefully I can swap them out with normal LEDs but can't be fully sure.

I want to use a [4x4 keypad](https://www.amazon.com/dp/B07ZQFCS91) on the central box. ABCD will coorespond to selecting the box to communicate with (pressing it will bring up the points of that box on the central 7 segment display), the keypad will function to set individual points, and I'll scratch off the pound and star keys and make them plus and minus keys, to just go and add points when someone gets it.

Not fully done working yet but I am gonna commit this so far. Been working for like an hour and 15 minutes.

2:35 PM: Continuing work so far.

Trying to figure out what Arduino board to use. There's 5V stuff here, so I can't use a Pico. Leaning towards a Nano, although I haven't used them before. Also found some decent looking battery packs [here](https://www.amazon.com/dp/B0DK2SYS2Y). 

Rough estimate of cost (not including filament and before tax):

- Central Box: 37.80
  - [Raspberry Pi Zero 2 W](https://www.microcenter.com/product/643085/raspberry-pi-zero-2-w): 14.99
  - [LCD Display](https://www.amazon.com/dp/B07T8ZG5D1): 2.78 (pack of 5)
  - [4 Digit 7 Segment Display](https://www.amazon.com/dp/B0BFQNFX6D): 1.60 (pack of 5)
  - [Big Button](https://www.amazon.com/dp/B01M7PNCO9) (assuming we do the 6cm ones): 3.78 (pack of 5)
  - [Keypad](https://www.amazon.com/dp/B07ZQFCS91): 5.75
  - [I2S Amp](https://www.microcenter.com/product/613583/adafruit-industries-max98357a-i2s-3w-class-d-amplifier-breakout): 5.95
  - [Speaker](https://www.microcenter.com/product/612824/adafruit-industries-speaker-3-diameter-4-ohm-3-watt): 2.95
- Buzzer Box: 14.04
  - [Arduino Nano](https://www.amazon.com//dp/B0B3CHSWKZ): 2.38 (pack of 4)
  - [LCD Display](https://www.amazon.com/dp/B07T8ZG5D1): 2.78 (pack of 5)
  - [4 Digit 7 Segment Display](https://www.amazon.com/dp/B0BFQNFX6D): 1.60 (pack of 5)
  - [Big Button](https://www.amazon.com/dp/B01M7PNCO9) (assuming we do the 6cm ones): 3.78 (pack of 5)
  - [Piezo Buzzer](https://www.amazon.com/dp/B07VK1GJ9X) (was gonna do speakers but realized I'd need an audio file on there which would mean an SD card, not gonna get into that): 1.75 (only costs so much because it's a pack of 10, it actually costs 70 cents per but it was cheaper to buy a pack of 10 than 4 of them)
  - [Battery Pack](https://www.amazon.com/dp/B0DK2SYS2Y): 1.75 (pack of 4)

Committing this now, I've worked a total of 2 hours and 15 minutes so far.


### June 15, 2025

12:50 PM: I didn't continue working on it yesterday, but I am now! Gonna try to work on CAD, unfortunately TinkerCAD won't fit the bill this time around, so Onshape it is!
