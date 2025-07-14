# Nvidia and Amd Switching in laptops that support nvidia optimus

* `lspci -vnn | grep '\''[030[02]\]'` use this command if you see two lines (two gpus) the laptop supports optimus and you can switch between them.
* Apparently ubuntu systems has nvidia-prime that has this feature inbuilt and switch between gpus easily. (Linux mint has this feature built in)

## Alternatives for Arch

* Disabling one of the GPUs in the BIOS
* nvidia-prime(only for ubuntu and ubuntu based distros)
* Bumblebee
* nvidia-xrun

**Honestly all these methods are kinda scuffed 🙂**
**[Sauce](https://www.reddit.com/r/linux_gaming/comments/6ftq10/the_ultimate_guide_to_setting_up_nvidia_optimus)**

## Better Sauce

* [How to use hybrid gpu](https://www.siberoloji.com/how-to-use-prime-for-hybrid-graphics-nvidia-optimus-on-arch-linux/)

* `__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia glxinfo | grep "OpenGL renderer"` -> nvidia
* `glxinfo | grep "OpenGL renderer"` -> amd
* then optimus is doing its thing.
