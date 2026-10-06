# TinyML on Arduino Nano 33 BLE

Embedded machine-learning project exploring how a trained model can run directly on a resource-constrained microcontroller.

## Objective

The project uses the Arduino Nano 33 BLE platform to study the complete TinyML workflow:

1. collect and prepare sensor data;
2. train and evaluate a compact model;
3. convert the model for embedded inference;
4. deploy it to the microcontroller;
5. measure the behaviour of the model on real hardware.

## Why TinyML?

Running inference locally can provide:

- low latency;
- offline operation;
- reduced network traffic;
- improved privacy;
- predictable energy and memory constraints.

## Target platform

- Arduino Nano 33 BLE
- Arm Cortex-M4F microcontroller
- Arduino IDE or Arduino CLI
- TensorFlow Lite for Microcontrollers-compatible workflow

## Typical workflow

```text
Sensor data -> preprocessing -> model training
            -> model conversion -> embedded deployment
            -> on-device inference and evaluation
```

## Repository status

This repository is currently a work in progress. The README documents the intended architecture; source code, datasets, trained models and measured results should be added as they are validated.

## Recommended project structure

```text
data/           # Raw and prepared datasets
training/       # Training and evaluation scripts
models/         # Exported embedded models
arduino/        # Firmware and inference sketches
results/        # Memory, latency and accuracy measurements
```

## Reproducibility checklist

Future experiments should report:

- dataset and class definitions;
- preprocessing and sampling frequency;
- model architecture and training parameters;
- validation accuracy and confusion matrix;
- flash and RAM usage;
- inference latency on the board.

## Author

Tedj El Moulk Sinacer
