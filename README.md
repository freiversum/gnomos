<p align="center">
  <img src="data/icons/hicolor/128x128/apps/de.linuxundich.Gnomos.png" alt="Gnomos icon" width="128" height="128">
</p>

<h1 align="center">Gnomos</h1>

<p align="center"><strong>A Sonos controller for Linux, at home on the GNOME desktop.</strong></p>

<p align="center">
  Play music, group rooms and set the volume in every room from a native GTK&nbsp;4 and libadwaita app.
  Gnomos talks to your speakers directly over your home network. No Sonos account and no cloud service needed.
</p>

<p align="center">
  <a href="https://github.com/linuxundich/gnomos/releases/latest"><strong>Download Flatpak</strong></a>
  &nbsp;·&nbsp; Flathub: planned &nbsp;·&nbsp;
  <a href="https://linuxundich.de/en/projects/gnomos/">Project page</a>
  &nbsp;·&nbsp;
  <a href="CHANGELOG.md">Changelog</a>
</p>

<p align="center">
  <img src="screenshots/gnomos-now-playing.webp" alt="Gnomos Now Playing view with a large cover, synced lyrics and playback controls" width="100%">
</p>

<p align="center">
  <a href="screenshots/gnomos-demo.mp4"><img src="screenshots/gnomos-demo-poster.webp" alt="Play the Gnomos demo video: synced lyrics, room groups, Quick Settings and the mini player" width="80%"></a>
  <br>
  <sub>Demo video (1:34). Music: <a href="https://www.joshwoodward.com/album/Breadcrumbs">“Border Blaster” by Josh Woodward</a>, CC BY 4.0.</sub>
</p>

## What it does

<table>
<tr>
<td width="33%" valign="top">

### Now Playing, with lyrics

Click the player bar and the current track fills the window: a large cover on a background in its own colors, what plays next, and time-synced lyrics. Click a line to jump to that part of the song. Prefer vinyl? The cover can spin as a record.

</td>
<td width="33%" valign="top">

### Every room in one place

The room picker shows what plays where. Drag a room onto another to group them, set each room's volume, or start and pause any room with one click.

</td>
<td width="33%" valign="top">

### Your whole music collection

Browse the music share on your network, your Sonos favorites and playlists, internet radio and the services you linked to Sonos, such as Spotify. Even large libraries open instantly as a cover grid.

</td>
</tr>
</table>

<p align="center">
  <img src="screenshots/gnomos-dark-record-player.webp" alt="Dark mode with the record player look and synced lyrics" width="32%">
  <img src="screenshots/gnomos-rooms.webp" alt="The room picker with two rooms: one plays, one is paused" width="32%">
  <img src="screenshots/gnomos-albums.webp" alt="1061 albums of the music share as a cover grid" width="32%">
</p>

<table>
<tr>
<td width="55%">
<img src="screenshots/gnomos-quick-settings.webp" alt="GNOME Quick Settings with a volume slider for every room next to the Gnomos window" width="100%">
</td>
<td valign="middle">

### Part of your GNOME desktop

Media keys, the lock screen and the media player in Quick Settings work right away.

### Room volumes in Quick Settings

An optional Shell extension adds the volume of the selected room to the Quick Settings, with an expandable “Other Rooms” list that has a slider for every speaker in the house.

</td>
</tr>
</table>

<table>
<tr>
<td valign="middle">

### Mini player, dark mode, notifications

A poster-style mini player, dark mode and desktop notifications are built in.

### Shortcuts and sleep timer

Keyboard shortcuts for playback, volume, search and the current track, and a sleep timer ring around the play button.

</td>
<td width="270" align="center">
<img src="screenshots/gnomos-mini-player.webp" alt="The poster-style mini player" width="250">
</td>
</tr>
</table>

<table>
<tr>
<td width="55%">
<img src="screenshots/gnomos-queue.webp" alt="The queue with the sidebar, the playing track marked and the player bar" width="100%">
</td>
<td valign="middle">

### Queue and playlists

Reorder or remove tracks in the queue, or save it as a Sonos playlist.

### Favorites, alarms and history

Favorites with search, alarms you can create, edit and duplicate, and a play history that Gnomos keeps locally because Sonos doesn't.

### Internet radio

Search internet radio stations by name or country and add them as your own stations.

</td>
</tr>
</table>

<table>
<tr>
<td valign="middle">

