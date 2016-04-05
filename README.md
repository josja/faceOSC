# faceOSC

Provides OSC messages to Wekinator, a Machine Learning tool written by Rebecca Fiebrink and used in her Kadenze course.

Dependencies:
- Webcam.
- CV, please use MAX's package manager in the file menu to find and install CV.
- Wekinator or any OSC agnostic machine learning model.

Usage:
In Wekinator, set the number of inputs (#inputs) to 300 (and enable the output to send class probabilities by OSC if you use my OSCvideos patch)

Running the patch:
- start the video cam using the 'open' button.
- start face detection and OSC data output using the [x] toggle.
- start training the first class of a 3 classes classifier model (I selected class 1 and recorded only happy faces, class 2 using angry faces and class 3 using neutral faces). 
- After you recorded at least 1000 records (frames) of each expression (you can keep the faceOSC patch running and) set your model to [running] instead of training and watch the results using the OSCvideos patch reacting to Wekinator's output (load some appropiate videos first in the OSCvideos patch, top = happy, middle = neutral and lowest = angry IIRC)


