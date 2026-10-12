# Student Autotester

## Description

Student Autotester is a desktop application that allows students to test their knowledge using multiple-choice questions. Users can select a subject, choose the number of questions, optionally set a timer, and complete a test through a simple graphical interface.

After finishing a test, users can view their score, percentage, and correct answers.

The application loads questions from JSON files, making it easy to add new subjects and question banks without modifying the executable.

## Setup and Usage

### 1. Setup

1. Download or extract the Student Autotester files.
2. Make sure the application executable (`Main.exe`) and the `questions` folder are in the same directory.
3. Ensure the `questions` folder contains the JSON files for the tests you want to take.

**You do not need to install Python to run the compiled executable.**

### 2. Launch the Application

Double-click `Main.exe` to open Student Autotester.

### 3. Start a Test

1. Select a subject from the test menu.
2. Choose the number of questions.
3. Optionally enable the countdown timer and set its duration.
4. Click **Start Test**.
5. Select your answers and navigate between questions using the navigation buttons.
6. Click **Finish Test** to submit your answers.

### 4. View Your Results

After submitting your test, you can view your score, percentage, and answer breakdown.

Click **Check Answers** to review your responses and see the correct answers.

Click **Make a New Test** to return to the main menu.

### 5. Adding More Tests

To add another subject:

1. Open the `questions` folder.
2. Add a new `.json` question file using the same format as the existing test files.
3. Reopen the application or click **Refresh Tests** if the application is already running.

Keep the executable and the `questions` folder together so the application can find your question files.
