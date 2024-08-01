# Commands & Resources
List of commands and resources that are personally useful for me.

VS Code Settings Markdown > Preview Scroll Editor/Preview with Preview/Editor
## Table of Contents
1. [Markdown Guide](#markdown-guide)
2. [Git Commands](#git-commands)
3. [Linux Commands & Resources](LinuxCmdRsrc.md)
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

> [Windows in a Bottle](https://usebottles.com/)<br>
> fastfetch [logo](https://github.com/fastfetch-cli/fastfetch/wiki/Logo-options)<br>
> Drawing - Image Editor<br>
> gThumb - Image Viewer<br>
> Vim - Text Editor<br>
> [It's FOSS](https://itsfoss.com/)<br>
> [sysguides](https://sysguides.com/)<br>
> [Linux Ricing](https://github.com/avtzis/awesome-linux-ricing)<br>

### Android
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
> Music Player [mpv](https://mpv.io/) [foobar2000](https://www.foobar2000.org/)<br>


### Web Browser
> [Popup Blocker](https://addons.mozilla.org/en-US/firefox/addon/popup-blocker/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Smart HTTPS](https://addons.mozilla.org/en-US/firefox/addon/smart-https-revived/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [The Camelizer - Price Tracker](https://addons.mozilla.org/en-US/firefox/addon/the-camelizer-price-history-ch/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [DocsAfterDark](https://addons.mozilla.org/en-US/firefox/addon/docsafterdark/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)<br>
> [Youtube Ad Auto-skipper](https://addons.mozilla.org/en-US/firefox/addon/youtube-ad-auto-skipper/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) <br>
>[Tabliss](https://addons.mozilla.org/en-US/firefox/addon/tabliss/)<br>
> [Firefox Color](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/)<br>
> [Website Blocker](https://addons.mozilla.org/en-US/firefox/addon/block-website/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) [Git](https://github.com/ray-lothian/Block-Site)

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
[aniwave](https://aniwave.to/)
[animepahe](https://animepahe.ru/)
[littleweeb](https://littleweeb.github.io/)
[kickassanime](https://kickassanime.am/)<br>
> Music [khinsider](https://downloads.khinsider.com/) <br>
> [Sheet Music agarrado](https://josh.agarrado.net/music/anime/index.php) <br>

### Game Stuff
> Osu replays https://ordr.issou.best/ <br>
> [Escape From Tarkov Wiki](https://escapefromtarkov.gamepedia.com/Escape_from_Tarkov_Wiki) [Armor](https://tarkov.dev/items/armors) [Ammo](https://www.eft-ammo.com/ammo-graph)<br>
> https://eftfg.com/ammo<br>
> [Steam](https://store.steampowered.com/)<br>
> [Switch Emulator](https://ryujinx.org/download)<br>
> [ATLauncher (Minecraft)](https://atlauncher.com/)

> [Girls' Frontline Cutscene Interpreter](https://gfl.amaryllisworks.pw/)
> [GFL Corner](https://www.gflcorner.com/)
> [GFL Music Player](https://girlsfrontline.kr/musicplayer)
> [GFL Logistics Calculator](https://tempkaridc.github.io/gf/) <br>
> [Arknights Tier List](https://ak.gamepress.gg/tier-list/arknights-operator-tier-list)
> [Arknights Aceship's Toolbox](https://aceship.github.io/AN-EN-Tags/index.html) <br>


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

<img src="ur cute/01 catgirlhuggies.webp"><img src="ur cute/02 kristineunicry.webp"><img src="ur cute/03 emiliaaa.webp"><img src="ur cute/04 noelsip.webp"><img src="ur cute/05 AquaHD.webp"><img src="ur cute/06 cryrosu.webp"><img src="ur cute/06 rosucrybread.webp"><img src="ur cute/06 rosuneutral.webp"><img src="ur cute/07 kiss~1.webp"><img src="ur cute/08 diaredevil.webp"><img src="ur cute/09 WATEFAK.webp"><img src="ur cute/10 shunyaaa.webp"><img src="ur cute/11 suck.webp"><img src="ur cute/12 unicry.webp"><img src="ur cute/13 KeqingGN.webp"><img src="ur cute/14 happy.webp"><img src="ur cute/15 NJgasm.webp"><img src="ur cute/16 gn.webp"><img src="ur cute/17 rikashock.webp"><img src="ur cute/18 AquaCry.webp"><img src="ur cute/19 TokoPat.webp"><img src="ur cute/20 ayameheart.webp"><img src="ur cute/21 murmwot.webp"><img src="ur cute/22 kokomisigh.webp"><img src="ur cute/23 nani.webp"><img src="ur cute/24 hornyisback.webp"><img src="ur cute/25 rosusigh.webp"><img src="ur cute/26 sob.gif"><img src="ur cute/27 yaedrive_chickenjagoo.gif"><img src="ur cute/28 wubbaboo_tired.webp"><img src="ur cute/29 WatameHuh.webp"><img src="ur cute/30 suiwave.webp"><img src="ur cute/31 limwat.webp"><img src="ur cute/32 AlstolfoBlush.webp"><img src="ur cute/33 AMsalute.webp"><img src="ur cute/34 ArcyPouty.webp"><img src="ur cute/35 catHUH.gif"><img src="ur cute/36 ChenShrug.webp"><img src="ur cute/37 ded.webp"><img src="ur cute/38 ElainaHeart.webp"><img src="ur cute/39 giveheart.gif"><img src="ur cute/40 goodmorning.webp"><img src="ur cute/41 goodnight.webp"><img src="ur cute/42 heh.gif"><img src="ur cute/43 hkpatpat.gif"><img src="ur cute/44 notlikethis.webp"><img src="ur cute/45 OkayuMogu.webp"><img src="ur cute/46 p7wink.webp"><img src="ur cute/47 pp90blush.webp"><img src="ur cute/48 rinkodespair.webp"><img src="ur cute/49 RoseDead.webp"><img src="ur cute/50 rosuhappy.gif"><img src="ur cute/51 rosunote.gif"><img src="ur cute/52 rosupatpat.gif"><img src="ur cute/53 rosupout.gif"><img src="ur cute/54 SanaYapi.webp"><img src="ur cute/55 SanaBox.webp"><img src="ur cute/56 SanaSad1.webp"><img src="ur cute/57 SanaSad2.webp"><img src="ur cute/58 SanaTeehee.webp"><img src="ur cute/59 SanaWorried.webp"><img src="ur cute/60 AMsmartthink.webp"><img src="ur cute/61 NijikaThink.webp"><img src="ur cute/62  yaethink_anyuki.webp"><img src="ur cute/63 yaesmart_chickenjagoo.gif"><img src="ur cute/64 AMthink.webp"><img src="ur cute/65 Yes.webp"><img src="ur cute/66 YES.webp"><img src="ur cute/67 AMyes.webp"><img src="ur cute/68 SakuyaPhew.webp"><img src="ur cute/69 AyameLaugh.webp"><img src="ur cute/70  rosulaugh.webp"><img src="ur cute/71 pleading.webp"><img src="ur cute/72 zerotwoheart.webp"><img src="ur cute/95 noted-anime.gif"><img src="ur cute/96 NeroGasm.webp"><img src="ur cute/97 Meow.gif"><img src="ur cute/98 fubukidance.gif"><img src="ur cute/99 awawa.gif">
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
<img src="ur cute/Large/22 suicheer.png">
<img src="ur cute/Large/23 AlstolfoBlush.webp">
<img src="ur cute/Large/24 ArcyPouty.webp">
<img src="ur cute/Large/25 awawa.webp">
<img src="ur cute/Large/26 pray.webp">
<img src="ur cute/Large/27 sob.gif">
<img src="ur cute/Large/28 yes.gif">
<img src="ur cute/Large/29 teehee.webp">
<img src="ur cute/Large/30 shrug.webp">
<img src="ur cute/Large/31 wubbaboo_tired.webp">
<img src="ur cute/Large/32 sway.gif">
<img src="ur cute/Large/33 ChenShrug.webp">
<img src="ur cute/Large/34 ded.webp">
<img src="ur cute/Large/35 ElainaFustrated.webp">
<img src="ur cute/Large/36 ElainaHeart.webp">
<img src="ur cute/Large/37 ElainaThumbsUp.webp">
<img src="ur cute/Large/38 WatameHuh.webp">
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
<img src="ur cute/Large/52 TakeNotes.webp">
<img src="ur cute/Large/53 pp90blush.webp">
<img src="ur cute/Large/54 Question.webp">
<img src="ur cute/Large/55 suijuice.webp">
<img src="ur cute/Large/56 sana Wink.webp">
<img src="ur cute/Large/57 SanaBox.webp">
<img src="ur cute/Large/58 sanacry.webp">
<img src="ur cute/Large/59 suiwave.webp">
<img src="ur cute/Large/60 AMsmartthink.webp">
<img src="ur cute/Large/61 NijikaThink.webp">
<img src="ur cute/Large/62  yaethink_anyuki.webp">
<img src="ur cute/Large/63 yaesmart_chickenjagoo.gif">
<img src="ur cute/Large/64 AMthink.webp">
<img src="ur cute/Large/65 Yes.webp">
<img src="ur cute/Large/66 YES.webp">
<img src="ur cute/Large/67 AMyes.webp">
<img src="ur cute/Large/68 SakuyaPhew.webp">
<img src="ur cute/Large/69 AyameLaugh.webp">
<img src="ur cute/Large/70  rosulaugh.webp">
<img src="ur cute/Large/71 pleading.webp">
<img src="ur cute/Large/88 Yae Miko Lick.gif">
<img src="ur cute/Large/89 fish bite.gif">
<img src="ur cute/Large/90 Trailblazer_Nom01.png">
<img src="ur cute/Large/91 Pout.png">
<img src="ur cute/Large/92 uuu.webp">
<img src="ur cute/Large/93 Firewatch Nuke.gif">
<img src="ur cute/Large/94 nachoSuneruHD.webp">
<img src="ur cute/Large/95 Perlica Ice Cream.webp">
<img src="ur cute/Large/96 rainbow-dance.gif">
<img src="ur cute/Large/97 Smug.png">
<img src="ur cute/Large/98 AlphaScream.gif">
<img src="ur cute/Large/99 CatNod.gif">

</details><br><br>



<details> 
  <summary>XLarge</summary>

<img src="ur cute/ExtraLarge/01 cry.jpg">
<img src="ur cute/ExtraLarge/02 Cute Cheer.gif">
<img src="ur cute/ExtraLarge/03 dance-happy.gif">
<img src="ur cute/ExtraLarge/05 heart.gif">
<img src="ur cute/ExtraLarge/07 omori-basil.gif">
<img src="ur cute/ExtraLarge/08 ozu_oz_yarimasu_heart.gif">
<img src="ur cute/ExtraLarge/09 paw.png">
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
<img src="ur cute/ExtraLarge/24 wataten-anime.gif">
<img src="ur cute/ExtraLarge/25 anime-anime-girl.gif">
<img src="ur cute/ExtraLarge/26 hu-tao-hungry.gif">
<img src="ur cute/ExtraLarge/27 onii-shy.gif">
<img src="ur cute/ExtraLarge/28 ehe-ehehe.gif">
<img src="ur cute/ExtraLarge/29 non-non-biyori-crying.gif">
<img src="ur cute/ExtraLarge/30 non-non-biyori-anime.gif">

</details><br><br>



<details> 
  <summary>XLargeCat</summary>

<img src="ur cute/ExtraLargeCat/01 cat-love.gif">
<img src="ur cute/ExtraLargeCat/02 cat.gif">
<img src="ur cute/ExtraLargeCat/03 cat-stare.gif">
<img src="ur cute/ExtraLargeCat/04 cat-stare-angry-cat.gif">
<img src="ur cute/ExtraLargeCat/05 emoji12-emoji-12.gif">
<img src="ur cute/ExtraLargeCat/06 huh-cat-huh-m4rtin.gif">
<img src="ur cute/ExtraLargeCat/07 suspicious-cat.gif">
<img src="ur cute/ExtraLargeCat/08 sad-sad-cat.gif">
<img src="ur cute/ExtraLargeCat/09 sad-cat.gif">
<img src="ur cute/ExtraLargeCat/10 cat-cat-pat.gif">
<img src="ur cute/ExtraLargeCat/11 huh-cat.gif">
<img src="ur cute/ExtraLargeCat/12 annoyed-disappointed.gif">
<img src="ur cute/ExtraLargeCat/13 rrane-battal.gif">
<img src="ur cute/ExtraLargeCat/14 cat-tired-cat-falling-asleep.gif">
<img src="ur cute/ExtraLargeCat/15 cute-kitten.gif">
<img src="ur cute/ExtraLargeCat/16 cat-staring.gif">
<img src="ur cute/ExtraLargeCat/17 cat-dance-dancing-cat.gif">
<img src="ur cute/ExtraLargeCat/18 cool-fun.gif">

</details><br><br>



<details> 
  <summary>Standard Wallpapers</summary>

<img src="Standard Wallpapers/120 Nobunga.jpg">
<img src="Standard Wallpapers/122 Saber Lily.png">
<img src="Standard Wallpapers/1ad3ba6.jpg">
<img src="Standard Wallpapers/20240119_232804.jpg">
<img src="Standard Wallpapers/316a1ff.png">
<img src="Standard Wallpapers/359 Sopmod.jpg">
<img src="Standard Wallpapers/404 Clouds.jpg">
<img src="Standard Wallpapers/404.jpg">
<img src="Standard Wallpapers/612 Rhine Lab.jpg">
<img src="Standard Wallpapers/613 Nearl.jpg">
<img src="Standard Wallpapers/621 EP - [Bridge to the Dawn].jpg">
<img src="Standard Wallpapers/624 Arknights Endfield.png">
<img src="Standard Wallpapers/Artoria 46.jpg">
<img src="Standard Wallpapers/Copy of IMG_20191008_215858.jpg">
<img src="Standard Wallpapers/Fate Servants.png">
<img src="Standard Wallpapers/G&K Extended.jpg">
<img src="Standard Wallpapers/GFL404 Clean.png">
<img src="Standard Wallpapers/GFLAR.png">
<img src="Standard Wallpapers/Griffin Emblem Extended.jpg">
<img src="Standard Wallpapers/Halo Reach Space.jpg">
<img src="Standard Wallpapers/Koenigsegg.jpg">
<img src="Standard Wallpapers/Okita.jpg">
<img src="Standard Wallpapers/Predator.png">
<img src="Standard Wallpapers/Red Wallpaper.jpg">
<img src="Standard Wallpapers/Saber 8.png">
<img src="Standard Wallpapers/Small Pic Svarog Heavy Industries.png">
<img src="Standard Wallpapers/tumblr_owrccebouC1u41kbzo1_1280.png">

</details> <br><br>



<details> 
  <summary>Other</summary>

        [![Love](https://media.tenor.com/QAU2oFvucdcAAAAC/heart.gif)](https://tenor.com/view/heart-gif-18231995)
        [![](Img)](Link)
        ![](Img)
        <a href=""><img src=""></a>
        <img src="ur cute/" alt="ur cute/">

                

        dir /b /ON > namelist.txt

        VSCode Search
        <img src="Standard Wallpapers/$1">
        <img src="ur cute/$1"> 
        </details> 

