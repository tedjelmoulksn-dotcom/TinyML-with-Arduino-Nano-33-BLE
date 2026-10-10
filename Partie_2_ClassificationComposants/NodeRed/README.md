# Node-RED Serial Receiver

The exported [flows.json](flow.json/flows.json) configures serial reception from the camera experiment at **115200 baud**.

## Setup

1. Install `node-red-node-serialport` in your Node-RED environment.
2. Import `flow.json/flows.json`.
3. Edit the serial port to match your device; the export uses `COM4`.
4. Connect the receiver to a debug node to inspect incoming messages.

The receiver references a missing downstream node. Add parsing and counter/dashboard nodes after establishing the firmware's message format. Those nodes are described in the original documentation but are not included in this export.
