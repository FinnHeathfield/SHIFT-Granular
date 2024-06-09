# SHIFT-Granular
 A 4-voice granulator combining Fluid Corpus Manipulation and Spatialisation with a custom TouchOSC controller.

The instrument generates a fluid corpus of sounds from a folder of samples which can then be traversed using the mouse. Once a sample is selected, it is played by the voice selected in the controller. The controller can controll and automate 15 parameters for each voice:
1. Azimuth and Distance (radar controller)
2. Single Grain Fire
3. Granulator On/Off
4. Grain Rate
5. Pitch
6. Adder (actually sets range of pitches that can be selected)
7. Reverb Livness
8. Cross Freq.
9. HF Damp
10. Reverb W/D
11. Reverb Level
12. Filter Type (LP, HP, BP, BS, PN, LS, HS)
13. Cutoff
14. gain
15. Q

There is then also a master gain controll for each voice controllable at all times.

PANIC turns off the DSP then resets values to initials.

RESET resets values of initials.

## Setup
The Max patch itself is annotated with further explanation of the coding and setup processes.

You will need to specfy a file path of a folder of audio sources to generate the corpus from and paste it into one of the message boxes above the conformpath object.

OSC messages are notmally sent from TouchOSC on 7001 and return messages are recieved on 7002 but these are all configurable. 

This project runs best on a private network. I just used an old WIFI router and when my devices asked if I wanted to connect despite no wifi, I said yes.

## Dependancies
This patch requires the Flucoma and Spat.5 packages. [Flucoma](https://learn.flucoma.org/) is avaliable from the Max package manager. Spat.5 is avaliable from the [IRCAM website](https://forum.ircam.fr/projects/detail/spat/).
