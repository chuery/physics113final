# Stellarator Fusion Reactors
## About
This is a final project for Physics 113 which aims to showcase how increasing parallel plasma current degrades magnetic field-line confinement in a simplified stellarator model. 
To do this, we built three different coil designs on a prescribed plasma shape and calculated their magnetic fields using Biot-Savart. Then, using an analytic magnetic field, we added plasma currents of varying strengths and measured confinement change.

We used a plasma boundary from the Constellaration dataset by Proxima Fusion. We tried three different coil designs: toroidal planar coils, helical coils, and both (which is what the W7-AS reactor used). Our Poincare analysis showed that the fields could not produce confinement and since we wanted to focus on the effects of plasma current perturbation on the field and not on coil optimization (which is the largest problem in stellarator design now), we used an analytic stellarator-like vacuum field for the remaining analysis. 
## Setup
To run main.ipynb and coildesign.ipynb, make sure that constellaration_row0.json is in the same folder as the notebooks. If you want to try another plasma boundary, follow the instructions on the [Constellaration README](https://github.com/proximafusion/constellaration) and use our plasmaboundary.ipynb to extract the row that you want to work with.

## Files
**main.ipynb:** main project notebook contains plasma boundary reconstruction, toroidal planar coil design, magnetic field calculations and tracing, Poincare and confinement analysis, and conclusion.

**coildesign.ipynb:** helical and planar + helical coil designs and their Poincare analyses.

**constellaration_row0.json:** the JSON file of the first plasma boundary in the Constellaration dataset. 

**plasmaboundary.ipynb:** loading and extracting the first plasma boundary from the Constellaration dataset, for more information about this see the [Constellaration](https://github.com/proximafusion/constellaration) repository 
## main.ipynb Overview 
**Part 0**- Load a realistic stellarator plasma boundary shape from the ConStellaration dataset and reconstruct its 3D surface from Fourier coefficients. 

**Part 1** - Design simplified offset coils, compute the vacuum magnetic field using the Biot-Savart Law, and trace magnetic field lines with RK4.

**Part 2** - Add a simplified parallel plasma current and measure how it degrades the nested-surface confinement structure using Poincaré sections. 

**Part 3** - Quantify the magnetic-field deviation caused by the current perturbation and define confinement metrics to analyze how confinement changes for different plasma-current values. 

**Part 4** - Summarize the main results and findings. 
