# Record Screencast on Linux(Ubuntu)
How Record a Screencast on Linux using SimpleScreenRecorder, MPlayer, Audacity, ffmpeg and youtube

1. Install [SimpleScreenRecorder](https://tecadmin.net/install-simple-screen-recorder-on-ubuntu-linuxmint/).
2. Install [MPlayer](https://itsfoss.com/mplayer/).
3. Configure MPlayer to run on top always, follow the following: [MPlayer configuration](https://ubuntuforums.org/archive/index.php/t-77329.html).
4. Run MPlayer using mplayer 
```
tv:// -tv driver=v4l2:width=400:height=300 -vo xv -geometry 100%:100% -noborder
```
5. Start and record your screencast using SimpleScreenRecorder.
6. Remove white noise with [Audacity](https://www.maketecheasier.com/remove-white-noise-audio-audacity/) .
7. Replace audio in screencast using. [ffmpeg](https://superuser.com/questions/1116326/replace-audio-sync-save-all-to-a-new-video-file-vlc). 
```
./ffmpeg -i "video1.mp4 " -i "audio_replace.m4a" -vcodec copy -acodec copy -map 0:0 -map 1:0 output.mp4
```

8. Upload your video to https://www.youtube.com/.
