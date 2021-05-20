# orbsmart s92, beelink r89, ubox tv box

## bootable sd card images

- https://github.com/hexdump0815/imagebuilder/releases/tag/210509-02

## tested systems - working

- orbsmart s92 tv box

## untested systems

- beelink r89
  - should just work as i think its the exact same hardware
- ubox tv box
  - should just work as i think its nearly the same hardware

## kernel build notes

- https://github.com/hexdump0815/linux-mainline-and-mali-generic-stable-kernel/blob/master/readme.av7

## u-boot build notes

the boot loader of those tv boxes seems to be encrypted and locked and thus cannot be easily replaced, but there is a properly signed etc. boot block which can get regular linux kernel booting - i have adjusted some scripts around this to create a boot block in the proper format from a mainline linux kernel, dtb and initrd at:

- https://github.com/hexdump0815/imagebuilder/tree/main/systems/orbsmart_s92_beelink_r89/extra-files/boot/r89-boot