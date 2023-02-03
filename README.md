#Face Detection and Verification API

##Introduction
This API allows users to perform face detection and verification. The API uses deep face and mediapipe libraries to detect and recognize faces. The API also supports liveness tests to prevent fraud.
Technologies
FastAPI
deep face
mediapipe
Pymongo
cv2

Features
Face detection and verification
Liveness tests (emotion and hand gestures)
MongoDB database support for storing session data

Usage
Run the API using uvicorn main: app --reload command
Make a post request to /verify the endpoint with two images (input and target) and session id as form data.
The API will return the verification result as "Similar" or "Missmatch".
The API also performs a liveness test and returns the result as "Liveness test Passed" or "Liveness test Failed".
MongoDB
The API uses MongoDB to store session data. The database name is GoodWorklabs and the collection name is Face_Recognition_&_Liveness. The session data consists of session id, liveness test result, and verification result.

Limitations
The API only supports images in jpg, png, or jpeg format.
The API only supports single-face detection. The API returns an error message if multiple faces are detected or no face is detected.
The API only supports specific hand gestures and emotions for liveness tests.


Run the file
Inputs  for verification
“Session_id” is a unique identity for each user  in text or number 
two Images of the user
The first image is stored in the storage for verification
The second is for comparing with the first image
Inputs liveness test
“Gesture”  to be informed of  (any one of them)
“Both_hands” text to be provided to identify both hands 
“Left” to  text to be provided to identify left hand 
“Right” to  text to be provided to identify right hand
“Happy” to  text to be provided to identify smile on the face 
“Session_id” as a unique identity for each user  in(text or number)
Image for the verification 
  

