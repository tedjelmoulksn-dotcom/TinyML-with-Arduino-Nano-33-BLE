# Electronic-Component Classification

Camera-based embedded classification using an Arduino Nano 33 BLE, an OV7670 camera and an exported Edge Impulse model.

## Repository guide

- [ArduinoCamera](ArduinoCamera/): camera/inference sketch.
- [Edge Impulse export](ei-electronics-arduino-1.0.4.zip): Arduino-library archive containing the model deployment package.
- [NodeRed](NodeRed/): serial-input flow and host setup guide.
- [Documentation](doc/documentation): original system description and proposed counting dashboard.

## Run the available code

Install the supplied Edge Impulse Arduino library and `Arduino_OV767X`, then open `nano_ble33_sense_camera.ino`. Confirm the target board, camera connections and model input settings against the exported library and sketch.

The firmware initializes serial communication at **115200 baud** and invokes `run_classifier` on captured image data.

Import [flows.json](NodeRed/flow.json/flows.json) into Node-RED after installing the serial-port node dependency. Select the actual device port; the saved configuration uses `COM4` at 115200 baud.

## Host integration status

The exported flow contains a serial receiver and port configuration. Its output references a node that is not included in the export.

The parsing function, component counters and dashboard described in the original documentation are not present in this flow. They remain integration work; the export does not yet reproduce a complete counting interface.

Check the firmware's actual output format before implementing the documented `CLASS:` message protocol. Dataset provenance, model performance and assembled-system operation require separate validation.
