---
title: "Mass measurement system with Labview"
excerpt: "Group leader  Top 10% Excellent Group <br/><img src='/images/Labview.png'>"
collection: portfolio
---
_My Duties_ 
Write Labview control system;Connect hardware device

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Labview.png" alt="Labview" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 3: Labview Programming</strong> <br>
    </p>
</div>

_1. Circuit Scheme_

By the power adapter connected to the ordinary AC power supply for the pressure transmitter (amplifier) power supply, amplifier sensor end connected to the pressure sensor, the output end connected to the data acquisition module, the data acquisition module to collect the data and will be transferred to the LabVIEW host computer, processed to get the data output. 

Pressure sensor, data acquisition module, amplifier and external power supply connection diagram:
<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Labview_experiment.png" alt="Labview" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 3: Hardware device connection diagram</strong> <br>
    </p>
</div>

_2. Labview Implementation_

2.1 Overview of the process

This procedure is roughly divided into 3 parts: data acquisition, data processing (low-pass filtering, array conversion, 2 waveform intercepts), and conversion of output voltage to quality results. 

2.2 Data Acquisition

Using a DAQ assistant to collect the data and display the raw waveform in a waveform graph. At the same time, the amplitude is measured because the output voltage of this pressure sensor is millivolt (mV) level, and after amplification by an amplifier (2000 times), the output voltage is volt (V) level, and a while loop is used to make sure that only signals with a voltage > 0.001V can be output. 

2.3 Data processing

2.3.1 _Low-pass filtering:_ Observation of the original signal reveals that the waveform has a lot of high-frequency noise, so a low-pass filter is used to filter out the high-frequency signal and retain the low-frequency signal. 

2.3.2 _Array conversion:_ save a one-dimensional array of numbers as a txt text file, and then read the array. 

2.3.3 _2-time waveform interception:_ 1-time waveform interception after the average amplitude is not accurate enough, so the use of 2-time waveform interception. 1-time waveform interception, take the maximum value index, export the second subarray, get the amplitude of the maximum value of the data; 2-time waveform interception, using the minimum value index, the export of the second subarray, get the maximum value of the intercepted waveform in the minimum value of the data after the data, greatly improving accuracy.

2.3.4 Add waveform charts to show the intercepted waveforms for easy debugging.

2.4 Conversion of output voltage to quality results

After 2 waveform intercepts, the amplitude and level measurement functions are used to read the mean (DC) amplitude and the numerical display space is used to show a more accurate amplitude value after 2 waveform intercepts. 
After obtaining a more accurate post-intercept output voltage, the output voltage needs to be converted into a quality result. 

Measurement of the excitation voltage with a multimeter, as well as the range of the amplifier output voltage (0-10V) and the range of the pressure transducer (0-30kg) gives the empirical formula for the mathematical operation of the calibration:

2.5 Specific calibration process

A 0.4kg and one 0.4kg and two 0.4kg weights were placed and the output voltage was read for calibration.
The results are shown in the table below:

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Calibration.png" alt="Calibration process" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 2.5.1: Specific calibration process</strong> <br>
    </p>
</div>

The theoretical equation obtained by assuming complete linearity of the sensor: _m=3U_

_U=0.33*m+0.035 , m=3.03*(U-0.035)_

The calibration is obtained accordingly.

The calculated calibration formula eliminates the zero residual error, but does not completely eliminate the error due to non-linearity. 

