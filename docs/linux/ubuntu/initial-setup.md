# Ubuntu
## Setup after Installation
### Intro
The following instructions have been written for Ubuntu 20.04 LTS. They may slightly or largely vary since Ubuntu went through a number of changes throughout the years.
### Setup Keyboard Layout
Adding a new keyboard option to Ubuntu Gnome is not very intuitive and can be rather frustrating for that reason.

For example, one does not add a keyboard under `System Settings > Keyboard`

Instead the option is located under `System Settings > Personal > Region & Language > Input Sources > +`

When one clicks the `+` sign one will see a list of languages and this is where some confusion and frustration may ensue: This is NOT a list of keyboard options, so do not peruse this rather lengthy list looking for your desired keyboard option.

Instead, click on the language you want. When you do that a new list will appear containing the list of keyboards available for that language.

From that list click your selection then click the Add button.

### Setup Wallpaper Carousel

### Setup Temperature Sensors
Install LM-Sensors and hddtemp.

Download from the [Ubuntu Store] (https://apps.ubuntu.
com/cat/applications/lm-sensors)  or install using apt

sudo apt-get install lm-sensors hddtemp

After installation start `sensors` in a terminal to start the detection of the on-board sensors

sudo sensors-detect