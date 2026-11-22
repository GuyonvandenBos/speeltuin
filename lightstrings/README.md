# Lightstrings

An air harp made of light. You start with an empty board, stretch glowing strings wherever you like, and swipe through them to pluck. Longer strings play lower notes.

## Play

**Mouse or touch:** open `index.html` in a browser and drag across the strings.

**Webcam (hand tracking):** the camera only works on `https://` or `localhost`, so serve the folder:

```sh
cd lightstrings
python3 -m http.server 8000
```

Open http://localhost:8000 in Chrome, click **Play with webcam** and allow the camera. Or play it online: https://guyonvandenbos.github.io/speeltuin/lightstrings/

Hand tracking runs fully in the browser with [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker). The video never leaves your machine; the first load needs internet to download the model.

## Controls

**Hands (webcam)**

| Gesture | Action |
| --- | --- |
| Swipe your index finger through a string | Pluck it (faster = louder) |
| Pinch a string with one hand and hold | Remove it |
| Pinch with both hands, hold, pull apart, let go | Add a string between your hands |
| Bring both pinches back together, let go | Cancel the new string |

**Mouse, touch and keyboard**

| Input | Action |
| --- | --- |
| Drag on an empty board | Stretch your first string |
| Drag / swipe across a string | Pluck it (faster = louder) |
| Shift + drag, or **Draw string** | Stretch a new string |
| Right-click, or long-press on touch | Remove a string |
| **Undo** or Ctrl+Z | Undo the last add or remove |
| Esc | Cancel the string you're drawing |
| Keys 1–9 | Pluck string 1–9 |
| Scale menu | Pentatonic, major, blues, dorian |
| **Clear** / **Example** | Remove all strings / load a set of example strings |

## How it works

- Sound: Karplus–Strong plucked-string synthesis with the Web Audio API, plus a generated reverb. No audio files.
- Pitch follows string length and the chosen scale, across three octaves from A2.
- Hand points are smoothed with a One Euro filter, and pinches use hysteresis so a relaxed hand doesn't count as a pinch.
- Everything is one self-contained HTML file; libraries load from jsDelivr only when webcam mode starts.

## Status

Mouse and touch mode tested. Webcam mode tested with recorded hand footage as a fake camera; first real-camera feedback is in.
