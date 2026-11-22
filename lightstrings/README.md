# Lightstrings

An air harp made of light. Glowing strings hang across the screen; swipe through them to pluck. Longer strings play lower notes, and you can stretch new strings anywhere.

## Play

**Mouse or touch:** open `index.html` in a browser and drag across the strings.

**Webcam (hand tracking):** the camera only works on `https://` or `localhost`, so serve the folder:

```sh
cd lightstrings
python3 -m http.server 8000
```

Open http://localhost:8000 in Chrome, click **Play with webcam** and allow the camera. Every fingertip plucks. Pinch with both hands and pull apart to stretch a new string.

Hand tracking runs fully in the browser with [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker). The video never leaves your machine; the first load needs internet to download the model.

## Controls

| Input | Action |
| --- | --- |
| Drag / swipe | Pluck strings (faster = louder) |
| Shift + drag, or **Draw string** | Stretch a new string |
| Keys 1–9 | Pluck string 1–9 |
| Scale menu | Pentatonic, major, blues, dorian |
| **Clear** / **Reset** | Remove all strings / restore the default set |

## How it works

- Sound: Karplus–Strong plucked-string synthesis with the Web Audio API, plus a generated reverb. No audio files.
- Pitch follows string length and the chosen scale, across three octaves from A2.
- Everything is one self-contained HTML file; libraries load from jsDelivr only when webcam mode starts.

## Status

Mouse and touch mode tested. Webcam mode not yet tested with a real camera.
