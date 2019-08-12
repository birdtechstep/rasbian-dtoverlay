# rasbian-dtoverlay
MakerLAB35 Display 3.5 Inches. 480x320 18 bits color [ili9488] with Capacitive touchscreen [ft6236] 

## Compile dtb and put it directly into it's destination:
~~~~
sudo dtc -@ -I dts -O dtb -o /boot/overlays/foo.dtbo foo-overlay.dts
~~~~
## cmdline.txt
~~~~
fbcon=map:10 fbcon=font:VGA8x16
~~~~
## config.txt
~~~~
dtoverlay=makerlabtft35-capacitive
dtparam=speed=62000000
dtparam=fps=60
dtparam=touch-swapxy=true
dtparam=touch-invx=true
~~~~

## PIN CONNECT
~~~~
DISPLAY SPI
cs-gpios    = CE0
sclk-gpios  = SCLK
mosi-gpios  = MOSI
miso-gpios  = MISO
dc-gpios    = BCM24 [pin18]
reset-gpios = BCM25 [pin22]
led-gpios   = BCM23 [pin16]
Capacitive Touch I2C
interrupts  = BCM17 [pin11]
~~~~
### BIRD TECHSTEP
