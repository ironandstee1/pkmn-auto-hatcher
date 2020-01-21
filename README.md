# Pokemon Sword/Shield auto hatcher

Automatically hatches pokemon in sword and shield with the aim of allowing users to farm shinies overnight. 

Scripts are currently complete for the following:
* 10240 base egg steps multi hatching (~10:00 for 3-5 eggs)
* 2560 base egg steps single egg hatching (~1:50/1 egg)
* 3840 base egg steps single egg hatching (~2:15/1 egg)
* 5120 base egg steps single egg hatching 
* 7680 base egg steps single egg hatching
* 10240 base egg steps single egg hatching
* 5 box release (releases 5 consecutive boxes of pokemon)

Scripts in the development stage:
* Multi hatching for all other egg steps
* Surprise trading
* Link trading

If you would like to just download the hex files for flashing, just click the link above. The directions on thie Readme are specifically for people who want to make the files themselves, either for the purpose of understanding or changing the code. 


## Requirements

### Hardware
* Teensy++ 2.0 
  * Teensy 2.0 may also have the ability to load and run these scripts, but not all will be compatible due to the hardware constraints.
  * Other hardware may also have the ability to be flashed and use these scripts (Arduino Uno, Leonardo, Pro Micro) but I will not be providing instructions for this. 
  * Must also have one of those fatter microUSB cables


### Software
* [Teensy Loader](https://www.pjrc.com/teensy/loader.html)
* [Atmel Gnu Toolchain](http://fab.cba.mit.edu/classes/863.16/doc/projects/ftsmin/windows_avr.html)
  * This is necessary if you want to build the code or edit the scripts in any way
  * I followed this tutorial up to installing avrdude
* [Git for windows](https://gitforwindows.org/)
  * Again, only necessary if ou want to build the code or edit the scripts in any way
  * Can be used to clone this repo as well, but downloading as zip will do

## How to use this

### Loading the script
1. Download the appropriate hex file for your pokemon's egg steps.
  * Hex files can be found [here]
  * A list of pokemon egg steps can be found here [https://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_base_Egg_cycles]
1. Plug your Teensy++ 2.0 into your computer
1. Load the Teensy Loader program
1. Click the Open Hex File button (a little gray list) and select the hex file
1. Press the button on the Teensy++ 2.0. You should now see it appear in the Teensy Loader program
1. Press the program button (green arrow going into the hole) 

### Preparing in game

1. Get the oval charm. Multi hatch scripts avoid some of the pitfalls of not having this, but this improves the efficiency. 
1. Get a pokemon with flame body in your party slot 6. I grabbed carkoal from the mine tracks as they can be easily caught due to low level and some already have the ability.
1. Make sure that your party is full and there are no eggs. 
1. Put your pokemon to breed in the daycare (look up the Shiny Charm and Masuda method - both will help your shiny chances)
1. Run around until the day care lady has an egg but don't grab it just yet. 
1. Warp to route 5. Make sure you are not on your bike. Make sure that when you open the menu that "Town Map" is where your selection defaults to when you press X. Don't move from in front of the camp. The script is pretty sensitive to positioning. If you need to, warp again once you're ready. 

### Getting going

1. Disconnect all your controllers from your switch. Attached joycons and procons included. If you are in the game this should not cause any issues and you will not see any pop ups. 
1. Plug the Teensy into one of your dock ports. 
1. Once your character walks up and starts talking to the day care lady and gets the first egg, you should be good to go

More specific instructions for certain scripts like Release and Surprise Trade can be found [here](https://github.com/ironandstee1/pkmn-hexes).

## Improvements from past scripts

* Added C macros
  * Simplifies the process of calling repetitive actions
  * Improves readability and editability of scripts
  * Main scripting work has been shifted off to the header file instead of the c file
* Added new buttons and button macros - not a large improvement, but these are available

## Future work

* Complete missing scripts
* Create videos for how to use the software
* Test timing for every script
* Create documentation and functions for future users

### Thanks

Thanks to Shiny Quagsire for his [Splatoon post printer](https://github.com/shinyquagsire23/Switch-Fightstick) and progmem for his [original discovery](https://github.com/progmem/Switch-Fightstick).

Thanks to [bertrandom](https://github.com/bertrandom/snowball-thrower/) the foundation of this script/method.

Thanks as well to all other contributors to previous projects. 
