# Classifying Leukemia Cells
## The Project
This project classifies images based on jpg files of blood cells. The AI model I made then classifies the image of blood cells as one of the four types of Leukemia. This is as a great way to detect if someone may or may not be healthy, and simplifying the work that doctor's do. This project allows for more efficiency, and easier processes to help not only doctor's but also patients, which proves the real-life use of this model.
This photo shows an output of my project. As you can see, my model can classify the pictures of blood cells as either benign, early, pre, and pro.
## My Algorithm
The algorithm of sorting the blood cells works by first being trained by being shown a series of images of each class. I organized the folder and then ran training with 100 epoches. The data I collected were of the two classes benign and malignent along with subtypes of malignant lymphoblastic samples(early, pre, and pro). Through the resnet tool, AI learns certain features of each class. After the AI knows what class images correspond to, the AI can be shown a new set of images, and will label them by class from their pre-trained knowledge. The images and output can then be exported. This project started at 50% accuracy and after about 70 epoches, it has reached about 99 percent accuracy.
## How To Run The Project 
1. Clone the jetson-inference project from GitHub using "git clone --recursive https://github.com/dusty-nv/jetson-inference" and change directories into it
2. Pull the code from this repository.
3. Put it in jetson-inference/python/training/classification directory.
4. Set NET=models/Run1 and DATASET=data/Original
5. Run the command imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/NAME OF CLASS FOLDER/NAME OF JPG TO CLASSIFY DESIRED NAME OF YOUR OUTPUT
6. The class of your image will appear in your terminal after running and it will also be labeled on your image.
