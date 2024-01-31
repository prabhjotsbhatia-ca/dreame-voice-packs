# Modified Voice Pack for Dreame Vacuum Robots

Uses voice from original Dreame vacuum, some of them are modified to reduce gain by 50 dB. For some reason the startup, shutdown and camera warnings do not respect the speaker volume setting. Therefore I edited those files to reduce their volume. 

MD5 sum of the prepackaged `modified_audio_files.tar.gz`:  
`26f413f713000b8a3d4528ab760bacc4`

Works at least with `L10 Pro`, `Z10 Pro`, `W10`, `D9`, `D10s Pro`. 

## Installation

1. In Valetudo go to "Robot Settings" -> "Misc Settings"
1. Enter the following information in the "Voice packs" section:
    - URL: `https://github.com/Findus23/voice_pack_dreame/raw/main/voice_pack.tar.gz`
    - Language Code: `ENUS`
    - Hash: `26f413f713000b8a3d4528ab760bacc4`
    - File size: `1325450` byte
1. Click "Set Voice Pack"

Interestingly on my L10 Pro running `Valetudo 2022.03.0` the .tar.gz doesn't seem to work and the newly created folder `/data/personalized_voice/ENUS` stays empty.
However, the language code is set correctly in Valetudo and manually copying the files into the right directory works:

```
git clone https://github.com/Findus23/voice_pack_dreame
scp voice_pack_dreame/output/* root@<YOUR_ROBOT_ADDRESS>:/data/personalized_voice/ENUS
```

-----
Thanks to https://github.com/ccoors/dreame_voice_packs and https://github.com/Findus23/voice_pack_dreame/ for the inspiration and the list of sounds.
