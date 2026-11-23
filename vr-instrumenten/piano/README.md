# Piano VR

Step 3 of the [VR-instrumenten plan](../PLAN.md): a three-octave keyboard (C3–C6) you play with all ten fingers in VR, free play.

**Play:** https://guyonvandenbos.github.io/speeltuin/vr-instrumenten/piano/

## On a Meta Quest

1. Open the link in the Quest browser. Tick **Big keys** if real-size keys are too fiddly with hand tracking.
2. Tap **Enter VR**. The keyboard appears at table height in front of you.
3. Put the controllers down to use your hands.

| Action | How |
| --- | --- |
| Play a note | Push a fingertip into a key. All ten fingers play; the key goes down with your finger. |
| Play louder or softer | Strike faster for louder, slower for softer. |
| Glissando | Keep a finger down and slide it across the keys. |
| Sustain | Tap the **Sustain** button on the back rail to toggle it. |
| Move the keyboard | Pinch and hold the back rail or a side cheek, then drag. |

With controllers: the white ball in front of each controller plays like a fingertip and vibrates on each key.

## In a browser (no headset)

Click or drag across the keys, or use your computer keyboard: `Z`–`M` (with `S D G H J` for the black keys) is the low octave, `Q`–`I` (with `2 3 5 6 7`) the middle one. Hold `Space` for sustain.

## How it works

- Three.js with WebXR hand input; one self-contained HTML file.
- A key presses when a fingertip pad goes 3 mm below its top while moving down, and releases when the finger lifts back to the surface. Black keys sit higher and are checked first.
- Velocity comes from how fast the fingertip was moving down; it sets both volume and brightness.
- Sound: [Salamander Grand Piano](https://archive.org/details/SalamanderGrandPianoV3) by Alexander Holm (CC-BY 3.0), loaded from the Tone.js sample host: one sample every three semitones, pitch-shifted in between. A simple synth plays until the samples load, or if they can't.

## Status

Browser preview tested. Not yet tried on a real Quest; key press depth and keyboard height will likely need tuning there.
