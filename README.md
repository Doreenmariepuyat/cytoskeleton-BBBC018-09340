# Cytoskeleton and Cell Morphology — BBBC018

## Student Information
- **Student ID:** 202303480
- **Selected phenotype:** Phospho-histone H3 dots
- **Image-field ID:** 09340
- **Actin filename:** 09340-actin.DIB
- **DNA filename:** 09340-DNA.DIB

## Dataset
This activity used image set BBBC018v1 from the Broad Bioimage Benchmark Collection (Ljosa et al., *Nature Methods*, 2012).

Dataset page: https://bbbc.broadinstitute.org/BBBC018

Download link: https://data.broadinstitute.org/bbbc/BBBC018/BBBC018_v1_images.zip

The selected phenotype was classified by visually comparing the downloaded fluorescence images with the phenotype examples on the BBBC018 webpage. The phenotype is a visual classification and is not a verified annotation for the selected field.

## Methods: Highlighted Procedures
The figures below illustrate the key steps of this activity, from selecting the Phospho-histone H3 dots phenotype and image field 09340 from the BBBC018 dataset to measuring five cells in Fiji and analyzing the results in RStudio. 

<img width="557" height="623" alt="image" src="https://github.com/user-attachments/assets/d3a093db-3d3c-4ec7-a34b-176ba63fc238" />

**Figure 1. Selection of the Phospho-histone H3 dots phenotype from the BBBC018 dataset.** The example images show different cellular phenotypes of HT29 human colon-cancer cells. The Phospho-histone H3 dots phenotype was selected for this activity.

<img width="319" height="122" alt="image" src="https://github.com/user-attachments/assets/01475263-07ce-49fa-ac30-46f0c7f6abb5" />

**Figure 2. Selection of image-field ID 09340 from the BBBC018 dataset.** The selected image field contains three corresponding fluorescence channels: 09340-actin.DIB, 09340-DNA.DIB, and 09340-pH3.DIB. 

<img width="678" height="717" alt="image" src="https://github.com/user-attachments/assets/c9e5a8e1-d5c1-4acb-b971-7e6d57db149f" />

**Figure 3. Opening the selected actin fluorescence image in Fiji.** The 09340-actin.DIB image from BBBC018 field 09340 was opened in Fiji to examine F-actin staining and identify cell outlines for morphology measurements.


<img width="796" height="684" alt="image" src="https://github.com/user-attachments/assets/f9fbde92-16a6-479d-b1a7-d2cb418ffa8f" />

**Figure 4. Setting the measurement parameters in Fiji.** The measurement settings were configured to record Area, Mean gray value, Shape descriptors, and Display label. The “Limit to threshold” option was left unchecked. 


<img width="810" height="726" alt="image" src="https://github.com/user-attachments/assets/c0c62726-0bea-4670-9cfd-9dee846213cf" />

**Figure 5. Opening the ROI Manager in Fiji.** The ROI Manager was opened to organize and manage the five selected regions of interest (ROIs) on the actin fluorescence image.


<img width="933" height="690" alt="image" src="https://github.com/user-attachments/assets/f136d8e3-d3da-4a15-b1ac-cea29d166f3b" />

**Figure 6. Selection of five cells using the Freehand Selection tool in Fiji.** Five regions of interest (ROIs) were traced around selected cells in the actin fluorescence image. These regions were used to measure cell area, mean actin fluorescence intensity, circularity, and aspect ratio that is shown in the results table.


<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/55a9a125-613c-444c-8d74-95926b5e09f9" />

**Figure 9.  RStudio script and console output for analyzing results of the five measured selected cells from BBBC018 image field 09340.** The R script reads the measurement data collected from Fiji for the five selected cells in image field 09340. It summarizes cell area, circularity, aspect ratio, and mean actin fluorescence intensity, then generates two plots: cell area versus circularity and mean actin fluorescence intensity per cell. 

## Results

### Figure 10. Cell Area versus Circularity
![Cell area versus circularity](figures/area_vs_circularity.png)

The five measured cells differed in area and circularity. Cell 2 had the largest area, while Cell 4 had the smallest. Cell 1 had the highest circularity, whereas Cell 3 had the lowest circularity, indicating a less round outline.

### Figure 11. Mean Actin Fluorescence Intensity
![Mean actin fluorescence intensity](figures/actin_intensity.png)

Mean actin fluorescence varied among the five selected cells. Cell 5 had the highest mean intensity, while Cell 1 had the lowest. These values describe the selected regions in this image field and should not be treated as directly comparable with raw intensities from other fields.

## Discussion Questions

### 1. Which specific phenotype did you choose, and what visible features support that choice?
I selected the **Phospho-histone H3 dots** phenotype. The pH3 image showed bright fluorescent dots against a dark background, which was consistent with the phenotype example on the BBBC018 webpage. This was a visual classification rather than a verified annotation.

### 2. Were your five cells mostly round or elongated?
The five cells varied in shape. Cell 1 had the highest circularity, suggesting a rounder shape, while Cell 3 had the lowest circularity, suggesting a more irregular outline. Aspect-ratio values were also used to assess cell elongation.

### 3. What role does actin play in maintaining cell shape and in cell movement?
Actin filaments form part of the cytoskeleton and help support cell shape. Changes in the actin cytoskeleton can also help cells change shape and generate forces involved in movement.

### 4. Why can a single fixed fluorescence image NOT show how fast a cell moves?
A fixed fluorescence image captures cells at one point in time. It does not show changes in cell position over time, so cell movement speed cannot be calculated from a single image.
