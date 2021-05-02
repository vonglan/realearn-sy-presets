# ReaLearn SY - Softsynth parameter mapping presets for ReaLearn
Presets for [ReaLearn](https://github.com/helgoboss/realearn), that map the control elements of controllers (for example Behringer X-Touch Mini or Sequential OB-6) to Software Synthesizers, e.g. u-he RePro or TAL J-8.

# Introduction
Based on the fantastic ReaLearn plugin which is available via ReaPack and discussed here (https://forum.cockos.com/showthread.php?t=178015), I created Mapping Presets for several analog-synth VSTs, to be controlled from OB6, Prophet-6, X-Touch Mini (8 Encoders, 16 buttons) or Midiplus X2 to X6 mini. With these presets, you can control up to 90 parameters in the VSTs from your controller (or suitable hardware synthesizer). Because it is based on ReaLearn, feedback is supported (parameter settings are instantly shown if you use a controller with LED-ring encoders like the X-Touch Mini).

# Features in Detail
Standard set of 92 virtual parameters, so Controller Mappings and Main (VST-specific) Mappings are _independent from each other_.
This allows mapping presets for other controller devices (or hardware synthesizers that allow this) and analog-synth VSTs to be created (with moderate effort), that will then work with the existing presets.

Currently available controller presets (Controller Mappings): 
- Behringer X-Touch Mini
- Midiplus X2 to X6 mini
- Sequential OB6
- Sequental Prophet-6

Currently available VST presets (Main Mappings): 
- TAL J-8
- TAL U-No
- TAL BaseLine 101
- u-he Repro (1 and 5)
- u-he Hive
Planned VST presets: 
- u-he Diva
- Sonicprojects OP-X Pro
Maybe Dexed (but that would be a different concept)

Possibly I will also create a controller preset for my old Akai APC20 (using just 8 faders and 16 pads).

Advanced features planned by Helgoboss: „make relative“ function for normal (absolute) knobs, and zoom function for fine control of parameters. (Vote for this here: https://github.com/helgoboss/realearn/issues/203 and https://github.com/helgoboss/realearn/issues/204 )


# Requirements

You need 
- Reaper
- Version 2.8.2 of ReaLearn (available via ReaPack or GitHub)
- One of the currently „supported“ synthesizers/controllers
- One of the currently „supported“ VSTs
- If you have some time and skills, you can create a Controller Mapping for other devices, using the existing presets as template.
- Similarly, you can create Main Mappings for other analog synth VSTs
