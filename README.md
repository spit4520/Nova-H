# Nova-H
This is the official repository for the Nova Optomized Virtual Applications Hypervizor this is a recursive acronym. 
This will allow for the automated process of passing physical devices to a Virtual Machine running in a form of container. 
This will hopefully allow users to run a Windows Virtual Machine inside of a Nova-H Container with a video card passed through for hardware acceleration and near native performance.


Before you start:

Welcome to Nova-H! Before you can start using Nova-H you must first enter your bios settings and tweek a few things.
First you must locate the Intel(VT) or the AMD(AMD-V) settings in your BIOS and enable them. This will allow for IOMMU
as well as other virtualization technologies to be enabled.

Next you need to locate a setting that will change you primary video output to be what ever video source you want to use for Linux
EX: under video options I selected IDG (Integrated Discrete Graphics) as my primary output. This will free up your video card
for use with Nova-H and can then be passed through to your VM.

Important Notes:

Nova-H uses existing software with a large amount of bash scripts as well as some python for a user friendly front end. QEMU-KVM
is doing all of the heavy lifting here this piece of software only uses the ability to create and spawn the Virtual Machines.
OVMF as well as other technologies are user here and they all of the aformentioned software will be dependencies for Nova-H

The ideal Kernel is 4.1+ 3.9 is known to work, but requires patching that is not planned on being integrated into the project
at this time as it adds complexity and detracts from the goal of Nova-H.

Your GRUB configuration as well as Linux Images will be rebuild to include the PCI stubbing required for this process. If your 
system becomes unstable because of settings that were changed by a manual rebuild of GRUB after Nova-H has done so you have been
warned.

Planned Features:

Automated set up of the system to allow for video cards as well as most other physical componets of the system within reason.
The system will then be able to spawn your Virtual Machine and run with the hardware that was stubbed at boot and passed along
ideally this set up will be used for gaming and hardware acceleration inside of Windows. The front end will have two different 
views one view will be similar to a iPad screen with all of the icons and apps laid out in a grid like system in a screen and
upon double click will launch the Virtual Machine with that program launching on start. The other view will be similar to a system
managment pane that can allow users to adjust the system memory, processor count, processor type, disk location, video card id's
and other physical id's.

All of the above features are relative until development comes underway
