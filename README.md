# ITT - Programming Assignment 01
# Digital-Signal-Generator

## Problem Statement:
Implement a digital signal generator:
Line coding schemes to be implemented:
1. NRZ-L, NRZ-I, Manchester, Differential Manchester, AMI and scrambling schemes: B8ZS, HDB3.
2. Pulse code modulation (PCM) or Delta modulation (DM)

(The code in in C++)

Input: Ask user for digital signal generation i.e., whether user wants to give
analog or digital input. Then, accordingly proceed with line encoding or PCM/DM.
For encoding you need to provide user with various options (NRZ-L, NRZ-I,
Manchester, Differential Manchester, AMI). If user asks for AMI, you need to
pop a query whether scrambling is needed or not, if answer is yes next query
would ask about the type of scrambling. For PCM/DM, take analog input and
process it based on the chosen technique, then the digital data generated can
be fed to one of line encoding techniques.
Output: Digital data stream given, longest palindrome in that data stream,
digital signal produced and in case of scrambling, scrambled signal produced.

## Features
- Supports both digital and analog input
- Generates encoded waveforms (amplitude vs time)
- Exports CSV files for plotting encoded signals
- Implements Manacher’s algorithm to find longest palindromic substring efficiently
- Compact, modular C++ code
- Compatible with any OS (Windows/Linux/Mac)

  ## Compilation
  1. Run ./digital_signal_generator
  2. Generates CSV files like: nrzl.csv, nrzi.csv, manchester.csv, diff_manchester.csv, ami.csv, ami_b8zs.csv, ami_hdb3.csv
  3. To visualize waveforms, you can use Python with Matplotlib: import pandas as pd -> import matplotlib.pyplot as plt -> df = pd.read_csv("nrzl.csv") -> plt.step(df['sample'], df['amplitude'], where='post')
       -plt.title("NRZ-L Waveform")
       -plt.xlabel("Samples")
       -plt.ylabel("Amplitude")
       -plt.grid(True)
       -plt.show()
