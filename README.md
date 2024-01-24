# Semantic Segmentation on Indian Driving Dataset

## Team Members: Abhishek N M, Sahana S D, Kusuma M

## About the project
We perform semantic segmentation using SegNet on the Indian Driving Datase to obtain at the performance of the SegNet model on the accuracy and IOU score.

## Dataset
The Indian Driving Dataset consists of 6906 and 979 high resolution images in the training and validation set. There are a total of 39 unique class labels. We worked only for 1 class that is drivable area.

## Data Preprocessing
For each image, we have a json file containing the number of different classes in the image and the polygon vertices for segmentation map of each class. We simplify this directory structure as follows:
  - img
    - train
    - val
  - seg
    - train
    - val
    
We create segmentation maps as .png files and store them in the seg directory. Refer to [Preprocessing.ipynb](https://github.com/anishmadan23/semantic-segmentation-indian-driving-dataset/blob/master/Preprocessing.ipynb) to understand how the preprocessing is done.

## Models
We refer to the implementaion by [zijundeng](https://github.com/zijundeng/pytorch-semantic-segmentation) for SegNet architecture. We use a pretrained VGG16 with batch normalization layers as a feature extractor for SegNet.

## Results
#### Accuracy And IOU Scores
The following summarises the accuracy and IOU for the trained networks on the validation set:
| Model  | Accuracy | IOU |
| ------------- | ------------- | ------------- |
| SegNet | 79.19  | 63.44  |

#### Qualitative Results for SegNet
The following are the visualizations of the output for the SegNet (from left to right- input, ground truth, model output):

![screenschot]([[https://github.com/Lohit-pro/Driving-Affordance-using-SegNet/blobs/master/imgs/segnet.png]](https://github.com/Lohit-pro/Driving-Affordance-using-SegNet/blob/main/imgs/segnet.png))


## Acknowledgements
We would also like to thank Zijun Deng for making their repository on semantic segmentation publicly available which we have referred to for FCN and SegNet architectures.
