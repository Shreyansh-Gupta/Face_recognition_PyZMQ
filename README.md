# Face_recognition_PyZMQ
Real time Face Recognition between server and client using PyZMQ.

## Brief about PyZMQ
PyZMQ is a python version of ZeroMQ which again is a library which is used to set up messaging and communication between applications and processes quick and asynchronously.
Although there are other methods available for file transfer in client server models ZMQ one of the greatest advantage of ZMQ is that it can be used for message queuing without a message borker.

If you wish to learn more about ZMQ and client server architechture ,then you can refer [here](https://github.com/Learn-Write-Repeat/Open-contributions/blob/master/Akshay_Python_PyZMQ.md).

## About the model.
First of all, my model is trained on a custom data made by me by images feeded in a folder named [train](https://github.com/Shreyansh-Gupta/Face_recognition_PyZMQ/tree/main/train). So clearly the only subject here was me. My model includes some functions
* Detecting face.
* Preparing and training images.
* Drawing rectangles, and labelling them.
* For final prediction on each frame.

which process the images coming from client's side in real time. For more reference, check out this [page](https://datascienceplus.com/face-recognition-with-opencv/).

## Workflow of Program
#### Libraries Needed - Cv2, dlib, zmq, numpy

* At first connections will be stablised by opening sockets from client side and binding it to server end and connect them using ip.
* Now client's camera will be on and it'll start sending the frames by converting it to buffer form.
* At server side as the buffer is recived it is reconstructed into frame using numpy.
* Now server performs all the detections and draws the boxes using dlib and cv2 and send back the frame to client using same buffer.
* Again the client reconstructs frame from buffer and then displays it.

## Result
The code was being runned on local host between two terminals one for **Server** *([Code is here](https://github.com/Shreyansh-Gupta/Face_recognition_PyZMQ/blob/main/Server%20Face%20Detection.ipynb))* and one for **Client** *([Code is here](https://github.com/Shreyansh-Gupta/Face_recognition_PyZMQ/blob/main/Client%20Face%20Detection.ipynb))*

Output:

My App detected my face and identified it as me by labelling it.


![Prediction](https://github.com/Shreyansh-Gupta/Face_recognition_PyZMQ/blob/main/Prediction.png)

For any query contact me through [Git](https://github.com/Shreyansh-Gupta) or [Mail](nvshreyanshgupta@gmail.com)
