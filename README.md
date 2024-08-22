# GEGL Sharp Bevel - a Gimp plugin
A new awesome GEGL Plugin that makes a bevel using a unique algorith.
![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/204c33a1-6070-490e-8aeb-1467467ac935)

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/31b24487-bebd-4f56-a051-0299d29aecb1)

A high quality bevel plugin that uses a unique algorithm that by its nature dictates
the bevel to be sharp in appearance. I have made many bevel plugins before this one
(bevel, custom-bevel, glossy-balloon ect... but all of them rely on the same theory. A blur
followed by an emboss. This is the first bevel plugin of mine to deviate from that rule.
Distance transform, color to alpha and emboss is the core principle behind sharp bevel.

To see its very different sister plugin go here. (Sharp's description cites Custom Bevel.)
https://github.com/LinuxBeaver/GEGL-Custom-Bevel/

## OS specific location to put GEGL Filter binaries 

Windows
C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins
 
 Linux 
 /home/(USERNAME)/.local/share/gegl-0.4/plug-ins
 
 Linux (Flatpak)
 /home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

**Linux**

To compile and install you will need the GEGL header files (libgegl-dev on Debian based distributions or gegl on Arch Linux) and meson (meson on most distributions).

meson setup --buildtype=release build
ninja -C build


If you have an older version of gegl you may need to copy to ~/.local/share/gegl-0.3/plug-ins instead (on Ubuntu 18.04 for example).

**Windows**

The easiest way to compile this project on Windows is by using msys2. Download and install it from here: https://www.msys2.org/

Open a msys2 terminal with C:\msys64\mingw64.exe. Run the following to install required build dependencies:

pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl

Then build the same way you would on Linux:

meson setup --buildtype=release build
ninja -C build

## More previews of this based plugin.

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/dc628f1f-18f7-42df-90d2-2f6c1f9f2ac2)

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/2095c24e-2f93-4d08-8931-49c8bc823884)

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/cb238a4c-f79f-49f9-a049-2d7a6ae7a9ee)

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/c058a372-d30d-4c44-bb17-982e40c33e0c)

![image](https://github.com/LinuxBeaver/GEGL_sharp_bevel_gimp_plugin/assets/78667207/361f7670-bdc5-415b-812b-8dfe97cc1e89)



