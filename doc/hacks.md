# HiFiBerryOS hacks

Not all features can be controlled and set from the HiFiBerryOS GUI. For specific use case, we implemented some hacks that allow you to configure additional things

Note: There is no guarantee that it will work as expected. Some of these hacks might have an impact on parts of the system. We won't guarantee that these will work and
there is no support from us. Use these only if you know hat you're doing!

## Enable DSP Volume in Roon

We don't recommend to use DSP Volume control in Roon as it is not compatible with other services. If you want to try it, make sure you don't change the volume 
in the user interface or with any other service as you won't be able to change it via Roon if you use DSPVolume

Create a file /etc/hifiberry_raat.softvol and restart the system to enable Roon DSP Volume control

## Config hacks that overwrite default HiFiBerryOS behavior

### /etc/hifiberry/mixer

Put the name of the mixer control to use into this file if it isn't detected correctly

### /etc/hifiberry/has_dsp

If the file exists, HiFiBerryOS will assume that a DSP is available even if it wasn't detected correctly.

### /boot/noap

If this file exists, HiFiBerryOS will not start an WiFi access point - even if no network connection is detected.
