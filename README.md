# count-the-no.-of-face-in-machine-learning-opencv
Count Faces in an Image  In this example, we will be counting no. of faces in an image using OpenCV.   1.Importing Library Firstly we will import the opencv library.   2.Loading Pre-trained Model The faceCascade will load the haarcascade_frontalface_default.xml file using the Cascade Classifiers. They are trained with several hundred "positive" sample views of a particular object and arbitrary1 "negative" images of the same size. After the classifier is trained it can be applied to a region of an image and detect the object in question.   The haarcascade_frontalface_default.xml is a pre-trained model, using which we can detect faces.  Then image is read using cv2.imread() 
3.Detecting faces After that we will detect the faces using the loaded model in faceCascade.   In detectMultiScale, the first parameter passed is the image name.  The second parameter passed is the scale factor, which is a parameter specifying how much the image size is reduced at each image scale.  The minNeighbors, specifies how many neighbors each candidate rectangle should have to retain it.  minSize is the minimum possible object size. Objects smaller than that are ignored
4. Counting Faces
We initiate a variable count with 0.

Then, we in the loop we increment it's value by 1 for each detected faces.

5. Drawing Rectangle
In above output we see four parameters in in each square brackets. Those are the face coordinates of each detected faces. We will represent those coordinates as x,y,w,h.

The x is the x-coordinate and y is the y-coordinate.

The w is the width of the face and h is the height of the face.

Hence, x+w and y+h will give the bottom right coordinates of the detected faces.

The cv2.rectangle() draws rectangle around the detected faces. We pass the image name and the (x,y)  and (x+w,y+h) coordinates to draw the rectangle.

(255,0,0) states the color of the rectangle. OpenCV works in BGR format. Hence 255 is for blue color, and two 0's following it are for green and red color respectively. Hence, color of the rectangle will be blue.

The last parameter '2' is the width of the rectangle formed.
6. Displaying Outpu
Now, we will display the output using imshow() function. First Parameter is the frame name of the window that will displayed and second parameter is the original image passed.

The imwrite() function saves the detected image in our workspace. First Parameter is the frame name of the image with which you want to save it and second parameter is the original image.

The waitKey(), stops the output in the screen.

The destroyAllWindows() will remove all the windows which were open after the program finishes.
