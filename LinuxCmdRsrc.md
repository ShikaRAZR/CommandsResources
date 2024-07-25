[Back to Commands & Resources](CommandsResources.md)

## Linux Commands
  https://lzone.de/cheat-sheet/DKMS

  https://linuxize.com/post/how-to-use-apt-command/

<details> 
  <summary>Install Linux Guest Additions</summary>
  <img src="guestadditions.png" alt="Zorin">

  - Device - Insert Guest Additions CD Image...
  - Go to disk and run:

        sudo ./VBoxLinuxAdditions.run
  - Give permissions to sharedfolder
  
        sudo adduser 'user' vboxsf
</details><br>





<details> 
  <summary>View Installed Packages (In date order)</summary>

  - ls -1t - get all dpkg.log* file names in chronological order
  - zcat -f - IF file is of gzip type then decompress it, ELSE just pass on the content.
  - tac - Reverse output of cat, line-by-line to makes sure we get the correct chronological order.
  - grep - Only check for installed or upgrade packages.
  - awk -F ':a' - Separate the architecture field from the package name
  - column -t - pretty print the columns separated by space
  - As shown above, it only works on ARM architecture and need slight modification for the architecture field separator 

        for x in $(ls -1t /var/log/dpkg.log*); do zcat -f $x |tac |grep -e " install " -e " upgrade "; done |awk -F ":a" '{print $1 " :a" $2}' |column -t
</details><br>





<details>
  <summary>APT vs DPKG vs Flatpak</summary>

  - APT Uses dpkg to Install Packages
  - APT Can Download Packages from remote repositories
  - APT is the native package manager on Debian-based systems. It installs files to your root file system (e.g. /usr/bin/pdflatex)
  - Dpkg Won't Install Dependencies
  - Dpkg Indexes Local Packages Only
  - Flatpak places configuration and data files in ~/.var, doesnt conform to XDG base directory specification
  - Flatpak isolates and sandboxes programs, a distribution-agnostic package format

        apt list --installed
        dpkg -l > apps.txt (sends to txt in home dir)
        apt-cache search <search term>
        apt-cache pkgnames <search_term>
</details><br>





<details>
  <summary>Uninstall/Remove Unused/Orphaned Packages - apt autoremove deborphan</summary>

        apt-get remove packagename

> will remove the binaries, but not the configuration or data files of the package packagename. It will also leave dependencies installed with it on installation time untouched.

        "apt-get purge packagename" or "apt-get remove --purge packagename"

> will remove about everything regarding the package packagename, but not the dependencies installed with it on installation. Both commands are equivalent. <br>
particularly useful when you want to 'start all over' with an application because you messed up the configuration. However, it does not remove configuration or data files residing in users home directories, usually in hidden folders there. There is no easy way to get those removed as well.

        apt-get autoremove

> removes orphaned packages, i.e. installed packages that used to be installed as an dependency, but aren't any longer. Use this after removing a package which had installed dependencies you're no longer interested in.

        "aptitude remove packagename" or "aptitude purge packagename" (likewise)

> will also attempt to remove other packages which were required by packagename on but are not required by any remaining packages. Note that aptitude only remembers dependency information for packages that it has installed.
</details><br>





<details>
  <summary>Nala</summary>

        sudo nala fetch
        Mirrors you want to keep separated by spaces (1..16): 1 2 3
> fetch debian mirrors test for fast download
        
        sudo nala update
        sudo nala upgrade
> ^DO ABOVE FIRST fetch lastest package, install updates

        sudo nala install packagename
> install package

        sudo nala purge packagename
        sudo nala autoremove
>uninstall package, remove unused packages

        nala list --upgradable
> see from update if anything can be upgraded

        nala search packagename
> search package
</details><br>





<details>
  <summary>Other Commands</summary>
  
        gnome-screenshot -a
> Gnome Screenshot - Snipping
</details><br>





<details> 
  <summary>Linux Mint 21.3 Custom</summary>

- Favorites: 
  - Extensions
  - Themes
  - Disks (gnome-disks)
  - Disk Usage Analyzer (baobab)
  - Update Manager
  - Firewall Configuration (gufw)
  - Timeshift
- Panel:
  - System monitor
  - Files
  - Firefox
  - Terminal
  - Software Manager
  - System Setting
  - Screenshot
  - Discord
  - VSCodium
