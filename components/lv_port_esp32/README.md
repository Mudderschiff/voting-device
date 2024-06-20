<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
# _Sample project_

(See the README.md file in the upper level 'examples' directory for more information about examples.)

This is the simplest buildable example. The example is used by command `idf.py create-project`
that copies the project to user specified path and set it's name. For more information follow the [docs page](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html#start-a-new-project)



## How to use example
We encourage the users to use the example as a template for the new projects.
A recommended way is to follow the instructions on a [docs page](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html#start-a-new-project).

## Example folder contents

The project **sample_project** contains one source file in C language [main.c](main/main.c). The file is located in folder [main](main).

ESP-IDF projects are built using CMake. The project build configuration is contained in `CMakeLists.txt`
files that provide set of directives and instructions describing the project's source files and targets
(executable, library, or both). 

Below is short explanation of remaining files in the project folder.

```
├── CMakeLists.txt
├── main
│   ├── CMakeLists.txt
│   └── main.c
└── README.md                  This is the file you are currently reading
```
Additionally, the sample project contains Makefile and component.mk files, used for the legacy Make based build system. 
They are not used or needed when building with CMake and idf.py.
=======
# esp32_ili9431
LittlevGL ported to ESP32 using ILI9341 display controller
>>>>>>> 840a043 (Initial commit)
=======
=======
# LittlevGL project for ESP32

![Example GUI with LittelvGL on ESP32](https://raw.githubusercontent.com/littlevgl/esp32_ili9431/master/screenshot.jpg)


## Get started 
### Install the ESP32 SDK
>>>>>>> a2e31c4 (Update README.md)
1. Install ESP-IDF: http://esp-idf.readthedocs.io/en/latest/
2. Get this projects: `git clone https://github.com/littlevgl/esp32_ili9431.git --recurse-submodules

### Add LittelvGL to the build
To link LittlevGL (lvgl) and lv_examples with ESP-IDF you need to add a **component.mk** file to each directory. Next to this REAMDE file you find two example component.mk files
- lvgl_component.mk
- lv_example_component.mk
Rename them to component.mk and copy to the lvgl and lv_examples directories.
<<<<<<< HEAD
>>>>>>> c507182 (move from lv_project)
=======

### Flash to ESP32
1. If you are not in the project's diectory: `cd esp32_ili9431`
2. `make`
3. `make flash`

## Drivers
This project comes with an **ILI9341** display driver and an **XPT2046** resistive touchpad driver. Both devices are communicating via SPI.

### ILI9341
The default pinout is:

| Name | Pin |
|------|-----|
| MOSI | 13 |
| SCLK | 14 |
| CS | 5 |
| DC | 19 |
| BCKL | 23 |
| RST | 18 | 

You can modify the pin configuration in `drv/disp_spi.h` and `drv/ili9341.h`

For ILI9341 HSPI is used.


### XPT2046

The default pinout is

| Name | Pin |
|------|-----|
| MOSI | 32 |
| MISO | 25 |
| SCLK | 26 |
| CS | 33 |
| IRQ | 25 |

You can modify the pin configuration in `drv/tp_spi.h` and `drv/spt2046.h`

For XPT2046 VSPI is used

>>>>>>> a2e31c4 (Update README.md)
