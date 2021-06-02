**Project TetraNet**
-
![image](https://user-images.githubusercontent.com/65915193/113542748-88617780-95aa-11eb-8952-399483f8c06a.png)

Project TetraNet is a novel research project used for wildfire mitigation using footage from rapid nanosatellite deployed into space. We created a nanosatellite that utilizes computer vision models, image segmentation U-Net convolutional networks, linear regression artifical neural networks, and heuristic fire spread simulators in order to accurately apply wildfire patterns to a real-world setting. The idea is to allow anyone to access quality terrain analysis for a fraction of the cost. 


## Logistics

Built and launched a nanosatellite that uses Computer Vision algorithms to actively monitor wildfire progression. This codebase is a web application to display the capabilities we would be able to offer local officials that would use tetranet to monitor wildfires in their area. The web application is built using googe Maps api along with Flask backend framework and Azure cloud.

![image](https://user-images.githubusercontent.com/65915193/113540522-edff3500-95a5-11eb-9b28-93b08da6b89f.png)


*Heat mapping for wildfire tracking*

![image](https://user-images.githubusercontent.com/65791148/113547014-c06cb880-95b2-11eb-91c7-9d91d07c00c5.png)

## Image Segmentation Analysis using U-Net Convolutional Neural Network

Our TetraNet nanosatellite conducts advanced image segmentation analysis to determine the terrain and topology of the land through scanning for dense vegetation on the ground. The images below provide insight into how we created the image segmentation U-Net convolutional neural network.

![image](https://user-images.githubusercontent.com/65915193/113466073-83f85b80-93fe-11eb-8fd1-9d46f0f20d39.png)

The above image was annotated using Apeer to produce the image below. All of our images were obtained through our original footage from our launch to space in 2021 and then annotated similarly using Apeer. 

![image](https://user-images.githubusercontent.com/65915193/113466742-b48ec400-9403-11eb-90d6-e0942d18d397.png)

Afterward, we converted our annotated Apeer image to the "mask" that we could use to train the image segmentation U-Net convolutional network.

![image](https://user-images.githubusercontent.com/65915193/113466307-62986f00-9400-11eb-9ea6-c8c17a10446e.png)

After applying our trained U-Net to the above image, it produced the "predicted mask" below, showing how our image segmentation model was highly accurate in detecting dense vegetation. 

![image](https://user-images.githubusercontent.com/65915193/113466312-6b894080-9400-11eb-905d-58190ceb45be.png)

Lastly, we overlayed the "predicted mask" images on the original images by utilizing OpenCV to further prove how accurate the model was.

<img src="https://user-images.githubusercontent.com/65915193/113470107-8bc4f980-9418-11eb-92be-ccad9027ff4b.png" width="850">

## Predicting Burned Area using Artifical Neural Network

Using the [forest fires data set](http://archive.ics.uci.edu/ml/datasets/Forest+Fires) from the UC Irvine Machine Learning Repository, we utilized the Azure Machine Learning services to automate the creation of neural network for predicting the number of hectares burned in a forest fire based on input values like temperature, relative humidity, wind, and rain as well as the FFMC, DMC, DC, and ISI indexes.

![image](https://user-images.githubusercontent.com/65915193/113236263-29c69180-926a-11eb-9d14-76c16691f2c6.png)

## Fire Spread Simulation

![video-4 (1)](https://user-images.githubusercontent.com/65791148/113903462-a390da80-9796-11eb-84b9-519c196f6f89.gif)

We utilized a mathematical model utilizing a heuristic to depict how fire spreading works while wind is blowing. The results of the code can be seen through this GIF.  

