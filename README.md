# BuzzerBox

This project is game-show style buzzers, powered by Arduino and a Raspberry Pi Zero 2 W. Here's the rundown of how it'll work:

- There'll be 4 buzzer boxes and a central box.
  - The buzzer boxes will be powered by some sort of Arduino-based device, possibly an ESP8266 or ESP32, but might use a different method of transmitting depending on how it ends up working. They'll have a big red button on the top and a 7 segment display on the front. They'll likely have small speakers in them as well.
  - The central box will be powered by a Raspberry Pi Zero 2. All the real magic will happen here. It'll have a bunch of different buttons and lights and displays to show different things, not exactly sure what yet! It'll also have a speaker to play sounds.
- The main function of the project will be game show mode. In that mode, it'll function like game show buzzers, where a question is asked, and then when someone presses the buzzer, it'll transmit a signal to the central hub. It'll then check which signal it received first, then send a signal back to all of the other boxes saying which one was first, cueing that box to light up. You'll be able to give or subtract points from the central box.

Gonna start work on the project now and update this README once I've got it done basically!
