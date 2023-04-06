# FaceDetection
Simple Face Detection with python


Setting up the environment:
1. Install OpenCV: This code uses the OpenCV library for face detection. You can install OpenCV using pip, the package installer for Python. 
   Open a terminal or command prompt and type the following command:
   pip install opencv-python
   
   
   
Readme:

the code loads the Haar cascade classifier for face detection by reading the "haarcascade_frontalface_default.xml" file from the OpenCV data directory. The classifier is used to detect faces in the video stream.

The code then initializes a camera object using cv2.VideoCapture(). If you want to use a video file instead of a camera, you can specify the file name in the function call.

The while loop continuously reads frames from the camera using the read() function. For each frame, the code converts it to grayscale using cv2.cvtColor(). This is necessary because the face detection algorithm works better on grayscale images.

The detectMultiScale() function of the cascade classifier is then used to detect faces in the grayscale image. The function returns a list of rectangular regions in which faces are detected. The scaleFactor, minNeighbors, and minSize parameters control the sensitivity of the face detection algorithm. Adjusting these parameters can improve the accuracy of the algorithm in different situations.

Finally, the code draws rectangles around the detected faces using cv2.rectangle(). The resulting frame with rectangles is displayed using cv2.imshow(). The cv2.waitKey() function waits for a key event, and if the user presses the 'q' key, the loop is terminated.

Once the loop is terminated, the camera object is released and all windows are closed using cv2.destroyAllWindows().
