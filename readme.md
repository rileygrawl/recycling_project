## Recyclable or Non-recyclable - A Classifier

 This is a retrained image recognition network that can differentiate recyclable objects from non-recyclable ones. This model could be highly impactful, particularly in its ability to educate and teach others about the importance of proper recycling. 




## The Algorithm

Using the Jetson Nano, I retrained resnet18 with a dataset I found on the Kaggle site that determined the recyclability of objects. I compiled the dataset into three folders: test, train, and val. After undergoing 34 epochs of training, it is able to categorise images of items as either recyclable ("classification 1') or non-recyclable (other) with decent accuracy.


## Running this project

1. Download the model here: https://drive.google.com/file/d/1CePcv9R0T77dxrEvSNNRHs8jJ4RvDSAw/view?usp=drive_link
2. Dowload labels.txt from this project.
3. Clone the jetson-inference project from Github using: git clone --recursive https://github.com/dusty-nv/jetson-inference and cd into it.
4. Make a build directory and run "cmake ../" in the directory
5. To run an image through the model enter: "imagenet.py --model=[model]/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=[label]/labels.txt [image] [output] To clarify, [model] is the folder where resnet18.onnx is stored, [label] is the folder where the labels.txt file is stored, [image] is the image file you wish to classify, and [output] is the name of the file you want to output the results to.
6. To attain the results you can scp the outputted file from the Jetson Nano onto your computer or just look at the feedback (as shown in video).

View the video explanation here: https://www.youtube.com/watch?v=Trgx76emXec
