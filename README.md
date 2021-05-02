# ReaLearn SY - Softsynth parameter mapping presets for ReaLearn
Presets for ReaLearn ([Homepage](https://www.helgoboss.org/projects/realearn/), [GitHub](https://github.com/helgoboss/realearn), (Reaper discussion thread)[https://forum.cockos.com/showthread.php?t=178015]) that map the control elements of Controllers (for example Behringer X-Touch Mini) or hardware synthesizers (for example Sequential OB-6) to Software Synthesizers like u-he RePro or TAL J-8.

ReaLearn is a plugin for the [Reaper](https://www.reaper.fm) DAW (Digital Audio Workstation).

# Introduction
Based on the fantastic ReaLearn plugin, I created Mapping Presets for several analog-synth VSTs, to be controlled from OB6, Prophet-6, X-Touch Mini or Midiplus X2 to X6 mini. With these presets, you can control up to 90 parameters in the VSTs from your controller (or suitable hardware synthesizer). Because it is based on ReaLearn, feedback is supported (parameter settings are instantly shown if you use a controller with LED-ring encoders like the X-Touch Mini).

# Features in Detail
Standard set of 92 virtual parameters, so Controller Mappings and Main (VST-specific) Mappings are _independent from each other_.
This allows mapping presets for other controller devices (or hardware synthesizers that allow this) and other analog-synth VSTs to be created (with moderate effort), that will then work with the existing presets.

Currently available controller presets (Controller Mappings): 
- Behringer X-Touch Mini (8 Encoders, 16 buttons)
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

Advanced features planned by Helgoboss: 
- „make relative“ function for normal (absolute) knobs (Vote for this [here](https://github.com/helgoboss/realearn/issues/203))
- zoom function for fine control of parameters (Vote for this [here](https://github.com/helgoboss/realearn/issues/204))

# Requirements

You need 
- Reaper
- Version 2.8.2 of ReaLearn (available via ReaPack or GitHub)
- One of the currently „supported“ synthesizers/controllers
- One of the currently „supported“ VSTs
- If you have some time and skills, you can create a Controller Mapping for other devices, using the existing presets as template.
- Similarly, you can create Main Mappings for other analog synth VSTs

# HowTo
- Install the ReaLearn SY mapping presets via ReaPack or directly from here: https://github.com/vonglan/realearn-sy-presets
- If you did not use ReaPack: put the presets in the corresponding Reaper folders Data/helgoboss/realearn/presets/controller and .../main (to navigate to this folder, use: Reaper menu Options / Show REAPER Resource Path in explorer/finder)
- Depending on the controller, some configurations on the controller have to be made, see below
- Put a ReaLearn instance in the same track as your VST, before it
- In ReaLearn, load the suitable Controller Mapping and Main Mapping
- In ReaLearn, select Control Input = <FX input> and your device as Feedback output
- Ready!

# VST Mapping Details

## TAL J-8
The two layers (lower and upper) are controlled with the "Other Layer" knob.
Note that there can be a mismatch between the layers (displayed layer is not the one that is currently controlled). In this case, change the layer in the VST GUI).

## u-he Hive
In this case, "Other Layer" switches between left and right side.

# Controller Mapping Details

## 

