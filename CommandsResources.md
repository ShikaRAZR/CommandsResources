# Commands & Resources
List of commands and resources that are personally useful for me.

VS Code Settings Markdown > Preview Scroll Editor/Preview with Preview/Editor
## Table of Contents
1. [Markdown, VSCode Guide](#markdown-vscode-guide)
2. [Git Commands](#git-commands)
3. [Linux Commands & Resources](LinuxCmdRsrc.md)
4. [General Application Link Stuff](#general-application-link-stuff)
5. [Youtube-dl](#youtube-dl)
6. [Emojis](#emojis)



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Markdown VSCode Guide 
#### Markdown
https://www.markdownguide.org/basic-syntax#paragraphs-1

https://www.markdownguide.org/basic-syntax/

https://google.github.io/styleguide/docguide/style.html

#### VSCode
> (Opening Tabs) When you [single-]click a file in the left sidebar's file browser or open it from the quick open menu (Ctrl-P, type the file name, Enter), Visual Studio Code opens it in what's called "Preview Mode", which allows you to quickly view files.
<br><br>
Preview Mode tabs are not kept open. As soon as you go to open another file from the sidebar, the existing Preview Mode tab (if one exists) is used. You can determine if a tab is in Preview Mode, by looking at its title in the tab bar. If the title is italic, the tab is in preview mode.
<br><br>
To open a file for editing (i.e. don't open in Preview Mode), double-click on the file in the sidebar, or single-click it in the sidebar then double click the title of its Preview Mode tab.
<br>

> Set default line endings in Visual Studio Code<br>
VSCode settings (F1)<br>
Preferences: Open User Settings (JSON)<br>
settings.json: "files.eol": "\n" (add)

        {
                "markdown.preview.scrollPreviewWithEditor": false,
                "files.eol": "\n"
        }
<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Git Commands
- Authentication

        sudo apt update
        sudo apt install gh
        gh auth login

> Github.com, HTTPS, Paste Authentication Token
        
        Name
        Only select repositories 
        Repository permissions: Contents (just for editing)

> Create Token on website: <br>
Settings > Developer Settings > Personal Access Tokens > Fine-grained Tokens


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

- Force Git to use LF instead of CR+LF CLRF under Windows? [stackoverflowlink](https://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-windows)

        git config --global core.autocrlf false

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

## General Application Link Stuff

### Linux
> [Nala](https://github.com/volitank/nala) - apt frontend<br>
> htop - Process Viewer<br>
> Git<br>
> Mission Center<br>
> Timeshift - OS Backup<br>
> fdisk, parted, gparted, gnome-disks - Partition Manager<br>
> [ufw](https://github.com/jbq/ufw) - firewall [Guide](https://christitus.com/linux-security-mistakes/)<br>
> [Firejail Sandbox](https://github.com/netblue30/firejail)<br>
> [tldr](https://tldr.sh/) [tealdeer](https://github.com/tealdeer-rs/tealdeer) - simiplified man pages (on website or command line)
> Hardinfo <br>

> fastfetch [logo](https://github.com/fastfetch-cli/fastfetch/wiki/Logo-options)<br>
> [Drawing](https://maoschanz.github.io/drawing/) - Image Editor<br>
> gThumb - Image Viewer<br>
> Vim - Text Editor<br>
> [Easytag](https://flathub.org/apps/org.gnome.EasyTAG), [PuddleTag](https://docs.puddletag.net/)<br>
> [Piper](https://github.com/libratbag/piper) (Mouse Perirpheral Editor)<br>
> Gimp<br>

> Weston<br>
> Waydroid<br>
> Proton Tricks<br>
> [Windows in a Bottle](https://usebottles.com/)<br>
> [Heroic Games Launcher](https://heroicgameslauncher.com/)<br>
> Goverlay (for mangohud config)<br>
> Mangohud (Flatpak ver for flatpak programs)<br>

> [It's FOSS](https://itsfoss.com/)<br>
> [sysguides](https://sysguides.com/)<br>
> [Linux Ricing](https://github.com/avtzis/awesome-linux-ricing)<br>
> [Titus Blog](https://christitus.com/)

### Android
> [Android FOSS List](https://github.com/offa/android-foss)<br>
> [Aurora Store](https://auroraoss.com/)<br>
> [Openboard](https://github.com/openboard-team/openboard)<br>
> [F-Droid](https://f-droid.org/en/)<br>
> [dvd (yt-dlp)](https://f-droid.org/packages/org.yausername.dvd/)<br>
> [New Pipe](https://f-droid.org/en/packages/org.schabi.newpipe/)<br>

### Applications
> [Chromium](https://www.chromium.org/getting-involved/download-chromium/)(Not-as-easy steps: Snapshots)<br>
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
> LibreOffice (Document Reader) [AbiWord](https://github.com/AbiWord/abiword?tab=readme-ov-file) [LaTeX (miktex)](https://www.latex-project.org/get/#tex-distributions)<br>
> [QEMU](https://www.qemu.org/download/#windows) [GUI](https://qtemu.org/)<br>
> Anki (Flashcard)<br>
> [Youtube TV](https://github.com/marcosrg9/YouTubeTV?tab=readme-ov-file)<br>
> [Bulk File Rename Utility](https://www.bulkrenameutility.co.uk/)<br>
> Music Player [mpv](https://mpv.io/) [foobar2000](https://www.foobar2000.org/) [fooyin](https://www.fooyin.org/)<br>
> [FreeTube](https://github.com/FreeTubeApp/FreeTube)<br>
> [Zen Browser](https://zen-browser.app/)<br>
> [WinMerge](https://winmerge.org/) (Compare windows files/folders, differencing merging tool)<br>
> [Gimp](https://www.gimp.org/)<br>
> [Oracle Virtual Box](https://www.virtualbox.org/)<br>


### Web Browser
> [Popup Blocker](https://addons.mozilla.org/en-US/firefox/addon/popup-blocker/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Smart HTTPS](https://addons.mozilla.org/en-US/firefox/addon/smart-https-revived/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Website Blocker](https://addons.mozilla.org/en-US/firefox/addon/block-website/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) [Git](https://github.com/ray-lothian/Block-Site) <br>
> [Feedbro Reader](https://addons.mozilla.org/en-US/firefox/addon/feedbroreader/)<br>
> [Untrap Hide Youtube Distractions](https://addons.mozilla.org/en-US/firefox/addon/untrap-for-youtube/)<br>
> [Youtube Dislike](https://addons.mozilla.org/en-US/firefox/addon/return-youtube-dislikes/)<br>
> [Reverse Image Search](https://addons.mozilla.org/en-US/firefox/addon/image-reverse-search/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Terms of Service; Didn’t Read](https://addons.mozilla.org/en-US/firefox/addon/terms-of-service-didnt-read/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Startpage - Private Search Engine](https://www.startpage.com/en/) <br>

> [Lock Tab Page](https://addons.mozilla.org/en-US/firefox/addon/lock-tab-page/)<br>
> [The Camelizer - Price Tracker](https://addons.mozilla.org/en-US/firefox/addon/the-camelizer-price-history-ch/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [DocsAfterDark](https://addons.mozilla.org/en-US/firefox/addon/docsafterdark/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Youtube Ad Auto-skipper](https://addons.mozilla.org/en-US/firefox/addon/youtube-ad-auto-skipper/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
> [Tabliss](https://addons.mozilla.org/en-US/firefox/addon/tabliss/)<br>
> [Firefox Color](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/)<br>
> [Browser Profile Spoofer](https://addons.mozilla.org/en-US/firefox/addon/chameleon-ext/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Stylus - CSS editor](https://addons.mozilla.org/en-US/firefox/addon/styl-us/)<br>
> [Instagram Video Scrubber](https://addons.mozilla.org/en-US/firefox/addon/video-scrubber-for-instagram/)

> [Steamable Video Hosting](https://streamable.com/) <br>
> https://regexr.com/ <br>
> [Hue Finder](https://colors.artyclick.com/color-hue-finder) <br>
> [Color Palettes](https://coolors.co/) <br>

Zen
> [Private Mode Highlighting](https://zen-browser.app/mods/58649066-2b6f-4a5b-af6d-c3d21d16fc00/) <br>
> [Remove Tab X](https://zen-browser.app/mods/1b88a6d1-d931-45e8-b6c3-bfdca2c7e9d6/)

### Personal
> [Discord History](https://github.com/Tyrrrz/DiscordChatExporter/releases) - [Guide](https://www.swipetips.com/how-to-download-your-chat-history-from-discord/) <br>
> [Streaming Letflix](https://letflixtv.pages.dev/) <br>
> [Reddit - multireddit of your subscriptions](https://old.reddit.com/r/0sanitymemes+1stPersonAnimations+ANormalDayInRussia+APK+Android+AndroidStudio+AniLick+AnimeInOurWorld+AnimeNoises+AnimeSleeves+AraAra+Arknuts+AzureLane+BDOBeautyAlbum+BMW+BTS+Battlefield+BirdsArentReal+Bitcoin+BitcoinBeginners+BitcoinMarkets+BlenderDoughnuts+CatastrophicFailure+Catswithjobs+Chonkers+Cytus+Damnthatsinteresting+EDM+EpicSeven+EscapefromTarkov+Etterna+FGOcomics+FGOfanart+Fate+FateExtra+FatePrismaIllya+Fencing+FiftyFifty+ForFashion+GFLNeuralCloud+GIRLSundPANZER+GearsOfWar+Genshin_Impact+Genshin_Memepact+GoblinSlayer+Gunime+Gunpla+HaloStory+HeadphoneAdvice+HighQualityReloads+HonkaiImpact+Itasha+JustKiddingNews+KurtzPel+Maplestory+MildFemboys+Minecraft+Music+OppaiLove+OsuSkins+OverlordNsfw+Overwatch+PcBuild+PetTheDamnCat+Piracy+ProgrammerHumor+PunishingGrayRaven+RealEstate+ReleaseMySoul+Rimuru+RoastMe+Saber+SelfDrivingCars+Shitty_Car_Mods+TacticalDolls+TarkovMemes+UnrestrictedGFL+WhatAWeeb+Whatcouldgowrong+YoujoSenki+androiddev+anime+animegifs+animenews+animenocontext+apexlegends+arknights+artknights+awwcoholics+bestofosu+blackdesertonline+blender+blenderhelp+bodyweightfitness+cars+cats+confusing_perspective+consentacles+cutelittlefangs+dankmemes+dogecoin+egg_irl+fateapocrypha+fatestaynight+fourminute+funny+gachagaming+gaming+gifs+girlsfrontline+goodanimemes+grailwhores+grandorder+hackernews+halo+hardware+instant_regret+insurgency+java+javagamedev+javahelp+jobs+karanokyoukai+killthecameraman+kpop+learnjava+learnjavascript+learnprogramming+lostarkgame+manga+massage+memes+modernwarfare+osugame+overlord+personalfinance+piano+pianocovers+pimpcats+pouts+red_velvet+sakimichan+science+smug+stalker+starcitizen+toarumajutsunoindex+touhou+tvxq+typemoon+u_CheetahSperm18+u_Chendroshee+u_Djinnfor+u_Hanada_Yanochi+u_Hentaki_Coco+u_Imagen-Breaker+u_Waifu-Is-Bae+u_ZumiDraws+u_chirofish+u_sevrivas262/)<br>
> [Calibre - ebook manager](https://calibre-ebook.com/)<br>
> [Books - Anna’s Archive](https://annas-archive.org/)<br>
> [Developer Roadmap](https://roadmap.sh/)<br>

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

> [My Anime List](https://myanimelist.net/)<br>
> Image Search [findit](https://findit.moe/) [iqdb](https://iqdb.org/) [saucenao](https://saucenao.com/)<br>
> Upscaler [waifu2x](https://waifu2x.udp.jp/) <br>
> Manga EN [mangadex](https://mangadex.org/) [tachiyomi](https://tachiyomi.org/)<br>
> Manga JP 
[j8jp](https://j8jp.com/manga/list-mode/) 
[welovemanga](https://welovemanga.one/manga-list.html) 
[nicomanga](https://nicomanga.com/)<br>
> Manga DL 
[Tachidesk](https://github.com/Suwayomi/Tachidesk-Server#what-is-tachidesk) [Kindle-Comic-Converter-kcc_5.6.2.exe](https://github.com/ciromattia/kcc) 
[Kindlegen](https://github.com/ciromattia/kcc/issues/371)<br>
> Anime DL 
[animekaizoku](https://animekaizoku.com/)
[animeout](https://www.animeout.xyz/)
[anidl](https://anidl.org/)
[kayoanime](https://kayoanime.com/)
[anidl](https://anidl.org/)
[animesenpai4u](https://www.animesenpai4u.com/)
[mkvshows](https://mkvshows.com/)<br>
> Stream 
[<s>aniwave</s>](https://aniwave.to/)
[animepahe](https://animepahe.ru/)
[littleweeb](https://littleweeb.github.io/)
[kickassanime](https://kickassanime.am/)
[kickassanimemx](www1.kickassanime.mx)<br>
> Music [khinsider](https://downloads.khinsider.com/) <br>
> [Sheet Music agarrado](https://josh.agarrado.net/music/anime/index.php) <br>

### Game Stuff
> Osu replays https://ordr.issou.best/ <br>
> Osu Beatmap Exporter https://github.com/kabiiQ/BeatmapExporter <br>
> [Escape From Tarkov Wiki](https://escapefromtarkov.gamepedia.com/Escape_from_Tarkov_Wiki) [Armor](https://tarkov.dev/items/armors) [Ammo](https://www.eft-ammo.com/ammo-graph)<br>
> https://eftfg.com/ammo<br>
> [Steam](https://store.steampowered.com/)<br>
> [Switch Emulator](https://ryujinx.org/download)<br>
> [ATLauncher (Minecraft)](https://atlauncher.com/)

> [Girls' Frontline Cutscene Interpreter](https://gfl.amaryllisworks.pw/) <br>
> [GFL Corner](https://www.gflcorner.com/) <br>
> [GFL Music Player](https://girlsfrontline.kr/musicplayer) <br>
> [GFL Logistics Calculator](https://tempkaridc.github.io/gf/) <br>
> [GFL Story Text Summary](https://www.reddit.com/r/GirlsFrontline2/comments/1hnx2i1/what_you_need_to_know_a_spoiler_free_quick_lore/) <br>
> [GFL Story Video Summary](https://www.youtube.com/playlist?list=PLwIAusSNRkbrH6iZrrT-ePN0J1wZmv3LD) <br>
> [PNC Doll Analysis](https://docs.google.com/spreadsheets/d/1FMK713okcJNQuCv625Ut0TZuQbm9RlHk7l1yOUF9Qdw/edit?gid=0#gid=0) <br>
> [GFL2 Spreadsheet](https://docs.google.com/spreadsheets/d/1DogyU3K7ZXw2qbhP1EhRXIAw5nCyIV5G5e-QWviBZME/edit?gid=543758471#gid=543758471) <br><br>
> [Arknights Tier List](https://ak.gamepress.gg/tier-list/arknights-operator-tier-list) <br>
> [Arknights Tier List 2](https://docs.google.com/spreadsheets/d/1E7HmgKWiV8pKpJpvpVzziYxnaQTP01Vtw_PXEdL7XPA/edit?gid=1108925005#gid=1108925005) <br>
> [Arknights Aceship's Toolbox](https://aceship.github.io/AN-EN-Tags/index.html) <br>


<details> 
  <summary style="font-weight:bold; font-size:1.3em">Learn JP</span></summary>
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

        New Terminal Tab
        Ctrl + Shift + T

        Terminal
        Ctrl + Alt + T

        Lockscreen 
        Ctrl + Alt + L

        Close an application window
        Ctrl + Q

        Run console
        Alt + F2

        Move Window (Keyboard Only)
        Alt + F7 (Esc- Cancel, Enter - Finish)

        Resize Window (Keyboard Only)
        Alt + F8 (Esc- Cancel, Enter - Finish)
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

        Cut
        Ctrl + X
</details>




<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Youtube-dl
- https://youtube-dl.org/ Old/Original
- https://github.com/yt-dlp/yt-dlp New/Update

### Main Commands 
#### ($ means input variable)

        yt-dlp.exe -f bestaudio $link -o "\Downloads\%(title)s.%(ext)s"
> Command Example

        -f bestaudio
        -f bestvideo
        -f bestaudio + bestvideo

        --cookies-from-browser [brave, chrome, chromium, edge, firefox, opera, safari]
        --add-header $link
        --autonumber-start $number
        --playlist-start $start
        --playlist-end $end

        -o "\Downloads\%(title)s.%(ext)s"
        -o "%(autonumber)0Nd-%(title)s.%(ext)s"
> Extension Options

        yt-dlp.exe -f bestaudio --autonumber-start $number --playlist-start $start --playlist-end $end $link -o "\Downloads\%(autonumber)0d-%(title)s.%(ext)s"

        yt-dlp.exe --add-header "Referer: https://girlsfrontline.kr/db/musicplayer/" -a templist.txt -o "\Downloads\%(autonumber)03d-(%(id)s).%(ext)s"

        yt-dlp.exe "Referer: https://downloads.khinsider.com/" -a templist.txt -o "\Downloads\%(id)s.%(ext)s"
> More Examples

        https://girlsfrontline.kr/db/musicplayer/
        <li><a href="#" data-src="
        everything before link

        "[\s\S]*$
        Everything after link


        https://downloads.khinsider.com/ (copy inner html)
        .+(?=\bhref\b)
        everything before href

        ^((?!href).)*$
        any lines that dont have href 

        (\r?\n)(?:\r?\n)+
        all blank lines 

        (?<=.mp3).*
        everything after .mp3 

        href="
        Replace with:
        https://downloads.khinsider.com

        command pallete - "delete duplicate lines"
> Regex





<details> 
  <summary>Commands</summary>


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
</details> 


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
<span>
<img src="ur cute/001 catgirlhuggies.webp">
<img src="ur cute/002 kristineunicry.webp">
<img src="ur cute/003 emiliaaa.webp">
<img src="ur cute/004 noelsip.webp">
<img src="ur cute/005 AquaHD.webp">
<img src="ur cute/006 cryrosu.webp">
<img src="ur cute/006 rosucrybread.webp">
<img src="ur cute/006 rosuneutral.webp">
<img src="ur cute/007 kiss~1.webp">
<img src="ur cute/008 diaredevil.webp">
<img src="ur cute/009 WATEFAK.webp">
<img src="ur cute/010 shunyaaa.webp">
<img src="ur cute/011 suck.webp">
<img src="ur cute/012 unicry.webp">
<img src="ur cute/013 KeqingGN.webp">
<img src="ur cute/014 happy.webp">
<img src="ur cute/015 NJgasm.webp">
<img src="ur cute/016 gn.webp">
<img src="ur cute/017 rikashock.webp">
<img src="ur cute/018 AquaCry.webp">
<img src="ur cute/019 TokoPat.webp">
<img src="ur cute/020 ayameheart.webp">
<img src="ur cute/021 murmwot.webp">
<img src="ur cute/022 kokomisigh.webp">
<img src="ur cute/023 nani.webp">
<img src="ur cute/024 hornyisback.webp">
<img src="ur cute/025 rosusigh.webp">
<img src="ur cute/026 sob.gif">
<img src="ur cute/027 yaedrive_chickenjagoo.gif">
<img src="ur cute/028 wubbaboo_tired.webp">
<img src="ur cute/029 WatameHuh.webp">
<img src="ur cute/030 suiwave.webp">
<img src="ur cute/031 limwat.webp">
<img src="ur cute/032 AlstolfoBlush.webp">
<img src="ur cute/033 AMsalute.webp">
<img src="ur cute/034 ArcyPouty.webp">
<img src="ur cute/035 catHUH.gif">
<img src="ur cute/036 ChenShrug.webp">
<img src="ur cute/037 ded.webp">
<img src="ur cute/038 ElainaHeart.webp">
<img src="ur cute/039 giveheart.gif">
<img src="ur cute/040 goodmorning.webp">
<img src="ur cute/041 goodnight.webp">
<img src="ur cute/042 heh.gif">
<img src="ur cute/043 hkpatpat.gif">
<img src="ur cute/044 notlikethis.webp">
<img src="ur cute/045 OkayuMogu.webp">
<img src="ur cute/046 p7wink.webp">
<img src="ur cute/047 pp90blush.webp">
<img src="ur cute/048 rinkodespair.webp">
<img src="ur cute/049 RoseDead.webp">
<img src="ur cute/050 rosuhappy.gif">
<img src="ur cute/051 rosunote.gif">
<img src="ur cute/052 rosupatpat.gif">
<img src="ur cute/053 rosupout.gif">
<img src="ur cute/054 SanaYapi.webp">
<img src="ur cute/055 SanaBox.webp">
<img src="ur cute/056 SanaSad1.webp">
<img src="ur cute/057 SanaSad2.webp">
<img src="ur cute/058 SanaTeehee.webp">
<img src="ur cute/059 SanaWorried.webp">
<img src="ur cute/060 AMsmartthink.webp">
<img src="ur cute/061 NijikaThink.webp">
<img src="ur cute/062  yaethink_anyuki.webp">
<img src="ur cute/063 yaesmart_chickenjagoo.gif">
<img src="ur cute/064 AMthink.webp">
<img src="ur cute/065 Yes.webp">
<img src="ur cute/066 YES.webp">
<img src="ur cute/067 AMyes.webp">
<img src="ur cute/068 SakuyaPhew.webp">
<img src="ur cute/069 AyameLaugh.webp">
<img src="ur cute/070  rosulaugh.webp">
<img src="ur cute/071 pleading.webp">
<img src="ur cute/072 zerotwoheart.webp">
<img src="ur cute/073 rosublush.webp">
<img src="ur cute/074 sigh.webp">
<img src="ur cute/075 yaeraidenkiss_limeria.webp">
<img src="ur cute/076 AMNoThanks.gif">
<img src="ur cute/077 g11sleepy.gif">
<img src="ur cute/078 AMcatcuddle.gif">
<img src="ur cute/079 AMCuddle.gif">
<img src="ur cute/080 AMastolfokiss.webp">
<img src="ur cute/081 astolfoblush.gif">
<img src="ur cute/082 AMBoyKisserDance.gif">
<img src="ur cute/083 AMmiyanoshrug.webp">
<img src="ur cute/084 nekooo.gif">
<img src="ur cute/085 AMsleepydrool.webp">
<img src="ur cute/086 InaFacepalm.webp">
<img src="ur cute/087 grizzlyFacepalm.webp">
<img src="ur cute/088 scared.gif">
<img src="ur cute/089 ScaredCrow.webp">
<img src="ur cute/090 BoneePat.webp">
<img src="ur cute/091 Shrug.webp">
<img src="ur cute/092 SCyes.gif">
<img src="ur cute/093 InaNod.gif">
<img src="ur cute/094 3.webp">
<img src="ur cute/095 JessicaBruh.webp">
<img src="ur cute/096 KitaScared.gif">
<img src="ur cute/097 KitaSob.webp">
<img src="ur cute/098 KitaFuwa.gif">
<img src="ur cute/099 KitaNotLikeThis.webp">
<img src="ur cute/100 SCinside.gif">
<img src="ur cute/101 Mahiru.webp">
<img src="ur cute/102 MahiruNo.gif">
<img src="ur cute/103 MahiruBonk.gif">
<img src="ur cute/104 Scared.webp">
<img src="ur cute/105 Felix_scared.webp">
<img src="ur cute/106 SuzuDance.webp">
<img src="ur cute/107 SuzuHeart.webp">
<img src="ur cute/108 SuzuNani.webp">
<img src="ur cute/109 SL8Nuke.webp">
<img src="ur cute/110 M4confused.webp">
<img src="ur cute/111 TaischConfused.webp">
<img src="ur cute/994 shijima-shimeji.gif">
<img src="ur cute/995 noted-anime.gif">
<img src="ur cute/996 NeroGasm.webp">
<img src="ur cute/997 Meow.gif">
<img src="ur cute/998 fubukidance.gif">
<img src="ur cute/999 awawa.gif">
</span>

<br><br>

<details> 
  <summary>Large</summary>

<img src="ur cute/Large/001 surprise.webp" height="96">
<img src="ur cute/Large/002 hkpatpat.gif" height="96">
<img src="ur cute/Large/003 notlikethis.webp" height="96">
<img src="ur cute/Large/004 yaedrive_chickenjagoo.gif" height="96">
<img src="ur cute/Large/005 catHUH.gif" height="96">
<img src="ur cute/Large/006 nod.gif" height="96">
<img src="ur cute/Large/007 goodmorning.webp" height="96">
<img src="ur cute/Large/008 goodnight.webp" height="96">
<img src="ur cute/Large/009 AMsalute.webp" height="96">
<img src="ur cute/Large/010 rosupatpat.gif" height="96">
<img src="ur cute/Large/011 rosuhappy.gif" height="96">
<img src="ur cute/Large/012 rosupout.gif" height="96">
<img src="ur cute/Large/013 rosunote.gif" height="96">
<img src="ur cute/Large/014 rosucry.webp" height="96">
<img src="ur cute/Large/015 cry.webp" height="96">
<img src="ur cute/Large/016 rosubread.webp" height="96">
<img src="ur cute/Large/017 emiliaaa.webp" height="96">
<img src="ur cute/Large/018 flushed.gif" height="96">
<img src="ur cute/Large/019 pointed fingers .gif" height="96">
<img src="ur cute/Large/020 melt.gif" height="96">
<img src="ur cute/Large/021 tail rub.gif" height="96">
<img src="ur cute/Large/022 suicheer.png" height="96">
<img src="ur cute/Large/023 AlstolfoBlush.webp" height="96">
<img src="ur cute/Large/024 ArcyPouty.webp" height="96">
<img src="ur cute/Large/025 awawa.webp" height="96">
<img src="ur cute/Large/026 pray.webp" height="96">
<img src="ur cute/Large/027 sob.gif" height="96">
<img src="ur cute/Large/028 yes.gif" height="96">
<img src="ur cute/Large/029 teehee.webp" height="96">
<img src="ur cute/Large/030 shrug.webp" height="96">
<img src="ur cute/Large/031 wubbaboo_tired.webp" height="96">
<img src="ur cute/Large/032 sway.gif" height="96">
<img src="ur cute/Large/033 ChenShrug.webp" height="96">
<img src="ur cute/Large/034 ded.webp" height="96">
<img src="ur cute/Large/035 ElainaFustrated.webp" height="96">
<img src="ur cute/Large/036 ElainaHeart.webp" height="96">
<img src="ur cute/Large/037 ElainaThumbsUp.webp" height="96">
<img src="ur cute/Large/038 WatameHuh.webp" height="96">
<img src="ur cute/Large/039 heh.gif" height="96">
<img src="ur cute/Large/040 Hug.png" height="96">
<img src="ur cute/Large/041 IllyaWhat.gif" height="96">
<img src="ur cute/Large/042 Kiss.gif" height="96">
<img src="ur cute/Large/043 Lick.gif" height="96">
<img src="ur cute/Large/044 MeguruHug.webp" height="96">
<img src="ur cute/Large/045 MeguruSmile.webp" height="96">
<img src="ur cute/Large/046 Mex.webp" height="96">
<img src="ur cute/Large/047 nekooo.gif" height="96">
<img src="ur cute/Large/048 OkayuMogu.webp" height="96">
<img src="ur cute/Large/049 owoHugs.gif" height="96">
<img src="ur cute/Large/050 p7wink.webp" height="96">
<img src="ur cute/Large/051 Peak.webp" height="96">
<img src="ur cute/Large/052 TakeNotes.webp" height="96">
<img src="ur cute/Large/053 pp90blush.webp" height="96">
<img src="ur cute/Large/054 Question.webp" height="96">
<img src="ur cute/Large/055 suijuice.webp" height="96">
<img src="ur cute/Large/056 sana Wink.webp" height="96">
<img src="ur cute/Large/057 SanaBox.webp" height="96">
<img src="ur cute/Large/058 sanacry.webp" height="96">
<img src="ur cute/Large/059 suiwave.webp" height="96">
<img src="ur cute/Large/060 AMsmartthink.webp" height="96">
<img src="ur cute/Large/061 NijikaThink.webp" height="96">
<img src="ur cute/Large/062  yaethink_anyuki.webp" height="96">
<img src="ur cute/Large/063 yaesmart_chickenjagoo.gif" height="96">
<img src="ur cute/Large/064 AMthink.webp" height="96">
<img src="ur cute/Large/065 Yes.webp" height="96">
<img src="ur cute/Large/066 YES.webp" height="96">
<img src="ur cute/Large/067 AMyes.webp" height="96">
<img src="ur cute/Large/068 SakuyaPhew.webp" height="96">
<img src="ur cute/Large/069 AyameLaugh.webp" height="96">
<img src="ur cute/Large/070  rosulaugh.webp" height="96">
<img src="ur cute/Large/071 pleading.webp" height="96">
<img src="ur cute/Large/072 rosublush.webp" height="96">
<img src="ur cute/Large/073 sigh.webp" height="96">
<img src="ur cute/Large/074 yaeraidenkiss_limeria.webp" height="96">
<img src="ur cute/Large/075 AMNoThanks.gif" height="96">
<img src="ur cute/Large/076 g11sleepy.gif" height="96">
<img src="ur cute/Large/077 AMCuddle.gif" height="96">
<img src="ur cute/Large/078 AMastolfokiss.webp" height="96">
<img src="ur cute/Large/079 astolfoblush.gif" height="96">
<img src="ur cute/Large/080 AMBoyKisserDance.gif" height="96">
<img src="ur cute/Large/081 AMmiyanoshrug.webp" height="96">
<img src="ur cute/Large/082 AMsleepydrool.webp" height="96">
<img src="ur cute/Large/086 InaFacepalm.webp" height="96">
<img src="ur cute/Large/087 grizzlyFacepalm.webp" height="96">
<img src="ur cute/Large/088 scared.gif" height="96">
<img src="ur cute/Large/089 ScaredCrow.webp" height="96">
<img src="ur cute/Large/090 BoneePat.webp" height="96">
<img src="ur cute/Large/091 Shrug.webp" height="96">
<img src="ur cute/Large/092 SCyes.gif" height="96">
<img src="ur cute/Large/093 3.webp" height="96">
<img src="ur cute/Large/094 JessicaBruh.webp" height="96">
<img src="ur cute/Large/095 KitaScared.gif" height="96">
<img src="ur cute/Large/096 KitaSob.webp" height="96">
<img src="ur cute/Large/097 KitaFuwa.gif" height="96">
<img src="ur cute/Large/098 KitaNotLikeThis.webp" height="96">
<img src="ur cute/Large/099 Mahiru.webp" height="96">
<img src="ur cute/Large/100 MahiruNo.gif" height="96">
<img src="ur cute/Large/101 MahiruBonk.gif" height="96">
<img src="ur cute/Large/102 Scared.webp" height="96">
<img src="ur cute/Large/103 Felix_scared.webp" height="96">
<img src="ur cute/Large/104 SuzuDance.webp" height="96">
<img src="ur cute/Large/105 SuzuHeart.webp" height="96">
<img src="ur cute/Large/106 SuzuNani.webp" height="96">
<img src="ur cute/Large/107 SL8Nuke.webp" height="96">
<img src="ur cute/Large/108 M4confused.webp" height="96">
<img src="ur cute/Large/109 TaischConfused.webp" height="96">
<img src="ur cute/Large/110 Pout.gif" height="96">
<img src="ur cute/Large/111 hey wyd.gif" height="96">
<img src="ur cute/Large/112 Squishy Cheeks.gif" height="96">
<img src="ur cute/Large/980 SCinside.gif" height="96">
<img src="ur cute/Large/981 lean.gif" height="96">
<img src="ur cute/Large/982 fat.gif" height="96">
<img src="ur cute/Large/983 wait.webp" height="96">
<img src="ur cute/Large/984 nomnommm.gif" height="96">
<img src="ur cute/Large/985 blue-archive-arona.gif" height="96">
<img src="ur cute/Large/986 stop-talking.gif" height="96">
<img src="ur cute/Large/987 Dear Dance.gif" height="96">
<img src="ur cute/Large/988 Yae Miko Lick.gif" height="96">
<img src="ur cute/Large/989 fish bite.gif" height="96">
<img src="ur cute/Large/990 Trailblazer_Nom01.png" height="96">
<img src="ur cute/Large/991 Pout.png" height="96">
<img src="ur cute/Large/992 uuu.webp" height="96">
<img src="ur cute/Large/993 Firewatch Nuke.gif" height="96">
<img src="ur cute/Large/994 nachoSuneruHD.webp" height="96">
<img src="ur cute/Large/995 Perlica Ice Cream.webp" height="96">
<img src="ur cute/Large/996 rainbow-dance.gif" height="96">
<img src="ur cute/Large/997 Smug.png" height="96">
<img src="ur cute/Large/998 AlphaScream.gif" height="96">
<img src="ur cute/Large/999 CatNod.gif" height="96">

</details><br><br>



<details> 
  <summary>XLarge</summary>

<img src="ur cute/ExtraLarge/001 cry.jpg" height="250">
<img src="ur cute/ExtraLarge/002 Cute Cheer.gif" height="250">
<img src="ur cute/ExtraLarge/003 dance-happy.gif" height="250">
<img src="ur cute/ExtraLarge/005 heart.gif" height="250">
<img src="ur cute/ExtraLarge/007 omori-basil.gif" height="250">
<img src="ur cute/ExtraLarge/008 ozu_oz_yarimasu_heart.gif" height="250">
<img src="ur cute/ExtraLarge/009 paw.png" height="250">
<img src="ur cute/ExtraLarge/011 sticker_1.gif" height="250">
<img src="ur cute/ExtraLarge/012 sticker_1.png" height="250">
<img src="ur cute/ExtraLarge/013 sticker_3.gif" height="250">
<img src="ur cute/ExtraLarge/014 sticker_5.png" height="250">
<img src="ur cute/ExtraLarge/015 sticker_6.gif" height="250">
<img src="ur cute/ExtraLarge/016 sticker_7.gif" height="250">
<img src="ur cute/ExtraLarge/017 sticker_9.gif" height="250">
<img src="ur cute/ExtraLarge/018 sticker_16.png" height="250">
<img src="ur cute/ExtraLarge/019 sticker_28.png" height="250">
<img src="ur cute/ExtraLarge/020 sticker_30.png" height="250">
<img src="ur cute/ExtraLarge/024 wataten-anime.gif" height="250">
<img src="ur cute/ExtraLarge/025 anime-anime-girl.gif" height="250">
<img src="ur cute/ExtraLarge/026 hu-tao-hungry.gif" height="250">
<img src="ur cute/ExtraLarge/027 onii-shy.gif" height="250">
<img src="ur cute/ExtraLarge/028 ehe-ehehe.gif" height="250">
<img src="ur cute/ExtraLarge/029 non-non-biyori-crying.gif" height="250">
<img src="ur cute/ExtraLarge/030 non-non-biyori-anime.gif" height="250">
<img src="ur cute/ExtraLarge/031 no-head-shaking.gif" height="250">
<img src="ur cute/ExtraLarge/032 HK416G11Sleep.gif" height="250">
<img src="ur cute/ExtraLarge/033 DushHairFlap.gif" height="250">
<img src="ur cute/ExtraLarge/034 shoujo-shuumtasu-ryouko-girls-last-tour.gif" height="250">
<img src="ur cute/ExtraLarge/035 miku-hello.gif" height="250">
<img src="ur cute/ExtraLarge/036 dancing-cat-dancing-kitten.gif" height="250">
<img src="ur cute/ExtraLarge/037 anime-cuteness.gif" height="250">
<img src="ur cute/ExtraLarge/038 nope-anime.gif" height="250">
<img src="ur cute/ExtraLarge/039 kawaii.gif" height="250">
<img src="ur cute/ExtraLarge/040 cat-block-eyes.jpg" height="250">
<img src="ur cute/ExtraLarge/041 anime-girl-blanket.gif" height="250">
<img src="ur cute/ExtraLarge/042 arknights-irene.gif" height="250">
<img src="ur cute/ExtraLarge/043 bocchi upset.jpg" height="250">
<img src="ur cute/ExtraLarge/044 bocchi-the-rock-nijika.gif" height="250">
<img src="ur cute/ExtraLarge/045 bratty-uoh.gif" height="250">
<img src="ur cute/ExtraLarge/046 emoji-crying.gif" height="250">
<img src="ur cute/ExtraLarge/047 cat vtuber.gif" height="250">
<img src="ur cute/ExtraLarge/048 honey-mitsukuni.gif" height="250">
<img src="ur cute/ExtraLarge/049 kiss-yuri.gif" height="250">
<img src="ur cute/ExtraLarge/050 nya-catboy.gif" height="250">
<img src="ur cute/ExtraLarge/051 pedro-henrique-wei-wei-wei-wei.gif" height="250">
<img src="ur cute/ExtraLarge/052 sad-i-love-you.gif" height="250">
<img src="ur cute/ExtraLarge/053 sora-no-method-celestial-method.gif" height="250">
<img src="ur cute/ExtraLarge/054 amiya-breakdance.gif" height="250">
<img src="ur cute/ExtraLarge/055 Anime Kiss.gif" height="250">
<img src="ur cute/ExtraLarge/056 Miyano Drool.gif" height="250">
<img src="ur cute/ExtraLarge/057 Wah Pleading Emoji.gif" height="250">
<img src="ur cute/ExtraLarge/058 Trapped.gif" height="250">
<img src="ur cute/ExtraLarge/059 Bocchi The Rock Nijika.gif" height="250">
<img src="ur cute/ExtraLarge/060 Shit Tarkov Grenade.gif" height="250">
<img src="ur cute/ExtraLarge/061 Stressed Out.gif" height="250">
<img src="ur cute/ExtraLarge/062 Elaina Pokerface.gif" height="250">
<img src="ur cute/ExtraLarge/063 Anime Girl Watching Movie.gif" height="250">
<img src="ur cute/ExtraLarge/064 30000 Usd.gif" height="250">
<img src="ur cute/ExtraLarge/065 hug mato yomi Black Rock.gif" height="250">
<img src="ur cute/ExtraLarge/066 Catgirl Red Head.gif" height="250">
<img src="ur cute/ExtraLarge/067 Azusawa Kohane Plead.gif" height="250">
<img src="ur cute/ExtraLarge/068 Love Lab Plead Cry.gif" height="250">
<img src="ur cute/ExtraLarge/069 Matt Do Your Homework.gif" height="250">
<img src="ur cute/ExtraLarge/070 Andrew do your homework.gif" height="250">
<img src="ur cute/ExtraLarge/071 Hi Adrian.gif" height="250">
<img src="ur cute/ExtraLarge/072 Minato Aqua Hi Matthew.gif" height="250">
<img src="ur cute/ExtraLarge/073 matthew-sama.gif" height="250">
<img src="ur cute/ExtraLarge/074 Anime Shy Kiss.gif" height="250">
<img src="ur cute/ExtraLarge/075 Tarkov Headshot.gif" height="250">
<img src="ur cute/ExtraLarge/076 Slap.gif" height="250">
<img src="ur cute/ExtraLarge/077 Nijika Dance.gif" height="250">
<img src="ur cute/ExtraLarge/078 Shika Dance.gif" height="250">
<img src="ur cute/ExtraLarge/079 Fran Sleepy.gif" height="250">
<img src="ur cute/ExtraLarge/080 Yuru Yuri Sleep Pat.gif" height="250">
<img src="ur cute/ExtraLarge/081 rest darling.gif" height="250">
<img src="ur cute/ExtraLarge/082 Mahiro Oyama Onimai Rawr.gif" height="250">
<img src="ur cute/ExtraLarge/083 Tbh Creature Ddr.gif" height="250">
<img src="ur cute/ExtraLarge/084 Hsr Honkai Cheeks.gif" height="250">
<img src="ur cute/ExtraLarge/085 yunayuispink Crayon Eat.webp" height="250">
<img src="ur cute/ExtraLarge/086 yunayuispink Crayon Share.gif" height="250">
<img src="ur cute/ExtraLarge/087 Kita Bocchi Doodle Dance.gif" height="250">
<img src="ur cute/ExtraLarge/088 Kanna Cuddle.gif" height="250">
<img src="ur cute/ExtraLarge/089 yuruyuri bath cuddle.gif" height="250">

</details><br><br>



<details> 
  <summary>XLargeCat</summary>
<img src="ur cute/ExtraLargeCat/001 cat-love.gif" height="250">
<img src="ur cute/ExtraLargeCat/002 cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/003 cat-stare.gif" height="250">
<img src="ur cute/ExtraLargeCat/004 cat-stare-angry-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/005 emoji12-emoji-12.gif" height="250">
<img src="ur cute/ExtraLargeCat/006 huh-cat-huh-m4rtin.gif" height="250">
<img src="ur cute/ExtraLargeCat/007 suspicious-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/008 sad-sad-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/009 sad-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/010 cat-cat-pat.gif" height="250">
<img src="ur cute/ExtraLargeCat/011 huh-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/012 annoyed-disappointed.gif" height="250">
<img src="ur cute/ExtraLargeCat/013 rrane-battal.gif" height="250">
<img src="ur cute/ExtraLargeCat/014 cat-tired-cat-falling-asleep.gif" height="250">
<img src="ur cute/ExtraLargeCat/015 cute-kitten.gif" height="250">
<img src="ur cute/ExtraLargeCat/016 cat-staring.gif" height="250">
<img src="ur cute/ExtraLargeCat/017 cat-dance-dancing-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/018 cool-fun.gif" height="250">
<img src="ur cute/ExtraLargeCat/019 wow-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/020 cat-wiggle-dance-cat-shake-dance.gif" height="250">
<img src="ur cute/ExtraLargeCat/021 walk sniff.gif" height="250">
<img src="ur cute/ExtraLargeCat/022 cat-yawning.gif" height="250">
<img src="ur cute/ExtraLargeCat/023 hug.jpg" height="250">
<img src="ur cute/ExtraLargeCat/024 mrfresh-sad-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/025 meow-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/026 cat-cat-jumping.gif" height="250">
<img src="ur cute/ExtraLargeCat/27 cat yawn.gif" height="250">
<img src="ur cute/ExtraLargeCat/28 lazy-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/29 cat-drag.gif" height="250">
<img src="ur cute/ExtraLargeCat/30 happy sad cat.jpg" height="250">
<img src="ur cute/ExtraLargeCat/31 dance-dancing.gif" height="250">
<img src="ur cute/ExtraLargeCat/32 reeeh.png" height="250">
<img src="ur cute/ExtraLargeCat/33 cat look hand.jpg" height="250">
<img src="ur cute/ExtraLargeCat/34 tole-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/35 cat-funny.gif" height="250">
<img src="ur cute/ExtraLargeCat/36 cat bounce.gif" height="250">
<img src="ur cute/ExtraLargeCat/37 cat trampoline.png" height="250">
<img src="ur cute/ExtraLargeCat/38 cat-wiggle.gif" height="250">
<img src="ur cute/ExtraLargeCat/39 cat-lying-cat-paws.gif" height="250">
<img src="ur cute/ExtraLargeCat/40 cat-upset-going-insane.gif" height="250">
<img src="ur cute/ExtraLargeCat/41 cat-kitty.gif" height="250">
<img src="ur cute/ExtraLargeCat/42 shh.png" height="250">
<img src="ur cute/ExtraLargeCat/43 judging-side.gif" height="250">
<img src="ur cute/ExtraLargeCat/44 exploding-car-explode.gif" height="250">
<img src="ur cute/ExtraLargeCat/45 kitty-stuck.gif" height="250">
<img src="ur cute/ExtraLargeCat/46 cat-shaking.gif" height="250">
<img src="ur cute/ExtraLargeCat/47 green screen cat.png" height="250">
<img src="ur cute/ExtraLargeCat/48 cats-scared.gif" height="250">
<img src="ur cute/ExtraLargeCat/49 bunnycat.gif" height="250">
<img src="ur cute/ExtraLargeCat/50 orange-cat-cat-hitting-cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/51 shhhhh.png" height="250">
<img src="ur cute/ExtraLargeCat/52 cat soda.gif" height="250">
<img src="ur cute/ExtraLargeCat/53 cat my reaction to that info.gif" height="250">
<img src="ur cute/ExtraLargeCat/54 Cat Close Stare.jpg" height="250">
<img src="ur cute/ExtraLargeCat/55 Cat Hide.gif" height="250">
<img src="ur cute/ExtraLargeCat/57 Violence Grrrr.gif" height="250">
<img src="ur cute/ExtraLargeCat/58 ATTEEEENSHUN.gif" height="250">
<img src="ur cute/ExtraLargeCat/59 Chipi Chapa Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/60 Dance Freaky Freaky Mode.gif" height="250">
<img src="ur cute/ExtraLargeCat/61 Sad Kitty Sad Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/62 Cat Explosion.gif" height="250">
<img src="ur cute/ExtraLargeCat/63 Cat Tail.gif" height="250">
<img src="ur cute/ExtraLargeCat/64 Silly Cat Silly Car.gif" height="250">
<img src="ur cute/ExtraLargeCat/65 Cat Stand Stare.gif" height="250">
<img src="ur cute/ExtraLargeCat/66 Cat Angry.gif" height="250">
<img src="ur cute/ExtraLargeCat/67 Cat Look.gif" height="250">
<img src="ur cute/ExtraLargeCat/68 Pleased Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/69 Small Cat Hang.gif" height="250">
<img src="ur cute/ExtraLargeCat/70 getting jiggy with it.gif" height="250">
<img src="ur cute/ExtraLargeCat/71 Cat lost mind.gif" height="250">
<img src="ur cute/ExtraLargeCat/72 Hey Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/73 Are You Serious Right Meow.gif" height="250">
<img src="ur cute/ExtraLargeCat/74 Sad Tired Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/75 Cat Explosion.gif" height="250">
<img src="ur cute/ExtraLargeCat/76 Cat Wave Sitting.gif" height="250">
<img src="ur cute/ExtraLargeCat/77 Cat toes stretch.gif" height="250">
<img src="ur cute/ExtraLargeCat/78 Kitty Slap.gif" height="250">
<img src="ur cute/ExtraLargeCat/79 Cat Fight.gif" height="250">
<img src="ur cute/ExtraLargeCat/80 Cat Tongue.gif" height="250">
<img src="ur cute/ExtraLargeCat/81 Cat Squish.gif" height="250">
<img src="ur cute/ExtraLargeCat/82 Cat Look.gif" height="250">
<img src="ur cute/ExtraLargeCat/83 Cat Paws.gif" height="250">
<img src="ur cute/ExtraLargeCat/84 Cat Dance.gif" height="250">
<img src="ur cute/ExtraLargeCat/85 Cat Dance.gif" height="250">
<img src="ur cute/ExtraLargeCat/86 Cat Pout Paw.gif" height="250">
<img src="ur cute/ExtraLargeCat/87 Cat Sushi.gif" height="250">
<img src="ur cute/ExtraLargeCat/88 Cat Kiss Cuddle.gif" height="250">
<img src="ur cute/ExtraLargeCat/89 Kitten poopin.gif" height="250">
<img src="ur cute/ExtraLargeCat/90 Sad Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/91 Sad Cat.gif" height="250">
<img src="ur cute/ExtraLargeCat/92 Cat Stand Dance.gif" height="250">
<img src="ur cute/ExtraLargeCat/93 Happy Cat Silly.gif" height="250">


</details><br><br>



<details> 
  <summary>Standard Wallpapers</summary>

<img src="Standard Wallpapers/Landscape/120 Nobunga.jpg" height="350">
<img src="Standard Wallpapers/Landscape/122 Saber Lily.png" height="350">
<img src="Standard Wallpapers/Landscape/359 Sopmod.jpg" height="350">
<img src="Standard Wallpapers/Landscape/404 Clouds.jpg" height="350">
<img src="Standard Wallpapers/Landscape/612 Rhine Lab.jpg" height="350">
<img src="Standard Wallpapers/Landscape/613 Nearl.jpg" height="350">
<img src="Standard Wallpapers/Landscape/621 EP - [Bridge to the Dawn].jpg" height="350">
<img src="Standard Wallpapers/Landscape/624 Arknights Endfield.png" height="350">
<img src="Standard Wallpapers/Landscape/GFL404 Clean.png" height="350">
<img src="Standard Wallpapers/Landscape/GFLAR.png" height="350">
<img src="Standard Wallpapers/Landscape/Halo Reach Space.jpg" height="350">
<img src="Standard Wallpapers/Landscape/Koenigsegg.jpg" height="350">
<img src="Standard Wallpapers/Landscape/Predator.png" height="350">
<img src="Standard Wallpapers/Landscape/Red Wallpaper.jpg" height="350">
<img src="Standard Wallpapers/Landscape/Small Pic Svarog Heavy Industries.png" height="350">
<br>
<img src="Standard Wallpapers/Portrait/1ad3ba6.jpg" height="350">
<img src="Standard Wallpapers/Portrait/20240119_232804.jpg" height="350">
<img src="Standard Wallpapers/Portrait/316a1ff.png" height="350">
<img src="Standard Wallpapers/Portrait/404.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Artoria 46.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Copy of IMG_20191008_215858.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Fate Servants.png" height="350">
<img src="Standard Wallpapers/Portrait/G&K Extended.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Griffin Emblem Extended.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Okita.jpg" height="350">
<img src="Standard Wallpapers/Portrait/Saber 8.png" height="350">
<img src="Standard Wallpapers/Portrait/tumblr_owrccebouC1u41kbzo1_1280.png" height="350">

</details> <br><br>



<details> 
  <summary>Other</summary>

        [![Love](https://media.tenor.com/QAU2oFvucdcAAAAC/heart.gif)](https://tenor.com/view/heart-gif-18231995)
        [![](Img)](Link)
        ![](Img)
        <a href=""><img src=""></a>
        <img src="ur cute/" alt="ur cute/">

                

        dir /b /ON > namelist.txt (Windows 10)
        cmd /r dir /b /ON > filename.txt (Windows 11)

        VSCode
        Search:
        ^(.+)$
        Replace:
        <img src="Standard Wallpapers/$1">
        <img src="ur cute/$1"> 

</details> 

