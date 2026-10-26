# Third-party notices

Aura Player is free to use under its own license (`LICENSE`). It includes the third-party components below, each under its own license. The full license texts are in the `licenses` folder next to `AuraPlayer.exe` (and in the `licenses` folder of the source tree).

## Components

| Component | Version | License | License file | Use |
| --- | --- | --- | --- | --- |
| LibVLC (VideoLAN, `VideoLAN.LibVLC.Windows`) | 3.0.24 | LGPL-2.1-or-later | `LGPL-2.1.txt` | Audio and video playback |
| LibVLCSharp, LibVLCSharp.WPF | 3.10.2 | LGPL-2.1-or-later | `LibVLCSharp.txt` | .NET binding for LibVLC |
| TagLib# (`TagLibSharp`) | 2.3.0 | LGPL-2.1 | `TagLibSharp.txt` | Tags and artwork |
| FFmpeg (BtbN LGPL shared build) | n9.0.2-17-g2a571b6068, build `autobuild-2026-09-30-13-08` | LGPL-3.0-or-later | `LGPL-3.0.txt`, `GPL-3.0.txt`, `ffmpeg/LICENSE-FFmpeg.txt` | Media analysis, remux and transcoding for casting |
| WPF-UI | 4.3.0 | MIT | `WPF-UI.txt` | Fluent controls and themes |
| CommunityToolkit.Mvvm | 8.4.2 | MIT | `CommunityToolkit.txt` | MVVM helpers |
| H.NotifyIcon, H.NotifyIcon.Wpf, H.GeneratedIcons.System.Drawing | 2.4.1 | MIT | `H.NotifyIcon.txt` | Tray icon |
| Velopack | 1.2.161 | MIT | `Velopack.txt` | Installer, updates, uninstall hooks |
| Zeroconf | 3.7.16 | MIT | `Zeroconf.txt` | Chromecast discovery (mDNS) |
| System.Reactive | 5.0.0 | MIT | `System.Reactive.txt` | Used by Zeroconf |
| .NET runtime, ASP.NET Core (Kestrel), Microsoft.Extensions | 10.0 | MIT | `dotnet-runtime.txt`, `aspnetcore.txt` | Runtime, local media server for casting, dependency injection, logging |

## LGPL components

LibVLC, LibVLCSharp, TagLib# and FFmpeg are used **unmodified**:

- LibVLC (`libvlc.dll`, `libvlccore.dll`, `plugins`), LibVLCSharp and TagLib# are dynamically linked libraries in the application folder.
- FFmpeg runs as separate programs (`ffmpeg/ffmpeg.exe`, `ffmpeg/ffprobe.exe`) with their own DLLs in the `ffmpeg` folder.

You may replace any of these files with your own build of the same library. The Aura Player license allows this, and reverse engineering as far as needed to debug such changes.

Aura Player ships 317 of the 321 LibVLC 3.0.24 plugins. It leaves out the four that are licensed under the GPL (`dolby_surround_decoder`, `headphone_channel_mixer`, `x26410b`, `lua`) and LibVLC's Lua scripts.

### Source code

| Component | Source |
| --- | --- |
| FFmpeg n9.0.2-17-g2a571b6068 | <https://github.com/FFmpeg/FFmpeg/tree/2a571b6068> (release branch `release/9.0`) |
| FFmpeg build scripts and pinned library versions | <https://github.com/BtbN/FFmpeg-Builds/tree/autobuild-2026-09-30-13-08> (variant `win64-lgpl-shared-9.0`) |
| FFmpeg build used by Aura Player | <https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-30-13-08> |
| LibVLC 3.0.24 | <https://code.videolan.org/videolan/vlc/-/tree/3.0.24> and <https://download.videolan.org/pub/videolan/vlc/3.0.24/> |
| LibVLC Windows package | <https://code.videolan.org/videolan/libvlc-nuget> |
| LibVLCSharp 3.10.2 | <https://code.videolan.org/videolan/LibVLCSharp/-/tree/3.10.2> |
| TagLib# 2.3.0 | <https://github.com/mono/taglib-sharp/tree/TaglibSharp-2.3.0.0> |

If any of these links stop working, ask the author on the issues page of the Aura Player releases repository (<https://github.com/novaua/AuraPlayer/issues>) for a copy of the corresponding source, which will be provided for at least three years after the last release that includes it.

### Libraries inside the FFmpeg build

The FFmpeg DLLs contain these libraries, statically linked by the BtbN build (versions pinned by its scripts at the tag above). License texts are in the `licenses` folder by license name.

| Library | License |
| --- | --- |
| OpenH264 | BSD-2-Clause (`OpenH264.txt`). Used only as a fallback encoder when Windows' Media Foundation H.264 encoder is not available. |
| dav1d, rav1e, librist, OpenJPEG | BSD-2-Clause |
| libaom, SVT-AV1 | BSD-2-Clause / BSD-3-Clause-Clear, with the Alliance for Open Media Patent License 1.0 |
| libvmaf | BSD-2-Clause-Patent |
| libvorbis, libogg, libtheora, libvpx, libwebp, libjxl, Opus, kvazaar, libopenmpt, snappy, uavs3d, OpenAPV | BSD-3-Clause |
| liblcevc-dec, vvenc | BSD-3-Clause-Clear |
| libxml2, HarfBuzz, Fontconfig, libaribcaption, AMF headers, nv-codec-headers, libvpl | MIT |
| libass, LV2 (lilv, serd, sord, sratom, zix) | ISC |
| FreeType | FTL |
| zlib, SDL2 | Zlib |
| XZ Utils (liblzma) | 0BSD |
| zimg | WTFPL |
| Vulkan loader, OpenCL ICD loader, opencore-amr | Apache-2.0 |
| libzmq, SRT | MPL-2.0 |
| FriBidi, libbluray, libplacebo, libssh, libsoxr, TwoLAME, Game Music Emu, Chromaprint, libzvbi, librsvg and its GLib, Cairo and Pango stack, libiconv | LGPL-2.1-or-later |
| LAME, OpenAL Soft | LGPL-2.0-or-later |
| GMP, libaribb24 | LGPL-3.0-or-later |

### Libraries inside LibVLC

The LibVLC plugins contain third-party libraries built by VideoLAN (for example FFmpeg's libavcodec, libass, FreeType, HarfBuzz, libdvbpsi, libebml, libmatroska, libbluray, libvpx, dav1d, Opus, Vorbis, FLAC, mpg123, TagLib, GnuTLS and libxml2). Their versions and licenses are defined by the VLC 3.0.24 contrib sources (`contrib/src` in the VLC source above).
