README.txt
DSSS-Based Anti-Jamming Communication System
=============================================

PROJECT OVERVIEW
----------------
This project implements a Direct Sequence Spread Spectrum (DSSS) communication 
system with anti-jamming capabilities. Two versions are available:

1. Simple DSSS Version - Basic implementation for educational purposes
2. Advanced DSSS Version - Enhanced version with adaptive processing gain 
   and memory optimization



PART 1: SIMPLE DSSS VERSION
============================
Files: Exp1_DSSS_jamm_1.m to Exp1_DSSS_jamm_3.m

DESCRIPTION:
------------
Simplified versions of the DSSS communication system for basic understanding.

HOW TO RUN:
-----------

STEP 1: Prepare Audio Source File
  • Locate your input audio file (WAV format recommended)
  • Copy the full file path to clipboard
    Example: C:\Users\YourName\Music\input_audio.wav

STEP 2: Open MATLAB
  • Launch MATLAB (R2018b or newer)
  • Navigate to the folder containing all MATLAB files

STEP 3: Open Main File
  • In MATLAB Current Folder, double-click "Exp1_DSSS_jamm_3.m"
  • File will open in MATLAB Editor

STEP 4: Configure Audio Source Path
  • Find SECTION 2 - LOAD AUDIO FILE (around line 30-40)
  • Locate this line:
    audio_src_file = 'C:\Users\YourName\Music\your_audio_file.wav';
  • Replace with your copied audio file path

STEP 5: Run the Simulation
  • Click RUN button (▶) in Editor toolbar
  • OR press F5 key
  • OR type in Command Window: >> Exp1_DSSS_jamm_3

STEP 6: View Results
  • Multiple figures will open automatically
  • Output audio saved in same folder as input with suffix "_RECOVERED_DSSS.wav"









PART 2: ADVANCED DSSS VERSION (AI-OPTIMIZED)
=============================================
File: Exp1_DSSS_jamm_4.m

KEY FEATURES:
-------------
✓ AI-Assisted Optimization - Improved code structure and memory management
✓ Formula-Based Parameters - No hardcoded values, all derived from formulas
✓ 3 Configurable Jammers - CW, swept, or multitone (user selectable)
✓ Adaptive Processing Gain - BER feedback controls PN code multiplier
✓ Audio Output Saving - Recovered audio automatically saved to disk
✓ Memory Optimized - Efficient handling for long audio files

HOW TO RUN:
-----------

STEP 1: Prepare Audio Source File
  • Select input audio file (WAV format recommended)
  • Copy complete file path to clipboard

STEP 2: Open MATLAB
  • Launch MATLAB (R2020a or newer recommended)
  • Navigate to project folder

STEP 3: Open Advanced Version
  • Double-click "Exp1_DSSS_jamm_4.m" in Current Folder

STEP 4: Configure Audio Source
  • Find SECTION 2 - LOAD AUDIO FILE (around line 40)
  • Locate: audio_src_file = 'C:\Users\Rizwan Ali\Music\output2.wav';
  • Replace with your audio file path

STEP 5: Select Jammer Type
  • Find SECTION 1 at top of file
  • Choose one jammer type by removing % symbol:
    
    JAMMER_TYPE = 'CW';        % Single frequency jammer
    % JAMMER_TYPE = 'swept';    % Frequency sweeping jammer
    % JAMMER_TYPE = 'multitone'; % Multiple frequency jammer

STEP 6: Run the Program
  • Click RUN button (▶)
  • OR press F5
  • OR type: >> Exp1_DSSS_jamm_4


STEP 7: Listen to Recovered Audio
  • Output saved as: [original_filename]_RECOVERED_DSSS.wav
  • Located in same folder as input file



SYSTEM REQUIREMENTS
===================

Software:
---------
• MATLAB Version: R2016b or newer (R2020a+ for advanced version)
• Required Toolboxes:
  - Communications Toolbox
  - Signal Processing Toolbox
  - DSP System Toolbox

Hardware:
---------
• RAM: Minimum 4GB (8GB recommended)
• Processor: Any modern Intel/AMD processor
• Storage: 100MB free space

Supported Audio Formats:
-----------------------
• WAV (recommended)
• MP3
• M4A


TROUBLESHOOTING
===============

Problem: File not found error
Solution: Check path format and file existence
         Windows: C:\Folder\file.wav
         Mac:     /Users/Name/file.wav
         Linux:   /home/Name/file.wav



EXPECTED OUTPUT
===============

Successful run shows:
----------------------
• Command window with complete parameter listing
• Nine figures opening automatically
• BER < 0.01 (1%) for typical conditions
• Recovered audio file created
• Final summary with all system parameters



FILE STRUCTURE
==============

DSSS_Project/
│
├── Exp1_DSSS_jamm_1.m
├── Exp1_DSSS_jamm_2.m
├── Exp1_DSSS_jamm_3.m
├── Exp1_DSSS_jamm_4.m          ← MOST ADVANCED VERSION
│
├── dsss_params.m
├── lfsr_pn_sequence.m
├── get_primitive_poly.m
├── jammer_generator.m
├── awgn_channel.m
├── psd_jammer_detect.m
├── plot_time_domain.m
├── plot_frequency_domain.m
├── despread_demodulate.m
└── adaptive_pg_controller.m


