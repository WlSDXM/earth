# earth

> A living ocean for [ZigZag FM](https://www.zig-zag.fm/): Kana/ASCII/dither visuals, sonar, fishing, sea life, and more. Userscript for Tampermonkey.

## Demo

<img width="1270" height="614" alt="Screenshot 2026-11-13 021737" src="https://github.com/user-attachments/assets/c7c0ddcf-8a07-4deb-ad51-232c3054c8e9" />
<img width="2557" height="1240" alt="sssalt" src="https://github.com/user-attachments/assets/356e5a57-e7fd-4a13-86e9-2f976bd42d07" />
<img width="1675" height="955" alt="Screenshot 2026-11-13 220858" src="https://github.com/user-attachments/assets/cd826dbe-8360-4e3a-9af5-1ce72e72fe2e" />


##  Features

### Visual Modes
- **Kana (Katakana)**, **ASCII**, and **Dither** rendering
- **CRT mode**, **Glitch mode**, **Matrix rain**, and **Shockwave** effects

### Ocean & Atmosphere
- Wave effects and shoreline rendering
- Fog banks and a full day/night cycle with a moon
- Seagulls circling above your boat

### Gameplay & Interactivity
- **Sonar** — ping your surroundings from your boat
- **Fishing** — cast a line and fill out a full logbook of your catches
- **Sea life** — whales, dolphins, sharks, turtles, octopuses, and the occasional kraken appear on the map; wildlife reacts to your boat
- **Encounters** — whirlpools, icebergs, floating bottles, and treasure can show up as you sail
- **Audio-reactive visuals** — effects respond to whatever's playing

##  Performance & Display Settings

- **Quality option** — dial the effects down if things get heavy on your machine
- **Cell size slider** — adjust the rendering cell size to taste
- **Native source map** — option to use the native source map alongside the other effects

##  How it works

Instead of heavy CPU processing, earth intercepts the WebGL canvas that ZigZag FM uses to draw the map. It captures the map frames and passes them through a custom GPU shader pipeline.

This shader shrinks the map into a grid, averages the colors, and renders ASCII, Dither, or Kana characters using a pre-rendered font atlas. Because the effects are calculated on your graphics card, the script can layer complex ocean waves, audio-reactive pulses, and sonar sweeps on top of the map without slowing down your browser. Audio data is captured securely via an injected script inside the YouTube player.

##  Compatibility

- Tested on **Firefox** and **Brave**
- Works on **Windows** and **macOS**
- Requires a userscript manager — [Tampermonkey](https://www.tampermonkey.net/)

##  Install

1. Install [Tampermonkey](https://www.tampermonkey.net/) for your browser.
2. Install the script from this repo: **[[(https://github.com/WlSDXM/earth/releases/tag/v2.8.9)]**
3. Open [ZigZag FM](https://www.zig-zag.fm/) and set sail.

##  License

MIT. See [LICENSE](LICENSE) for details.