- Extensions
  - Transparent Panels Reloaded (#181237/Opacity 70)
  - gTiles 1(3,1.5---1) 2(3,1.5---1,1) 3(1,1---1) 4(.3,3,.3,4.5,.3---.5,8,.5)
- Applets
  - Command Launcher
  
        gnome-screenshot -w (screenshot current window)
        gnome-terminal -- waydroid first-launch (run waydroid on terminal)
- Keyboard > Shortcuts
  - Windows > Position > Move Window (Add)

        Shift + Ctrl + Alt + Z
  - Custom Shortcuts > gnome-screenshot-snip (Make)

        gnome-screenshot -a
        Shift + Ctrl + Alt + S

- Other
  - [Tela Icon](https://github.com/vinceliuice/Tela-icon-theme) [Guide](https://www.youtube.com/watch?v=oWRHumOldS8)
  - Commands:

        git clone https://github.com/vinceliuice/Tela-icon-theme.git
        sudo -s
        cd Tela-icon-theme/
        ./install.sh -d /usr/share/icons/

  - Terminal Color #181237/Preferences: Alt+Enter/No Menubar/Opacity/Palette:<br>
    [Option 1](https://coolors.co/22276e-a5a3d4-5b61ae-4b3e7f-e7e2f2-7e6ba2-2596be-d2d5ee)<br>
    [Option 2](https://coolors.co/7f8acd-7368a5-dbdbef-131a6a-cac7e9-6f75c3-37397f-efeaf5)
    [Accents (Raw)](https://coolors.co/293fc8-d1a993-efdae9-9c7db5-d0e0f7)
    [Primary (Raw)](https://coolors.co/4e3473-614ea0-2b38a0-8590d0-e8e6f3)
    [Accents (Firefox)](https://coolors.co/0020f0-c7deff-ffccf1-ff9c66-a333ff)
    [Primary (Firefox)](https://coolors.co/2f1f46-3b2f60-1a2361-394794-7367b6)
    [Accents (VSCode)](https://coolors.co/334eff-4760ff-85b8ff-c7deff-ffccf1-ff85de-ff9c66)
    [Primary (VSCode)](https://coolors.co/2f1f46-3b2f60-3f4ea2-2f40b1-8075bd-11152c-161f50-362e60)<br>

  - Firefox: Toolbar-Popup Color #5B61AE, Text #C7DEFF, Background-Search #1A2361, Tab Highlight #FFCCF1
  - Background 404 Clouds
  - ~/.config/gtk-3.0/[gtk.css](gtk.css) OR /usr/share/themes/404-Cloud-Mint-Y-Dark-Blue/gtk-3.0/[gtk.css](gtk.css)
  - Window Tiling - Drag to top maximizes
  - Sound - Sounds - Tiling and snapping windows (Off)
</details><br>





<details> 
  <summary>KVM Qemu VirtManager</summary>

[Install KVM Properly](https://www.youtube.com/watch?v=LHJhFW7_8EI)<br>
[Article](https://sysguides.com/install-kvm-on-linux)

</details><br>





<details> 
  <summary>Waydroid</summary>

[Linux Mint Waydroid Setup](https://medium.com/@tony.j.miri/android-on-linux-mint-with-waydroid-setup-guide-ff0ca8eab22)<br>
[Waydroid Extras Script For Gaming](https://github.com/casualsnek/waydroid_script?tab=readme-ov-file)<br>
[Waydroid Resolution Change](https://docs.waydro.id/usage/waydroid-prop-options)

### Waydroid Install Commands

        sudo apt install curl ca-certificates -y
> curl certificates for safe connections to servers

        export DISTRO="jammy"
> version of Linux Mint - [jammy](https://www.linuxmint.com/download_all.php), create a persistent variable that holds our distro name

        sudo curl --proto '=https' --tlsv1.2 -Sf https://repo.waydro.id/waydroid.gpg --output /usr/share/keyrings/waydroid.gpg
> download a file on the internet in specified location in our local file system

        echo "deb [signed-by=/usr/share/keyrings/waydroid.gpg] https://repo.waydro.id/ $DISTRO main" | sudo tee /etc/apt/sources.list.d/waydroid.list
> add the new repository to our list of sources

        sudo apt update
> Update to use repository

        sudo apt install waydroid -y
> install waydroid

        sudo apt install weston
>install weston (optional) ONLY for distros that don't use wayland

        waydroid first-launch
> launch waydroid

<br><br>
### Waydroid Extras Script

    sudo apt install lzip
> required for script to run

    git clone https://github.com/casualsnek/waydroid_script
    cd waydroid_script
    python3 -m venv venv
    venv/bin/pip install -r requirements.txt
    sudo venv/bin/python3 main.py
> install/run script

<br><br>
### Granting full permission for apps data (HACK), combat against the apps permission issue on Android 11

    sudo waydroid shell
> run only when installing gacha game data

    chmod 777 -R /sdcard/Android
    chmod 777 -R /data/media/0/Android 
    chmod 777 -R /sdcard/Android/data
    chmod 777 -R /data/media/0/Android/obb 
    chmod 777 -R /mnt/*/*/*/*/Android/data
    chmod 777 -R /mnt/*/*/*/*/Android/obb
> permissions

<br><br>
### Waydroid Settings

> You can invert colors in Settings > Accessibility > Advanced/Color Inversion 

    waydroid prop set persist.waydroid.width 0-9999 (int)
    waydroid prop set persist.waydroid.height 0-9999 (int)
> Resolution

</details><br>