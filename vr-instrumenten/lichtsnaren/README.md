# Lichtsnaren VR

Step 1 of the [VR-instrumenten plan](../PLAN.md): Lightstrings in VR. Stretch strings of light in the air around you and pluck them with your fingers, with real depth from the headset's hand tracking.

**Play:** https://guyonvandenbos.github.io/speeltuin/vr-instrumenten/lichtsnaren/

## On a Meta Quest

1. Open the link above in the Quest browser.
2. Tap **Enter VR** and allow hand tracking if asked. Put the controllers down to use your hands.
3. Optional: tick **Start with example strings** first for a harp to play right away.

| Gesture | Action |
| --- | --- |
| Pinch with both hands, hold, pull apart, let go | Stretch a new string between your hands |
| Bring both pinches back together, let go | Cancel the new string |
| Push your index finger into a string | It bends with your finger, then sounds when pushed about 3.5 cm |
| Ease your finger back before it sounds | Let the string go quietly |
| Pinch a string with one hand and hold | Remove it |

With controllers: the small white ball in front of each controller is your fingertip, and the trigger works as pinch. Each pluck gives a short vibration.

## In a browser (no headset)

The mouse is a fingertip on a flat sheet in front of you: drag to stretch a string, drag through a string to pluck it, right-click to remove, Ctrl+Z to undo. There's no depth here, so it's only a preview.

## How it works

- Three.js with WebXR hand input; one self-contained HTML file.
- Each string is a tube whose shape is recomputed when it bends or vibrates.
- Sound: Karplus–Strong plucked strings, placed in 3D with an HRTF panner so each note comes from its string.
- Pitch follows string length (1.2 m lowest, 15 cm highest) in a minor pentatonic scale.

## Status

Browser preview tested. Not yet tried on a real Quest.
