[Project Webpage Link](https://bhadra24.github.io/)

# Restaurant-Based Chatbot And Text Summarization Using Dialog Flow 
<div align="center">
    <a><img width="720" src="images/title_3.png" alt="soft"></a>
</div>

## Table of Contents

- [Restaurant-Based Chatbot And Text Summarization Using Dialog Flow](#Restaurant-Based-Chatbot-And-Text-Summarization-Using-Dialog-Flow)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
      - [Project Description](#project-description)
      - [Website](#website-screenshots)
  - [Dataset Preparation ](#dataset-preparation)
      - [Raw Images](#raw-images-data-collection)
      - [Processed Images ](#processed-images)
  - [Method](#method)
      - [RetinaFace](#retinaface)
      - [Face Recognition](#face-recognition)
  - [Implementation](#implementation)
  - [Results](#results)
  - [Technical Information](#technical-information)
  - [Benefits](#benefits)
  - [Applications](#applications)
  - [Citations](#citations)
   
## Introduction

### Project Description

This project introduces a Restaurant Bot a proof-of-concept powered by Dialog Flow. With advanced natural language processing capabilities, it allows users to effortlessly place food orders, track their status, assist customers by answering FAQs, and table reservations, provide menu details, and accommodate special requests. Our project aim is divided into two parts
- **Part 1:** Create a restaurant bot using Dialog Flow.
- **Part 2:** Generates Text Summarization from the bot and user which is further used to do the sentiment analysis of the user so that it will help the owner to enhance customer satisfaction and drive business growth.

### Website Screenshots

<figure align="center"> 
  <img src="images/AddCourse.png" alt="drawing" height="400"/>
  <figcaption>Screen to Facilitate Course Addition</figcaption>
</figure>

<figure align="center"> 
  <img src="images/CaptureAttendance.jpg" alt="drawing" height="400"/>
  <figcaption>Screen to Capture Course Attendance</figcaption>
</figure>

<figure align="center"> 
  <img src="images/RecordAttendance.jpg" alt="drawing" height="400"/>
  <figcaption>Screen to Modify, Save or Download Attendance CSV.</figcaption>
</figure>


## Dataset Preparation:
**1. Teaching the Chatbot Our Language:** We define user goals (intents) like "View Menu" and provide examples of how users might ask for them. The variety and quality of these examples directly impact the chatbot's understanding.
**2. Extracting Key Details:** We identify important information users might provide (entities) like "number of guests" or "reservation time." Defining entities helps the chatbot pinpoint these details within user queries.
**3. Connecting the Chatbot to the Back-End (Fulfillment):** For dynamic responses or actions (e.g., checking availability), we'll use APIs (built with FASTAPI) to connect the chatbot to our systems, allowing it to retrieve information or complete tasks based on user interactions

### Raw Images:
<figure align="center"> 
  <img src="images/training112.png" alt="drawing" height="400"/>
  <figcaption>Raw Images of Dimension 112x112</figcaption>
</figure>

### Processed Images:
<figure align="center"> 
  <img src="images/training50.png" alt="drawing" height="400"/>
  <figcaption>Processed Images Ready for Embeddings 50x50</figcaption>
</figure>

## Method:

### RetinaFace:

RetinaFace is a robust single-stage face detector that performs pixel-wise face localization on various scales of faces by taking advantage of joint extra-supervised and self-supervised multi-task learning.

### Detected Faces:
<figure align="center"> 
  <img src="images/15_Detection.jpg" alt="drawing" height="720"/>
  <figcaption>RetinaFace detection output on Classroom Image</figcaption>
</figure>


### Face Recognition:
Face Recognition is a Python library that can be used to recognize and manipulate faces. It is built on top of Dlib modern C++ toolkit that contains machine-learning algorithms and tools for creating complex software in C++ to solve real-world problems. As a part of facial recognition, after the facial images have been extracted, cropped, resized, and often converted to grayscale, the face recognition algorithm takes on the task of identifying features that most accurately represent the image.

### Recognized Faces:
<figure align="center"> 
  <img src="images/15_predicted.jpg" alt="drawing" height="720"/>
  <figcaption>Face Recognition on group image</figcaption>
</figure>

## Implementation:

**1. Train Image Data Collection:**
- Go to the folder 'Student Image Data Collection' and download the 'Dataset_Collecting Images.py' and 'haarcascade_frontalface_default.xml'.
- Create a folder 'Face_Recognition_Images' on your desktop and copy/paste the Python script and haarcascade.xml into the folder. 
- Run the code.
   ```
   Dataset_Collecting Images.py
   ```
python Dataset_Collecting Images.py 
  
**2. Test Image Data Collection:**
- You can collect the Group test images from your mobile preferably Apple iPhone or from good-resolution smartphones.

**3. Generate Embeddings:**
- Download the 'Generate Embeddings.py' file to generate the embedding of the known faces.
- It will create an embedding file that can be used as ground truth embedding for recognition.
   ```
   Generate Embeddings.py
   ```

**4. Face Recognition:**
- Go to our website homepage and select/add the course as per your University courses and Upload the class_list.csv (Sample can be found in the Demo folder).
- Select the date for which attendance should be taken and press the button 'Take Attendance'.
- Now choose the Group Image for which the attendance is to be taken and upload the file and press the button 'Take Attendance'. 
- After which you see the recognized faces on the image along with the attendance displayed which can be manually edited and downloaded into a CSV file.

## Results:


## Demo:
https://github.com/YoushanZhang/AiAI/assets/62828547/ca918506-9f5e-435f-9b19-e51496da88b8


## Technical Information:

- **Programming Language**: Python.
- **Cloud Service**: Google Dialog Flow.
- **Website scripting languages**: HTML , CSS, Javascript.
- **API framework**: Fast API.
- **Coding Environment**: VS Code.
- **Database**: Mysql for restaurant data, MongoDB for Chat data.


## Benefits:

- **Empowered Customers**: Chatbots can answer questions, generate reports, and offer personalized recommendations based on customer needs.
- **Data-Driven Insights**: Summarized reports on customer interactions to identify product demand and common pain points.
- **Enhanced Convenience**: Provides a faster and more user-friendly approach for everyone.

## Applications:

- **Sales Projections**: Utilize a chatbot to assess sales projections for the upcoming quarter, compare them against the budget, and pinpoint areas for improvement.
- **Summarized Reports**: Summarized reports reveal frequently asked questions, highlighting areas for product development or improved communication.
- **Customer Sentiments**: Sentiment analysis combined with slow resolution times can indicate frustrated customers, prompting a focus on faster issue resolution.

## Citations:
1. [RetinaFace](https://arxiv.org/abs/1905.00641)
2. [Title Image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.timedynamo.com%2Fblog%2Fface-recognition-attendance-system&psig=AOvVaw2FkF7iZtn_xnR0WqiLOgx8&ust=1713675455940000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCMjdmdmA0IUDFQAAAAAdAAAAABAS)

