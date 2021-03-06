# [LinuxDrivers](LinuxDrivers)
##### >[Psychtoolbox](Psychtoolbox)>[PsychHardware](PsychHardware)>[LinuxDrivers](LinuxDrivers)

Psychtoolbox/[PsychHardware](PsychHardware)/[LinuxDrivers](LinuxDrivers)  
  
Customized device drivers for Linux.  
  
The subfolder [NVidiaOptimus](NVidiaOptimus)/ contains a customized  
display modesetting driver and configuration files  
for 64-Bit X-Server 1.19, to use [NVidia](NVidia) Optimus  
Laptops with the proprietary [NVidia](NVidia) graphics driver  
instead of the open-source nouveau driver.  
  
This folder contains some customized drivers for old  
Ubuntu 14.04.2 LTS. Nowadays you should rather upgrade  
your Linux distribution to Ubuntu 14.04.5 LTS er even  
better to Ubuntu 16.04 LTS, instead of installing these  
custom drivers for old and outdated Ubuntu versions.  
  
  
CAUTION: These drivers are only for specific processor  
architectures and versions of the X-Server, and thereby  
only for specific versions of specific Linux distributions.  
  
Installation of these drivers on a mismatched/unsuitable  
distribution will likely make your machines GUI unuseable  
by preventing successfull startup of the X-Server!  
  
You can find out which version of X-Server is used on your  
system by typing...  
  
xdpyinfo | grep 'X.Org version'  
  
... into a terminal window. It should report version 1.16 for a  
[XOrg](XOrg) 1.16 server.  
  
### Currently the following drivers are provided:  
  
  
Drivers for 64-Bit Ubuntu/[KUbuntu](KUbuntu)/\*buntu versions 14.04.2 LTS  
and 14.10, as well as other compatible 64-Bit distributions with a  
[XOrg](XOrg) 1.16 X-Server:  
  
FOR INTEL graphics cards, install intel\_drv.so\_64BitForXOrg1-16  
  
This binary driver is built from intel-ddx driver version 2.99.917.  
It contains some useful bug fixes and multi-display improvements  
over the standard 2.99.914 driver that is included in Ubuntu  
14.04.2-LTS and 14.10 by default. It also contains a modification to  
disable graphics triple-buffering by default.  
  
0. If the file isn't available in your [LinuxDrivers](LinuxDrivers) directory, you  
can simply download it from this URL:  
  
https://github.com/Psychtoolbox-3/Psychtoolbox-3/blob/master/Psychtoolbox/[PsychHardware](PsychHardware)/[LinuxDrivers](LinuxDrivers)/intel\_drv.so\_64BitForXOrg1-16?raw=true  
  
### 1. Install it from a terminal window via:  
  
sudo cp intel\_drv.so\_64BitForXOrg1-16 /usr/lib/x86\_64-linux-gnu/xorg/extra-modules/intel\_drv.so  
  
2. Logout and login again, so the new driver gets loaded.  
  
The source code (and license) from which this binary driver  
was built can be found in the following tar.gz file:  
  
xf86-video-intel-2-99-917+[MKTripleBufferOff](MKTripleBufferOff).tar.gz  
  
The patch which was applied to the original 2.99.917 source to  
disable triple buffering by default can be found in the file:  
0001-Disable-triple-buffering-by-default.patch  
  




<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/Psychtoolbox/PsychHardware/LinuxDrivers/Contents.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/Psychtoolbox/PsychHardware/LinuxDrivers/Contents.m">changelog</a></span>
</div>
<div class="code">
  <code>Psychtoolbox/PsychHardware/LinuxDrivers/Contents.m</code>
</div>

{{category}}