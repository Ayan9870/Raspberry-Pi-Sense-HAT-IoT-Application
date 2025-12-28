# Raspberry Pi Sense HAT IoT Application

---

## Project Overview

A comprehensive IoT application built on Raspberry Pi with Sense HAT integration, featuring real-time environmental monitoring, animated emoji displays, and interactive device orientation tracking. The system continuously monitors temperature, humidity, pressure, and orientation with user-defined thresholds, storing readings in a local database. Built with object-oriented Python, the application provides color-coded LED feedback, joystick controls, and data visualization capabilities.

---

## Access to Code 🔒

The source code for this project is **private** and available upon request.

If you're an **employer** or **recruiter** and would like to review the code, please **request access via email** at **ayanhashmi205@yahoo.com**.

---

## Installation 📦

#### Prerequisites
- Raspberry Pi 4 or 3
- Sense HAT module
- Python 3.5+ and pip
- SQLite (built-in)

#### Setup

```bash
# Clone repository
git clone https://github.com/ayan9870/raspberry-pi-sensehat-iot.git
cd raspberry-pi-sensehat-iot

# Install dependencies
pip install -r requirements.txt
pip install sense-hat matplotlib seaborn pandas numpy

# Run applications
python ModuleA/SensorMonitor.py
python ModuleB/analytics.py
python ModuleC/moodAnimator.py
python ModuleD/calculator.py
```

---

## Features 📋

### Module A: Environmental Monitoring System
* **Real-time Sensor Polling** - Temperature, humidity, pressure every 10 seconds
* **Orientation Tracking** - Pitch, roll, yaw with alignment detection
* **Configuration Management** - JSON-based threshold definitions
* **Temperature Calibration** - Automatic offset correction for internal heat
* **Database Logging** - SQLite storage with timestamped readings
* **LED Display** - Color-coded status indicators rotating every 5 seconds
* **Joystick Control** - Pause/resume functionality

### Module B: Data Visualization & Analytics
* **Dual Libraries** - matplotlib and seaborn for comprehensive analysis
* **Multiple Chart Types** - Line plots, scatter plots, histograms, bar charts
* **Temperature Trends** - Time-series analysis of environmental readings
* **Orientation Patterns** - Distribution analysis of device positioning
* **Statistical Insights** - Mean, median, standard deviation calculations
* **PNG Export** - High-resolution image generation

### Module C: Interactive Mood Display
* **Animated Emoji Faces** - Six emotions with 3+ frame animations
* **Multi-color Design** - Minimum 3 colors per frame
* **Joystick Navigation** - Left/right to switch moods, middle to pause
* **Idle Timeout** - Sleep mode after 20 seconds of inactivity
* **Orientation-Based Moods** - Tilt detection triggers emotion changes
* **Rapid Flip Detection** - Special reaction for quick movement (>60° in 0.5s)

### Module D: Interactive Number Calculator
* **LED Display** - Real-time number visualization on 8x8 matrix
* **Joystick Operations** - Up/down increment/decrement, left/right square/root
* **Default Value** - Starts at x = 4 with middle press reset
* **Immediate Feedback** - Instant display updates on input

---

## Technology Stack 🔧

### Hardware
* **Raspberry Pi 4** - Primary computing platform
* **Sense HAT** - Environmental sensors and LED matrix
* **GPIO Interface** - Hardware control

### Software
* **Python 3.8+** - Core programming language
* **sense-hat Library** - Sensor and LED control
* **SQLite** - Lightweight embedded database
* **JSON** - Configuration format

### Data Visualization
* **matplotlib** - Static plotting and chart generation
* **seaborn** - Statistical data visualization
* **pandas** - Data manipulation
* **numpy** - Numerical computing

---

## Configuration 📝

### enviro_config.json Format
```json
{
  "temperature": {
    "min": 18,
    "max": 26,
    "unit": "celsius"
  },
  "humidity": {
    "min": 40,
    "max": 60,
    "unit": "percent"
  },
  "pressure": {
    "min": 1000,
    "max": 1025,
    "unit": "hPa"
  },
  "orientation": {
    "pitch_max": 15,
    "roll_max": 15,
    "yaw_range": 30
  }
}
```

---

## Object-Oriented Design 🗂️

### Key Classes

**SensorMonitor (Module A)**
- `load_config()` - Parse and validate JSON settings
- `calibrate_temperature()` - Apply offset correction
- `classify_reading()` - Determine status categories
- `log_to_database()` - Store readings with parameterized queries
- `update_led_display()` - Color-coded visualization

**MoodAnimator (Module C)**
- `create_emoji_frames()` - Multi-frame animation definitions
- `display_animation()` - Non-blocking frame rendering
- `handle_navigation()` - Joystick event processing
- `detect_idle()` - Timeout monitoring

---

## LED Display Patterns 🎨

### Module A: Environmental Status
- **Green** - Comfortable/Normal range
- **Red** - High values or alerts
- **Blue** - Low values
- **Amber** - Tilted orientation warning

### Module C: Emoji Animations
- **Happy** - Yellow smiley with bouncing effect
- **Sad** - Blue frown with tear animation
- **Angry** - Red face with steam puffs
- **Surprised** - White face with expanding eyes
- **Neutral** - Green calm expression
- **Special** - Rainbow rapid-flip reaction

---

## Joystick Controls 🕹️

### Module A (SensorMonitor)
- **Middle Press** - Pause/resume monitoring

### Module C (MoodAnimator)
- **Right/Left Press** - Navigate emoji moods
- **Middle Press** - Pause/resume animation

### Module D (Calculator)
- **Up/Down Press** - Increment/decrement by 1
- **Left Press** - Square x (x²)
- **Right Press** - Square root of x (√x)
- **Middle Press** - Reset to default (x = 4)

---

## Author ✨

| <a href="https://github.com/ayan9870" target="_blank">**Muhammad Ayan Hashmi**</a> |
|:--:|
| ![Ayan Hashmi](https://github.com/ayan9870.png?size=100) |
| [`github.com/ayan9870`](https://github.com/ayan9870) |

---

## License
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
