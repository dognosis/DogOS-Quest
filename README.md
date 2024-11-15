# DogOS-Quest Dataset
## Overview
This dataset contains EEG recordings and behavioral data from Snow's gunpowder detection training sessions. The data captures neural and behavioral responses when Snow is differentiating between target and non-target odors.

## Dataset Structure
The dataset contains multiple file types:

### EEG Data
- Files starting with `Explore_84CF_ExG_ExG_stream`
- Contains EEG recordings during the detection sessions

### Sniffing Behavior Data
- IR sensor data recording Snow's sniffing activity
- 8 columns representing different scent ports
- Values:
  - 1: Port being sniffed
  - 0: No sniffing activity

### Marker Data
- Files starting with `Explore_84CF_Marker_Markers_stream`
- Contains event markers including:
  - `sw1`: Positive marker (timestamps indicate specific events)

### Calibration Data
- Files containing/starting with `calibration`
- Baseline EEG recordings taken before detection sessions
- Recorded during rest state

### ORN Data
- ORN data is the inbuilt IMU data from the eeg amplifier 

## Time Synchronization
- LSL (Lab Streaming Layer) is used for time synchronization
- Ensures all data streams (EEG, IR sensors, markers) are synchronized to the same clock
- Maintains temporal alignment across all recordings

## Contact
engineering@dognosis.tech
