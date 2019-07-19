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

* navigate to `sim-arduboy` folder:
``` ShellSession
> cd sim-arduboy
```

* copy `22_ArduBoy` folder to the desires Launcher's menu folder. \
e.g. for main menu copy to `/home/cpi/apps/Menu`:
``` ShellSession
> cp -r ~/games/ArduBoy/sim-arduboy/22_ArduBoy ~/apps/Menu/
```

* restart the Launcher on _GameSH>_ (or reboot it)

* put some ArduBoy games (hex-files. you can find some [here](https://community.arduboy.com/c/games)) into `/home/cpi/games/ArduBoy` folder

* launch `ArduBoy` from Menu, and select desired game from the list 

* have fun (use `A` and `B` buttons to action/back,`menu` button to exit)

##### To rebuild "ArduBoy" by yourself

* SSH to your _GameSH>_
* setup Dependencies:

``` ShellSession
> sudo apt update && sudo apt install build-essential libelf-dev libsdl2-dev freeglut3-dev
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