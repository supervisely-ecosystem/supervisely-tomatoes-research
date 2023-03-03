<div align="center" markdown> 

<img src="https://i.imgur.com/UdBujFN.png" width="250"/> <br>

<img src="https://user-images.githubusercontent.com/119248312/222499136-015c8321-60c8-49a3-b4a7-604326e532f9.jpg" width="100"/> 

# Tomatoes Annotated  

<p align="center">

  <a href="#abstract">Abstract</a> •
  <a href="#download">Download</a> •
  <a href="#keywords">Keywords</a> •
  <a href="#statistics">Statistics</a> •
  <a href="#introduction">Introduction</a> •
  <a href="#research-methods">Research methods</a> •
  <a href="#labeling-process">Labeling process</a> •
  <a href="#post-processing-and-analysis">Post-Processing and Analysis</a> •
  <a href="#conclusion">Conclusion</a> 
</p>

[![](https://img.shields.io/badge/slack-chat-green.svg?logo=slack)](https://supervise.ly/slack) 
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/supervisely-ecosystem/supervisely-tomatoes-research)
[![views](https://app.supervise.ly/img/badges/views/supervisely-ecosystem/supervisely-tomatoes-research.png)](https://supervise.ly)
[![downloads](https://app.supervise.ly/img/badges/downloads/supervisely-ecosystem/supervisely-tomatoes-research.png)](https://supervise.ly)
</div>




## Abstract

This article focuses on the benefits of using a deep learning model for tomato segmentation. We talked about all the stages of data collection for further neural network training. After testing, it was determined that through the use of AI, the segmentation rate of tomatoes increased with no loss in precision.
Such post may be useful to specialists in agricultural activities.

## Download
Direct download: [tar archive](https://github.com/supervisely-ecosystem/supervisely-tomatoes-research/releases/download/1.0.1/tomato-slices.tar) (1.02 GB)

## Keywords
- AI
- Deep Learning
- Computer vision
- Labeling
- Automated
- Tomato
- Phenotype
- Phenotyping
- Segmentation

## Statistics

Project contains 66 datasets with 424 images in it, with a total of 2560 annotated objects.

<img src="https://user-images.githubusercontent.com/115161827/222809839-5ac60b95-5420-4afc-89a6-2ed015ac36b1.png" width="700"/>

## Introduction

The tomatoes are one of the most consumed fruits in the world. No wonder tomato cultivation is so popular among farmers. Demand for high quality tomatoes is only growing.

The vast majority of commercially available tomatoes are hybrids created by crossing two cultivars. These tomatoes take the best qualities from their parents: they are disease resistant, have good taste and growth qualities. One of the main tasks of the manufacturer is to improve the quality and safety of grown products.
Phenotyping methods are widely used for selection and development of new cultivars with desired properties. In tomato breeding, fruit phenotypes are important agronomic traits as a reference.

Tomato annotation is a crucial part of the research process, as it allows scientists to gain insights into the tomato’s genetic makeup, nutritional value, and other properties. Our goal is to teach the Deep Learning system by segmenting images to automatically determine the external and internal structure of a tomato, as well as automate the process of collecting information about the size and color of tomatoes. In the long term, this should facilitate and speed up the phenotyping process.
Traditional measurement methods based on manual labeling limit the effective collection of data on the morphology of tomato fruits. The risk of making a mistake by manual labeling is higher. In addition, manual labeling is more difficult and time-consuming than computer vision technologies.

 
*The basis for the creation of this post was the original scientific research article ["Quantitative Extraction and Evaluation of Tomato Fruit Phenotypes Based on Image Recognition"](https://www.frontiersin.org/articles/10.3389/fpls.2022.859290/full), taken from an open source.*


## Research methods 

First of all, we needed to get tomatoes of different cultivars. This is important so that AI learns to label up completely different structures of tomatoes and does it correctly.
The size of the tomato, the number of locules, the thickness of the pericarp and many other parameters differ from cultivar to cultivar. Perhaps in the future we can train an AI to recognize between tomato cultivars and tag them.


Before we started photographing tomatoes, we generated a QR-code with parameters of 6.9 cm x 6.9 cm, which will be its data. Later on, it will help to calculate the area of an object in the photos and straighten the photos themselves.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444731-a29c1ff3-92fd-42d4-9802-41aba1631948.png" width="150"/>
</p>

During the entire process of photographing the camera was on a tripod in a fixed position.
The light was positioned so that there was almost no shadow of the object. This is useful so that when labeling a tomato with a smart brush tool, the selection of an object is more accurate.
Additionaly, we placed a pad under the tomato in order for it to stay flat. 

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444860-b8666b1e-b11a-4033-addb-0c9839f3b6e4.jpg" width="500"/>
</p>

Before shooting, all the tomatoes were washed. Also, each part of the tomato was wiped with a dry napkin in order to avoid glare in photographs. Glare significantly complicates the labeling process.

<p align="center">
 Photo No.1: The tomato must be positioned so that its navel / sepals look up.
</p>
  
<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444861-3bffd6d4-3386-4dde-834b-126288dee02c.jpg" width="700"/>
</p>

<p align="center">
Photo No.2: The tomato must be turned upside down.
</p>
<p align="center">
  Next, we made a vertical cut in the middle of the tomato. 
</p>
<p align="center"> 
    The tomato must stay in the same position.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444862-4357fa05-ba4c-4f54-9ecf-a1b02ec81486.jpg" width="700"/>
</p>

<p align="center">
Photo No.3: The left side of a vertical slice of a tomato.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444864-b330c5d0-df68-4699-9493-6196e85e92ee.jpg" width="700"/>
</p>

<p align="center">
Photo No.4: The right side of a vertical slice of a tomato.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444867-053dad06-ef3e-4542-afce-ae2b01fa81d3.jpg" width="700"/>
</p>

<p align="center">
Then we connected the left and right parts of the tomato together and made a horizontal cut.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444868-ef3c8f57-25d0-401b-b5e9-ca46a1a0b3ad.jpg" width="700"/>
</p>

<p align="center">
Photo No.5: Connected left and right parts of a tomato with a navel.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444871-787ffe15-4986-4938-8fc2-b8e638fea807.jpg" width="700"/>
</p>

<p align="center">
Photo No.6: Connected left and right parts of a tomato with a top(point).
</p>
  
<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444873-39a26e7d-ea20-4ba1-ab7c-5202dee93a74.jpg" width="700"/>
</p>

It is important to follow the same sequence when cutting and photographing tomatoes. This will make it easier to organize photos.

From one tomato, we got 6 photos, except for those tomatoes that had sepals, in this case there were 7 photos.

### Data organization on the platform

To systematize all the tomatoes, a project was created with many datasets. In each of the datasets, photos of tomatoes are presented in the same sequence.
All photos were large in size.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222507408-2eddba75-9682-4a84-b6e7-471c41921ca1.png" width="700"/>
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222507461-c6a87ec0-4999-47a4-a0f3-d036d9a555a8.png" width="700"/>
</p>

Each dataset contains all photos of one tomato of a particular cultivar.

To designate the fruit cultivar, we used a tag system.
We also used a tag system to distribute images by angles. That way, we got:
- Photo №1: top
- Photo №2: bottom
- Photo №3: vertical cut left
- Photo №4: vertical cut right
- Photo №5: horizontal cut top
- Photo №6: horizontal cut bottom

<p align="center">
<img src="https://user-images.githubusercontent.com/115161827/222559571-f6d39632-ae86-4979-8ee2-6cd9f4f2eaf5.png" width="300"/> <img src="https://user-images.githubusercontent.com/115161827/222557886-bc010627-3cbf-4db1-9d73-fc1bc9dc7473.png" width="300"/>
</p>                                                                                  



If  you need to calculate the area of the tomatoes and are not sure about the straightness of your camera angle or stability of your pictures, you need to use this APP [“Perspective transform using QR-code”](https://dev.supervise.ly/ecosystem/apps/perspective-transform-using-qr-code) to straighten the photos before starting the labeling process. In our case, this was not necessary.

After we made sure that the photos were uploaded in the correct order, we started labeling objects

<p align="center">
<img src="https://user-images.githubusercontent.com/115161827/222567402-ea3d905b-0f49-462a-b775-de9281ac4ad3.png" width="300"/>  <img src="https://user-images.githubusercontent.com/115161827/222567759-340dbb87-a4e2-47a0-99da-eced7ccc615e.png" width="300"/>
</p>                                                                                  



## Labeling process

First, we needed to create classes with which we will label certain parts of the tomato. It was important to choose a tool with which to mark one or another object. Choosing the right tool will help you complete the labeling faster and clearer. Also, we made sure to have diverse colors so that the parts of the tomato did not merge with each other. 

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444895-566d5cdd-243f-4265-b447-c8272b4ea686.png" width="700"/>
</p>

### Layering

It is important to note that labeling is done by stacking layers, where the top layers cut out the bottom ones.

**How it works:** 

To begin with, we started the labeling with the parts that take the most time. It is important to point out that we labeled them, paying close attention only to those gaps that are not in contact with the parts that we are labeling on top.
Thus, the placenta and septum are labeled with circles, and the locules, which are the topmost layer, are accurately labeled along the borders, thereby cutting off the excess selection.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444899-e33479bc-fede-40b1-9430-9f0cb3675936.jpg" width="700"/>
</p>

Large parts of the tomato, such as the whole tomato and the pericarp, were annotated with a smart tool, as it defines objects against the background quite accurately.
The annotation of more detailed objects was done by the polygon tool.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222733420-b933c1af-a221-4c12-891c-598f5a905309.jpg" width="700"/>
</p>

<p align="center">
<a href="https://tea.solgenomics.net/anatomy_viewer/microscopy/slm82_fruit">You can find more about the structure of tomatoes here</a>
</p> 
  
<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444902-bbc5650a-a6c3-4ed0-9558-bba6764f95ce.jpg" width="700"/>
</p>

<p align="center">
Step 1: With a smart tool <tr><td><kbd><b>0</b></kbd></td></tr>, we selected the whole tomato in all the photos.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444907-0b2013a5-5d21-412f-be2b-8faa0fbab6df.gif" width="700"/>
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444922-87ca9817-32e3-4f95-9edf-3bda2732a93d.gif" width="700"/>
</p>

<p align="center">
Step 2: After we copied the tomato layer in the slice photos and repeated it, changing the class to pericarp (click on the layer and tap <tr><td><kbd><b>ctrl+c/ctrl+v</b></kbd></td></tr>). On the pericarp layer, the outer parts of the fetus were removed.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444933-0f8d62ab-c6d3-439b-a008-cbb487a18e37.gif" width="700"/>
</p>

<p align="center">
Step 3: Label the navel with a smart tool. If the tomato also has a sepal, it can be labeled with a smart tool.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444829-a8af1cb2-3f8f-4beb-9987-af12d9a6380a.gif" width="700"/>
</p>

<p align="center">
Step 4: We selected the placenta with the polygon tool <tr><td><kbd><b>8</b></kbd></td></tr>.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444841-bd732fb4-bb57-4ac7-82e7-b64a31cf6448.gif" width="700"/>
</p>

<p align="center">
Step 5: We selected the septum with the polygon tool.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444849-0187cf97-5569-4c7d-838c-a5ac3a6a92c9.gif" width="700"/>
</p>

<p align="center">
Step 6: In the photos of the vertical sections of the tomato, we have identified the core.
</p> 
  
<p align="center">
Step 7: We selected the locules with the polygon tool. It's important to select the locules carefully because this is our topmost layer.
</p>  

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222444852-3fc8ee22-c312-4fe4-b338-b5be637b2c23.gif" width="700"/>
</p>

<p align="center">
Step 8: Сolumella we labeled only on those photos where it was visible.
</p>
  
<p align="center">
The most important thing is that at maximum opacity, the labeling should match the parts of the tomatoes. 
</p>
  
<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/222445104-93a34bb6-383e-4d03-9085-26d120b46a0b.gif" width="700"/>
</p>


## Post-Processing and Analysis

After all the tomatoes were labeled, we used the APP [“Rasterize objects”](https://dev.supervise.ly/ecosystem/apps/rasterize-objects-on-images) to get rid of the overlaying. Therefore, the upper layers were cut out the lower. 
You can learn more about how this app works [HERE](https://dev.supervise.ly/ecosystem/apps/rasterize-objects-on-images). 

## Conclusion

Thus, this article claims that the Supervisely team has made progress in automating the collection of data on tomato phenotypes. Deep Learning methods can effectively help human labor, saving time and budget.
Taken together, our results are consistent with the conclusion of the article ["Quantitative Extraction and Evaluation of Tomato Fruit Phenotypes Based on Image Recognition"](https://www.frontiersin.org/articles/10.3389/fpls.2022.859290/full). The measurement accuracy was comparable to manual labeling, and the time spent on labeling was significantly reduced.
Tomato annotation also helps to create accurate models for predicting the tomato’s growth and yield. This can help farmers to increase their crop yield and improve the quality of their tomatoes.Received consistent and quantitative data on the phenotype can also help in genomic, metabolomic, and transcriptomic studies of the tomato.
It is worth noting that this technique can be extended to the phenotyping of other fruit crops.
