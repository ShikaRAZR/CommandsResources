# Commands & Resources
List of commands and resources that are personally useful for me.

## Markdown Guide
https://www.markdownguide.org/basic-syntax#paragraphs-1

<br> <br> <br> <br> <br> <br> <br> <br>

## Git Commands
- Set Up Git:
  > git config --global user.name "Your Name"<br>
  > git config --global user.email "youremail@domain.com"
  
- Saving Commands
  > git clone ***url*** (makes a local copy of a repository)<br>
  > git add (file names)<br>
  > git commit -m "(committed message)<br>
  > git push -u origin ***master***<br>
  > git remote add origin ***master*** (url)<br>
  > git commit<br>
  > git pull (download the master branch online into your pc)<br>
  > git push origin ***master***
  
- Other Commands
  > git init (initialize local repo)<br>
  > git status<br>
  > git config --list
___
- Adding To A Repository On Git - (MAIN)
  > git add (will show differences in code and possible conflicts)<br>
    >> git add *.java (add a folder without the '/')<br>
      >>> git add . (adds modified files)<br>
      >>> git add filename.filetype<br>
      >>> git add -A (adds all changes, what I usually use)<br>
      
  > git commit -m "comment"<br>
  > git push origin ***branchName***

___
- New Branch - used to isolate new features that are being created
  > git branch (shows total branches, and the one your in)<br>
  > git checkout ***use-case-001*** (switches to different branches/changes the content of the folder according to branch)<br>
  > git branch ***use-case-002*** (creates a new branch)
___
- Add Branch
  > git checkout ***master*** (directly adds feature to master branch)<br>
    >> git checkout ***use-case-002*** (go here if you want to merge this branch with master, master isn't changed)<br>
    >> git merge ***master*** (only used if master branch was changed, will merge into master and show differences in code and possible conflicts)<br>
- *repeat ADDING process, 'git push' shows command below, pushing is done as below*<br>
  > git push --set-upstream origin ***use-case-002*** (connects this branch to the repository, for the FIRST TIME)<br>
    >> git push ***use-case-002*** (continuous pushes afterwards)

___
- Pull New Branch
  > git branch ***branch_name***<br>
  > git checkout ***branch_name***<br>
  > git pull origin ***branch_name***
<p>(might need to add and commit changes)</p>

___
- ABORT MERGE
  > git merge --abort

- DELETE BRANCH
  > git branch -d branch_name

- PULL SPECIFIC branch
  > git fetch origin branch_name:branch_name

- GET CHANGES FROM MASTER INTO BRANCH
  > git checkout branch_name
  > it merge master

- DISCARD CHANGES IN BRANCH
  > git checkout -- <file>...

- File Management
  - .gitignore (File)<br>
    >> __pycache__/ (Ignore folder)<br>
    >> macrolist/*.txt (Ignore file)<br>
  - .gitkeep (File that keeps folders)
  
- Windows Git Shortcut<br>
[![Window Git Shortcut](https://img.youtube.com/vi/kIgZEdyn1dA/0.jpg)](https://www.youtube.com/watch?v=kIgZEdyn1dA)

<br> <br> <br> <br> <br> <br> <br> <br>

## VM Window Auto Resize Linux
  ![Alt text](guestadditions.png)
- Go to disk and run:
  > sudo ./VBoxLinuxAdditions.run<br>
  > sudo adduser 'user' vboxsf

<br> <br> <br> <br> <br> <br> <br> <br>

  ## Linux Commands
  https://lzone.de/cheat-sheet/DKMS

<br> <br> <br> <br> <br> <br> <br> <br>

  ## General Application/Link Stuff
- Linux
> gThumb - Image Viewer<br>
> Drawing - Image Editor<br>
> Timeshift - OS Backup<br>
> htop - Process Viewer<br>
> VLC Player - Video Player<br>
> Firefox - Web Browser <br>
> File manager<br>
> Vim - Text Editor<br>
> Git - Github

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

- Personal
> Anime Image Search https://findit.moe/ <br>
> Temporary Video Sharing https://streamable.com/ <br>
> Osu replays https://ordr.issou.best/ <br>
> https://github.com/Tsuk1ko/nhentai-helper <br>
> Discord History https://github.com/Tyrrrz/DiscordChatExporter/releases https://www.swipetips.com/how-to-download-your-chat-history-from-discord/ <br>
> https://animekaizoku.com/ <br>
> https://www.animeout.xyz/ <br>
> https://anidl.org/ 

<br> <br> <br> <br> <br> <br> <br> <br>

## Youtube-dl
- https://youtube-dl.org/ Old/Original
- https://github.com/yt-dlp/yt-dlp New/Update

> .\youtube-dl.exe --help<br>
> youtube-dl -F "link" //displays video options to dowload<br>
> youtube-dl -f "number" "link" //"number" - to select video quality<br>
> youtube-dl -f bestaudio "link"<br>
> youtube-dl -f bestvideo "link"

- FILE TRIM:
> ffmpeg -i output1.mp3 -ss 00:00:30 -to 00:00:40 -c copy output.mp3

- FILE CONVERSION:
> ffmpeg.exe

- BATCH CONVERT
> for %a in ("*.webp") do ffmpeg -i "%a" "%~na.png"<br>
> for %a in ("%CD%\*.webp") do ffmpeg -i "%a" "%CD%\%~na.png"<br>
> for %a in ("Convert\*.webm") do ffmpeg -i "%a" "Converted\%~na.mp3"<br>
> for %a in ("Convert\*.webp") do ffmpeg -i "%a" "Converted\%~na.png"

- COMBINE
> ffmpeg -i "video.mp4" -i "audio.mp3" -map 0:v -map 1:a -c:v copy -c:a copy output.mp4 -y

- BATCH COMBINE
> for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.mp3" -map 0:v -map 1:a -c:v copy -c:a copy "Combined\%~na.mp4" -y

- SUBTITLE COMBINE (NOT WORKING CORRECTLY)
> ffmpeg -i "input.mp4" -i "subtitles.srt" -c:s mov_text -c:v copy -c:a copy output.mp4

- BATCH SUBTITLE COMBINE (NOT WORKING CORRECTLY)
> for %a in ("Combine\*.mp4") do ffmpeg -i "Combine\%~na.mp4" -i "Combine\%~na.srt" -c:s mov_text -c:v copy -c:a copy "Combined\%~na.mp4"

So to add auto-numbering, use -A

- DOWNLOAD FROM TXT
> youtube-dl -f best -o "%(autonumber)0Nd-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 63 --add-header ""

Use output template with %(autonumber)0Nd, where N in the number of digits instead.

>youtube-dl -f best -o "%(autonumber)03d-%(title)s.%(ext)s" -a GFLSongs.txt --autonumber-start 66 --add-header "


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

