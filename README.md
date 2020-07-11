# LineageOS 16.0 builds for the Nintendo Switch
**Installation instructions based on** https://gitlab.com/ZachyCatGames/shitty-pie-guide

Download the build .zip, the boot.img and tegra210-icosa.dts files from the lastest release.

Download hekate and extract it on the root of your SD card.

Put https://gitlab.com/ZachyCatGames/shitty-pie-guide/-/raw/master/00-android.ini?inline=false in `/bootloader/ini` on the SD card.

Put these in `/switchroot/android/` on the SD card:
https://cdn.discordapp.com/attachments/667093920005619742/702602200991662210/coreboot.rom  
https://gitlab.com/switchroot/bootstack/switch-uboot-scripts/-/jobs/artifacts/master/raw/common.scr?job=build    
https://gitlab.com/switchroot/bootstack/switch-uboot-scripts/-/jobs/artifacts/master/raw/sd.scr?job=build  
and rename sd.scr to boot.scr.

Copy `boot.img` and `tegra210-icosa.dtb` directory to `/switchroot/install` on the SD card.

Copy `lineage-16.0-[date]-UNOFFICIAL-[device name].zip` to the root of the SD card.

Download https://drive.google.com/open?id=1KUaQThm6S2xYPYD98qxZsb4JPeRJAM5K & extract `twrp.img` to `/switchroot/install` on the SD card.

Launch Hekate and navigate to `Tools` -> `Arch bit • RCM • Touch • Partitions` -> `Partition SD Card`.

You can use the `Android ` slider to choose how much storage you want Android to have access too, then press `Next Step`, then `Start`.

Once that finishes press `Flash Android`, then `Continue`.

Press `Continue` again and it should reboot to TWRP.

In TWRP tap mount, then check every partition.

Now go back and press `Install` then navigate to `external_sd` then to wherever you put `lineage-16.0-[date]-UNOFFICIAL-[device name].zip` and tap on it.

Swipe to confirm and it should install the rest of Android.

Now just reboot, load hekate again, select the config, and hope it boots
