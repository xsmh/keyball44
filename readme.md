MCKWorkshop：<br/>
trackballseries firmware<br/>
本系列layout参考了:[keyball](https://github.com/Yowkees/keyball)<br/>
firmware代码是基于[Charybdis](https://bastardkb.com)的源码进行二次开发，增加了一些实用性功能<br/>
后缀为ctc的就是双type c连接的版本，不带ctc的为trs连接版本<br/>
如果你的键盘名称后缀带V2/V3使用的传感器是PMW3389传感器，如果不带后缀则使用的是PMW3360传感器<br/>
如果想编译自己的固件，只需要根据键盘后缀判断自己的传感器，然后调整各配列下v2/splinky/rules.mk中的POINTING_DEVICE_DRIVER即可<br/>


# Firmware building steps:
- Install qmk using pacman.
- Clone the (Vial fork)[https://github.com/vial-kb/vial-qmk] of qmk.
- Clone this MCK repo.
- cd into the Vial fork repo and create a symlink of the MCK repo inside the keyboards folder of the Vial repo by running `ln -s MCK_REPO_PATH keyboards`
- From the Vial repo run `git submodule update --init --recursive`
- To compile run `qmk compile -kb trackballseries/44_ctc/v2/splinky -km vial`
- Set the bootloader key on each half of the keyboard.
- Connect only one half and press the bootloader key.
- Mount the keyboard and copy the compiled .uf2 file into the mounted partition. Wait until it has finished flashing.
