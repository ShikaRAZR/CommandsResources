# Commands & Resources
List of commands and resources that are personally useful for me.

## Table of Contents
1. [Markdown Guide](#markdown-guide)
2. [Git Commands](#git-commands)
3. [Linux Commands](#linux-commands)
4. [General Application Link Stuff](#general-application-link-stuff)
5. [Youtube-dl](#youtube-dl)
6. [Emojis](#emojis)



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Markdown Guide 
https://www.markdownguide.org/basic-syntax#paragraphs-1

https://www.markdownguide.org/basic-syntax/

https://google.github.io/styleguide/docguide/style.html



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Git Commands
- Set Up Git:

        git config --global user.name "Your Name"
        git config --global user.email "youremail@domain.com"
  
- Saving Commands

        git clone ***url*** (makes a local copy of a repository)
        git add (file names)
        git commit -m "(committed message)
        git push -u origin ***master***
        git remote add origin ***master*** (url)
        git commit
        git pull (download the master branch online into your pc)
        git push origin ***master***

- Adding To A Repository On Git - (MAIN)

        git add (will show differences in code and possible conflicts)
          git add *.java (add a folder without the '/')
            git add . (adds modified files)
            git add filename.filetype
            git add -A (adds all changes, what I usually use)
      
        git commit -m "comment"
        git push origin ***branchName***

- Check Remote Branch Difference

        git fetch
        git diff <mainbranch_path> <remotebranch_path>

<details>
<summary>OTHER</summary>

___
- Other Commands

        git init (initialize local repo)
        git status
        git config --list

- New Branch - used to isolate new features that are being created

        git branch (shows total branches, and the one your in)
        git checkout ***use-case-001*** (switches to different branches/changes the content of the folder according to branch)
        git branch ***use-case-002*** (creates a new branch)
___
- Add Branch

        git checkout ***master*** (directly adds feature to master branch)
          git checkout ***use-case-002*** (go here if you want to merge this branch with master, master isn't changed)
          git merge ***master*** (only used if master branch was changed, will merge into master and show differences in code and possible conflicts)
- *repeat ADDING process, 'git push' shows command below, pushing is done as below*<br>

        git push --set-upstream origin ***use-case-002*** (connects this branch to the repository, for the FIRST TIME)
          git push ***use-case-002*** (continuous pushes afterwards)

___
- Pull New Branch

        git branch ***branch_name***
        git checkout ***branch_name***
        git pull origin ***branch_name***
<p>(might need to add and commit changes)</p>

___
- ABORT MERGE

        git merge --abort

- DELETE BRANCH

        git branch -d branch_name

- PULL SPECIFIC branch

        git fetch origin branch_name:branch_name

- GET CHANGES FROM MASTER INTO BRANCH

        git checkout branch_name
        it merge master

- DISCARD CHANGES IN BRANCH

        git checkout -- <file>...
</details>
<br>

- File Management
  - .gitignore (File)<br>
    > __pycache__/ (Ignore folder)<br>
    > macrolist/*.txt (Ignore file)<br>
  - .gitkeep (File that keeps folders)
  
<details> 
  <summary>Window Git Shortcut</summary>
  <a href="https://www.youtube.com/watch?v=kIgZEdyn1dA"><img src="https://img.youtube.com/vi/kIgZEdyn1dA/0.jpg" alt="WinGit"></a>
</details>



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Linux Commands
  https://lzone.de/cheat-sheet/DKMS

  https://linuxize.com/post/how-to-use-apt-command/

<details> 
  <summary>Install Linux Guest Additions</summary>
  <img src="guestadditions.png" alt="Zorin">

  - Device - Insert Guest Additions CD Image...
  - Go to disk and run:

        sudo ./VBoxLinuxAdditions.run<br>
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
</details>

        for x in $(ls -1t /var/log/dpkg.log*); do zcat -f $x |tac |grep -e " install " -e " upgrade "; done |awk -F ":a" '{print $1 " :a" $2}' |column -t

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
        
        sudo nala install packagename
> install package

        sudo nala purge packagename
        sudo nala autoremove
>uninstall package, remove unused packages

        sudo nala update
        sudo nala upgrade
> fetch lastest package, install updates

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
- Other
  - [Tela Icon](https://github.com/vinceliuice/Tela-icon-theme) [Guide](https://www.youtube.com/watch?v=oWRHumOldS8)
> Commands

        git clone https://github.com/vinceliuice/Tela-icon-theme.git
        sudo -s
        cd Tela-icon-theme/
        ./install.sh -d /usr/share/icons/

  - Terminal Color Alt+Enter:Preferences/No Menubar/#181237/Opacity/Palette:
> [Option 1](https://coolors.co/22276e-a5a3d4-5b61ae-4b3e7f-e7e2f2-7e6ba2-2596be-d2d5ee)<br>
> [Option 2](https://coolors.co/7f8acd-7368a5-dbdbef-131a6a-cac7e9-6f75c3-37397f-efeaf5)<br>
> [Accents (Raw)](https://coolors.co/293fc8-d1a993-efdae9-9c7db5-d0e0f7)<br>
> [Primary (Raw)](https://coolors.co/4e3473-614ea0-2b38a0-8590d0-e8e6f3)<br>
> [Accents (Firefox)](https://coolors.co/0020f0-c7deff-ffccf1-ff9c66-a333ff)<br>
> [Primary (Firefox)](https://coolors.co/2f1f46-3b2f60-1a2361-394794-7367b6)<br>
> [Accents (VSCode)](https://coolors.co/334eff-4760ff-85b8ff-c7deff-ffccf1-ff85de-ff9c66)<br>
> [Primary (VSCode)](https://coolors.co/2f1f46-3b2f60-3f4ea2-2f40b1-8075bd-11152c-161f50-362e60)<br>
> Toolbar-Popup Color #5B61AE, Text #C7DEFF, Background-Search #1A2361, Tab Highlight #FFCCF1
  - Background 404 Clouds
  - ~/.config/gtk-3.0/[gtk.css](gtk.css) OR /usr/share/themes/404-Cloud-Mint-Y-Dark-Blue/gtk-3.0/[gtk.css](gtk.css)
  - Window Tiling - Drag to top maximizes
</details><br>



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## General Application Link Stuff

### Linux
> Timeshift - OS Backup<br>
> htop - Process Viewer<br>
> fdisk, parted, gparted, gnome-disks - Partition Manager<br>
> [Nala](https://github.com/volitank/nala) - apt frontend<br>
> [ufw](https://github.com/jbq/ufw) - firewall [Guide](https://christitus.com/linux-security-mistakes/)<br>
> [Firejail Sandbox](https://github.com/netblue30/firejail)<br>
> Git

> [Windows in a Bottle](https://usebottles.com/)<br>
> fastfetch [logo](https://github.com/fastfetch-cli/fastfetch/wiki/Logo-options)<br>
> Drawing - Image Editor<br>
> gThumb - Image Viewer<br>
> Vim - Text Editor<br>
> [It's FOSS](https://itsfoss.com/)
> [Linux Ricing](https://github.com/avtzis/awesome-linux-ricing)

### Applications
> [OBS](https://obsproject.com/)<br>
> [ffmpeg](https://ffmpeg.org/)<br>
> [youtube-dl](https://github.com/yt-dlp/yt-dlp)<br>
> [mkvtoolnix](https://mkvtoolnix.download/)<br>
> [process_lasso](https://bitsum.com/)<br>
> vscodium<br>
> [vlc](https://www.videolan.org/vlc/)<br>
> 7zip<br>
> gpuz<br>
> cpuz<br>
> [WinDirStat](https://windirstat.net/)<br>
> [Crystaldiskinfo](https://crystalmark.info/en/software/crystaldiskinfo/)<br>
> [Mp3tag](https://www.mp3tag.de/en/)<br>
> [PC Benchmark](https://www.userbenchmark.com)<br>
> All info ip can get off you https://ipleak.net/<br>
> [Wireshark](https://www.wireshark.org/)<br>
> Firefox - Web Browser<br>
> [Image Editor](https://www12.lunapic.com/editor/?action=transparent)<br>
> Git - Github<br>
> [LosslessCut](https://github.com/mifi/lossless-cut)<br>
> [Discord](https://ptb.discord.com/download)<br>
> [Czkawka Duplicate File Search](https://github.com/qarmin/czkawka?tab=readme-ov-file)<br>
> Windy Weather Forecast https://www.windy.com<br>
> [Everything (Fast File Explorer Search)](https://www.voidtools.com/)<br>
> [Remote Desktop](https://parsec.app/)<br>
> LibreOffice (Document Reader)<br>
> Anki (Flashcard)


### Web Browser
> [Popup Blocker](https://addons.mozilla.org/en-US/firefox/addon/popup-blocker/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [Smart HTTPS](https://addons.mozilla.org/en-US/firefox/addon/smart-https-revived/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [The Camelizer - Price Tracker](https://addons.mozilla.org/en-US/firefox/addon/the-camelizer-price-history-ch/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [DocsAfterDark](https://addons.mozilla.org/en-US/firefox/addon/docsafterdark/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [Youtube Ad Auto-skipper](https://addons.mozilla.org/en-US/firefox/addon/youtube-ad-auto-skipper/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
>[Tabliss](https://addons.mozilla.org/en-US/firefox/addon/tabliss/) <br>
> [Firefox Color](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/)

> [Steamable Video Hosting](https://streamable.com/) <br>
> https://regexr.com/ <br>
> [Hue Finder](https://colors.artyclick.com/color-hue-finder) <br>
> [Color Palettes](https://coolors.co/)

### Personal
> [Discord History](https://github.com/Tyrrrz/DiscordChatExporter/releases) - [Guide](https://www.swipetips.com/how-to-download-your-chat-history-from-discord/) <br>
> [Streaming](https://letflix.tv/movie/watch-stalker-17191) <br>
> [Reddit - multireddit of your subscriptions](https://old.reddit.com/r/0sanitymemes+1stPersonAnimations+ANormalDayInRussia+APK+Android+AndroidStudio+AniLick+AnimeInOurWorld+AnimeNoises+AnimeSleeves+AraAra+Arknuts+AzureLane+BDOBeautyAlbum+BMW+BTS+Battlefield+BirdsArentReal+Bitcoin+BitcoinBeginners+BitcoinMarkets+BlenderDoughnuts+CatastrophicFailure+Catswithjobs+Chonkers+Cytus+Damnthatsinteresting+EDM+EpicSeven+EscapefromTarkov+Etterna+FGOcomics+FGOfanart+Fate+FateExtra+FatePrismaIllya+Fencing+FiftyFifty+ForFashion+GFLNeuralCloud+GIRLSundPANZER+GearsOfWar+Genshin_Impact+Genshin_Memepact+GoblinSlayer+Gunime+Gunpla+HaloStory+HeadphoneAdvice+HighQualityReloads+HonkaiImpact+Itasha+JustKiddingNews+KurtzPel+Maplestory+MildFemboys+Minecraft+Music+OppaiLove+OsuSkins+OverlordNsfw+Overwatch+PcBuild+PetTheDamnCat+Piracy+ProgrammerHumor+PunishingGrayRaven+RealEstate+ReleaseMySoul+Rimuru+RoastMe+Saber+SelfDrivingCars+Shitty_Car_Mods+TacticalDolls+TarkovMemes+UnrestrictedGFL+WhatAWeeb+Whatcouldgowrong+YoujoSenki+androiddev+anime+animegifs+animenews+animenocontext+apexlegends+arknights+artknights+awwcoholics+bestofosu+blackdesertonline+blender+blenderhelp+bodyweightfitness+cars+cats+confusing_perspective+consentacles+cutelittlefangs+dankmemes+dogecoin+egg_irl+fateapocrypha+fatestaynight+fourminute+funny+gachagaming+gaming+gifs+girlsfrontline+goodanimemes+grailwhores+grandorder+hackernews+halo+hardware+instant_regret+insurgency+java+javagamedev+javahelp+jobs+karanokyoukai+killthecameraman+kpop+learnjava+learnjavascript+learnprogramming+lostarkgame+manga+massage+memes+modernwarfare+osugame+overlord+personalfinance+piano+pianocovers+pimpcats+pouts+red_velvet+sakimichan+science+smug+stalker+starcitizen+toarumajutsunoindex+touhou+tvxq+typemoon+u_CheetahSperm18+u_Chendroshee+u_Djinnfor+u_Hanada_Yanochi+u_Hentaki_Coco+u_Imagen-Breaker+u_Waifu-Is-Bae+u_ZumiDraws+u_chirofish+u_sevrivas262/)

<details> 
  <summary style="font-weight:bold; font-size:1.3em">Anime</summary>
  <a href="https://danbooru.donmai.us/">danbooru</a>
  <a href="https://gelbooru.com/">gelbooru</a>
  <a href="https://www.pixiv.net/en/">pixiv</a>
  <a href="https://github.com/Tsuk1ko/nhentai-helper">Tsuk1ko/nhentai-helper</a>
  <a href="e-hentai.org">e-hentai</a>
  <a href="https://nhentai.net/">nhentai</a>
  <a href="https://hanime.tv/">hanime</a>
  <a href="https://www.zerochan.net/">zerochan</a>
  <a href="https://kemono.su/">kemono</a>
  <a href="https://rule34.xyz/">rule34xyz</a>
  mangadex mangalife mangahub
</details>

> My Anime List https://myanimelist.net/<br>
> Image Search https://findit.moe/ https://iqdb.org/ https://saucenao.com/<br>
> Upscaler https://waifu2x.udp.jp/ <br>
> Manga EN https://mangadex.org/ https://tachiyomi.org/<br>
> Manga JP https://j8jp.com/manga/list-mode/ https://welovemanga.one/manga-list.html https://nicomanga.com/<br>
> Manga DL 
[Tachidesk](https://github.com/Suwayomi/Tachidesk-Server#what-is-tachidesk) [Kindle-Comic-Converter-kcc_5.6.2.exe](https://github.com/ciromattia/kcc) 
[Kindlegen](https://github.com/ciromattia/kcc/issues/371)<br>
> Anime DL https://animekaizoku.com/ https://www.animeout.xyz/ https://anidl.org/ https://kayoanime.com/ https://anidl.org/ https://www.animesenpai4u.com/ https://mkvshows.com/<br>
> Stream https://aniwave.to/ https://animepahe.ru/ https://littleweeb.github.io/ https://kickassanime.am/<br>
> Music https://downloads.khinsider.com/ <br>
> Sheet Music https://josh.agarrado.net/music/anime/index.php <br>

### Game Stuff
> Osu replays https://ordr.issou.best/ <br>
> https://www.gflcorner.com/ <br>
> [GFL Logistics Calculator](https://tempkaridc.github.io/gf/) <br>
> [Arknights Aceship's Toolbox](https://aceship.github.io/AN-EN-Tags/index.html) <br>
> [Escape From Tarkov Wiki](https://escapefromtarkov.gamepedia.com/Escape_from_Tarkov_Wiki) [Armor](https://tarkov.dev/items/armors) [Ammo](https://www.eft-ammo.com/ammo-graph)<br>
> https://eftfg.com/ammo<br>
> [Steam](https://store.steampowered.com/)<br>
> [Switch Emulator](https://ryujinx.org/download)<br>
> [ATLauncher (Minecraft)](https://atlauncher.com/)

<details> 
  <summary style="font-weight:bold; font-size:1.3em">JP</span></summary>
  <a href="https://github.com/yudataguy/Awesome-Japanese#beginner-guide">General</a> <br>
  <a href="https://supernative.tv/ja/">TV Show Phrases</a> <br>
  <a href="http://www.technologyimprov.com/HiraganaAudioQuiz">Hiragana Audio Memorize</a> <br>
  <a href="https://realkana.com/hiragana/">Memorize Kana</a> <br>
  <a href="https://laits.utexas.edu/japanese/joshu/index.php">Many Resources</a> <br>
  <a href="https://www.nhk.or.jp/lesson/en/letters/hiragana.html">Stroke Order</a> <br>
  <a href="https://ankiweb.net/shared/decks?search=japanese">Anki Decks</a> <br>
  <a href="https://apps.ankiweb.net/">Anki</a> <br>
  <a href="https://animelon.com/">JP Sub Anime</a>
  
</details>
<br>
<details> 
  <summary style="font-weight:bold; font-size:1.3em">Hotkeys</span></summary>

- Windows

        Task Manager 
        Ctrl + Shift + Esc

        Preview (File)
        Alt + P

        Snipping
        Window + shift + s

        Move windows
        Window + shift + arrow

- Linux

        Shutdown
        Ctrl + Alt + End

        Restart
        Ctrl + Alt + Esc

        Paste in Terminal
        Ctrl + Shift + V

        Terminal
        Ctrl + Alt + T

        Lockscreen 
        Ctrl + Alt + L

        Close an application window
        Ctrl + Q

        Run console
        Alt + F2

- Both

        Properties (File)
        Alt + Enter

        Opens File Explorer (File)
        Windows logo key + E

        Creates another instance of the current folder in a new window (File)
        Ctrl + N

        Opens a tab (File, Firefox)
        Ctrl + T

        Moves across tabs (File, Firefox)
        Ctrl + Tab, Ctrl + Shift + Tab

        Close Tab (File, Firefox)
        Ctrl + W
</details>




<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Youtube-dl
- https://youtube-dl.org/ Old/Original
- https://github.com/yt-dlp/yt-dlp New/Update

        .\youtube-dl.exe --help
        youtube-dl -F "link" //displays video options to dowload
        youtube-dl -f "number" "link" //"number" - to select video quality
        youtube-dl -f bestaudio "link"
        youtube-dl -f bestvideo "link"

- FILE TRIM:

        ffmpeg -i output1.mp3 -ss 00:00:30 -to 00:00:40 -c copy output.mp3

- FILE CONVERSION:
        
        ffmpeg.exe

- BATCH CONVERT

        for %a in ("*.webp") do ffmpeg -i "%a" "%~na.png"
        for %a in ("%CD%\*.webp") do ffmpeg -i "%a" "%CD%\%~na.png"
        for %a in ("Convert\*.webm") do ffmpeg -i "%a" "Converted\%~na.mp3"
        for %a in ("Convert\*.webp") do ffmpeg -i "%a" "Converted\%~na.png"

- COMBINE

        ffmpeg -i "video.mp4" -i "audio.mp3" -map 0:v -map 1:a -c:v copy -c:a copy output.mp4 -y

- BATCH COMBINE

        for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.mp3" -map 0:v -map 1:a -c:v copy -c:a copy "Combined\%~na.mp4" -y

- DOWNLOAD FROM TXT

        youtube-dl -f best -o "%(autonumber)0Nd-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 63 --add-header ""

Use output template with %(autonumber)0Nd, where N in the number of digits instead.

        youtube-dl -f best -o "%(autonumber)03d-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 66 --add-header "


<details> 
  <summary>OTHER</summary>

- SUBTITLE COMBINE (NOT WORKING CORRECTLY)

        ffmpeg -i "input.mp4" -i "subtitles.srt" -c:s mov_text -c:v copy -c:a copy output.mp4

- BATCH SUBTITLE COMBINE (NOT WORKING CORRECTLY)

        for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.srt" -c:s mov_text -c:v copy -c:a copy "Combined\%~na.mp4"

So to add auto-numbering, use -A

___
NOT WORKING CORRECTLY<br>
Headache to rename and sort the files based on the order.<br>
So to add auto-numbering, use -A like,<br>
youtube-dl https://www.youtube.com/playlist?list=PLOU2XLYxmsILe6_eGvDN3GyiodoV3qNSC -A

Or to keep playlist index,<br>
youtube-dl -o '%(playlist_index)s. %(title)s.%(ext)s' https://www.youtube.com/playlist?list=PLOU2XLYxmsILe6_eGvDN3GyiodoV3qNSC

This will add nice numbering to the downloaded files.<br>
And if you are downloading files which is not in playlist, you can add numbers manually to the file,<br>
youtube-dl -o "1-%(uploader)s%(title)s.%(ext)s" https://youtu.be/862r3XS2YB0

Here I have manually added 1- to the filename while downloading.<br>
--devo
___
RESOURCES:<br>
https://github.com/ytdl-org/youtube-dl/blob/master/docs/supportedsites.md<br>
https://video.online-convert.com/convert-to-webm<br>
https://www.zamzar.com/convert/m4a-to-mp3/<br>
https://trac.ffmpeg.org/wiki/HowToBurnSubtitlesIntoVideo<br>
https://captionsconverter.com/<br>
https://downsub.com/<br>
Google2SRT
</details> 


<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Emojis
- Small<br>
<img src="ur cute/01 catgirlhuggies.webp"><img src="ur cute/02 kristineunicry.webp"><img src="ur cute/03 emiliaaa.webp"><img src="ur cute/04 noelsip.webp"><img src="ur cute/05 AquaHD.webp"><img src="ur cute/06 cryrosu.webp"><img src="ur cute/06 rosucrybread.webp"><img src="ur cute/06 rosuneutral.webp"><img src="ur cute/07 kiss~1.webp"><img src="ur cute/08 diaredevil.webp"><img src="ur cute/09 WATEFAK.webp"><img src="ur cute/10 shunyaaa.webp"><img src="ur cute/11 suck.webp"><img src="ur cute/12 unicry.webp"><img src="ur cute/13 KeqingGN.webp"><img src="ur cute/14 happy.webp"><img src="ur cute/15 NJgasm.webp"><img src="ur cute/16 gn.webp"><img src="ur cute/17 rikashock.webp"><img src="ur cute/18 AquaCry.webp"><img src="ur cute/19 TokoPat.webp"><img src="ur cute/20 ayameheart.webp"><img src="ur cute/21 murmwot.webp"><img src="ur cute/22 kokomisigh.webp"><img src="ur cute/23 nani.webp"><img src="ur cute/24 hornyisback.webp"><img src="ur cute/27 sob.gif"><img src="ur cute/31 limwat.webp"><img src="ur cute/32 AlstolfoBlush.webp"><img src="ur cute/33 AMsalute.webp"><img src="ur cute/34 ArcyPouty.webp"><img src="ur cute/35 catHUH.gif"><img src="ur cute/36 ChenShrug.webp"><img src="ur cute/37 ded.webp"><img src="ur cute/38 ElainaHeart.webp"><img src="ur cute/39 giveheart.gif"><img src="ur cute/40 goodmorning.webp"><img src="ur cute/41 goodnight.webp"><img src="ur cute/42 heh.gif"><img src="ur cute/43 hkpatpat.gif"><img src="ur cute/44 notlikethis.webp"><img src="ur cute/45 OkayuMogu.webp"><img src="ur cute/46 p7wink.webp"><img src="ur cute/47 pp90blush.webp"><img src="ur cute/48 rinkodespair.webp"><img src="ur cute/49 RoseDead.webp"><img src="ur cute/50 rosuhappy.gif"><img src="ur cute/51 rosunote.gif"><img src="ur cute/52 rosupatpat.gif"><img src="ur cute/53 rosupout.gif"><img src="ur cute/54 rosusigh.webp"><img src="ur cute/55 SanaBox.webp"><img src="ur cute/56 SanaSad1.webp"><img src="ur cute/57 SanaSad2.webp"><img src="ur cute/58 SanaTeehee.webp"><img src="ur cute/59 SanaWorried.webp"><img src="ur cute/60 SanaYapi.webp"><img src="ur cute/61 suiwave.webp"><img src="ur cute/62 WatameHuh.webp"><img src="ur cute/63 wubbaboo_tired.webp"><img src="ur cute/64 yaedrive_chickenjagoo.gif"><img src="ur cute/65 zerotwoheart.webp"><img src="ur cute/95 noted-anime.gif"><img src="ur cute/96 NeroGasm.webp"><img src="ur cute/97 Meow.gif"><img src="ur cute/98 fubukidance.gif"><img src="ur cute/99 awawa.gif">
<br><br>

<details> 
  <summary>Large</summary>

<img src="ur cute/Large/01 surprise.webp">
<img src="ur cute/Large/02 hkpatpat.gif">
<img src="ur cute/Large/03 notlikethis.webp">
<img src="ur cute/Large/04 yaedrive_chickenjagoo.gif">
<img src="ur cute/Large/05 catHUH.gif">
<img src="ur cute/Large/06 nod.gif">
<img src="ur cute/Large/07 goodmorning.webp">
<img src="ur cute/Large/08 goodnight.webp">
<img src="ur cute/Large/09 AMsalute.webp">
<img src="ur cute/Large/10 rosupatpat.gif">
<img src="ur cute/Large/11 rosuhappy.gif">
<img src="ur cute/Large/12 rosupout.gif">
<img src="ur cute/Large/13 rosunote.gif">
<img src="ur cute/Large/14 rosucry.webp">
<img src="ur cute/Large/15 cry.webp">
<img src="ur cute/Large/16 rosubread.webp">
<img src="ur cute/Large/17 emiliaaa.webp">
<img src="ur cute/Large/18 flushed.gif">
<img src="ur cute/Large/19 pointed fingers .gif">
<img src="ur cute/Large/20 melt.gif">
<img src="ur cute/Large/21 tail rub.gif">
<img src="ur cute/Large/22 AlphaScream.gif">
<img src="ur cute/Large/23 AlstolfoBlush.webp">
<img src="ur cute/Large/24 ArcyPouty.webp">
<img src="ur cute/Large/25 awawa.webp">
<img src="ur cute/Large/26 pray.webp">
<img src="ur cute/Large/27 sob.gif">
<img src="ur cute/Large/28 yes.gif">
<img src="ur cute/Large/29 teehee.webp">
<img src="ur cute/Large/30 shrug.webp">
<img src="ur cute/Large/31 CatNod.gif">
<img src="ur cute/Large/32 sway.gif">
<img src="ur cute/Large/33 ChenShrug.webp">
<img src="ur cute/Large/34 ded.webp">
<img src="ur cute/Large/35 ElainaFustrated.webp">
<img src="ur cute/Large/36 ElainaHeart.webp">
<img src="ur cute/Large/37 ElainaThumbsUp.webp">
<img src="ur cute/Large/38 fish bite.gif">
<img src="ur cute/Large/39 heh.gif">
<img src="ur cute/Large/40 Hug.png">
<img src="ur cute/Large/41 IllyaWhat.gif">
<img src="ur cute/Large/42 Kiss.gif">
<img src="ur cute/Large/43 Lick.gif">
<img src="ur cute/Large/44 MeguruHug.webp">
<img src="ur cute/Large/45 MeguruSmile.webp">
<img src="ur cute/Large/46 Mex.webp">
<img src="ur cute/Large/47 nekooo.gif">
<img src="ur cute/Large/48 OkayuMogu.webp">
<img src="ur cute/Large/49 owoHugs.gif">
<img src="ur cute/Large/50 p7wink.webp">
<img src="ur cute/Large/51 Peak.webp">
<img src="ur cute/Large/52 Pout.png">
<img src="ur cute/Large/53 pp90blush.webp">
<img src="ur cute/Large/54 Question.webp">
<img src="ur cute/Large/55 rainbow-dance.gif">
<img src="ur cute/Large/56 sana Wink.webp">
<img src="ur cute/Large/57 SanaBox.webp">
<img src="ur cute/Large/58 sanacry.webp">
<img src="ur cute/Large/59 Smug.png">
<img src="ur cute/Large/60 suijuice.webp">
<img src="ur cute/Large/61 suiwave.webp">
<img src="ur cute/Large/62 TakeNotes.webp">
<img src="ur cute/Large/63 WatameHuh.webp">
<img src="ur cute/Large/64 wubbaboo_tired.webp">
</details><br><br>


<details> 
  <summary>XXLarge</summary>

<img src="ur cute/ExtraLarge/01 cry.jpg">
<img src="ur cute/ExtraLarge/02 Cute Cheer.gif">
<img src="ur cute/ExtraLarge/03 dance-happy.gif">
<img src="ur cute/ExtraLarge/04 Firewatch Nuke.png">
<img src="ur cute/ExtraLarge/05 heart.gif">
<img src="ur cute/ExtraLarge/06 nachoSuneruHD.webp">
<img src="ur cute/ExtraLarge/07 omori-basil.gif">
<img src="ur cute/ExtraLarge/08 ozu_oz_yarimasu_heart.gif">
<img src="ur cute/ExtraLarge/09 paw.png">
<img src="ur cute/ExtraLarge/10 Perlica Ice Cream.webp">
<img src="ur cute/ExtraLarge/11 sticker_1.gif">
<img src="ur cute/ExtraLarge/12 sticker_1.png">
<img src="ur cute/ExtraLarge/13 sticker_3.gif">
<img src="ur cute/ExtraLarge/14 sticker_5.png">
<img src="ur cute/ExtraLarge/15 sticker_6.gif">
<img src="ur cute/ExtraLarge/16 sticker_7.gif">
<img src="ur cute/ExtraLarge/17 sticker_9.gif">
<img src="ur cute/ExtraLarge/18 sticker_16.png">
<img src="ur cute/ExtraLarge/19 sticker_28.png">
<img src="ur cute/ExtraLarge/20 sticker_30.png">
<img src="ur cute/ExtraLarge/21 suicheer.png">
<img src="ur cute/ExtraLarge/22 Trailblazer_Nom01.png">
<img src="ur cute/ExtraLarge/23 uuu.webp">
<img src="ur cute/ExtraLarge/24 wataten-anime.gif">
</details><br><br>

<details> 
  <summary>Standard Wallpapers</summary>

<img src="Standard Wallpapers/1ad3ba6.jpg">
<img src="Standard Wallpapers/316a1ff.png">
<img src="Standard Wallpapers/404 Clouds.jpg">
<img src="Standard Wallpapers/404.jpg">
<img src="Standard Wallpapers/Artoria 46.jpg">
<img src="Standard Wallpapers/Copy of IMG_20191008_215858.jpg">
<img src="Standard Wallpapers/Fate Servants.png">
<img src="Standard Wallpapers/G&K Extended.jpg">
<img src="Standard Wallpapers/GFL404 Clean.png">
<img src="Standard Wallpapers/GFL404.png">
<img src="Standard Wallpapers/GFLAR.png">
<img src="Standard Wallpapers/Griffin Emblem Extended.jpg">
<img src="Standard Wallpapers/Halo Reach Space.jpg">
<img src="Standard Wallpapers/Koenigsegg.jpg">
<img src="Standard Wallpapers/Okita.jpg">
<img src="Standard Wallpapers/Predator.png">
<img src="Standard Wallpapers/Red Wallpaper.jpg">
<img src="Standard Wallpapers/Saber 8.png">
<img src="Standard Wallpapers/tumblr_owrccebouC1u41kbzo1_1280.png">
</details> <br><br>

<details> 
  <summary>Other</summary>

        [![Love](https://media.tenor.com/QAU2oFvucdcAAAAC/heart.gif)](https://tenor.com/view/heart-gif-18231995)
        [![](Img)](Link)
        ![](Img)
        <a href=""><img src=""></a>
        <img src="ur cute/" alt="ur cute/">

                

        dir /b > namelist.txt

        VSCode Search
        ^(.+)$
        <img src="ur cute/$1"> 
        </details> 

