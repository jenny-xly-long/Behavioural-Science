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
