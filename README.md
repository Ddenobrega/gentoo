# GENTOO 
This repository is available to the public but <b> NOT </b>intended for public use.

## Included Modules

- <a href="./kernel/">My Kernel Configuration</a>.
- <a href="./portage/make.conf">Portage Configuaration</a>.
- <a href="./kernel/scripts/compile-kernel">Custom Kernel Compile Script</a>.
- <a href="./picom/picom.conf">Compositor Configuration</a>.

## Kernel

My Kernel was configured with minimalism considered and will NOT work on setups without similar specifications as the ones' it's initially configured. Although multiple kernel configurations are inevitable for different systems, there is no guarantee of support for your device.

### Kernel support List

#### <a href="./kernel/">.config</a>

- Intel Skylake (Atom or Newer) support.
- Intel Microcode loading support.
- Intel UHD graphics Support.
- Nouveau support is <b>removed</b> and replaced with Nvidia binary driver [not included in kernel].
- Wifi and Bluetooth support (Intel Wireless card [<b>linux-firmware</b> required]).
- Soundcard Support (Intel HD).
- Most Bloat Stripped out [WIP].
- ZSTD compression.
- Initramfs support.
- Lvm and Luks support.
- OpenRc support.

### <a href="./kernel/scripts/compile-kernel">Kernel Compilation Script</a>

- Compiles Kernel.
  - 6 Jobs (12gb+ ram and at least six threads recommended).
- Installs all the kernel modules.
- Copies Kernel Binary to /boot directory.
  - Make sure /boot is mounted.
- Generates InitramFS.
  - LVM support.
  - Luks support.
  - Zstd Compression.
- Updates grub configuration in /boot.

#### Configuring

&nbsp; Edit configuration options starting from `:3` <br>

```
  KERNEL_DIR - Kernel Directory <br>
  MAKE_OPTS - Amount Of Jobs the compiler should use <br>
  INITRAMFS_OPTIONS - Genkernel paramaters <br>
  GRUB_CONFIG_DIR - Grub configuration directory <br>
  NVIDIA - Nvidia proprietary kernel modules rebuild <br>
```

