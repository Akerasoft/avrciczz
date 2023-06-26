avrciczz.asm - source code
avrciczz.elf - binary + fuse bits settings
avrciczz.hex - binary only.

SUT_CKSEL fuse should be set to "ext clock + 0ms" in case if avrciczz.hex was used, avrciczz.elf already contains this setting
Push the reset 4-8 times after than system region was changed, or if cic used at first time
chip pinout inside of avrciczz.asm file

avrdude -c usbtiny -p t13 -U flash:w:avrciczz.elf:e
avrdude -c usbtiny -p t13 -U lfuse:w:0x70:m -U hfuse:w:0xfb:m

