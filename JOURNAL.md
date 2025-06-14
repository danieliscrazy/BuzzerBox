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
  - 4 digit 7 segment display to show points (possible link [here](https://www.amazon.com/WWZMDiB-Module%EF%BC%8CLED-Brightness-Adjustable-Accessories/dp/B0BFQNFX6D))
  - Small speaker to play buzzing noises
  - If possible, a 16x2 LCD display for displaying names and potentially error messages? Found a 5 pack [here](https://www.amazon.com/Display-Module-Backlight-Arduino-MEGA2560/dp/B07T8ZG5D1)
  - Battery pack
  - On/Off Switch (might come with battery pack)
- Central box
  - Raspberry Pi Zero 2 W as a control hub, also with an NRF24L01
  - Button array to add points, will elaborate on this after I finish the list out
  - Speaker, probably same system I used as the Jukebox
  - The leftover 7 segment display and 16x2 LCD
  - Maybe a big button too, because I'll likely find it it a 5 pack as well and might as well use it
 
For the button, I found a couple Amazon listings, but they're more of a color variety pack. Wanted them to all be red, but it could work still. They have [6cm](https://www.amazon.com/EG-STARTS-Illuminated-Buttons-Operated/dp/B01M7PNCO9) and [10cm](https://www.amazon.com/dp/B086ZNTZ8H) diameter buttons. The one issue I see with this is that they use 12V LED lights. Hopefully I can swap them out with normal LEDs but can't be fully sure.

I want to use a [4x4 keypad](https://www.amazon.com/dp/B07ZQFCS91) on the central box. ABCD will coorespond to selecting the box to communicate with (pressing it will bring up the points of that box on the central 7 segment display), the keypad will function to set individual points, and I'll scratch off the pound and star keys and make them plus and minus keys, to just go and add points when someone gets it.

Not fully done working yet but I am gonna commit this so far. Been working for like an hour and 15 minutes.
