# indian-sign-language
Indian Sign Language is a real time translation tool that generates english transcripts by capturing indian signs from a video feed. This was a self project undertaken from a learning perspective to start out in the field of Computer Vision.

## Dataset
The dataset for this project was created by me and my friends using a [sign_generator.py](https://github.com/keew13/indian-sign-language/blob/main/sign_generator.py). The aim of the project was to find the simplest way through which we can classify indian signs. It was decided that the best way to do so would be threholding the images that will be captured. Sample images that were created look like

| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
|<img width="1604" alt="1" src="https://github.com/keew13/indian-sign-language/blob/main/images/1.jpg">|<img width="1604" alt="b" src="https://github.com/keew13/indian-sign-language/blob/main/images/b.jpg">|<img width="1604" alt="r" src="https://github.com/keew13/indian-sign-language/blob/main/images/r.jpg">|

Sign 2 was skipped during creation due to its similarity with character V. Custom characters to incorporate deleting the characters and providing space were also created.<br>
Same script with custom changes can be executed to create your own custom dataset. The script also creates the folders in required hierarchy that helps later during the training stage.

## Training
Training of the project can be achieved using [isl_classifier.py](https://github.com/keew13/indian-sign-language/blob/main/isl_classifier.py). Required parameters of path and others can be changed in the file. Necessary callbacks like early stopping and other required methods have been defined and can be used as required. Training can be resumed in case an interruption occured. Some of the weights that were saved during the training process are also available in this repository's root path.

## Working
The real time translation can be brought into action using [real_time_isl.py](https://github.com/keew13/indian-sign-language/blob/main/real_time_isl.py). It generates the necessary windows for displaying the camera feed and displaying the classified signs collectively as a transcript. Following are the screenshots of transcipt generation in process:
| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
|<img width="1604" height="1000" alt="1" src="https://github.com/keew13/indian-sign-language/blob/main/images/output1.jpeg">|<img width="1604" alt="b" src="https://github.com/keew13/indian-sign-language/blob/main/images/output2.jpeg">|<img width="1604" alt="r" src="https://github.com/keew13/indian-sign-language/blob/main/images/output3.jpeg">|


## References
* [Sign Language Recognition](https://data-flair.training/blogs/sign-language-recognition-python-ml-opencv/)<br>
* [Evilport](https://github.com/evilport2/sign-language)
