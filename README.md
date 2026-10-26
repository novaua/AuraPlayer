# Aura Player

Your media, without the noise.

Aura Player is a free Windows player for your local music and videos. It plays a broad range of audio and video formats and casts them to Chromecast, Google TV and DLNA devices such as Xbox and smart TVs, converting files on the fly when a device can't play them directly.

This repository hosts the releases. The source code is not published here.

## Download

- **Installer:** [AuraPlayer-win-Setup.exe](https://github.com/novaua/AuraPlayer/releases/latest/download/AuraPlayer-win-Setup.exe). It installs for your user account only, so no administrator rights are needed, and the app updates itself.
- **Portable:** [AuraPlayer-win-Portable.zip](https://github.com/novaua/AuraPlayer/releases/latest/download/AuraPlayer-win-Portable.zip). Unzip it anywhere and run `AuraPlayer.exe`.

All versions are on the [releases page](https://github.com/novaua/AuraPlayer/releases).

**Requirements:** Windows 10 22H2 or Windows 11, 64-bit.

**Windows SmartScreen:** the installer is not code-signed yet, so Windows may show "Windows protected your PC". Choose **More info**, then **Run anyway**.

## Features

- Audio: MP3, FLAC, WAV, AAC/M4A, Ogg. Video: MP4, MKV, AVI, MOV, WebM, with subtitles and audio-track choice.
- Library with search, queue and playlists, drag and drop, mini player, tray, Windows media keys.
- Casting to Chromecast and Google TV, and to DLNA renderers such as Xbox and smart TVs.
- Opens media files from File Explorer, and you can set it as the default app.
- Updates in the background and asks before restarting. Automatic checks can be turned off in Settings › About.

## Casting and Windows Firewall

Casting devices fetch media from your PC over the local network. If Windows Firewall blocks them, Aura Player explains why before a cast and can add the rule it needs (Windows asks for permission). On a home network, marking the network as Private in Windows settings also works.

## License

Aura Player is free to use; see [LICENSE](LICENSE).

It is built on open-source components, including LibVLC and FFmpeg, each under its own license. They are listed in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md), with links to their source code, and their license texts are in [licenses](licenses). The same files come with the app (Settings › About).

## Feedback

Questions, problems and ideas are welcome on the [issues page](https://github.com/novaua/AuraPlayer/issues).
