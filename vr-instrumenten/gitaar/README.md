# Gitaar VR

Step 2 of the [VR-instrumenten plan](../PLAN.md): a guitar you play with your hands in VR, free play.

**Play:** https://guyonvandenbos.github.io/speeltuin/vr-instrumenten/gitaar/

## On a Meta Quest

1. Open the link in the Quest browser. Tick **I play left-handed** if you do.
2. Tap **Enter VR**. The guitar appears at hip height in front of you, neck toward your fretting hand.
3. Put the controllers down to use your hands.

| Hand | What it does |
| --- | --- |
| Fretting hand (left for right-handers) | Rest any fingertip on a chord name on the neck to hold that chord. Lift it off for open strings. |
| Strumming hand | Strum or pick the strings over the sound hole with your index finger. Strings bend slightly, then sound. |
| Either hand | Pinch and hold the body (not the strings) to move the guitar. |

Chords on the neck, from the headstock down: **G, C, D, Em, Am, F, Dm, E**. Each uses its real fingering in standard tuning, including muted strings.

With controllers: the white ball in front of each controller is your fingertip; the trigger works as pinch; the strumming controller vibrates on each string.

## In a browser (no headset)

Pick a chord with the buttons or keys 1–8 (0 for open strings), and drag down or up across the strings to strum.

## How it works

- Three.js with WebXR hand input; one self-contained HTML file.
- Chord zones are a simplification: real finger positions are too fine for hand tracking to read reliably, so the fretting hand picks a whole chord.
- Sound: Karplus–Strong steel strings in standard tuning (E2 A2 D3 G3 B3 E4), with a body resonance filter and a little reverb. A new pluck stops the previous note on the same string, as on a real guitar.
- Strums roll across the strings in the order your finger meets them.

## Status

Browser preview tested. Not yet tried on a real Quest; guitar placement and chord-zone size will likely need tuning there.
