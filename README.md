# RunCPM_VGA32
A fork of RunCPM for the TTGO VGA32 v1.4 & Olimex ESP32-SBC FabGL

![RunCPM_BootScreen](https://github.com/guidol70/RunCPM_VGA32/raw/main/pictures/RunCPM_v6_1_VGA32_GL20230609.jpg?raw=true)

for getting RunCPM onto the TTGO VGA32 v1.4 via a precompiled binary see:<br/>
(maybe that doesnt work for newer versions :( )<br/>
https://lehwalder.wordpress.com/2021/04/28/getting-runcpm-v5-3-fast-onto-the-ttgo-vga32-v1-4/<br/>


or use esptools.py

python3 /home/pi/esptool/esptool.py --chip esp32 --port /dev/ttyACM0 --baud 921600 --before default_reset <br/>
--after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size detect <br/>
0xe000 ./boot_app0_0xe000.bin <br/>
0x1000 ./bootloader_qio_80m_0x1000.bin <br/>
0x10000 ./RunCPM_VGA32_v6_1_24072023_0x10000.bin <br/>
0x8000 ./RunCPM_VGA32_v6_1_24072023_0x8000_0x8000.bin <br/>

<br/>
for compiling RunCPM for your TTGO VGA32 v1.4 yourself - having more options ;) - see:<br/>
https://lehwalder.wordpress.com/2021/04/07/runcpm-on-the-lilygo-ttgo-vga32-v1-4/<br/>
<br/>
This project is derived from the following projects:<br/>
<br/>
RunCPM<br/>
from Marcelo Dantas<br/>
https://github.com/MockbaTheBorg/RunCPM<br/>
<br/>
FabGL<br/>
from Fabrizio Di Vittorio<br/>
https://github.com/fdivitto/FabGL<br/>

and the 1st RunCPM fork for VGA32 / HomeBrew-VGA32<br/>
from Derek Cooper<br/>
https://github.com/coopzone-dc/RunCPM<br/>
<br/>
<br/>
Additional Links:<br/>
<br/>
RunCPM TTGO VGA32 USB & Mirror Edition in the german VzEkC-Forum <br/>
https://forum.classic-computing.de/forum/index.php?thread/23452-runcpm-v5-1-ttgo-vga32-usb-serctl-mirror-edition/<br/>
<br/>
CP/M Users and Programmers on Facebook<br/>
https://www.facebook.com/groups/cpmusers/<br/>


## GLTerm for VGA32
A fork of the FabGL ANSI-Terminal with parts of the VGA32 RunCPM-port<br>
useable as serial TTL-Terminal (GP(IO) 20&21) for the Picomite<br>
(Raspberry Pi Pico with MMBASIC)<br>

![GLTerm VGA32 BootScreen](https://github.com/guidol70/RunCPM_VGA32/raw/main/GLTerm_VGA32/GLTerm_Rev_GL22020911.jpg?raw=true)
