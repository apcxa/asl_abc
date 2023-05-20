# ASL Translator Project 

This project uses still images to recognize different ASL letters.

![result image of the model predicting a picture of the letter 'e'](https://github.com/apcxa/asl_abc/assets/133288638/80ff687f-109c-4c87-bec6-1384edc22109 "Image of Working Model") 



## The Algorithm

This model used a dataset from a GitHub project by LoicMarie (Project Name: Sign Language Alphabet Recognizer). The simplified process of this model is that it takes a zip file that contains the dataset, unzips it into Colab, then trains the model. You then export it into the Nano and test it out!

## Running this project

1. (optional for retraining model from scratch) Follow all the steps in the Google Colab - all steps for getting all the files, training the model, and exporting are all in there. [Google Colab Notebook Link - ASL](https://colab.research.google.com/drive/1ld_ep21-Ex49o_1cWYhzghTiafUBDQXk?usp=sharing)
2. Make sure the jetson inference project is set up (set up jetson inference project linked here: [Jetson Inference GitHub](https://github.com/dusty-nv/jetson-inference))
3. All required libraries in order to train the model are in the requirements.txt 
4. Make sure your nano is set up and ready to go before you export it!
5. Quick Tip: Pressing the up arrow will allow you to use the image prediction command multiple times without copying and pasting (you have to copy and paste it the first time)!

[View a video demonstration here]([Video of Working Model](https://youtu.be/hMjLQokgAl8))
