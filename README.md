# ReaLearn SY - Softsynth parameter mapping presets for ReaLearn
Presets for ReaLearn ([Homepage](https://www.helgoboss.org/projects/realearn/), [GitHub](https://github.com/helgoboss/realearn), [Reaper discussion thread](https://forum.cockos.com/showthread.php?t=178015)) that map the control elements of Controllers (for example Behringer X-Touch Mini) or hardware synthesizers (for example Sequential OB-6) to Software Synthesizers like u-he RePro or TAL J-8.

ReaLearn is a plugin for the [Reaper](https://www.reaper.fm) DAW (Digital Audio Workstation).

# Introduction
Based on the fantastic ReaLearn plugin, I created Mapping Presets for several analog-synth VSTs, to be controlled from OB6, Prophet-6, X-Touch Mini or Midiplus X2 to X6 mini. With these presets, you can control up to 90 parameters in the VSTs from your controller (or suitable hardware synthesizer). Because it is based on ReaLearn, feedback is supported (parameter settings are instantly shown if you use a controller with LED-ring encoders like the X-Touch Mini).

In addition to the analog-synths, I created presets for the Dexed synthesizer, which follow a similar concept but use a completely different virtual parameter set.

# Features in Detail
Standard set of 92 virtual parameters, so Controller Mappings and Main (VST-specific) Mappings are _independent from each other_.
This allows mapping presets for other controller devices (or hardware synthesizers that allow this) and other analog-synth VSTs to be created (with moderate effort), that will then work with the existing presets.

Currently available controller presets (Controller Mappings): 
- Behringer X-Touch Mini (8 Encoders, 16 buttons)
- Midiplus X2 to X6 mini
- Sequential OB6 (new 2022/04: absolute and relative modes)
- Sequental Prophet-6 (new 2022/04: absolute and relative modes)

Currently available VST presets (Main Mappings): 
- TAL J-8
- TAL U-No
- TAL BaseLine 101
- u-he Repro (1 and 5)
- u-he Diva
- u-he Hive
- Sonicprojects OP-X Pro II
 
VST preset with a different parameter set ("DX" instead of "SY"): 
- Dexed

Important Restriction:
The presets were developed and tested with the VSTi version of these softsynths. With VST3i and AUi, problems can occur. (In some cases the parameter numbers differ between AUi and VSTi. There are also sometimes differences between VSTi and AUi for the behavior regarding parameters with discrete values.)

# Requirements and How To

You need 
- Reaper
- ReaLearn (available via ReaPack or GitHub) (Version 2.8.2 or higher, but not 2.9 flat)
- One of the currently supported synthesizers/controllers, see list above
  - If you have some time and skills, you can create a Controller Mapping for other devices, using the existing presets as template. If you do this, please share your Mapping!
- One of the currently supported VSTs, see list above
  - Similarly, you can create Main Mappings for other analog synth VSTs. Again, it would be nice to add these Mappings here.

How to:
- Install the ReaLearn SY mapping presets via ReaPack or directly
  - Via ReaPack: like ReaLearn, but use repository URL https://github.com/vonglan/reaper-packages/raw/main/index.xml
  - Directly: download individual files from here: https://github.com/vonglan/realearn-sy-presets and put the presets in the corresponding Reaper folders Data/helgoboss/realearn/presets/controller and .../main (to navigate to these folders, use: Reaper menu Options / Show REAPER Resource Path in explorer/finder)
- Depending on the controller, some configurations on the controller have to be made, see below
- Put a ReaLearn instance in the same track as your VST, before it
- In ReaLearn, load the suitable Controller Mapping and Main Mapping
- In ReaLearn, select Control Input = <FX input> and your device as Feedback output
- Ready!

# VST Mapping Details (for Dexed, see at the end)

## TAL J-8
The two layers (lower and upper) are controlled with the "Other Layer" knob.
Note that there can be a mismatch between the layers (displayed layer is not the one that is currently controlled). In this case, change the layer in the VST GUI).

## u-he Hive
In this case, "Other Layer" switches between left and right side.

## Sonicprojects OP-X Pro II
This plugin was configured and tested with the VST3 version.

Some special mappings:		

|Virtual Parameter|OP-X Target|
|---|--------------|
|Osc2 PW|Spread (Osc Tuning)|
|HP Cutoff|Filter Type|
|Feedback Level|Filter Damping/Brilliance|
|LFO1 Sync|Wheel LFO|
|ModMx1Amount|Aftertouch Vibrato Amount|
|ModMx2Amount|Aftertouch Filter Amount|
|ModMx3Amount|Env PW Amount|
|Unison Mode|Filter Slop|
|Layer Mix|Envelope Slop|

Some parameters trigger multiple targets, to work intuitively.
In the case of
- Cutoff Velocity Modulation
you need to make sure to deactivate the Hold/VEL button manually, if you want to switch off the Velocity Modulation (just setting it to 0 is not the same).

# Controller Mapping Details

## Behringer X-Touch Mini

### General Configuration
- You need to configure MinValue for all Encoders to Relative1 via the preset files [here](https://github.com/vonglan/realearn-sy-presets/tree/main/resources), or as described in ReaLearn User’s Guide for the X-Touch compact https://www.helgoboss.org/projects/realearn/user-guide#behringer-x-touch-compact
- Currently (March 2021) the Behringer Editor for this is only available for Windows. But it is portable and only required once, so it is worth the effort, even if you normally use OS-X.
	
### Used controller elements	
- Layer A is for Analog Synth
- The 8 encoders work in 9 banks
- Pressing an encoder resets the parameter to a "neutral" value
- The upper row of buttons is for selecting the first 8 banks
- In the lower row
  - the 4 first buttons are for functions in the selected bank
  - Buttons 5 and 6 are reserved, for example for a “Zoom” function, see https://github.com/helgoboss/realearn/issues/204
  - button 7 is for selecting "alternate layer" (for synths like Hive or J-8). (This is duplicate to General / Button 3)
  - the last button is for selecting bank 9
- Details: see tables below or in [Banks of 8 Layout](https://github.com/vonglan/realearn-sy-presets/tree/main/doc)

![image](https://user-images.githubusercontent.com/17814756/116811138-f8cacc80-ab47-11eb-91f8-7e857d70d49d.png)

![image](https://user-images.githubusercontent.com/17814756/116811206-5232fb80-ab48-11eb-9ce1-f6f5c4eb23a0.png)

### Unused controller elements
- Layer B is not used (could be used for controlling Reaper functions)
- The fader is not used

## Midiplus X2 to X6 mini

### General Configuration
- According to the manual, this should work for Midiplus X2 to X6 mini. I tested with X3 mini
- If you have changed anything, reset to Factory Default: hold button 1 and 2 while unplugging and replugging the Midiplus, keep holding for 3 seconds after power-up. "rst" is displayed
- Press shift and each of the 6 buttons, to change the color to blue (default is red).
	
### Used controller elements	
- The 6 buttons select the bank.
- The 4 knobs control 4 parameters for each bank.
- Details: see table below or in [Banks of 4 Layout](https://github.com/vonglan/realearn-sy-presets/tree/main/doc) 

![image](https://user-images.githubusercontent.com/17814756/116825824-2ee06e80-ab91-11eb-9609-3fbb31318279.png)

## Sequential OB-6

### General Configuration	
Switch “Param Xmit” and “Param Rcv” to NRPN:
-	Globals
- 5 (then again for 6)
-	Use Bank and Tens to select "nr", if not already selected
-	Globals	
		
### Shift Function

|OB6|Virtual Target|
|---|--------------|
|Arp On/Off|SHIFT|
|Osc 1 Freq|Osc 1 Pitch Fine|
|Osc 2|Osc 3|
|Noise Mix|Feedback Level|
|Filter Freq|HP Cutoff|
|LFO|LFO 2|
|X-Mod F.Env|Mod Matrix 1 Amount|
|X-Mod Osc2|Mod Matrix 2 Amount|
|Osc1 Pulsewidth|Layer Mix|
|Osc1 Waveform|Osc CrossMod/FM|
		
### Special		

|OB6|Virtual Target|
|---|--------------|
|LFO Mod Switch: Filter Mode|RELATIVE MODE (new 2022/04)|	
|BP|BP or Filter Slope|
|LFO Initial|Amount LFO1 Decay|
|LFO VCO 2|Pitch Env Amount|
|X-Mod F.Env| Mod Matrix 1 Amount|
|X-Mod Osc2|Mod Matrix 2 Amount|
|AmpEnv Velo|Other Layer|

Some continuous parameters for which the OB6 only offers a button (like Filter Keytrack) work with an "incremental button" mechanism

LFO Shape: moving (up or down) always increments by 1.	
		
### Unused Buttons		
-	All AT Mod Switches	
-	All Xmod Switches	

### Unused Knobs		
-	AT Mod	
-	Arp Range	
-	Tempo	

## Sequential Prophet-6

I did not test this (because I do not have a Prophet-6), I only created it based on the OB6 mapping and the Prophet-6 documentation.
Especially, I am not sure whether the buttons LFO LP, HP and Amp are correctly mapped – please tell me if these are wrong.

### General Configuration	
Switch “Param Xmit” and “Param Rcv” to NRPN:
-	Globals
- 5 (then again for 6)
-	Use Bank and Tens to select "nr", if not already selected
-	Globals	
		
### Shift Function

|Prophet-6|Virtual Target|
|---|--------------|
|Arp On/Off|SHIFT|
|Osc 1 Freq|Osc 1 Pitch Fine|
|Osc 2|Osc 3|
|Noise Mix|Feedback Level|
|LFO|LFO 2|
|PolyMod F.Env|Mod Matrix 1 Amount|
|PolyMod Osc2|Mod Matrix 2 Amount|
|Osc1 Pulsewidth|Layer Mix|
|Osc1 Waveform|Osc CrossMod/FM|
		
### Special		

|Prophet-6|Virtual Target|
|---|--------------|
|LFO Mod Switch: Freq 2|RELATIVE MODE (new 2022/04)|	
|HP Velo Env Amount|BP or Filter Slope|
|LFO Initial|Amount LFO1 Decay|
|LFO VCO 2|Pitch Env Amount|
|PolyMod F.Env| Mod Matrix 1 Amount|
|PolyMod Osc2|Mod Matrix 2 Amount|
|AmpEnv Velo|Other Layer|
|HP Resonance|Filter Type|

Some continuous parameters for which the Prophet-6 only offers a button (like Filter Keytrack) work with an "incremental button" mechanism

LFO Shape: moving (up or down) always increments by 1.	
		
### Unused Buttons		
- All AT Mod Switches	
- All Xmod Switches
- HP Key Amount	

### Unused Knobs		
- AT Mod	
- Arp Range	
- Tempo	
- HP Env Amount

# Special: [Dexed](https://asb2m10.github.io/dexed/) (Open Source FM Synthesizer)
Instead of the usual "SY" presets, this has the prefix/suffix "DX". Controller and Main Mapping are required.

## With Behringer X-Touch Mini as controller

The upper row of buttons select the operator (or global / all), the lower row buttons select the area:

![image](https://user-images.githubusercontent.com/17814756/118041818-90fc5900-b373-11eb-9a8b-7c5c0180f5a0.png)

Depending on this selection, the encoders then control all of Dexed's parameters:

![image](https://user-images.githubusercontent.com/17814756/118041370-fef45080-b372-11eb-9fad-f47fda8687a9.png)

Pressing an Encoder resets the parameter to an initial value.
Exception: All Operators / Level/Active toggles Operator active/inactive

## With OB-6

This does not work as well, because the OB-6 does not have encoders (and [this ReaLearn feature request](https://github.com/helgoboss/realearn/issues/203) has not yet been implemented).

The X-Modulation buttons select the operator (or LFO VCO1/2 for global / all), and the lower row LFO buttons select the area:

![image](https://user-images.githubusercontent.com/17814756/118182722-9de38000-b439-11eb-9768-d86617b58a26.png)

The 8 envelope knobs (without "Amount") are used to change parameters (individual assignment see above for X-Touch Mini):

![image](https://user-images.githubusercontent.com/17814756/118182833-bbb0e500-b439-11eb-91f6-f6d7d9121b7f.png)

## With Prophet-6

Similar to OB-6 (and I haven't tested it myself).

The LFO and Aftertouch buttons select the operator (or global / all), and the Poly Mod buttons select the area:

![image](https://user-images.githubusercontent.com/17814756/118183147-10ecf680-b43a-11eb-8d5a-f573b81762a4.png)

Like for the OB-6, the 8 envelope knobs (without "Amount") are used to change parameters (individual assignment see above for X-Touch Mini).

![image](https://user-images.githubusercontent.com/17814756/118183383-54476500-b43a-11eb-8692-67f2ad293fa0.png)
