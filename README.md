# Video Trimming Script

This Python script trims the first 5 seconds of each video file in a specified input folder and saves the trimmed videos to a designated output folder. The script uses OpenCV for video processing.

## Input and Output Folders

- `input_folder`: The path to the folder containing the original video files.
- `output_folder`: The path to the folder where trimmed videos will be saved.

## Code Overview

1. **Folder Setup:**
   - Set the paths for the input and output folders (`input_folder` and `output_folder`).
   - Create the output folder if it doesn't exist.

2. **Video Trimming:**
   - Loop through all video files in the input folder.
   - For each video file with the '.mp4' extension:
     - Open the input video file using OpenCV (`cv2.VideoCapture`).
     - Get video properties such as frames per second (fps) and total frame count.
     - Set the starting and ending frame numbers for trimming (trim the first 5 seconds).
     - Create a VideoWriter object to save the trimmed video file.
     - Loop through the frames between the starting and ending frames, writing them to the output video file.
     - Release the input and output video objects.

3. **Execution:**
   - Replace 'videos' with the path to the actual directory containing the original video files.
   - Replace 'trimmed_videos' with the path to the desired output directory.
   - Execute the script to trim the first 5 seconds of each video and save the trimmed videos in the output folder.

## Note
- The script assumes that the input videos are in the '.mp4' format. You can modify the condition `if filename.endswith('.mp4')` to match the format of your input videos.

