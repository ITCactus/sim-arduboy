# ClockWorkPI Sim-Arduboy
[Arduboy](https://arduboy.com/) board implementation using simavr, \
tweaked for [ClockWork(_GameSH>_)](https://clockworkpi.com)


### How to install

* SSH to your _GameSH>_
* create folder `/home/cpi/games/ArduBoy`:
``` ShellSession
> mkdir ~/games/ArduBoy
```

* navigate to that folder, and clone the repo:
``` ShellSession
> cd ~/games/ArduBoy
> git clone --recursive https://github.com/ITCactus/sim-arduboy.git
```

* copy `22_ArduBoy` folder to the desired Launcher's menu folder. \
e.g. for main menu copy to `/home/cpi/apps/Menu`:
``` ShellSession
> cp -r ~/games/ArduBoy/sim-arduboy/22_ArduBoy ~/apps/Menu/
```

* build/rebuild:
``` ShellSession
> sudo apt-get update && sudo apt-get install build-essential libelf-dev libsdl2-dev freeglut3-dev
> cd ~/games/ArduBoy/sim-arduboy/
> make
```

* restart the Launcher on _GameSH>_ (or reboot it)

* make sure, you switched to the `Lima` GPU driver via `Settings->GPU Driver Switch->Lima driver` (with Fbturbo, emulator either running too slow, or not starting at all)

* put some ArduBoy games (hex-files. you can find some [here](https://community.arduboy.com/c/games)) into `/home/cpi/games/ArduBoy` folder

* launch `ArduBoy` from Menu, and select desired game from the list 

* have fun (use `A` and `B` buttons to action/back,`menu` button to exit)

##### To rebuild "ArduBoy" by yourself

* SSH to your _GameSH>_
* setup Dependencies:
``` ShellSession
> sudo apt-get update && sudo apt-get install build-essential libelf-dev libsdl2-dev freeglut3-dev
```

* build/rebuild:

``` ShellSession
> cd ~/games/ArduBoy/sim-arduboy/
> make
```

### Limitations
* emulation speed is not accurate (feel free to contribute improvements for it to the *current* repo)
* no sound emulated (feel free to contribute improvements for it to the *original* `sim-arduboy` repo)
* no RGB LEDs/lights emulated 


### Note
tested on *__ClockWork OS__* v0.4 and *__Launcher__* 1.25