### Speaker settings

Bass, treble, loudness, night mode, sub gain and fixed line-out volume for every speaker, plus a device info dialog with model, IP address and software version.

### Your look

Colors from the cover, blurred background, record player and tile size are in the preferences.

### A second life for older speakers

Gnomos works with any Sonos system on your network and keeps first-generation players going, the ZP80, ZP90, ZP100, ZP120 and CR100, which the current Sonos apps no longer support.

</td>
<td width="55%">
<img src="screenshots/gnomos-preferences.webp" alt="The preferences dialog on the Appearance page: color scheme, cover colors, blurred background, record player and tile size" width="100%">
</td>
</tr>
</table>

## At a glance

| | |
|---|---|
| **Runs on** | Linux with GNOME, as a Flatpak (GNOME 51 runtime) or a `.deb` for Debian testing (forky) or newer; needs libadwaita 1.9 |
| **Works with** | any Sonos system on your network, including the first-generation ZP80, ZP90, ZP100, ZP120 and CR100 |
| **Account** | none: no Sonos account and no cloud service needed |
| **Online lookups** | only lyrics from LRCLIB and artist photos from Deezer, both off until you turn them on |
| **Languages** | English and German included |
| **Licence** | GPL-3.0-or-later |

## Install

> [!NOTE]
> A release on Flathub is planned. For now, install the Flatpak bundle from the Releases page.

<table>
<tr>
<th width="50%">Flatpak bundle</th>
<th width="50%">Debian package</th>
</tr>
<tr>
<td valign="top">

1. Download `gnomos-<version>-x86_64.flatpak` from the [latest release](https://github.com/linuxundich/gnomos/releases/latest).
2. Install it:

```sh
flatpak install --user gnomos-*.flatpak
```

Flatpak fetches the GNOME 51 runtime from Flathub if it is missing. Bundles don't update themselves, so check the Releases page for new versions.

</td>
<td valign="top">

Gnomos needs libadwaita 1.9 or newer, so the `.deb` targets Debian testing (forky) or newer; Debian 13 (trixie) ships libadwaita 1.7 and is too old. Build it with Podman:

```sh
build-aux/deb/build.sh
sudo apt install ./build-aux/deb/out/gnomos_*.deb ./build-aux/deb/out/gnome-shell-extension-gnomos-volume_*.deb
```

</td>
</tr>
</table>

Optional: the [GNOME Shell extension](gnome-shell-extension/gnomos-volume@linuxundich.de/README.md) for room volumes in Quick Settings. To build Gnomos yourself, see [docs/BUILDING.md](docs/BUILDING.md).

## How it works

1. Gnomos finds your Sonos speakers on the local network by itself.
2. It plays everything Sonos can reach: your music share, radio stations and linked services.
3. Everything else stays at home. Lyrics from LRCLIB and artist photos from Deezer are the only online lookups, and both stay off until you turn them on.

Under the hood Gnomos uses [libnoson](https://github.com/janbar/noson), the library behind [noson-app](https://github.com/janbar/noson-app).

## On the blog

Gnomos has its own page on my blog
[Linux und Ich](https://linuxundich.de/en/projects/gnomos/), with more
details on the app and news about upcoming versions. The
[project overview](https://linuxundich.de/en/projects/) lists everything else
I build for the Linux desktop. Questions, ideas or feedback that don't fit
into an issue? [Get in touch](https://linuxundich.de/en/contact/), I read
every message.

## More

- [Project page on linuxundich.de](https://linuxundich.de/en/projects/gnomos/): details, background and news
- [All features](docs/FEATURES.md) (the full list, including everything above) · [Changelog](CHANGELOG.md) · [Architecture notes](ARCHITECTURE.md)
- [Translate Gnomos](docs/TRANSLATING.md) into your language (English and German included)
- Found a bug or tested other Sonos hardware? [Open an issue](https://github.com/linuxundich/gnomos/issues)

## Use of AI

Gnomos is AI-assisted. Most of the code, the icon and the translations were
written with AI assistance, directed by me: I set the requirements, made the
design decisions, reviewed the results and tested the app on my own
first-generation Sonos household. Commits written with AI assistance carry a
`Co-Authored-By` line.

Gnomos is free software under the [GPL-3.0-or-later](LICENSE). It is a personal project, tested on the author's own first-generation Sonos household. Album covers in the screenshots belong to their artists and labels.
