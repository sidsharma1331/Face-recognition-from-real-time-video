# Face-recognition-from-real-time-video
Its simple code to detect the face from the real time video.#college_project#face_detection#real-time-video
import cv2
import sys
face_cascade = cv2.CascadeClassifier('C:\\Users\\Siddhant Sharma\\Downloads\\opencv\\build\\etc\\haarcascades\\haarcascade_frontalface_default.xml')
video_capture=cv2.VideoCapture(0)
while True:
    retval,frame = video_capture.read()
    gray=cv2.cvtColor(frame,cv2.COLOR_BGR2GRAY)
    faces=face_cascade.detectMultiScale(gray,scaleFactor=1.05,minNeighbors=5,minSize=(35,35))
    for x,y,w,h in faces:
        cv2.rectangle(frame,(x,y),(x+w,y+h),(0,255,0),2)
    cv2.imshow("video",frame)
    if cv2.waitKey(1)&0xff==ord('q'):
        sys.exit()
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



