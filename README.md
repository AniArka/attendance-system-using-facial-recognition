# Face Recognition Attendance System

This Python script uses the face_recognition library to perform real-time face recognition and attendance marking. The script captures faces through a webcam, compares them with pre-trained images in the 'trainData' directory, and marks attendance in a CSV file.

## Prerequisites

- Python 3.x
- OpenCV (`pip install opencv-python`)
- NumPy (`pip install numpy`)
- dlib (`pip install dlib`)
- face_recognition (`pip install face_recognition`)

## Usage

1. Clone the repository:

    ```bash
    git clone <https://github.com/AniArka/attendance-system-using-facial-recognition.git>
    cd <repository-directory>
    ```

2. Organize your training images:

    - Create a directory named `trainData`.
    - Add individual directories for each person inside `trainData`, with images of that person.

3. Run the script:

    ```bash
    python face_recognition_attendance.py
    ```

4. The webcam will open, and the script will start recognizing faces.

## How it works

1. The script reads the training images from the 'trainData' directory and encodes the faces using the face_recognition library.
2. It initializes the webcam and continuously captures frames.
3. For each frame, it detects faces and compares them with the pre-trained encodings.
4. If a match is found, it marks attendance in the 'attendance.csv' file with the current time.
5. The recognized face is highlighted in the webcam feed with a bounding box and corresponding name.

## Keyboard Shortcuts

- Press 'q' to exit the webcam feed.

## Notes

- The script uses the HoG (Histogram of Oriented Gradients) model for face detection.
- Adjust the `tolerance` parameter in the `compare_faces` function for more or less strict face matching.
- Make sure to have proper lighting conditions for accurate face recognition.

## Acknowledgments

- The script utilizes the face_recognition library, which is built on top of dlib and OpenCV.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to customize the script based on your needs and contribute to its improvement!
