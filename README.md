# faceOSC

Provides OSC messages to Wekinator, a Machine Learning (ML) tool written by Rebecca Fiebrink and used in her Kadenze course.

Dependencies:
- Max.
- Webcam.
- CV, please use MAX's package manager in the file menu to find and install CV.
- Wekinator or any OSC agnostic machine learning model.

Wekinator configuration:
In Wekinator, set the number of inputs (#inputs) to 300, select a SVM Linear classifier with 3 classes (1 for each expression) and enable its output to send class probabilities by OSC (if you use my OSCvideos output patch).

Running the patch:
- Start the video cam using the 'open' button.
- Start face detection and OSC data output using the [x] toggle.
- Adjust the zoom rotary control to exclude as much as background as possible.
- Start training the first class of a 3 classes classifier model in Wekinator (I selected class 1 and recorded only happy faces, class 2 using angry faces and class 3 using neutral faces). The patch will only send out frames when it detects your face (it will be max 2 frames per second defined by the qmetro object, experiment with this number if you want).
- The [size] message buttons left of the zoom control enables you to use higher resolution input frames, higher res will enable more zoom (greater distances from the camera, but it surely will eat CPU power).
- After you have recorded at least 1000 records (frames) of each class/expression (you can keep the faceOSC patch running in the background) set your model to [running] instead of training and watch your trained ML model react to the live webcam feed. To make the output numbers more fun use my OSCvideos patch (load it some appropiate videos first, top video container = happy, middle = neutral and lowest = angry IIRC)
- My best achieved result was by using the SVM Linear model but hey, your face maybe different :) do experiment...

