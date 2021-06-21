# Emotion-Music-Recommendation
Recommending music based on your facial expressions using FER 2013 dataset and Sporify api

# Project Description:
The a emotion recognition model is trained on FER 2013 dataset. It can detect 7 emotions. The project works by getting live video feed from web cam, pass it through the model to get a prediction of emotion. Then according to the emotion predicted, the app will fetch playlist of songs from Spotify through spotipy wrapper and recommend the songs by displaying them on the screen.

# Tech Stack:
- Keras
- Tensorflow
- Spotipy
- Tkinter
- Flask

# Current condition:
The gui is made with tkinter. Initialised seperate thread for webcam detection leading to better FPS during live detection. Music recommendation doesn't work properly as of yet.

Tkinter gui is only for prototyping, something made to test the app. Final version of app will NOT be in Tkinter. Rather it will be made with FLASK as served as web app. 

Update: Added flask web app. Needs Styling

# Project Components:
- Spotipy is a module for establishing connection to and getting tracks from Spotify using Spotipy wrapper
- haarcascade is for face detection
- app_csv is the version of app which displays songs which are already fetched and stored in csv format in 'songs' directory
- app is the version which fetches and displays songs on the go at the moment of prediction without storing it and hence is dynamic

# Running the app:
Clone the project:
1. Tkinter:
- Install all libraries required (Keras, OpenCv, PIL, Numpy, Pandas, Pandastable, Soptipy)
- In Spotipy.py enter your credentials generated by your Spotify Developer account in auth_manager
- Switch on web cam and run app.py or app_csv.py

2. Flask: 
- Install all libraries required (Keras, OpenCv, PIL, Numpy, Pandas, Pandastable, Soptipy)
- In Spotipy.py enter your credentials generated by your Spotify Developer account in auth_manager
- run "python main.py" and give camera permission if asked.

Note: Model accuracy is not that great. It is ~66%. Further training and finetuning required. May try Vision Transformer Model.