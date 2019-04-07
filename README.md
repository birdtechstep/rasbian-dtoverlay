# rasbian-dtoverlay
MakerLAB35 Display 3.5 Inches. 480x320 18 bits color [RGB666] with Capacitive touchscreen [ft6236] 

## Compile dtb and put it directly into it's destination:
sudo dtc -@ -I dts -O dtb -o /boot/overlays/foo.dtbo foo-overlay.dts

## cmdline.txt
fbcon=map:10 fbcon=font:VGA8x16

## config.txt
dtoverlay=makerlabtft35-capacitive,touch-swapxy=true,touch-invx=true

# BIRD TECHSTEP
