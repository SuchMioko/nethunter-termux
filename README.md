<h1 align="center">NetHunter Termux</h1>

<p align="center">Install NetHunter on your termux with Root and without Root</p>

# Information NetHunter

[Nethunter Rootless](https://www.kali.org/docs/nethunter/nethunter-rootless/) is a nethunter that can be installed without requiring root, but has many shortcomings and cannot be used as much as possible, this also applies to nethunter installed with root users because it does not provide a custom kernel, but the advantage is that it supports using the [Kali Nethunter Application](https://store.nethunter.com/)

# Installion Dependecies

> **Attention!**
> [Termux must be **F-Droid** Version](https://f-droid.org/en/packages/com.termu) because Termux from Playstore no longer maintained because there are someproblems with the Playstore publishing

To run NetHunter in termux requires a package called PRoot for using new root file system without root [**"chroot"**](https://en.m.wikipedia.org/wiki/Chroot) for NetHunter to run with root requires the `tsu` package to log into the root user although you can use `su` but `tsu` is suggested to run fine.

<summary><strong>Update Repository & Install Package Dependecies</strong></summary>

```bash
pkg update && pkg upgrade
pkg install -y dialog
pkg install -y git 
pkg install -y proot
pkg install -y pv
pkg install -y tsu
```
<summary><strong>Clone or Download Repository</strong></summary>

```bash
git clone https://github.com/ryuuou-nyaw/nethunter-termux.git
```

## Start Running NetHunter Script

1. Move to nethunter-termux folder `cd nethunter-termux`
2. Give execution permission `chmod +x nethunter`
3. run the nethunter script `./nethunter` to run the nethunter script as root user use `tsu` before running the script.

After this you will be redirected to choose the type of nethunter.

- **Nano** It is very small in size but only a few penetration tools are available and there is no desktop environment installed, you can install them manually!
- **Minimal** This type has a size of more than 2GB with metasploit already installed in it, but no desktop environment installed.
- **Full** Fully installed of penetration tools and desktop environment.

## Configurasi file

This configuration can only be used for users who run the nethunter script as root, in which you can add an external card to mount to rootfs, the file of this configuration will appear in **/data/data/com.termux/files/home/.config/nethunter-termux/**