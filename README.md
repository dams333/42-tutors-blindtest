# Redirect tutors dump sound to 42 sono

## Setup virtual audio device
- Run these commands (only available on tutors dump):
```bash
pactl load-module module-null-sink sink_name=vspeaker sink_properties=device.description=virtual_speaker

pactl load-module module-remap-source master=vspeaker.monitor source_name=vmic source_properties=device.description=virtual_mic
```
- Set your audio input to `virtual_mic` in Discord

## Connect your navigator to the virtual audio device

- Start `pavucontrol`
- In `playback` redirect your navigator to `virtual_speaker`
- In `input devices` check that `virtual_mic` play sound (you can manage volume from here)

## Play music

- Ask staff for access to Discord `MICRO-CLUSTER` channel
- Be in `push to talk` (Discord doesn´t like music played in `voice detection`)
- Play music in your navigator