# Best yuzu compatibility settings guide.

Hello user!

This is a guide on the best yuzu settings as of December 6th 2021, so this could be outdated if you veiw it a year after it was last edited, but settings don't change that much month to month so don't worry it'll be outdated the next day you go play your games.

To start this guide a few things need to be cleared up:
 1. Not all hardware is equal, so don't expect your games to run fullspeed just because you followed this guide or you feel like the game is light enough to run.
 2. Optimal settings only do so much to your playing experience, some games will run, some will with a couple of issues and others might not even boot, this is not a miraculous fixer for all issues.
 3. Different hardware requires different settings, so stick to the correct section according to what you have (if you don't know exactly what you have on your PC opening Task Manger `Ctrl + Shift + Esc` and going to the `Performance` tab will show you your specs.

## General settings for all users (and where to find them).

- Enable Docked mode - `toggle in the bottom left corner of the emulator.`
- Enable Multicore CPU emulation - `emulation > configure > general > general.`
- Enable Auto CPU accuracy - `emulation > configure > CPU`
- Enable Disk pipeline cache - `emulation > configure > graphics > graphics`
- Enable Asynchronous GPU emulation - `emulation > configure > graphics > graphics`
- Enable Fast GPU time - `emulation > configure > graphics > advanced`
- Dump your console's firmware and install it in `AppData\Roaming\yuzu\nand\system\Contents\registered` (Drop all the .nca files from the firmware)
- Make a bigger page file (for 8gb RAM users use 25000 for both values and 16gb+ RAM use 20000 for both values), needs a computer reboot to take effect.

https://user-images.githubusercontent.com/65554156/144896068-eacc2048-b49b-4e92-b72e-6926f23d27a3.mp4
- Update your drivers to their latest version (sometimes newer drivers can have issues with yuzu, so the linked ones are the most optimal)

### Windows 10/11
- Nvidia (desktop) - <https://developer.nvidia.com/vulkan-beta-47277-windows-1110>
- Nvidia (laptops) - <https://developer.nvidia.com/vulkan-beta-47277-windows-1110>
- AMD 21.11.3 - <https://www.amd.com/en/support/apu/amd-ryzen-processors/amd-ryzen-5-desktop-processors-radeon-vega-graphics/amd-ryzen-5-1>
- Intel 101.1069 - <https://www.intel.com/content/www/us/en/download/19344/intel-graphics-windows-10-windows-11-dch-drivers.html>
- (Intel laptops and prebuilt computer users with old driver versions might need to follow this video tutorial: <https://www.youtube.com/watch?v=BZG50Nm5sOM&>)

### Linux
- <https://github.com/yuzu-emu/yuzu/wiki/Recommended-GPU-Drivers-for-Linux>
- Nvidia - Use what your distribution offers.
- AMD - mesa-git, force AMDGPU on older first and second GCN products: <https://wiki.archlinux.org/title/AMDGPU#Enable_Southern_Islands_(SI)_and_Sea_Islands_(CIK)_support>.
- Intel - mesa-git, the required Iris Gallium driver is enabled by default with mesa 20.

## Nvidia GPUs:
- Use Vulkan - `emulation > configure > graphics > graphics`
- If Vulkan has any problems try OpenGL (GLASM to compile shaders and GLSL for best performance) - `emulation > configure > graphics > graphics`
- Set up your Nvidia GPU control panel settings
1. OpenGL rendering GPU: *your GPU*
2. Power management mode: Prefer maximum performance
3. Threaded optimization: On
4. Vertical sync: Off

![image](https://user-images.githubusercontent.com/65554156/144901299-729288ff-7fca-4c57-8f6d-2ef1d8fa20bf.png)

## AMD GPUs:
- Use Vulkan - `emulation > configure > graphics > graphics`
- Add yuzu as a profile on Radeon Software, this will add a driver level cache to Vulkan

## Intel iGPUs:
- Use Vulkan - `emulation > configure > graphics > graphics`


