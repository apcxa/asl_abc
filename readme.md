# ASL Translator Project 

This project uses still images to recognize different ASL letters.

![result image of the model predicting a picture of the letter 'e'](https://github.com/apcxa/asl_abc/assets/133288638/80ff687f-109c-4c87-bec6-1384edc22109 "Image of Working Model") 



## The Algorithm

This model used a dataset from a GitHub project by LoicMarie (Project Name: Sign Language Alphabet Recognizer). The simplified process of this model is that it takes a zip file that contains the dataset, unzips it into Colab, then trains the model. You then export it into the Nano and test it out!

## Running this project

### Optional: Re-Training the Model From Scratch 
1. Follow all the steps in the Google Colab - all steps for getting all the files, training the model, and exporting are all in there. [Google Colab Notebook Link - ASL](https://colab.research.google.com/drive/1ld_ep21-Ex49o_1cWYhzghTiafUBDQXk?usp=sharing)
---
### Using the Pre-Trained Model (Recommended)
1. First, make sure the jetson inference project is set up (set up jetson inference project linked here: [Jetson Inference GitHub](https://github.com/dusty-nv/jetson-inference))
2. All required libraries in order to train the model are in the requirements.txt 
3. Open the Jetson Inference folder in VS Code and in the terminal use the command `git clone https://github.com/apcxa/asl_abc.git`
4. Using `ls`, you should see a folder named "asl_abc"
5. Type `cd asl_abc/` to move directories.
6. Using `ls`, you should see 8 files (nuswide.py, onnx_export.py, onnx_validate.py, readme.md, requirements.txt, reshape.py, train.py, voc.py) and a folder named "model" 
7. Type "imagenet" and press TAB, NOT the ENTER or RETURN key (if you accidentally press enter or return, use control c to stop whatever program you set in motion and then type in the correct command.)
8. You should see imagenet.py in the options that come up. We're just making sure we're in the right place.
9. Set NET variable in the terminal: `NET=model`
10. Run this command to see how accurate your model is! You can run the ImageNet model using the pre-trained network using the following command.

`imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$NET/labels.txt input_file.jpg output_file.jpg
`
Substitute your input and output file names.

Finding Your Input File Name: Drag and drop a test image or find an existing image if you downloaded the dataset. It is recommended to use a picture from the dataset to get the most accurate result, but you can test it on any image. Find the image where you dragged and dropped it. Right click on the image and click "Copy Path". Paste into where "input_file.jpg" is in the command. 

output_file.jpg is the name you want your ouput image to be. For example, Aresult1.jpg 


6. Quick Tip: Pressing the up arrow will allow you to use the image prediction command multiple times without copying and pasting (you have to copy and paste it the first time)!

[Video of Working Model](https://youtu.be/I5Wovvr9eCw)

[Link to Dataset ZIP File - unzip this on your computer to test images. following the steps for using the PRE-TRAINED MODEL](https://drive.google.com/file/d/1QuE0X-WaNOxC5QAFjvEK-46xM2xz-qtf/view?usp=share_link)