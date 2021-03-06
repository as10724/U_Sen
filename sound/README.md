# NYU_CUSP_UrbanSoundSensing2017

## Author: Avikal Somvanshi (as10724)

This lecture introduces students to the fundamentals and application of sensing urban sound.

Gathering and making use of data from these environments requires knowledge of real-time data acquisition techniques and considerations when capturing and visualizing acoustic data. Time and frequency domain visualization approaches will be introduced, facilitated by a data collection initiative based around a “smart” sound sensing tool.

Prerequisites

* Knowledge of data I/O using Python libraries
* Visualization and handling of large datasets
* Basic understanding of multithreaded scripting

### Assignment Task

Using the audio_record.py script, monitor the sound environment from the window of your apartment for around an hour.

As it is, the script will only print to the console if a certain level is exceeded. You need to modify it so that it logs `rms` to a CSV file with timestamps continuously. The level sampling occurs very quickly (~20/s) so you should also average this data using some kind of moving average. After this you can convert to decibels using the information on the slides.

Remember to switch off auto noise cancellation and auto gain control if they are on. Set the input gain to maximum in the OS settings. Before you start the process take some test measurements to ensure the system is working.

You need to provide a paragraph or two on the context around the measurement process, such as the conditions the laptop is setup in, distance to window, height above street level, intersection details, weather, pictures of the setup, time of day, etc etc. As much information as you can gather.

You can email me at: cmydlarz@nyu.edu if you have any questions

### Context and study setup

The study was conducted from the second storey apartment at the intersection of Franklin Ave and Clifton Place in Brooklyn. The interection conner where the apartment is located is commerical with two bars, a taco joint, a live music venue and an active construction site. It is a really noisy conner and inteestingly my home. The laptop was placed on the window sill of my bedroom and recording took place from 9:29pm to 10:29pm on Saturday, 2:29am to 3:29am on Sunday and 7:26am to 8:26am on Sunday.

![Setup Assignment 3:](laptop_setup.jpeg)

### Results

![Plot 1 Assignment 3:](noiseC.png)

Figure1. Noise levels are consistantly high in the evening with the taco joint crowd being the major contributor to the noise levels, the night levels are lesser but still not quiet enough for a decent sleep as the live music venue is operational till 4am. Levels in morning are high but erratic with instances of very sharp nosie mostly a reflective of morning traffic and nature of construction activity.

Individual plots of each time slot can be found in the ipython notebook Noise_visiualization.ipynb

Evening data is stored as as10724_rms.csv and as10724_decibel.csv

Night data is stored as as10724_rms2.csv and as10724_decibel2.csv

Morning data is stored as as10724_rms3.csv and as10724_decibel3.csv

#### Note: In absence of caliberation for this study, the lowest recorded rms during the study was used as reference for calculating decibels from recorded rms.
