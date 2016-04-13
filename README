This builds the Wayland-Weston AGL image with the basic AGL interface. 
Demos can then be run on top of this.

This image has only been run on i.MX 6QP Sabre and Sabre Auto.
It is not supported nor tested.  It is simply a demo showing that the basic image runs.
It runs on the 4.1.15-1.0.0 Freescale release of Linux.

Build instructions:
To get the BSP you need to have `repo` installed.

Install the `repo` utility (only need to do once per user):
--------------------------------------------------

$: mkdir ~/bin
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$: chmod a+x ~/bin/repo
$: PATH=${PATH}:~/bin

Download the BSP Yocto Project Environment into your directory:
-------------------------------------------

$: mkdir fsl-arm-yocto-bsp
$: cd fsl-arm-yocto-bsp
$: repo init -u git://git.freescale.com/imx/fsl-arm-yocto-bsp.git -b imx-4.1.15-1.0.0_agl-demo
$: repo sync

Setup and Build for Wayland (currently, only one supported)
-------------------------------------------
$: DISTRO=nxp-imx-agl-wayland MACHINE=imx6qpsabreauto source nxp-setup-agl.sh -b bld-agl

IMAGES
-------------------------------------------
Most interesting results currently seen with:
$: bitbake agl-demo-platform

Other images:
$: bitbake agl-image-minimal
$: bitbake agl-image-ivi
$: bitbake agl-image-weston

The CES2016 demo is in this image.  To run it, you need to connect an HDMI monitor in the "portrait" orientation.
The dimensions in the demos are hard coded.  The files used are in /opt/AGL/CES2016 and /etc/xdg/weston.
