<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video Surveillance Processing for Shopping Mall and Retail Analysis</title>
</head>
<body>

<h1>Video Surveillance Processing for Shopping Mall and Retail Analysis</h1>

<p>This repository provides solutions for six different video processing tasks aimed at analyzing and managing retail and shopping mall environments. Each task is implemented in <strong>Python</strong> using <strong>OpenCV</strong>, focusing on detecting, tracking, and analyzing objects or people in various scenarios like tracking dwell times, detecting peak shopping periods, and counting people entering/exiting a store.</p>

<h2>Requirements</h2>
<p>To run the code, ensure you have the following packages installed:</p>
<ul>
    <li><strong>Python 3.7+</strong></li>
    <li><strong>OpenCV</strong></li>
    <li><strong>Matplotlib</strong> (for plotting peak shopping durations)</li>
    <li><strong>Numpy</strong></li>
</ul>
<p>Install the requirements with:</p>
<pre><code>pip install opencv-python-headless numpy matplotlib</code></pre>

<hr>

<h2>Task 1: Tagging and Tracking a Person Based on Appearance</h2>

<h3>Objective</h3>
<p>Tag and track a person across frames in a video based on appearance using traditional image processing techniques.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Video</strong>: Load the video file using OpenCV.</li>
    <li><strong>Person Detection</strong>: Use <strong>background subtraction</strong> or <strong>frame differencing</strong> to detect moving people in the video. Extract features like <strong>color histograms</strong> and <strong>edge features</strong> to identify the target person.</li>
    <li><strong>Person Tracking</strong>: Use a tracking algorithm (e.g., <strong>centroid-based tracking</strong> or <strong>optical flow</strong>) to maintain the identity of the person as they move through frames.</li>
    <li><strong>Tagging Output</strong>: Display the video with a <strong>bounding box</strong> around the identified person.</li>
</ol>

<hr>

<h2>Task 2: Strategic Marketing – Peak Shopping Duration</h2>

<h3>Objective</h3>
<p>Identify <strong>peak shopping durations</strong> by analyzing when the most people are present in the shopping area.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Video</strong>: Load the surveillance video using OpenCV.</li>
    <li><strong>People Detection</strong>: Detect motion and identify people entering the frame using <strong>frame differencing</strong> or <strong>optical flow</strong>.</li>
    <li><strong>Peak Duration Identification</strong>: Count the number of people in each frame and compute the total count for time intervals (e.g., 10-minute blocks). <strong>Plot people count</strong> over time and identify peak intervals.</li>
</ol>

<h3>Result</h3>
<p>Provides a graph displaying <strong>peak shopping times</strong> and outputs frames from these periods.</p>

<hr>

<h2>Task 3: Facial Recognition to Check Fraud Cases</h2>

<h3>Objective</h3>
<p>Identify a suspect by comparing <strong>facial features</strong> in a video to a reference image using traditional facial recognition techniques.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Images and Video</strong>: Load a reference image of the suspect and the video to be analyzed.</li>
    <li><strong>Face Detection</strong>: Use <strong>Haar Cascades</strong> to detect faces in the reference image and the video.</li>
    <li><strong>Feature Matching</strong>: Extract facial features (e.g., <strong>edge detection</strong> or <strong>geometric facial features</strong> like eye spacing) and compare the detected faces to the reference.</li>
    <li><strong>Result</strong>: Highlight the frames where a <strong>match is detected</strong>.</li>
</ol>

<hr>

<h2>Task 4: Counting People Entering and Exiting the Shop</h2>

<h3>Objective</h3>
<p>Count the number of people <strong>entering and exiting</strong> a shop using motion detection techniques.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Video</strong>: Load the surveillance video of the shop entrance.</li>
    <li><strong>Motion Detection</strong>: Detect people moving in and out of the shop entrance using <strong>frame differencing</strong> or <strong>optical flow</strong>.</li>
    <li><strong>Counting People</strong>: Define a region near the entrance and track the <strong>direction of motion</strong> to determine whether a person enters or exits.</li>
    <li><strong>Result</strong>: Display the total counts of <strong>entries and exits</strong>.</li>
</ol>

<hr>

<h2>Task 5: Dwelling Time in a Shopping Mall</h2>

<h3>Objective</h3>
<p>Measure how long a person or object remains in a <strong>specified area of the mall</strong>.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Video</strong>: Load the mall surveillance video using OpenCV.</li>
    <li><strong>Object/Person Detection</strong>: Detect objects/people using <strong>background subtraction</strong> or <strong>motion detection</strong> and track them within the specified region.</li>
    <li><strong>Dwelling Time Calculation</strong>: Track the time each detected object/person spends in the <strong>region of interest (ROI)</strong>.</li>
    <li><strong>Result</strong>: Display the total dwelling time for each person/object detected in the ROI.</li>
</ol>

<hr>

<h2>Task 6: Spotting and Counting a Branded Car in a Video</h2>

<h3>Objective</h3>
<p>Identify and count the number of branded cars (e.g., a specific logo or color) in a video sequence using feature-based matching.</p>

<h3>Methodology</h3>
<ol>
    <li><strong>Load Video</strong>: Load the provided video showing vehicles.</li>
    <li><strong>Car Detection</strong>: Use <strong>background subtraction</strong> or <strong>motion detection</strong> to detect moving cars in the video.</li>
    <li><strong>Feature Matching</strong>: Use <strong>color-based detection</strong> or <strong>template matching</strong> to identify the specific branded car (e.g., a car with a specific color or logo).</li>
    <li><strong>Counting</strong>: Count the number of times the branded car appears in the video.</li>
</ol>

<h3>Result</h3>
<p>Output the total count and display the frames where the branded car is detected.</p>

</body>
</html>

