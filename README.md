Video Surveillance Processing for Shopping Mall and Retail Analysis
This repository provides solutions for six different video processing tasks for shopping mall and retail analysis using Python and OpenCV. Each task focuses on detecting, tracking, and analyzing objects or people in various scenarios, such as tracking dwell times, detecting peak shopping periods, and counting people entering/exiting a store.

Requirements
Python 3.7+
OpenCV
Matplotlib (for plotting peak shopping durations)
Numpy
Install requirements with:

bash
Copy code
pip install opencv-python-headless numpy matplotlib
Task 1: Tagging and Tracking a Person Based on Appearance
Objective
Tag and track a person across frames in a video based on appearance using traditional image processing techniques.

Methodology
Load Video: Load the video file using OpenCV.
Person Detection: Use background subtraction or frame differencing to detect moving people in the video. Extract features like color histograms and edge features to identify the target person.
Person Tracking: Use a tracking algorithm (e.g., centroid-based tracking or optical flow) to maintain the identity of the person as they move through frames.
Tagging Output: Display the video with a bounding box around the identified person.
Task 2: Strategic Marketing – Peak Shopping Duration
Objective
Identify peak shopping durations by analyzing when the most people are present in the shopping area.

Methodology
Load Video: Load the surveillance video using OpenCV.
People Detection: Detect motion and identify people entering the frame using frame differencing or optical flow.
Peak Duration Identification: Count the number of people in each frame and compute the total count for time intervals (e.g., 10-minute blocks). Plot people count over time and identify peak intervals.
Result
Provides a graph displaying peak shopping times and outputs frames from these periods.

Task 3: Facial Recognition to Check Fraud Cases
Objective
Identify a suspect by comparing facial features in a video to a reference image using traditional facial recognition techniques.

Methodology
Load Images and Video: Load a reference image of the suspect and the video to be analyzed.
Face Detection: Use Haar Cascades to detect faces in the reference image and the video.
Feature Matching: Extract facial features (e.g., edge detection or geometric facial features like eye spacing) and compare the detected faces to the reference.
Result: Highlight the frames where a match is detected.
Task 4: Counting People Entering and Exiting the Shop
Objective
Count the number of people entering and exiting a shop using motion detection techniques.

Methodology
Load Video: Load the surveillance video of the shop entrance.
Motion Detection: Detect people moving in and out of the shop entrance using frame differencing or optical flow.
Counting People: Define a region near the entrance and track the direction of motion to determine whether a person enters or exits.
Result: Display the total counts of entries and exits.
Task 5: Dwelling Time in a Shopping Mall
Objective
Measure how long a person or object remains in a specified area of the mall.

Methodology
Load Video: Load the mall surveillance video using OpenCV.
Object/Person Detection: Detect objects/people using background subtraction or motion detection.
Dwelling Time Calculation: Define an ROI representing a specific area of the mall, and track how long each detected object spends in that area.
Result: Display the total dwelling time for each object detected in the ROI.
Task 6: Spotting and Counting a Branded Car in a Video
Objective
Identify and count occurrences of a specific branded car based on color or logo.

Methodology
Load Video: Load the video showing vehicles.
Car Detection: Detect moving cars using background subtraction or motion detection.
Feature Matching: Use color-based detection or template matching to identify the branded car.
Counting: Track and count the occurrences of the branded car in the video frames.
Running the Code
Each task can be run individually with its specific script (e.g., task1_person_tracking.py, task2_peak_duration.py, etc.). Ensure each file is configured with the correct paths to video files and any necessary reference images.

For example, to run Task 1:

bash
Copy code
python task1_person_tracking.py
Results
Each task outputs processed video frames with annotations and summary results:

Bounding boxes or tags for tracked persons.
Summary plots (Task 2) and dwell times (Task 5).
Total count of people (Task 4) and branded cars (Task 6).
Contributing
Feel free to submit issues, fork the repository, and make pull requests to add additional functionality or optimize existing code.

License
This project is licensed under the MIT License. See the LICENSE file for more details.
