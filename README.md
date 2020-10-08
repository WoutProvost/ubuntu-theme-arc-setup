# ubuntu-theme-arc-setup
Follow these steps to style your Ubuntu distro using the Arc theme like the picture below.
![screenshot](img/screenshot.png)

## Update package cache
```Bash
sudo apt update
```

## Desktop background
Open a browser and go to [this](https://pixabay.com/photos/glacier-mountain-snow-hillside-869593/) URL to download the image. Put the image in the `Pictures` folder of your home directory and rename it to `background.jpg`.

## Profile picture
Put your desired profile picture in the `Pictures` folder of your home directory and rename it to `profile.jpg`.

## Arc theme
```Bash
sudo apt install arc-theme
```

## Pocillo icons
```Bash
sudo apt install pocillo-icon-theme
```

## GNOME Tweaks
```Bash
sudo apt install gnome-tweak-tool
```
To disable mouse acceleration, launch Gnome Tweaks, go to the `Keyboard & Mouse` tab and set `Acceleration Profile` to `Flat`.

## GNOME Shell Extensions
```Bash
sudo apt install gnome-shell-extensions
```
Log out and log back in to reload the GNOME shell. Launch GNOME Tweaks, go to the `Extensions` tab, enable `User Themes`, relaunch GNOME Tweaks, go to the `Appearance` tab and select the `Arc-Dark` shell theme. Set the `Applications` theme to `Arc-Dark` and the `Icons` theme to `Pocillo`. Select the `background.jpg` image in the `Pictures` folder of your home directory for both the `Background Image` and the `Lock Screen Image`. Go to the `Top Bar` tab and enable `Clock Date`. Launch the computer settings, go to the `Users` tab and select the `profile.jpg` image in the `Pictures` folder of your home directory.

## Screenfetch
```Bash
sudo apt install screenfetch
```
The `screenfetch` command should display `WM Theme: Arc-Dark`, `GTK Theme: Arc-Dark [GTK2/3]` and `Icon Theme: Pocillo`.

## Ubuntu login background
**Ubuntu 18.04:**
Open `/usr/share/gnome-shell/theme/gdm3.css` and edit `#lockDialogGroup` by commenting out the existing `background` style and adding `background-color: #383c46;`. A reboot might be required for these changes to take effect.

**Ubuntu 20.04:**
See [this](https://github.com/PRATAP-KUMAR/focalgdm3) repo.
