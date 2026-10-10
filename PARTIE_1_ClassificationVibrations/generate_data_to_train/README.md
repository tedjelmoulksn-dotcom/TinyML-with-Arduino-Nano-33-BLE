# IMU Data Acquisition

The Arduino sketch captures six channels: accelerometer `aX/aY/aZ` and gyroscope `gX/gY/gZ`. Each triggered motion recording contains **119 samples**.

## Use

1. Install `Arduino_LSM9DS1` and confirm that it matches your board's IMU.
2. Open and upload [generate_data_to_train.ino](generate_data_to_train.ino).
3. Install the logger dependency with `python -m pip install pyserial`.
4. Edit the serial port and output filename in [serial_data_to_csv.py](serial_data_to_csv.py), then run `python serial_data_to_csv.py` from this folder.

Both programs use **9600 baud**. Close other serial monitors before starting the logger.

Collect multiple sessions per gesture and keep class labels consistent with the training notebook and inference outputs. Validate the actual sampling cadence; the source comments' approximate duration is not a measured timing result.

The existing `env.rar` is retained as an original environment archive. The Python script can be inspected and used independently.
