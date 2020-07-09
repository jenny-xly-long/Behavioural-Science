# Behavioural-Science

This current file outlines the steps to analyze the recorded videos to obtain desired information.

## Opening Anaconda Powershell Prompt
1. Go to Windows search bar and type "anaconda", click on "Anaconda Powershell Prompt"
2. Type the following into the prompt and enter: "**cd i://wongshared//DLC_NEW**" (this is the directory where all the jupyter notebook files are stored)
3. Then type "**conda activate DLC-windowsGPU**" and enter (this command activates the virtual environment for our project)
4. Type in "**jupyter notebook**" and enter
5. Now you will see the browser opens up and leading you to the directory where you can open all the Jupyter Notebook files

## Labeling and Training the Videos
1. Open "DLC_Analysis" jupyter notebook file and follow the steps on this file. This will output "**.h5**" files in the directory of "**i://wongshared//DLC_NEW//folder_being_analyzed//video**"

## Extract Coordinates Information and Dimension Transformation
1. Open "Get Transformed Coordinates, Distances and Angles" and follow the steps on this file.
2. For videos whose 4 corner coordinates are unknown, we need to label the 4 corners of the video similar to what we did in the previous section
3. ***Distance*** we calculated both head-to-head and head-to-body distances
4. ***Angle*** the angle is calculated to be that between the neck-to-head vector of one rat and the neck-to-target vector
5. ***Compass Angle*** the compass angle is calculated from a reference direction (north). For SI, we took the short side of the rat enclosure to be "north"; for 2 and 3animals, we took the top of the video to be "north" when vertical and we took the left of the video to be the "north" whe horizontal

## Functions of different Jupyter notebook files
1. The files "**neuronSFunctionsSI**", "**neuronSFunctionsAlignSI**" and "**neuronSFunctionsTwoAnimals**" contain functions that are written and imported to be used in other files. So if everything functions well, you will not need to open or modify these files.
2. The file "**Binned Frame Analysis**" calculates the values of spikes per second, spikes per second per cell, intensity per second, intensity per second per cell for each of the SI files
3. The file "**2 Animals_Binned Frame Analysis**" does the same as above, but for 2 animals as the name indicates
4. The file "**Alignment Plot**" plots the neuron firing data aligned with time for each of the SI files to help with visualization
5. The file "**Raw Neuron Data Plots**" outputs the heatmaps for every SI files with the y-axis as the neuron numbers and the x-axis the distance bins or angle bins
6. The file "**Get Frame According to Criterial**" allows us to extract the frames according to distance, angle, zone, etc.
6. The file "**Timestamp Rematching by Binning**" matches the MS frames and the behavioural frames according to a given bin size. We then take the average values of the distances and angles from the behavioural frames within that bin, and the sum of neuron spikes and intensity from the MS frames within the bin
