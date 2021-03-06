# How to Test tauOS

### Please Backup Your System and Review Known Issues before following These Instructions.

## Installing from tauOS Images
1. Download the latest [ISO Build](https://github.com/tau-OS/isos/actions/workflows/build.yml)
2. Download [BalenaEtcher](https://www.balena.io/etcher/)
3. Get a USB Drive, It should hold at least 4GB.
4. Open BalenaEtcher, select the file you downloaded earlier, then your drive, finally click flash.
5. Now to use the USB Drive instead of your hard drive.

If you use an Apple Computer, hold the `Option` key after turning it on. You will see a menu with at least 2 options, use the mouse to click the option that says "UEFI boot".

  If you use a modern Windows computer, hold the `Shift` key and press Restart in your start menu. A menu on a blue background will appear. First Click "Use a Device", then click your drive (It may have "UEFI" in the name, it is supposed to do this.

6. Select either option and wait for the installation program to load.

*Note*: Manual partitioning accepts all layouts, even those that will not work, please use automatic partitioning for the time being.

**WARNING**: This will erase *EVERYTHING* on your drive. Do not continue if you have important files on your drive.

7. Follow the instructions shown by the installer

8. Restart your computer and enjoy


## Converting an Existing Fedora Silverblue, Kionite, iOT or CoreOS Install
1. Download [convert2tau](https://github.com/tau-OS/testers/blob/main/convert2tau)
2. Open a terminal and go to the folder where convert2tau is saved.
3. Make it executable using `chmod u+x convert2tau`
Note: Your System will reboot after the conversion. Save any work.
4. Run convert2tau as root using `sudo bash convert2tau`
5. Enjoy tauOS



## Installing from Fedora Server Images - **DEPRECATED - KEPT ONLY FOR POSTERITY**
1. Download this [file.](https://download.fedoraproject.org/pub/fedora/linux/releases/35/Server/x86_64/iso/Fedora-Server-netinst-x86_64-35-1.2.iso) Save it somewhere you can find it again.
2. Download [BalenaEtcher](https://www.balena.io/etcher/)
3. Get a USB Drive, It should hold at least 4GB.
4. Open BalenaEtcher, select the file you downloaded earlier, then your drive, finally click flash.
5. Now to use the USB Drive instead of your hard drive.

If you use an Apple Computer, hold the `Option` key after turning it on. You will see a menu with at least 2 options, use the mouse to click the option that says "UEFI boot".

  If you use a modern Windows computer, hold the `Shift` key and press Restart in your start menu. A menu on a blue background will appear. First Click "Use a Device", then click your drive (It may have "UEFI" in the name, it is supposed to do this.

6. Now a white menu on a black background will appear with options to start Fedora. Press the `E` key.

7. You will now see a menu to edit options starting with "setparams", use your arrow keys to navigate to the end of the line starting with linuxefi, add a space, and type `inst.ks=https://kickstart.tau.innatical.com/desktop-x86_64.cfg`, finally press `Ctrl+X`

 Note: If the steps above did not work, try pressing "tab" which will show an editable line starting with "vmlinuz" use your arrow keys to navigate to the end of the line, add a space, and type `inst.ks=https://kickstart.tau.innatical.com/desktop-x86_64.cfg`, finally press the `Enter` key or the `Return` key.

8. Wait for the system to turn on.

**WARNING**: Step 9 will erase *EVERYTHING* on your drive. Do not continue if you have important files on your drive.

9. Follow the instructions shown by the installer

Note: Manual partitioning accepts all layouts, even those that will not work, please use automatic partitioning for the time being.

10. Restart your computer and enjoy
