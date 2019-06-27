# Ursa Major Clover Theme
A clean theme for [the Clover UEFI bootloader](http://sourceforge.net/projects/cloverefiboot)
based off [clover-theme-minimal](https://github.com/al3xtjames/clover-theme-minimal) 
by Alex James.

![Screenshot of the theme](screenshot.png)

This theme also features custom colored OS icons, based on the Ursa Major colorscheme.

## Installation

1. Mount the EFI partition where Clover is installed. For me, it's /dev/sdb1:

```bash
sudo mkdir /mnt/macos
sudo mount /dev/sdb1
```

2. Clone this repository to your disk. the Clover theme directory (/EFI/CLOVER/themes). 

```bash
git clone https://github.com/kgoettler/ursa-major-clover.git
```

3. Copy the `ursa-major-clover` directory in this repository to the Clover 
   theme directory (/EFI/CLOVER/themes)

```bash
sudo cp -r ./ursa-major-clover/ursa-major-clover /mnt/EFI/CLOVER/themes/
```

4. Edit your Clover config.plist (/EFI/CLOVER/config.plist) to select the theme.

```plist
<key>GUI</key>
<dict>
	<key>Theme</key>
	<string>ursa-major-clover</string>
</dict>
```

## Credits
Thanks to Alex James for the original Clover Minimal Theme, and Evan Purkhiser 
for the [rEFInd-minimal](https://github.com/EvanPurkhiser/rEFInd-minimal) theme
on which that was based.

