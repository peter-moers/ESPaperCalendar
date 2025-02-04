# ESPaperCalendar
 iCal driven ESP32 + ePaper calendar
 Pictures and more instructions in Dutch can be found here: https://papamaakthetwel.be/nerdzone/kalender-met-e-paper-en-esp32/

# Used hardware
- ESP32 compatible
    - Wemos S2 mini
    - ESP32 Devkit v1
- ePaper / e-ink screen
    - Waveshare 7.5 inch 3 color e-Paper with universal hat. [More info here](https://www.waveshare.com/e-paper-driver-hat.htm).
    - Waveshare 4.2 inch 3 color e-Paper with integrated hat. [More info here](https://www.waveshare.com/4.2inch-e-paper-module-b.htm).
# Configuration
## Software configuration
- Copy Example.Credentials.h to Credentials.h
- Open the Credentials.h file and fill in your wifi and calendar information.
- Verify the correct pin configuration in the ino file.

## Hardware Configuration

### Screen size and capabilities
Choose between 7.5" and 4.2" e-paper screens 
Also choose between Black&White (BW) or 3-Colors (3C) screens

### Pin layout
#### Pin layout for Wemos S2 mini
I used a Wemos/Lolin S2 mini with the pin configuration as shown below. If you make the connections as shown below the e-paper should work.

|Color|HAT|S2|
|-|-|-|
|Gray|VCC|3V3|
|Brown|GND|GND|
|Blue|DIN|11|
|Yellow|CLK|7|
|Orange|CS|4|
|Green|DC|17|
|White|RST|16|
|Purple|BUSY|4|

#### Pin layout for ESP32 Devkit v1
If you make the connections as shown below the e-paper should work.

|Color|HAT|S2|
|-|-|-|
|RED|VCC|3V3|
|Black|GND|GND|
|Blue|DIN|D23|
|Yellow|CLK|D18|
|Orange|CS|D5|
|Green|DC|TX2|
|White|RST|RX2|
|Purple|BUSY|D4|


# Todo
- UTF-8 Support
- Recurring events are not implemented yet
