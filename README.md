# video-trimming
This Python code loops through all the video files in an input folder and trims the first 5 seconds of each video. It then saves the trimmed videos to an output folder using the same video format as the input videos
The code first uses the os module to list all files in the input folder and filters out files that do not end with the .mp4 extension (or any other video file format). It then sets the input and output video paths using the os.path.join() method.

Next, the code loads the input video file using OpenCV's cv2.VideoCapture() method and extracts its properties, such as the frames per second and total number of frames, using the video capture object's get() method. It also sets the starting and ending frame numbers to trim the first 5 seconds of the video.

The code creates a VideoWriter object to save the output video file with the same format as the input video using the cv2.VideoWriter() method. It then sets the starting frame using the video capture object's set() method and loops through the frames from the starting frame to the ending frame, reading each frame using the video capture object's read() method and writing it to the output video using the VideoWriter object's write() method.
