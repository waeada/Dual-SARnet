# LocBSAR
It is a pytorch implementation for LocBSAR which can generate complex SAR ship image at a specified location.
We will add to this project when our paper is published.
## Setup
## Datasets
We re-labeled the HRSID dataset, using rotated boxes for all targets. Noted that land and sea usually have horizontal edges, we used a rotated frame with an angle of 0 in the labeling. Besides, in order to balance the number of ships with other classes of targets in the dataset, we added another about 600 images of only land and sea targets using data enhancement methods, which will allow the model to better learn the features of other targets (especially land). In total, the dataset contains 2364 images with rotated box.

The datasets will be pubilshed after the paper is pubished.
### Prepare data
We provide two label formats, txt format and xml format. When you unzip it, its format is shown as follows.
```
|——Multicata HRSID
  |——images # 2364 images
    |——['.jpg']
    |——  ...
    |——['.jpg']
  |——annotations
    |——xml
      |——['.xml']
      |—— ...
      |——['.xml']
    |——txt
      |——['.txt']
```
There is only one text file, where each line is formatted as follows:path rotatedbox1 catagory1 rotatedbox2 catagory2 ... like the image below shows.

In the catagory information, 0 is for land, 1 is for sea and 2 is for ship. 
### Dataset visualization 


## Visualization generates results
With our new labled dataset, our model achieves an amazing results.

We are most proud of the model's feature learning for terriestrial targets. In order to show the power of our model, we used 200 pure land images to train it as well, the results after training are shown below. Guess which one is real and which one is fake?


## Display UI
