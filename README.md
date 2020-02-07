# Configure Kensington SlimBlade Trackball Buttons for Ubuntu

Add following lines to the file: **/usr/share/X11/xorg.conf.d/10-evdev.conf.**

```
# Kensington Slimblade Settings

Section "InputClass"
Identifier "Kensington Slimblade Trackball"
MatchProduct "Kensington Slimblade Trackball"
MatchIsPointer "on"
MatchDevicePath "/dev/input/event*"
Driver "evdev"

Option "ButtonMapping" "1 8 3 4 5 6 7 9"

EndSection
```

Button's numbers
```
2 - middle-click
8 - backward
9 - forward 
```
Use **xev** tool to figure out the number of each button on your mouse.

And restart Service or PC

### For changing scroll speed
```
sudo apt install imwheel
cd /etc/X11/imwhell
sudo vim imwheelrc
imwheel --kill --buttons "4 5"
```

