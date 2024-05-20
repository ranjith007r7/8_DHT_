# 8_DHT_
Displaying Humidity and Temperature of the room using DHT sensor &amp; LCD

# DHT11 Temperature and Humidity Sensor Display

## Overview

This project utilizes an Arduino along with a DHT11 sensor to measure temperature and humidity. The measurements are displayed on a 16x2 LCD screen. This project is useful for monitoring environmental conditions in various settings.

## Components

- Arduino board (e.g., Uno, Mega)
- DHT11 temperature and humidity sensor
- 16x2 LCD screen with I2C interface
- Breadboard and jumper wires

## Circuit Diagram

1. **DHT11 Sensor**
   - Connect the positive (+) pin of the DHT11 sensor to 5V on the Arduino.
   - Connect the negative (-) pin of the DHT11 sensor to GND on the Arduino.
   - Connect the signal (data) pin of the DHT11 sensor to digital pin 7 on the Arduino.

2. **LCD Screen**
   - Connect the SDA pin of the LCD screen to A4 on the Arduino.
   - Connect the SCL pin of the LCD screen to A5 on the Arduino.
   - Connect the VCC pin of the LCD screen to 5V on the Arduino.
   - Connect the GND pin of the LCD screen to GND on the Arduino.

## Code Explanation

### Libraries

- `LiquidCrystal_I2C.h`: For interfacing with the LCD screen using I2C communication.
- `DHT.h`: For reading temperature and humidity data from the DHT11 sensor.

### Variables and Objects

- `lcd`: Object for controlling the LCD screen.
- `dht`: Object for interacting with the DHT11 sensor.
- `tempMessage`: String variable to store the temperature message.
- `humMessage`: String variable to store the humidity message.

### Setup

In the `setup()` function:
- The LCD screen is initialized with its I2C address and dimensions.
- The DHT11 sensor is initialized.
- Serial communication is initialized at 9600 baud.
- A welcome message is printed to the Serial Monitor.

### Loop

In the `loop()` function:
- Temperature and humidity readings are obtained from the DHT11 sensor.
- If the readings are valid, the temperature and humidity messages are formatted as strings.
- The messages are printed to the Serial Monitor for debugging.
- The LCD screen is cleared, and the messages are displayed on it.
- The loop repeats with a delay of 1 second.

## Usage Instructions

1. Assemble the circuit as per the circuit diagram.
2. Upload the provided code to the Arduino board.
3. Open the Serial Monitor from the Arduino IDE (Tools -> Serial Monitor) to view temperature and humidity readings.
4. Observe the LCD screen to view real-time temperature and humidity measurements.

## Example Output

- The Serial Monitor will display temperature and humidity readings in the format: "Temp: XX.X°C    Hum: XX.X%".
- The LCD screen will show the temperature and humidity measurements on separate lines, updating every second.

This project provides a simple and effective way to monitor temperature and humidity using an Arduino and a DHT11 sensor, with real-time display capabilities on an LCD screen.

---


