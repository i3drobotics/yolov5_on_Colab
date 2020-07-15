# yolov5_on_Colab

Instructions for running Yolov5 on a dataset on Google Colab.

# Step 1- Only if you need o convert from VOC XML to yolo format
Go to desired directory and type:
git clone https://github.com/i3drobotics/Convert-VOC-to-YOLO.git
Load images and the VOC XML to the images folder.
Open "convert_voc_to_yolo.py" and change the classes in line 9 to those you are using.

# Step 2- Open the Colab notebook
Go to https://colab.research.google.com/drive/1Ihs30PoTJJSfVXH7hup0Jd9eOIvv0xfz?usp=sharing

This will open the Colab notebook template. Save a copy of the notebook in your google drive and rename. 

# Step 3- Mount your Google drive, set up the environment and clone the YOLOv5 repository
Run the first three cells to allow for the mounting of the Google drive, setting up the environment and cloning the YOLOv5 repository

# Step 4- Download config files
Run the fourth cell to download the clothing.yaml file and the yolov5x.yaml config files. 
Download the “clothing.yaml” file from the “yolov5/data/” folder

# Step 5- Edit config files
Edit yaml file
Change the “train” and “val” paths to desired names.
Change “names” to your desired classes.
An example yaml file for tools should look like:
![alt text](https://github.com/i3drobotics/yolov5_on_Colab/blob/master/example2.png?raw=true)

Save the yaml file with the desired name and upload it back to “data” folder on colabs.

Download the model config file you wish to use from the models directory. The following shows an example of “yolov5x.yaml” file. Edit "nc" in line 2 to correlate with the number of classes in the first config file. 
Upload this file back to the models directory on Google Colab.

# Step 6- Upload images
Create two directories- one called "images" and one called "labels".
Create two directories called "train" and "val" in both the "images" and "labels" directories.
Place the training and validation images and training and validation labels in the corresponding directories. 

Upload these to the ml_yolo folder. 
Once this is completed, the folder structure should look like the following:
![alt text](https://github.com/i3drobotics/yolov5_on_Colab/blob/master/example3.png?raw=true)

# Step 7- Train the model
run the “Run the training” cell. It is reccommended that this is initially run for 30 epochs to ensure that everything is working correctly. This should increase to 1000's for a more accurate model.

# Step 8- Detect
Upload images to the yolov5/inference/images folder.
run the "Run detection" cell. The output will display the detected objects. THe images with detection will also be displayed in the yolov5/inference/output folder











