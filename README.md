# ECG Signal Filtering Using Butterworth Filters
This code demonstrates how to load and filter an ECG signal from a .mat file. The signal undergoes several filtering stages to remove baseline wander and high-frequency noise, including powerline interference, using Butterworth filters.

# Key Steps:
### 1. Reading the ECG Signal:
The ECG signal is read from a .mat file using the scipy.io library.
The signal is stored in a variable sig, and the sampling frequency (fs) is set to 720 Hz.

### 2. Initial Plotting:
The entire ECG signal is plotted to visualize the raw data.
A zoomed-in version, showing the first 500 samples, is also plotted for closer inspection.

### 3. Filtering the Signal:
#### 3.1 Baseline Wander Removal:
A high-pass Butterworth filter with a cutoff frequency of 0.5 Hz is applied to remove low-frequency components (baseline wander).
The filtered signal is plotted alongside the original signal for comparison.
#### 3.2 Powerline Noise Removal:
A low-pass Butterworth filter with a cutoff frequency of 20 Hz is used to remove high-frequency noise, such as powerline interference.
The result is plotted to visually compare it with the original signal.
#### 3.3 Bandpass Filtering (Simultaneous Removal of Baseline Wander and Powerline Noise):
A bandpass Butterworth filter is applied with cutoff frequencies of 0.5 Hz and 40 Hz. This filter simultaneously removes both baseline wander and high-frequency noise in a single step.
The resulting signal is plotted to compare it with the original unfiltered signal.
