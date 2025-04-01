# AI-Based Attendance System

An AI-powered attendance system built using facial recognition technology. This system detects faces in a classroom image, matches them against a pre-stored database of student faces, and automatically marks attendance for each student.

## Project Overview

The AI-based Attendance System uses deep learning to identify students based on their face embeddings. The system ensures accuracy by matching face embeddings captured during class with pre-stored embeddings in the database. The system also verifies image authenticity using metadata (capture time and GPS coordinates).

### Key Features:
- **Facial Recognition**: Detect and recognize faces in classroom images using FaceNet for 128-dimensional embeddings.
- **Attendance Marking**: Automatically mark attendance based on recognized faces.
- **Metadata Extraction**: Capture image metadata (time and location) to verify the authenticity of uploaded images and prevent fraud.
- **Web Interface**: Faculty or class representative (CR) can upload classroom images through a web interface for easy attendance tracking.
- **Dashboard**: Administrators can review attendance records and manually manage faculty and class representative accounts.

## Technologies Used

- **Frontend**: React, Tailwind CSS, Vite
- **Backend**: Node.js, Express
- **Machine Learning**: FaceNet (for facial recognition)
- **Database**: MongoDB (for storing attendance and user data)
- **Face Recognition Library**: TensorFlow (or Keras), OpenCV
- **Image Metadata**: EXIF for capturing image time and GPS location

## Setup Instructions

### Prerequisites

1. Node.js (v16+)
2. Python (for training models and running the facial recognition system)
3. MongoDB (local or hosted)
4. Git

### Clone the repository

```bash
git clone https://github.com/yourusername/Attendance_System.git
cd Attendance_System
```

### Install Backend Dependencies
Navigate to the backend directory and install the required packages:

```bash
cd backend
npm install
```

### Install frontend Dependencies
Navigate to the frontend directory and install the required packages:

```bash
cd frontend
npm install
```

### Run the Project
To start the backend server:

```bash
cd backend
npm run dev
```
To start the frontend development server:

```bash
cd frontend
npm run dev
```

### Train the Model
1.Use the provided dataset of cropped face images to train the facial recognition model.
2.The model uses FaceNet for embedding extraction. After training, save the embeddings in .csv and .npy formats.

### Upload Images for Attendance
1.Faculty or CR can upload the classroom image through the web interface.

2.The system will detect faces, match them with stored embeddings, and mark attendance automatically.

3.Metadata from the image is used to verify its authenticity (capture time and GPS location).

### How the Attendance System Works
Image Upload: Faculty or CR uploads a classroom image via the web interface.

Face Detection & Recognition: The system detects faces, matches them with the stored face embeddings in the database.

Attendance: Based on recognized faces, the system marks attendance in the database.

Image Verification: The system checks image metadata to ensure it is authentic and prevents fraud.

Admin Dashboard: Administrators can review attendance data, manually add faculty/CR users, and manage records.


### Contribution
Feel free to fork this repository and contribute. Please follow the standard Git workflow for contributions.

Fork the repository.

Create a new branch for your feature.

Push your changes and create a pull request.
