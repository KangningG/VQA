# VQA
**Introduction**

The project topic we choose is Visual Question Answer. 
The idea comes from a paper of Virginia Tech named “VQA: Visual Question Answering”. 
They posted their resource on www.visualqa.org, like dataset, demo. 
Our goal is to reproduce the LSTM+CNN Model in their paper by keras, and use our model to answer some open-ended questions.

In vqa dataset, it has three parts: images, answers, and questions. 
Images from MSCOCO, answers and questions created by human.  
Based on our syllabus, we are going to reach some approaches like CNN, LSTM and MLP. Our project uses top 1000 answers as the labels. 
CNN part deals with extracting image features and LSTM deal with extracting features from questions, then we feed above two parts of features into a fully connected network to predict the most answer (the most likely answer in top 1000 answers).  


**Data set**

Image				
We use the 204,721 training images from the Microsoft Common Objects in Context (MS COCO) dataset. 
COCO is a large-scale object detection, segmentation, and captioning dataset. 
Each image in COCO contains a lot of informations. What we need is just the image file and image id.

Text: Question and Answers
There are 1,105, 904 questions and answers. 
The answers and questions are created by human. 
For each image, dataset collected three question and answered them. 
Some of questions only require low level computer vision techniques. Like ‘Is that a dog?’, ‘How many apples in the picture?’ 
Moreover, dataset also has some questions like ‘What sound does the pictured animal make? ’ which is not only based on recognizing objects from picture.
