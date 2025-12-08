# Major-depression-MRI-file-data-visualisation

### Juhi Sanjay Mishra

Date completed: December 5, 2025

Neurosynth link: [Major Depression Analysis – Neurosynth](https://neurosynth.org/analyses/terms/major%20depression/)

 ![alt text](image-1.png)

 ##  Understanding This fMRI Image (Major Depression)

This figure shows brain regions that are **more or less active in people with Major Depressive Disorder (MDD)** compared to healthy individuals.  
The colored areas (orange → yellow) represent **significant changes in brain activity**.

### What You’re Seeing (Three Views)

**1. Coronal View (y = 23)**  
- Slice from front to back.  
- Activity in the **medial prefrontal cortex** and **right frontal/parietal regions**.  
- These areas are linked to:  
  - Overthinking and rumination  
  - Difficulty regulating emotions  
  - Self-focused thoughts  

**2. Sagittal View (x = −6)**  
- A side view near the midline of the brain.  
- Activity in the **anterior cingulate cortex (ACC)**, **posterior cingulate (PCC)**, and **precuneus**.  
- These regions are involved in:  
  - Emotional control  
  - Internal thoughts (Default Mode Network)  
  - Negative thought loops often seen in MDD  

**3. Axial View (z = 39)**  
- A top-down slice.  
- Shows changes in the **superior frontal** and **parietal areas**.  
- These areas are linked to:  
  - Attention  
  - Problem-solving  
  - Mental effort (which is often reduced in depression)

### Colorbar Meaning
- Red → Orange → Yellow = **stronger brain activation differences**.  
- Higher values on the bar (like 11 or 15) mean **stronger effects**.

###  What This Means for MDD
- Overactive Default Mode Network (DMN) → *thought loops and rumination*.  
- Changes in ACC → *difficulty with emotional regulation*.  
- Changes in frontal/parietal regions → *reduced concentration and cognitive load*.

Overall, this image highlights **brain regions commonly affected in depression**, explaining symptoms like rumination, emotional difficulty, and slowed thinking

![alt text](image-2.png)

##  Understanding the Histogram of MRI Activations (Major Depression)

This histogram shows the **distribution of voxel intensities** in the brain regions that were activated in people with **Major Depressive Disorder (MDD)**.

###  What the Histogram Represents
- Each bar shows **how many voxels (3D pixels in the brain)** have a certain activation intensity.
- The x-axis (**Voxel Intensity**) represents how strong the brain activation is.
- The y-axis (**Number of Voxels**, log scale) shows how many voxels fall into each intensity range.  
  - Because the scale is logarithmic, big drops look smaller and small differences become more visible.

###  How to Read This for MDD
- There are **many voxels with lower activation values** (around 5–7).  
  This is common in fMRI: most of the brain shows small/moderate changes.
- As intensity increases (8 → 10 → 12 → 14),  
  the **number of voxels decreases sharply**.  
  This means:
  - Only a **small number** of brain regions show **very strong activation differences**.
  - These strong activations usually correspond to **key regions altered in depression**, such as:
    - Medial prefrontal cortex (mPFC)  
    - Anterior cingulate cortex (ACC)  
    - Default Mode Network hubs (PCC/precuneus)

###  Why This Matters
This histogram helps you understand:
- **How widespread** the activation changes are in MDD.
- **How strong** those changes are.
- Whether the activation pattern is dominated by **many weak effects** or **a few strong ones**.

For MDD, this pattern (many small activations, few large ones) is typical and reflects:
- Widespread mild dysregulation in emotional and cognitive networks  
- Plus a few highly affected regions related to rumination and emotional control




**Python version:** 3.14.0

### Python packages used:
- `nilearn`
- `nibabel`
- `matplotlib`
- `glob`
- `pathlib`
