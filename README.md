# TinyML on Arduino Nano 33 BLE — Project Roadmap

A project outline for deploying compact machine-learning inference on a microcontroller. Two application tracks are described: inertial vibration recognition and camera-based electronic-component recognition.

**Current repository status:** the published material consists of this README and the [project overview](Overview). Training code, datasets, exported models, firmware and performance measurements are not yet included.

## Track 1 — IMU vibration recognition

The proposed pipeline collects inertial measurements, forms fixed-length windows, extracts or normalises features, trains a classifier and exports a TensorFlow Lite model for microcontroller inference.

Important implementation parameters include sampling frequency, window length, overlap, input units and training/inference preprocessing consistency. Train/test partitions should separate acquisition sessions where possible to avoid leakage between neighbouring windows.

## Track 2 — Electronic-component recognition

The overview proposes camera-based classification of components such as LEDs, resistors and capacitors, with Edge Impulse and a Node-RED interface for displaying counts.

A camera is an additional hardware requirement; the board name alone does not establish an integrated imaging pipeline. Image dimensions, colour format, model operators and inference memory requirements must be specified before deployment.

## Embedded engineering targets

| Area | What to establish |
|---|---|
| Model representation | Input/output tensor shapes, supported operators and quantisation parameters |
| RAM budget | Tensor arena, input buffers and runtime peak usage |
| Flash budget | Model size, runtime code and application footprint |
| Timing | Acquisition period, preprocessing cost and measured inference latency |
| Validation | Confusion matrix, held-out acquisitions and robustness to changed conditions |
| Integration | Firmware acquisition/inference interface and host reporting format |

These are planned verification objectives, not published results.

## Next implementation steps

1. Select one application and define the acquisition hardware.
2. Commit a reproducible data schema and capture script.
3. Add a training/export pipeline with fixed evaluation partitions.
4. Publish firmware and a documented memory/timing measurement procedure.
5. Compare host-model and on-device predictions using the same inputs.

## Access

```bash
git clone https://github.com/tedjelmoulksn-dotcom/TinyML-with-Arduino-Nano-33-BLE.git
cd TinyML-with-Arduino-Nano-33-BLE
git switch test
```

The current default branch is `test`. There is no runnable deployment procedure yet.

## Licence

No project-wide licence has been defined.
