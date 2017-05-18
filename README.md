# chainsaw
A synth made in Pure Data that is inspired by a Supersaw waveform. Chainsaw is a 4 voice polyphonyc synth.

Project Purpose

Use this patch in music production is my ultimate goal. Also future plans (or dreams) involve this patch in a workstation app for Raspberry Pi and Android Devices that will emulate Computer-less music production on a computer (that doesn't sound right, i know). But for mow I wnat to use it in my small synth rig on a Raspberri pi with Midi keyboard attached.

TODO:
1. Test this on Raspberry Pi (and I don't know how to compile [moog~] for the Pi)
2. Make Sawtooth, Square and Sine waves for LFO and replace Volume controlling knob with LFO waveform selection
3. Create a GUI that actualy looks like a synth for this patch. this will probably envolve making this patch an abstrastion.
4. Make computer keyboard play notes on this synth.
5. Create own resonant low pass filter abstration if possible
6. Create effects rack (od/fuzz/clip, delay, reverb at least)

Dependencies:
Pure Data Pd 0.47.1
Ggee [moog~] external

Installation

1. Install Pure data on your system
2. Install Ggee externals library or just the moog~ external
3. Run chainsaw.pd file with PD

Included Abstractions

supersaw.pd - an oscillator which accepts midi notes and modulation messages for detuning. Outputs signal
adsr.pd - an ADSR envelope. Accepts signal, velocity. Outputs signal, modulation ammount at the signal rate.  Atack, Decay, Sustain, Release are received inside the abstraction. // TODO: move receiving parameters to inlets
apkknobs.pd - an abstraction mapping 8 midi knobs (cc 1-8) to outlets. Since I have only 8 midi knobs on my controller, I used moses to control ADSR with just one knob

Synth Architecture

midi note > oscillator > Envelope > Filter > DAC

About the author

I'm a non professional and non commercial musician. I play guitar and now some synths also. When I got my first analog synth I was blown away with what you can do if you don't have to navigate menus for doing stuff. So in this project I will try my best to stick with "One Knob = One Function" concept. (at least for my APK Mini)

