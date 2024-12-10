# Face Recognition Attendance Management System

This project provides an **Attendance Management System** based on **Face Recognition** using **Python** and **OpenCV**. It allows users to record attendance via facial recognition or manually, with the ability to store the data in a CSV file or a MySQL database. The system has been specifically **tuned for Mac** users to ensure smooth operation.

### Requirements

To run this project, you need the following libraries:

- **OpenCV**: `pip install opencv-python`
- **Tkinter**: (Already available in Python)
- **Pillow**: `pip install Pillow`
- **Pandas**: `pip install pandas`
- **MySQL**: You will need a **MySQL database** for storing attendance records. 

### Steps to Run the Project

1. **Clone the Repository**:  
   Download or clone this repository to your local machine.

2. **Create Required Folders**:  
   - Create a folder named `TrainingImage` in your project directory. This folder will store the images captured for training the face recognition model.
   - Create another folder named `TrainingImageLabel` to save the trained model.

3. **Configure Paths**:  
   - Open the `AMS_Run.py` file.
   - Change all paths in the code to match your system's paths (e.g., the path to `TrainingImage` and `TrainingImageLabel`).

4. **Database Setup**:  
   - Install MySQL.
   - Open **phpMyAdmin** and create the following databases:
     - `manually_fill_attendance` (for storing manual attendance data).
     - `Face_reco_fill` (for storing automatic attendance data).
   - Update the `AMS_Run.py` script with the correct database names.

### Project Structure
Face-Recognition-Attendance-Management-System/
│
├── AMS_Run.py                  # Main script to run the attendance system
├── TrainingImage/               # Folder to store captured images for training
├── TrainingImageLabel/          # Folder to save the trained model
├── Attendance/                  # Folder to store attendance CSV files
│   └── Manually Attendance/     # Folder for manually entered attendance
├── StudentDetails.csv           # CSV file for storing student details (ID, Name)
└── README.md                    # This file

### Database Setup

If you want to store attendance in MySQL, follow these steps to set up your databases:

1. Open **phpMyAdmin** (or use any other MySQL client).
2. Create two databases:
   - `manually_fill_attendance`
   - `Face_reco_fill`
3. Create a table in each of the databases with the following structure:

```sql
CREATE TABLE attendance (
    ID INT NOT NULL AUTO_INCREMENT,
    ENROLLMENT VARCHAR(100) NOT NULL,
    NAME VARCHAR(50) NOT NULL,
    DATE VARCHAR(20) NOT NULL,
    TIME VARCHAR(20) NOT NULL,
    PRIMARY KEY (ID)
);

Update your connection settings in AMS_Run.py to match the correct database names.

Notes
This project requires high processing power (8GB RAM recommended).
The quality of the images used for training is important; poor-quality images may reduce the accuracy of the face recognition system.

##License
This project is licensed under the MIT License.


