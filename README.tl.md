# Jasheroke para sa Windows

<img width="1672" height="941" alt="WINDOWS" src="https://github.com/user-attachments/assets/aa51e2e5-c803-4d3b-b5f5-be4dcc715acc" />

**Bersyon 1.3.0** | StackSync Solutions

[English](README.md) | Tagalog

Ang Jasheroke ay isang karaoke application para sa Windows PC na may sabay na lyrics at tugtog, MIDI playback, singer profiles at pagpapareserba ng kanta gamit ang Android phone. Gamitin ang iyong lokal na koleksiyon ng kanta, iayon ang key at tempo sa iyong boses, at pamahalaan ang pila ng mga kakanta.

## Pag-download

I-download ang **Jasheroke.exe** mula sa seksiyong **Releases** ng repositoryong ito. Para makapagpareserba gamit ang telepono, i-install ang **Jasheroke.apk** sa Android device.

| Application | Kasalukuyang bersyon | Gamit |
| --- | --- | --- |
| Jasheroke para sa Windows | 1.3.0 | Karaoke player sa PC at host ng mga reserbasyon |
| Jasheroke para sa Android | 2.0.0 | Pagpapareserba gamit ang telepono at karaoke sa Android |

## Mga kailangan

- Windows PC na may x64 processor at naka-install na **.NET 10 Windows Desktop Runtime (x64)**.
- Speaker o headphone; mikropono kung gagamitin ang mga microphone feature.
- Compatible na song library at `.sf2` SoundFont para sa lokal na MIDI playback.
- Iisang lokal na network o Wi-Fi para sa pagpapareserba gamit ang telepono.
- Internet para sa online na paghahanap ng kanta at lyrics. Ginagamit ng lokal na playback ang mga file na nasa iyong computer.

Kung humingi ng .NET ang Windows sa pagbukas ng app, i-install ang **Windows Desktop Runtime** at buksan muli ang Jasheroke.

## Mga tampok

- Lyrics na naka-highlight kasabay ng tugtog at opsiyonal na background video.
- Palaging nakikita sa itaas ng stage ang mga numero ng nakapilang kanta.
- Lumalabas ang score sa pagtatapos ng kanta.
- Key at tempo adjustment, microphone controls, echo at equalizer settings.
- Guest at pinangalanang singer profiles, mga paboritong kanta at kasaysayan ng mga natapos na kanta.
- Naaalalang key at tempo ng bawat kanta para sa bawat singer.
- Pagbabalik ng na-save na pila kapag naputol ang session.
- Mga temang Dark Videoke, Light Mode, Neon KTV at Retro Arcade.
- Online na paghahanap ng MIDI at synchronized lyrics, depende sa availability ng provider.
- **Smart Chords (BETA):** inayos na paglalagay ng chord labels upang hindi magsiksikan sa ibabaw ng lyrics.
- **Vocal Guide (BETA):** gabay sa nota na nakatapat sa mga pantig ng lyrics. Nakadepende ang katumpakan sa MIDI melody at timing ng lyrics.

## Pagsisimula

1. Ilagay ang `Jasheroke.exe` sa folder na maaari mong sulatan, gaya ng sariling folder para sa Jasheroke.
2. Buksan ang application at pumunta sa **Settings**.
3. Itakda ang lokasyon ng song library at SoundFont. Maaari ring magtakda ng folder para sa background videos.
4. Buksan ang songbook, pumili ng kanta at patugtugin ito o idagdag sa pila ng reserbasyon.
5. Pumili ng singer profile upang maitala ang mga paboritong kanta at mga setting ng singer.

### Pag-set up ng song library

Panatilihing magkasama ang magkaparehang file ng bawat library:

| Uri ng library | Mga kailangang file |
| --- | --- |
| Indexed library | `jashidx` at `jashblob` |
| Paired library | `lyrics.jash` at `mid.jash` |

Piliin sa Settings ang tamang lokasyon ng library. Ang SoundFont ang nagbibigay ng tunog ng mga instrumento para sa MIDI playback. Itakda ang **SoundFont Instrument Bank (sf/)** sa folder na may iyong mga `.sf2` file, pagkatapos ay piliin ang nais na SoundFont sa audio settings.

Hiwalay na inihahanda ang song library, external SoundFont at background videos. Maaari silang manatili sa sarili mong mga folder; itakda lamang ang kanilang lokasyon sa app.

## Pagpapareserba gamit ang telepono

1. Ikonekta ang PC at Android phone sa iisang lokal na network o Wi-Fi.
2. Sa PC, piliin ang **Phones → Start room**.
3. Tingnan ang ipinapakitang host address at anim na digit na room PIN.
4. Sa Android app, buksan ang **Phone** at ilagay ang address, pangalan ng singer at PIN.
5. Maghanap sa songbook ng host at piliin ang **Reserve**. Buksan ang **Live queue** upang makita ang kasalukuyang kanta at mga naghihintay na reserbasyon.

Ginagamit ng telepono ang library ng host kaya hindi nito kailangan ng sariling song files. Maaaring kanselahin ng bisita ang sarili niyang naghihintay na reserbasyon. Ang host ang namamahala sa playback, paglaktaw ng kanta at pila.

Payagan ang Jasheroke sa Windows Firewall para sa iyong private network kapag hiniling. Ginagamit ng room ang port **17890**; halimbawa ng address ang `192.168.1.20:17890`. Panatilihing bukas ang host app. Kapag ni-restart ang room, sumali muli gamit ang ipinapakitang detalye.

Maaari ring gawing host ang Android device sa pamamagitan ng **Room → Open reservation room** sa Jasheroke para sa Android.

## Pagpapatuloy ng na-save na session

Kapag naibalik ang na-save na pila, suriin ito at piliing ipagpatuloy. Ang naputol na kanta ay ibabalik sa unahan ng pila at magsisimula sa umpisa. Hindi awtomatikong magsisimula ang playback.

## Pag-update ng app

Isara ang Jasheroke bago palitan ang `Jasheroke.exe` ng bagong release. Panatilihin ang iyong media folders, settings at na-save na singer/session data.

Karaniwang nasa tabi ng EXE ang settings. Kung hindi maaaring sulatan ang folder na iyon, ise-save ang mga ito sa `%APPDATA%/Jasheroke`. Nasa `Data/User` sa loob ng lokasyon ng settings ang singer at recovery data.

## Paglutas ng problema

| Problema | Dapat suriin |
| --- | --- |
| Humihingi ng .NET ang app | I-install ang x64 .NET 10 Windows Desktop Runtime. |
| Walang laman ang songbook | Suriin ang lokasyon ng library at panatilihing magkasama ang mga katapat na file. |
| Walang tunog ang MIDI | Suriin ang SoundFont, audio output at volume. |
| Hindi makakonekta ang telepono | Suriin ang address, PIN, firewall at Wi-Fi device isolation. Sumali muli pagkatapos i-restart ang room. |
| Hindi tugma ang chords o guide timing | Nasa beta ang mga tampok na ito; nakadepende ang resulta sa MIDI at lyric data. |

## Pag-uulat ng problema

Gamitin ang seksiyong **Issues** ng repositoryong ito. Isama ang bersyon ng app at Windows, mga hakbang upang maulit ang problema at anumang mensahe ng error. Para sa problema sa reserbasyon, isama ang platform ng host at bersyon ng companion app.

Binuo ng **StackSync Solutions**.
