# LeapNotes

> [!NOTE]
> I don't plan on updating this for the forseeable future since I wrote this before I was aware of the [LFHacks](https://github.com/lfhacks/) project, but if there *are* any updates they'll be over on [Codeberg](https://codeberg.org/applecuckoo/LeapNotes), not here on GitHub. Thanks!

These are some notes on my experience from ripping from silly LeapFrog products.

## Hacking the thing

So, you may wonder *how* exactly we get any sort of asset from the LeapPad. Well, first we use something called [LeapPad Manager](https://web.archive.org/web/20210507031610/https://spiffyhacks.com/uploads/leappad-manager.zip) to actually connect to the LeapPad and turn on 'developer mode' as per [The Cutting Room Floor](https://tcrf.net/LeapPad_Explorer#Developer_Mode). It seems that you can also set up developer mode on a Linux host as per [Clayton Carter](https://gist.github.com/claytonrcarter/847fe44f5a5066ce6a1e33524740b037) but I haven't used that method to set the LeapPad into developer mode, only to setup the FTP interface.

## Getting the files

At that point I used the details from the aforementioned guide from Clayton Carter, but instead of connecting via the command line, you can connect via your file manager. There should be an option like 'Connect to Server', but you may need to look around. In GNOME Files, you'd go to 'Other Locations' and type `ftp://192.168.0.111` at the bottom. The LeapPad is always at this IP address. However, it will only expect an IP address from 192.168.0.xxx, so we have to set the IP to `192.168.0.1` for this to work. The username is `root` and there isn't a password. Most of the files will be stored under the `LF` folder, but some files may be stored in other places, i.e. `/var`.

## Ripping sounds from games

Sounds will be stored in one of three formats, or even redundantly duplicated in one of them. They'll either be an MP3 file, an Ogg Vorbis file, or a WAV file with IMA ADPCM data.

