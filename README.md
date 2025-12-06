# Major-depression-MRI-file-data-visualisation
It extract data from MRI file and represents the affected area in depression
Explaining the code cell -

This code locates all - plotting MRI Brain region for affected areas in the brain-

 `.nii` MRI files in a specified folder, then loads the anatomical scan and the corresponding uniformity-test image using `nibabel`. Using `nilearn.plotting`, it overlays the uniformity map (`unitest`) onto the anatomical image (`anat`) to highlight affected regions. The visualization applies a threshold of 0.5, an autumn colormap, and a black background for better contrast. Finally, the orthogonal brain slices are displayed to allow clear inspection of intensity abnormalities.

Understanding the code block- plotting histogram-

This code below loads an fMRI image using `nib.load()` and extracts all voxel values with `get_fdata()`. The 3D data is flattened into a 1D array using `.flatten()`, and only positive activation values above a threshold of 0.1 are kept using boolean indexing. A histogram is then plotted with `plt.hist()` to show how these meaningful activations are distributed, using `log=True` so the y-axis is easier to interpret. Finally, `plt.show()` displays the histogram, helping visualize the intensity of brain activations related to major depression.

