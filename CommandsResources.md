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
  
- Other Commands

        git init (initialize local repo)
        git status
        git config --list
___
- Adding To A Repository On Git - (MAIN)

        git add (will show differences in code and possible conflicts)
          git add *.java (add a folder without the '/')
            git add . (adds modified files)
            git add filename.filetype
            git add -A (adds all changes, what I usually use)
      
        git commit -m "comment"
        git push origin ***branchName***

___
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

- File Management
  - .gitignore (File)<br>
    > __pycache__/ (Ignore folder)<br>
    > macrolist/*.txt (Ignore file)<br>
  - .gitkeep (File that keeps folders)
  
- Windows Git Shortcut<br>

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
</details>

- Device - Insert Guest Additions CD Image...
- Go to disk and run:

        sudo ./VBoxLinuxAdditions.run<br>
        sudo adduser 'user' vboxsf



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## General Application Link Stuff
- Linux
> gThumb - Image Viewer<br>
> Drawing - Image Editor<br>
> Timeshift - OS Backup<br>
> htop - Process Viewer<br>
> File manager<br>
> Vim - Text Editor<br>

- Windows
> OBS https://obsproject.com/ <br>
> ffmpeg https://ffmpeg.org/ <br>
> youtube-dl https://github.com/yt-dlp/yt-dlp <br>
> mkvtoolnix https://mkvtoolnix.download/ <br>
> process_lasso https://bitsum.com/ <br>
> vscodium <br>
> vlc https://www.videolan.org/vlc/ <br>
> 7zip <br>
> gpuz <br>
> cpuz <br>
> WinDirStat https://windirstat.net/ <br>
> Crystaldiskinfo https://crystalmark.info/en/software/crystaldiskinfo/ <br>
> Mp3tag https://www.mp3tag.de/en/ <br>
> PC Benchmark https://www.userbenchmark.com<br>
> All info ip can get off you https://ipleak.net/ <br>
> Wireshark https://www.wireshark.org/ <br>
> Firefox - Web Browser <br>
> Image Editor https://www12.lunapic.com/editor/?action=transparent <br>
> Git - Github

- Personal
> https://regexr.com/ <br>
> Temporary Video Sharing https://streamable.com/ <br>
> [Discord History](https://github.com/Tyrrrz/DiscordChatExporter/releases) - [Guide](https://www.swipetips.com/how-to-download-your-chat-history-from-discord/) <br>
> [Discord](https://ptb.discord.com/download)

<details> 
  <summary>Anime</summary>
  <a href="https://danbooru.donmai.us/">danbooru</a>
  <a href="https://gelbooru.com/">gelbooru</a>
  <a href="https://www.pixiv.net/en/">pixiv</a>
  <a href="https://github.com/Tsuk1ko/nhentai-helper">Tsuk1ko/nhentai-helper</a>
  <a href="e-hentai.org">e-hentai</a>
  <a href="https://nhentai.net/">nhentai</a>
  <a href="https://hanime.tv/">hanime</a>
</details>

> Image Search https://findit.moe/ https://iqdb.org/ https://saucenao.com/<br>
> Upscaler https://waifu2x.udp.jp/ <br>
> Manga https://mangadex.org/ https://j8jp.com/ https://tachiyomi.org/<br>
> DL https://animekaizoku.com/ https://www.animeout.xyz/ https://anidl.org/ <br>
> Stream https://9anime.nl/ https://animepahe.ru/ https://littleweeb.github.io/ <br>
> Music https://downloads.khinsider.com/ <br>
> Sheet Music https://josh.agarrado.net/music/anime/index.php <br>

- Game Stuff
> Osu replays https://ordr.issou.best/ <br>
> https://www.gflcorner.com/ <br>
> [GFL Logistics Calculator](https://tempkaridc.github.io/gf/) <br>
> [Arknights Aceship's Toolbox](https://aceship.github.io/AN-EN-Tags/index.html) <br>
> https://escapefromtarkov.gamepedia.com/Escape_from_Tarkov_Wiki <br>
> https://eftfg.com/ammo  <br>
> [Steam](https://store.steampowered.com/)

<details> 
  <summary>JP</summary>
  <a href="https://github.com/yudataguy/Awesome-Japanese#beginner-guide">General</a> <br>
  <a href="https://supernative.tv/ja/">Phrases</a> <br>
  <a href="https://www.technologyimprov.com/HiraganaAudioQuiz">Hiragana Audio Memorize</a> <br>
  <a href="https://realkana.com/hiragana/">Memorize Kana</a> <br>
  <a href="https://laits.utexas.edu/japanese/joshu/index.php">Many Resources</a>
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
> ffmpeg.exe

- BATCH CONVERT

        for %a in ("*.webp") do ffmpeg -i "%a" "%~na.png"
        for %a in ("%CD%\*.webp") do ffmpeg -i "%a" "%CD%\%~na.png"
        for %a in ("Convert\*.webm") do ffmpeg -i "%a" "Converted\%~na.mp3"
        for %a in ("Convert\*.webp") do ffmpeg -i "%a" "Converted\%~na.png"

- COMBINE

        ffmpeg -i "video.mp4" -i "audio.mp3" -map 0:v -map 1:a -c:v copy -c:a copy output.mp4 -y

- BATCH COMBINE

        for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.mp3" -map 0:v -map 1:a -c:v copy -c:a copy "Combined\%~na.mp4" -y

- SUBTITLE COMBINE (NOT WORKING CORRECTLY)

        ffmpeg -i "input.mp4" -i "subtitles.srt" -c:s mov_text -c:v copy -c:a copy output.mp4

- BATCH SUBTITLE COMBINE (NOT WORKING CORRECTLY)

        for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.srt" -c:s mov_text -c:v copy -c:a copy "Combined\%~na.mp4"

So to add auto-numbering, use -A

- DOWNLOAD FROM TXT

        youtube-dl -f best -o "%(autonumber)0Nd-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 63 --add-header ""

Use output template with %(autonumber)0Nd, where N in the number of digits instead.

        youtube-dl -f best -o "%(autonumber)03d-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 66 --add-header "


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



<br> <br> <br> <br> <br> <br> <br> <br>



<span style="font-size:12px"><a href="#top">Back to top</a></span>

## Emojis
- Small<br>
![](https://cdn.discordapp.com/emojis/1009944658215964692.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1010727401174609970.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1009944657129635921.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1009054288984674384.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994400877899157535.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008951861056917584.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008933434690899989.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1009014557332742164.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994400996732182638.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994391665693433957.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994400901970284574.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994595815727312987.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1003541293915459715.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1003542290498850896.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/996787275566415923.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008943280530128969.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/994400797418860644.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008943429973196810.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1009944659398762586.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008943445294985350.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008943324830367774.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1020764778723020921.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008944349557559297.webp?size=44&quality=lossless)
![](https://images-ext-2.discordapp.net/external/O3tjk3f17HpkgELKqJ6XSi_zaD-Fbe_C2Ng4MTmG98U/%3Fsize%3D44%26quality%3Dlossless/https/cdn.discordapp.com/emojis/621806265815007253.gif)
![](https://cdn.discordapp.com/emojis/1008959215940939858.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1037899706451365959.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1037899706451365959.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1037899679532318740.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008933567088312360.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1025597703226400890.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/1026012316988346438.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/878169827951398912.webp?size=44&quality=lossless)
![](https://cdn.discordapp.com/emojis/966134363974684723.webp?size=44&quality=lossless)
<br><br>
- Medium<br>
![](https://cdn.discordapp.com/emojis/724367095512694825.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/944211230422368338.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/362261098042490880.webp?size=64)
![](https://cdn.discordapp.com/emojis/907735601976074300.gif?size=64)
<br><br>
- Large<br>
![](https://cdn.discordapp.com/emojis/1008933567088312360.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1025532028596264970.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/585570082961489930.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/774990963310985226.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/586089930678337537.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/737698266279444522.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/879239220659634257.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008933763658559591.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/747680403778699304.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/621806265815007253.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1009944658215964692.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/725701811499171990.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1024665531032272976.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1032083443561005167.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/619630409705193531.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/777074089197568021.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/878169827951398912.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/878169786130006017.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/1008943379377303662.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/968733546875351050.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/attachments/1037744564796133468/1127875535821877278/nekooo.gif)
![](https://cdn.discordapp.com/emojis/850356405445591080.gif?size=96&quality=lossless)
![](https://cdn.discordapp.com/emojis/828643173571231824.webp?size=96&quality=lossless)
![](https://cdn.discordapp.com/attachments/662512876279431168/805239545930842152/UwuHug.png)
![](https://cdn.discordapp.com/attachments/662512876279431168/805239639031283763/NeroCry.jpg)
![](https://cdn.discordapp.com/attachments/662512876279431168/805239640453021766/NeroSmug.jpg)
![](https://cdn.discordapp.com/attachments/662512876279431168/805239642885849108/156401486598743612.png)
![](https://cdn.discordapp.com/emojis/602513888378093578.webp?size=96&quality=lossless)

<br><br>
- Extra Large<br>
![](https://cdn.discordapp.com/attachments/1025614305225351168/1119391392939130941/ezgif-4-82e974469a.gif)
![](https://cdn.discordapp.com/emojis/702810323111116800.gif?v=1)
![](https://cdn.discordapp.com/attachments/662512876279431168/1015194334720708658/unknown.png)
![](https://cdn.discordapp.com/attachments/662512876279431168/1007950501813420032/output-onlinepngtools1.png)
![](https://cdn.discordapp.com/emojis/436660999957774336.webp?size=96&quality=lossless)
[![](https://media.tenor.com/o0obZG4WdnYAAAAi/rainbow-dance.gif)](https://tenor.com/view/rainbow-dance-neko-sway-discord-gif-18951681)
<br><br>
<details> 
  <summary>XXLarge</summary>
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1122393794134945834/1.png">
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1122393794550173806/2.png">
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1122393794906697789/image.png">
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1122393795217068032/4.png">
  <img src="https://cdn.discordapp.com/attachments/1037744564796133468/1127503982676410440/image.png">
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1130271620674617384/image.png">
  <br>
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1013933817444184174/baef86257e732b51ac56e6b0f967a081a3a741b090b85efea8032b94f7de1edd.jpeg">\
  <a href="https://tenor.com/view/elaina-nod-gif-25532943"><img src="https://media.tenor.com/lNkVGL4mLDAAAAAC/elaina-nod.gif"></a>
  <a href="https://tenor.com/view/omori-basil-kiss-gay-gif-25386247"><img src="https://media.tenor.com/0b-eojIy5WoAAAAC/omori-basil.gif"></a>
  <a href="https://tenor.com/view/wataten-anime-gif-13473080"><img src="https://media.tenor.com/48kR48pMSgMAAAAC/wataten-anime.gif"></a>
  <img src="https://cdn.discordapp.com/attachments/662512876279431168/1122393796047540234/FntBZwuXwAEXwtL.png">
</details>
<br>

[![Love](https://media.tenor.com/QAU2oFvucdcAAAAC/heart.gif)](https://tenor.com/view/heart-gif-18231995)

[![](Img)](Link)
![](Img)
<a href=""><img src=""></a>