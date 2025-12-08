# Major-depression-MRI-file-data-visualisation
It extract data from MRI file and represents the affected area in depression
Explaining the code cell -

This code locates all - plotting MRI Brain region for affected areas in the brain-

 `.nii` MRI files in a specified folder, then loads the anatomical scan and the corresponding uniformity-test image using `nibabel`. Using `nilearn.plotting`, it overlays the uniformity map (`unitest`) onto the anatomical image (`anat`) to highlight affected regions. The visualization applies a threshold of 0.5, an autumn colormap, and a black background for better contrast. Finally, the orthogonal brain slices are displayed to allow clear inspection of intensity abnormalities.

 import pandas as pd
import os
import glob
from nilearn import plotting
import nibabel as nib
import matplotlib.pyplot as plt
import numpy as np

#getting the current working directory

print(os.getcwd())
folder = "/Users/juhi/Desktop/Home assignment"
file_ex = "*.nii"      #getting all the files with this suffix
find_files = os.path.join(folder, file_ex)
all_files =glob.glob(find_files)


anat = nib.load(all_files[0]) #loading the data from mri file
unitest= nib.load(all_files[1]) #loading the data from uniformity test file


plotting.plot_stat_map(
    unitest,
    bg_img=anat,            # brain image as background
    display_mode='ortho',
    threshold=0.5,          # show only affected area
    cmap='autumn',          # color of affected area (yellow-red)
    black_bg=True,          # black background
    draw_cross=False,
    title = "Major depression areas in the brain"
    
)

plotting.show()



 ![alt text](image-1.png)

Understanding the code block- plotting histogram-

This code below loads an fMRI image using `nib.load()` and extracts all voxel values with `get_fdata()`. The 3D data is flattened into a 1D array using `.flatten()`, and only positive activation values above a threshold of 0.1 are kept using boolean indexing. A histogram is then plotted with `plt.hist()` to show how these meaningful activations are distributed, using `log=True` so the y-axis is easier to interpret. Finally, `plt.show()` displays the histogram, helping visualize the intensity of brain activations related to major depression.



# Load MRI data
functional_image = nib.load(all_files[1])
data = functional_image.get_fdata()

# Flatten data to 1D
voxels = data.flatten()

# Keep only meaningful positive values (ignore noise)
threshold = 0.1 
positive_voxels = voxels[voxels > threshold]

# Plot histogram
plt.figure(figsize=(10, 6))
plt.hist(positive_voxels, bins=10, color='skyblue', edgecolor='black', log=True)
plt.title("Histogram of MRI Activations (Major Depression)")
plt.xlabel("Voxel Intensity")
plt.ylabel("Number of Voxels (log scale)")
plt.grid(False)
plt.show()


image-2.png

