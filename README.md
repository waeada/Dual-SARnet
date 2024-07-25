# Dual-SARnet
It is a pytorch implementation for Dual-SARnet which can generate SAR image at a specified location.
We will add to this project when our paper is published.
## Setup
## Datasets
We re-labeled the HRSID dataset, using rotated boxes for all targets. During the labeling process, we noted that land and background usually have horizontal edges, so we used a rotated frame with an angle of 0 for the labeling. In addition to this, in order to balance the number of ships with other classes of targets in the dataset, we added another 600 images of only land and sea targets using data enhancement methods, which will allow the model to better learn the features of other targets (especially land).

The datasets will be pubilshed after the paper is pubished.
## Visualization generates results


## Display UI
