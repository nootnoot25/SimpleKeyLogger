# Keylogger
based on the tutorial here https://thepythoncode.com/article/write-a-keylogger-python

## Overview
This project implements a keylogger that records all keystrokes on the keyboard and saves them to a log file. The keylogger is designed to run in the background and periodically report the captured keystrokes.

## Features
- Captures all keystrokes, including special keys like space, enter, and decimal.
- Records keystrokes in a log file with a timestamp.
- Can be configured to report keylogs via different methods (currently supports file).

## Requirements
- Python 3.x
- `keyboard` module
- `datetime` module
- `threading` module

## Installation
1. Ensure you have Python 3.x installed on your system.
2. Install the `keyboard` module using pip:
    ```sh
    pip install keyboard
    ```
3. Clone this repository or download the `keylogger.py` file to your local machine.

## Usage
1. Open a terminal or command prompt.
2. Navigate to the directory where `keylogger.py` is located.
3. Run the keylogger:
    ```sh
    python keylogger.py
    ```
4. The keylogger will start capturing keystrokes and reporting them to a log file every 60 seconds (default interval).

## Code Explanation
### Keylogger Class
- `__init__(self, interval, report_method="file")`: Initializes the keylogger with the specified interval and report method.
- `callback(self, event)`: Captures keyboard events and appends them to the log.
- `update_filename(self)`: Updates the filename for the log file based on the current timestamp.
- `report_to_file(self)`: Writes the captured keystrokes to a log file.
- `report(self)`: Called every `interval` seconds to report the captured keystrokes.
- `start(self)`: Starts the keylogger and begins capturing keystrokes.

## Example
To start the keylogger and capture keystrokes, run:
```sh
python keylogger.py
