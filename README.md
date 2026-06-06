# MRI T2 Relaxometry Using Mono-Exponential Curve Fitting

## MRI Relaxometry

Magnetic Resonance Imaging (MRI) Relaxometry is a quantitative MRI technique used to estimate intrinsic tissue properties by measuring the relaxation behavior of hydrogen nuclei following radiofrequency excitation. Unlike conventional MRI, which produces qualitative contrast-weighted images, relaxometry generates quantitative maps of physical parameters such as the transverse relaxation time (T2).

T2 relaxation describes the decay of transverse magnetization resulting from the gradual loss of phase coherence among spins. Different tissues exhibit different T2 values due to variations in water content, molecular composition, and microstructural organization.

In T2 relaxometry, images are acquired at multiple echo times (TEs). For each voxel, the measured signal intensity is modeled using a mono-exponential decay function:

[
S(TE) = S_0 e^{-TE/T_2}
]

where:

* (S(TE)) is the measured signal intensity at echo time (TE)
* (S_0) is the theoretical signal intensity at (TE = 0)
* (T_2) is the transverse relaxation time

The signal intensities observed at different echo times are fitted to this model, allowing estimation of a T2 value for every voxel in the image volume. The resulting voxel-wise estimates are combined to generate a quantitative T2 map.

---

## Dataset Description

The dataset used in this project consists of MRI images acquired at two echo times for T2 relaxometry analysis.

### Dataset Properties

* Total number of images: **240**
* Number of echo times: **2**
* Number of z-positions: **30**
* Images acquired per z-position per echo time: **4**
* Image resolution: **300 × 320 pixels**

For each z-position, four images are available at each of the two echo times, resulting in eight images per z-position. Across all thirty z-positions, this corresponds to a total of 240 images.

The dataset can be represented by the dimensions:

[
(30,;2,;4,;300,;320)
]

corresponding to:

* 30 z-positions
* 2 echo times
* 4 acquisitions per echo time
* 300 × 320 spatial resolution

---

## Data Availability

The MRI dataset used in this project is not publicly available. The data were provided by the National Institute of Mental Health and Neurosciences (NIMHANS), Bengaluru, India, for research purposes.

As the dataset contains non-anonymized clinical imaging data, it cannot be distributed, shared, or uploaded to public repositories. Consequently, this repository contains only the source code and documentation required to perform T2 relaxometry analysis.

