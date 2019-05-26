# Face-recognition-from-real-time-video
Its simple code to detect the face from the real time video.#college_project#face_detection#real-time-video

cv2 is the library of programming function mainly aimed at real time computer vision.
CascadeClassifier class to datect objects in video stream.
Here in above code we have used haarcascade_frontalface_default to detect faces from the video.
Haarcascade is machine learning detection algorithm used to identify objects in an image or video and based on the concept of features.
It is a machine learning based approach where a cascade function is trained from a lot of positive and negative images. It has been used to detect objects in other images.
Algorithmn has four stages:-

*)Haar feature selection

*)creating intrgra images

*)adaboost training

*)cascading classifiers

Then we are entering in infinite while loop in which video_capture.read() captures the first frame and retval is the boolean return type variable. We first capture the frame then we change the color of that fram to pass that as parameter in face_cascade.detectMultiScale() function. Its parameter are input grey image , scalefactor, min neighbours and minsize.

This line uses face_cascade object for detectMultiScale()method which is a general function to detect objects, in this case, it'll detect faces since we called in the face cascade. 
If it finds a face, it returns a list of positions of said face in the form “Rect(x,y,w,h).”, if not, then returns “None”.
image:- the grayscale image
ScaleFactor:- This function compensates a false perception in size that occurs when one face appears to be bigger than the other simply because it is closer to the camera.
minNeighbors:-This is a detection algorithm that uses a moving window to detect objects, 
it does so by defining how many objects are found near the current one before it can declare the face found.

for x,y,w,h in faces:

    img=cv2.rectangle(img,(x,y),(x+w,y+h),(0,255,0),3)

loop over the list of faces (rectangles) it returned and drew those rectangles using yet another built-in OpenCV rectangle function on our original colored image to see if it found the right faces. Then we display this frame with the detected face. As this is in while loop it will capture next image and do this process again. Till we press "q"
button to close the camera and release all the resourses.
