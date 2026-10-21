![Jasheroke for Windows](assets/jasheroke-windows-banner.png)

# Jasheroke for Windows

**Version 1.3.0** | StackSync Solutions

English | [Tagalog](README.tl.md)

Jasheroke brings a karaoke stage to your Windows PC, with synchronized lyrics, MIDI playback, singer profiles and song reservations from Android phones. Play from your local library, adjust the music to your voice and manage the singing queue from one place.

## Download

Download **Jasheroke.exe** from this repository's **Releases** section. For phone reservations, install **Jasheroke.apk** on an Android device.

| Application | Current version | Purpose |
| --- | --- | --- |
| Jasheroke for Windows | 1.3.0 | PC karaoke player and reservation host |
| Jasheroke for Android | 2.0.0 | Phone reservations and Android karaoke player |

## Requirements

- Windows PC with an x64 processor and the **.NET 10 Windows Desktop Runtime (x64)** installed.
- Speakers or headphones; a microphone for microphone features.
- A compatible song library and an `.sf2` SoundFont for local MIDI playback.
- A shared local network or Wi-Fi connection for phone reservations.
- Internet access for online song and lyric searches. Local playback uses the files already on your computer.

If Windows asks for .NET when opening the app, install the **Windows Desktop Runtime**, then open Jasheroke again.

## Features

- Synchronized lyric highlighting and optional video backgrounds.
- Reserved song numbers remain visible at the top of the stage.
- Scores appear at the end of the song.
- Key and tempo adjustments, microphone controls, echo and equalizer settings.
- Guest and named singer profiles, favorites and completed-song history.
- Remembered song key and tempo for each singer.
- Saved queue recovery after an interrupted session.
- Dark Videoke, Light Mode, Neon KTV and Retro Arcade themes.
- Online MIDI and synchronized lyric searches, subject to provider availability.
- **Smart Chords (BETA):** chord labels arranged to reduce clutter above the lyrics.
- **Vocal Guide (BETA):** note guidance aligned to lyric syllables. Accuracy depends on the song's MIDI melody and lyric timing.

## Get started

1. Save `Jasheroke.exe` in a folder you can write to, such as a dedicated Jasheroke folder.
2. Open the application and go to **Settings**.
3. Configure your song library and SoundFont locations. Add a background video folder if desired.
4. Open the songbook, select a song and play it or add it to the reservation queue.
5. Select a singer profile to keep that singer's favorites and song preferences.

### Set up the song library

Keep each library's matching files together:

| Library format | Files needed |
| --- | --- |
| Indexed library | `jashidx` and `jashblob` |
| Paired library | `lyrics.jash` and `mid.jash` |

Select the appropriate library location in Settings. A SoundFont supplies the instrument sounds for MIDI playback. Set **SoundFont Instrument Bank (sf/)** to the folder containing your `.sf2` files, then choose the desired SoundFont in the audio settings.

Song libraries, external SoundFonts and background videos are supplied separately. You can keep them in your own folders and configure their locations in the app.

## Reserve songs from a phone

1. Connect the PC and Android phone to the same local network or Wi-Fi.
2. On the PC, select **Phones → Start room**.
3. Note the displayed host address and six-digit room PIN.
4. On the Android app, open **Phone** and enter the address, your singer name and the PIN.
5. Search the host's songbook and select **Reserve**. Open **Live queue** to see the current song and waiting reservations.

The phone uses the host's library, so it needs no local song files. Guests can cancel their own waiting reservations. Playback, skipping and queue management remain with the host.

Allow Jasheroke through Windows Firewall on your private network when prompted. Rooms use port **17890**; an address may look like `192.168.1.20:17890`. Keep the host app running. If the room restarts, join again with the displayed details.

An Android device can also host a room through **Room → Open reservation room** in Jasheroke for Android.

## Continue a saved session

When a saved queue is recovered, review it and choose to resume. An interrupted song returns to the front of the queue and starts from the beginning. Playback does not start automatically.

## Update the app

Close Jasheroke before replacing `Jasheroke.exe` with the new release. Keep your media folders, settings and saved singer/session data.

Settings are normally saved beside the EXE. If that folder is not writable, they are saved in `%APPDATA%/Jasheroke`. Singer and recovery data are stored in `Data/User` under the settings location.

## Troubleshooting

| Problem | What to check |
| --- | --- |
| App requests .NET | Install the x64 .NET 10 Windows Desktop Runtime. |
| Songbook is empty | Check the library location and keep its matching files together. |
| MIDI playback is silent | Check the SoundFont, audio output and volume. |
| Phone cannot connect | Check the host address, PIN, firewall and Wi-Fi device isolation. Join again after a room restart. |
| Chords or guide timing seem inaccurate | These features are in beta; their results depend on the MIDI and lyric data. |

## Report an issue

Use this repository's **Issues** section. Include the app version, Windows version, steps to reproduce the problem and any visible error message. For reservation problems, include the host platform and companion app version.

Developed by **StackSync Solutions**.
