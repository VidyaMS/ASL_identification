# ASL identification.  
ASL stands for American Sign Language.   
It consists of various gestures with which each letter of the English alphabet can be interpreted. More details can be found at https://en.wikipedia.org/wiki/American_Sign_Language.   
The data source for this analysis :  https://www.kaggle.com/grassknoted/asl-alphabet. 
We are provided with train images (87000) and test images(24) for each letter.  
I have also downloaded few ASL images from the web and used them for further testing.  

The notebooks in this repo serve the following  purposes: 
Step 1:   
In the notebooks : sign_language_identification_RGB.ipynb and sign_language_identification_grayscale.ipynb , Neural Network models are built for the purpose of identification of ASL images and getting the best test set accuracy.    
Step 2 :   
the model giving the best accuracy on test images is selected and further tested for variance and bias. i.e for folds of 3 , 87K images are split into training and validation images, model learns from the images and is tested against the test images . The noteboooks - sign_language_identification-cv1 .... to cv3.ipynb and sign_language_identification-cnn-2-cv1.ipynb ...to cv3.ipynb peform the cross validation.  
For each of the fold, the test set accuracy is checked for any variance.  

Step 3:   
Once we find that the selected model's performance is consistent across all the three cross validation, we test it further for the new ASL images downloaded from the net.  

Summary :  
It's seen that Neural Network consisting of 2 - 3 layers of CNN + Max Pooling gives a sufficiently good test set accuracy for the the given 24 images.The number of filters required is small at 8, 16 and 32.  
How ever , when the above models are tested against the new images downloaded from the net , we see a degradation in accuracy . We may need to further work on the images and recheck the model performance.  
