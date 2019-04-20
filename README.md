# ubuntu-theme-arc-setup
Follow these steps to style your Ubuntu distro using the Arc theme like the picture below.
![screenshot](img/screenshot.png)

## Update package cache
```Bash
sudo apt-get update
```

## Desktop background
```Bash
curl https://pixabay.com/get/e133b80a21f71c22d9584518a33219c8b66ae3d01cb4144597f3c67e/glacier-869593_1920.jpg > ~/Pictures/background.jpg
```
If that doesn't work, open a browser and go to the following URL: https://pixabay.com/photos/glacier-mountain-snow-hillside-869593/.

## Profile picture
```Bash
curl -L https://www.dropbox.com/s/xnijntyzt74c3rv/slash_hat_and_guitar.jpg?dl=1 > ~/Pictures/profile.jpg
```

## Arc theme
```Bash
sudo apt-get install arc-theme
```

## Pocillo icons
```Bash
sudo apt-get install pocillo-icon-theme
```

## GNOME Tweaks
```Bash
sudo apt-get install gnome-tweak-tool
```
Set `Acceleration Profile` to `Flat` in the `Keyboard & Mouse` tab to disable mouse acceleration.

## GNOME Shell Extensions
```Bash
sudo apt-get install gnome-shell-extensions
```
Log out and log back in to reload the GNOME shell. Launch GNOME Tweaks, go to the `Extensions` tab, enable `User Themes`, relaunch GNOME Tweaks and go the the `Appearance` tab to select the `Arc-Dark` shell theme. Set the `Applications` theme to `Arc-Dark` and the `Icons` theme to `Pocillo`. Select the `background.jpg` image in the `Pictures` folder of your home directory for both the `Background Image` and the `Lock Screen Image`. Enable the `Clock Date` in the `Top Bar` tab. Select the `profile.jpg` image in the `Pictures` folder of your home directory for your profile picture in the `Users` tab of the computer settings.

## Screenfetch
```Bash
sudo apt-get install screenfetch
```
The `screenfetch` command should display `WM Theme: Arc-Dark`, `GTK Theme: Arc-Dark [GTK2/3]` and `Icon Theme: Pocillo`.

## Ubuntu login background
Open `/usr/share/gnome-shell/theme/gdm3.css` and edit `#lockDialogGroup` by commenting out the existing style and adding `background-color: #383c46;`. A reboot might be required for these changes to take effect.
