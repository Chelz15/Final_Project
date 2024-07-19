# Planets in the Solar System Image Identification

 Beyond our complicated Earth, there are many other planets that share this solar system with us that are deserving of recognition. However, much of the educated population on Earth cannot seem to name or recognize many of these planets. This machine opens the possibility to teach children how to identify planets through AI and Machine Learning! As someone who always had a passion for astronomy, I think it is important to inspire the younger generation to have interest in this topic. I have trained this machine to recognize planets, which can help students not only learn about our solar system but also about AI!

![add image descrition here](direct image link here)

## The Algorithm

This machine depends on Image Classification (ImageNet) and ResNet18 network. I have trained the model to learn and analyze an image and from that result, sort it into a catagory. In this case, those catagories were the planets. The computer takes a bunch of images of each planet and finds similarities and differences between them. Once it becomes confident enough that it can sort an image based on its characteristics, then it has successfully trained itself to classify the images.

Potential Sources of Error: When the image appears, there is a subtitle that says the percentage of confidence and a class number. Unfortunately, when I had first tested out my code, I had not specified how to name the class number, and so it appears as just "Class #". This was meant to be the planet name. However, the following Class #'s correspond to each planet. Another source of error is the fact that the code can only run specific images that have an underscore. For some reason, the code did not like parentheses or spaces, so I had to manually go through some of the images and change their name so that it had an underscore in it.

Class #0 = Earth
Class #1 = Jupiter
Class #2 = Mars
Class #3 = Mercury
Class #4 = Neptune
Class #5 = Pluto
Class #6 = Saturn
Class #7 = Uranus
Class #8 = Venus


## Running this project

1. Install GitHub to reach the model and Visual Studio Code to run the model
2. Once the project has been opened on Visual Studio Code, open the terminal and make sure you are on nvidia@ubuntu
3. Type in cd jetson-inference/python/training/classification and push enter. This will get you to the right folder to run the code.
4. Type in this code: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/[WANTED PLANET FOLDER NAME]/[WANTED PLANET IMAGE NAME].jpg [PLANET NAME].jpg
5. Push enter and find in the explorer where the image is. It should have a purple icon next to the name [PLANET NAME].jpg

[View a video explanation here](video link)
