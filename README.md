# indian-sign-language
Indian Sign Language is a real time translation tool that generates english transcripts by capturing indian signs from a video feed. This was a self project undertaken from a learning perspective to start out in the field of Computer Vision.

## Dataset
The dataset for this project was created by me and my friends using a [sign_generator.py](https://github.com/keew13/indian-sign-language/blob/main/sign_generator.py). The aim of the project was to find the simplest way through which we can classify indian signs. It was decided that the best way to do so would be threholding the images that will be captured. Sample images that were created look like

| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
|<img width="1604" alt="1" src="https://github.com/keew13/indian-sign-language/blob/main/images/1.jpg">|<img width="1604" alt="b" src="https://github.com/keew13/indian-sign-language/blob/main/images/b.jpg">|<img width="1604" alt="r" src="https://github.com/keew13/indian-sign-language/blob/main/images/r.jpg">|

Sign 2 was skipped during creation due to its similarity with character V. Custom characters to incorporate deleting the characters and providing space were also created.
Same script with custom changes can be executed to create your own custom dataset.

## Training
that can be 
A lot of this has been referred and inspired from the following places:<br>
https://data-flair.training/blogs/sign-language-recognition-python-ml-opencv/ <br>
https://github.com/evilport2/sign-language
<br>
First the sign_generator.py file should be run. It creates the required folder hierarchy and helps in creating a dataset. You can tweak the file as required and create additional signs which might help you in generating the transcript more easily.<br>
Following this the model can be trained using the isl_classifier.py where there is provision for early stopping, reducing the lr on plateu and saving the model after every epoch in which val_accuracy improves. It also allows for continuing with the training again if it was interrupted in middle.<br>
Lastly one can run the real_time_isl.py which allows you to create a transcript of whatever signed communication is happening.<br>
I have also added the saved models that were generated after every epoch of best val_accuracy when I trained the model.
