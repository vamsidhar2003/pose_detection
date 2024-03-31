# pose_detection
This Python script uses the MediaPipe library to perform real-time pose detection from a webcam or video feed using OpenCV (`cv2`). Here's a breakdown of the code:

1. **Importing Libraries**:
   - `cv2`: OpenCV library for computer vision tasks.
   - `mediapipe`: MediaPipe library for pose estimation.

2. **Initializing MediaPipe Pose Model**:
   - Creates a MediaPipe Pose model instance (`mp_pose.Pose`) with specified confidence thresholds for detection and tracking.

3. **Accessing Webcam or Video Feed**:
   - Initializes a video capture object from the default webcam (index 0). You can change the index or specify a video file path.

4. **Main Loop for Real-time Pose Detection**:
   - Captures frames from the video stream in a loop until the user presses 'q' to quit.
   - Converts each frame from BGR to RGB format (required by MediaPipe).
   - Processes each RGB frame using the MediaPipe Pose model to detect pose landmarks.
   - Draws pose landmarks on the frame using `mp_drawing.draw_landmarks`.
   - Displays the annotated frame with pose landmarks in a window named 'Pose Detection'.

5. **Exiting the Program**:
   - Pressing the 'q' key closes the program and releases the video capture resources.

To run this script:
1. Install OpenCV (`cv2`) and MediaPipe (`mediapipe`) if you haven't already.
2. Ensure your webcam is connected and accessible.
3. Run the script, and it will open a window showing real-time pose detection from the webcam or video source.
4. Press the 'q' key to exit the program.

You can customize the code further to perform additional actions based on the detected pose landmarks or to save annotated frames to disk, depending on your application requirements.
