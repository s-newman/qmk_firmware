Install `dfu-programmer` from official repos
Install `qmk` from AUR

```shell
# At root of qmk_firmware repo
qmk setup
qmk compile -kb keebio/iris/rev4 -km s-newman
# Put keyboard into reset mode
sudo dfu-programmer atmega32u4 erase --force
sudo dfu-programmer atmega32u4 flash keebio_iris_rev4_s-newman.hex 
sudo dfu-programmer atmega32u4 reset
```