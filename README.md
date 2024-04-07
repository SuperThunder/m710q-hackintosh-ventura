# Lenovo M710q macOS 13 Ventura Hackintosh
macOS 13 Ventura Hackintosh files for Lenovo M710q Tiny

Guides used:
- https://dortania.github.io/OpenCore-Install-Guide/
- https://dortania.github.io/OpenCore-Post-Install/#how-to-follow-this-guide

# Important notes
- My M710q came with an addon DisplayPort. This doesn't work in macOS! One of the motherboard DisplayPorts needs to be used.
- Whenever I use it with my TV I need to switch the TV to a different HDMI a couple of times after turning the M710q on to get macOS display working
    - Similarly, if you have trouble getting a display output with a monitor, try plugging and unplugging the cable and try all your ports
- Despite the older and low power i5-7400T the general experience is actually pretty nice and smooth with a good SSD and 16GB RAM

# Hardware
M710q Tiny
- i5-7400T 2.4GHz base / 3GHz single core turbo / 2.8GHz quad core turbo with UHD630
- Samsung 980 (not pro) 512GB NVMe SSD (note: the SSD that came with many Lenovo/Dell of this era, PM981, has severe issues with macOS and should not be used)
- 2x8GB 2400MHz (upgrading from 8GB to 16GB made a big improvement in responsiveness)
- Intel 8265 ac wireless
- Intel I219-V ethernet
- ALC294 audio

# Working and not working
### Working
- Pretty much everything for active use
- USB, audio, wifi, ethernet
- Multiboot with Windows 11 (see below)

### Not working
- DisplayPort addon
- Sleep. I turned it off entirely since it seemed to freeze when it tries to sleep.
- Hassle free TV use


# Multiboot Windows 10/11 after installing MacOS
- See 'macOS installed first' https://www.insanelymac.com/forum/topic/346365-guide-dual-boot-for-windows-1011-and-macos-on-the-same-disk-windows-installed-first-macos-installed-first-empty-drive/
- Basically, open Disk Utility in macOS, reduce your partition size and make an MS-DOS partition. Boot to a Windows installer, reformat the new partition, install to it.
- You can choose between macOS and Windows at the OpenCore boot selection screen that is available for a few seconds at startup