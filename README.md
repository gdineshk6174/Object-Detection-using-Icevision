# Object-Detection-using-Icevision
Dataset and model preparation: <br>
- There are two folder train and test with images on the given problem statement and an annotation.csv file with details of image name,bboxes and product brand.<br>
- the annotations.csv file contains both train and test imagenames so i had to create a seperate.
dataframe with only train images and details.<br>
- in addition to the given infromation on the images bbox(name, x_min, y_min, width, height), we need information of the width and height of the each image.so i have written a function to get image's width and height and create two columns for the dataframe.<br>
- next we create a classmap. since we want only to know if there is product or not. we remove all the brands and just rename them as "cig" if there is a product and "background" if there isn't. <br>
- next we create a object detection parser from the dataframe and create train and validation dataloaders from it. <br>
- data agumentation: i have applied default agumentation from "albumentation lib" such as random rotation of +/- 45 deg. <br>
- detection network used is "**RETINANET**" <br>
- CNN architecture used is "**resnet50 pretrained**" <br>
- deep learning engine used is **fastai** (https://www.fast.ai/) <br>
- imp - there were some corrupt images i have mentioned them in the notebook. <br>
