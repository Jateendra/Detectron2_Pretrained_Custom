Pretrained by Detectron2
==============

Main Intro : https://github.com/facebookresearch/detectron2

Downloading files :  https://drive.google.com/drive/folders/1pW4D--yW-Yt01lbJ97aIcp1jXmAYWtsm

COCO Object Detection baseline : https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md

1 ) Predict an image based on pre-trained model ( Segmentaion ):

	- Refer 'Colab Notebook' hyperlink 
  
	- Here, we will go through some basics usage of detectron2, including the following:

		> Run inference on images or videos, with an existing detectron2 model
    
		> Train a detectron2 model on a new dataset
		
2 ) 
-- import some common detectron2 utilities

	from detectron2 import model_zoo  # https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md

	from detectron2.engine import DefaultPredictor # 

	from detectron2.config import get_cfg  # https://github.com/facebookresearch/detectron2/tree/main/configs , based on Developer's requirement .

	from detectron2.utils.visualizer import Visualizer

	from detectron2.data import MetadataCatalog, DatasetCatalog  # Annotations and Images respectively .




3 ) 
cfg.merge_from_file(model_zoo.get_config_file("COCO-InstanceSegmentation/mask_rcnn_R_50_FPN_3x.yaml")) 

	- you can change the above with "COCO-Detection/faster_rcnn_R_50_FPN_3x.yaml" 
	
	- ** Ref # https://github.com/facebookresearch/detectron2/blob/main/configs/COCO-Detection/faster_rcnn_R_50_FPN_3x.yaml
	
	- ** We are trying to do "Object Detection" here ( Not Segmentaion as like the above one ) .
	
	- you can change again with "COCO-Detection/faster_rcnn_R_101_C4_3x.yaml"
	
	- ** Ref # https://github.com/facebookresearch/detectron2/blob/main/configs/COCO-Detection/faster_rcnn_R_101_C4_3x.yaml
	
4 ) Check with another .jpg file .
		- Download any .jpg file from pixel.com
		
		- Upload to Google Drive ( By doing upload to session storage in Google Colab )
		
		- Change the .jpg filename as below
		
			# im = cv2.imread("./input.jpg")
			
			im = cv2.imread("./pexels-kaique-rocha-109919.jpg")
			

Detectron2 Custom Training
===================================

Mediapipe - Google's project : https://google.github.io/mediapipe/solutions/solutions.html


1 . Downloading files :  https://drive.google.com/drive/folders/1pW4D--yW-Yt01lbJ97aIcp1jXmAYWtsm

2 . Create a "detectron2" folder in Google Drive and place all the downloaded files .

3 . Right click on "Custom_Training_Detectron2_(1).ipynb" file -> Open with -> Google Collaboratory .

4 . Change run time to "GPU". 

5 . Skip first 2 lines of  code in the file and copy paste new lines of codes and run that .

6 . In below code , you can choose the model of your choice : 

	- cfg.merge_from_file(model_zoo.get_config_file("COCO-Detection/faster_rcnn_R_50_FPN_3x.yaml"))
	
7 . ** Open "/content/drive/MyDrive/detectron2/data_detectron2/output.json" in JSON URL : http://jsonviewer.stack.hu/

8 . ** CVAT ( https://cvat.org/) : mypython1.pradhan@gmail.com . mypython / Katapali1 	

9 . You can give more number of epochs to get better result .

** The above steps are for Object Detection . If you want to do for Segmentaion

	- Change the dataset
	
	- Do the annotation from Scratch .
	
	- Change the model name ( .yaml file )
