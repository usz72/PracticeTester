# Student Autotester

## 1. Overview

Student Autotester is a Python desktop application that allows students to test their knowledge using multiple-choice questions.

The application uses a graphical user interface (GUI) built with Tkinter. Questions are loaded from JSON files, allowing users to create tests for different subjects.

AI question generation is planned as a future feature and has not yet been implemented.

## 2. Features

* Select tests from different subjects.
* Choose how many questions to answer.
* Randomize the order of questions.
* Answer multiple-choice questions with four options.
* Navigate between questions using Previous and Next buttons.
* Jump directly to a question using the numbered navigation panel.
* See which questions have been answered.
* Enable an optional countdown timer.
* Automatically submit the test when the timer expires.
* Calculate the final score and percentage.
* View the number of correct, incorrect, and unanswered questions.
* Review submitted answers and compare them with the correct answers.
* Start another test without restarting the application.
* Load additional tests by adding JSON files.
* Use fullscreen mode during a test.

## 3. Requirements

* Python 3.10 or later is recommended.
* Tkinter, which is included with most standard Python installations.
* No external Python packages are required for the core application.

If Tkinter is missing from your Python installation, you may need to install the appropriate system package.

## 4. Project Structure

The project should have the following folder structure:

StudentAutotester/
|
|-- Main.py
|
|-- questions/
|   |-- Biology.json
|   |-- Mathematics.json
|   |-- History.json
|
|-- README.txt

### File descriptions

**Main.py**

Contains the main application, graphical interface, test logic, timer, automatic marking, results screen, and answer review.

**questions/**

Contains JSON files with the questions for each subject.

**Biology.json, Mathematics.json, History.json**

Example question banks. You can add more subjects by creating additional JSON files.

**README.txt**

Contains the project's documentation and instructions.

## 5. Installation

1. Install Python if it is not already installed.
2. Create a folder named `StudentAutotester`.
3. Save the application code as `Main.py` inside that folder.
4. Create a folder named `questions` inside `StudentAutotester`.
5. Add your JSON question files to the `questions` folder.
6. Make sure each question file follows the required JSON format.

## 6. Running the Application

Open a terminal or command prompt in the `StudentAutotester` folder.

### Windows

Run:

```
python Main.py
```

Alternatively, you can use:

```
py Main.py
```

### macOS and Linux

Run:

```
python3 Main.py
```

The application should open and display the test selection screen.

If the application does not start, check that Python is installed correctly and that the required files are in the correct folders.

## 7. Creating Question Files

Questions are stored in JSON format.

Each question must contain:

* `question`: The question text.
* `options`: A list containing exactly four different answer options.
* `answer`: The correct answer, matching one of the options exactly.

### Example

```
[
    {
        "question": "Which planet is known as the Red Planet?",
        "options": [
            "Venus",
            "Mars",
            "Jupiter",
            "Mercury"
        ],
        "answer": "Mars"
    }
]
```

### Important rules

1. Each question must contain exactly four options.
2. The four options must be different.
3. The correct answer must exactly match one of the options.
4. Question text and options must be enclosed in double quotation marks.
5. Separate questions with commas.
6. Do not add a comma after the final question.
7. The file must contain valid JSON.
8. Save the file with the `.json` extension.

The application validates question files when a test is selected. If a file is invalid, an error message will explain what needs to be corrected.

## 8. Adding a New Subject

To add a new subject:

1. Open the `questions` folder.
2. Create a new JSON file, such as `Chemistry.json`.
3. Add questions using the required JSON structure.
4. Save the file.
5. Click **Refresh Tests** on the application's home screen.

The new subject should appear in the test selection menu.

You do not need to modify `Main.py` to add a normal JSON question bank.

## 9. Taking a Test

1. Launch the application.
2. Select a subject.
3. Choose the number of questions.
4. Optionally enable the countdown timer and set its duration.
5. Click **Start Test**.
6. Select an answer for each question.
7. Use Previous, Next, or the numbered question buttons to navigate.
8. Click **Finish Test** when you are ready to submit.

If some questions are unanswered, the application will warn you before submission.

If the countdown reaches zero, the test will be submitted automatically.

## 10. Understanding the Results

After submission, the results screen displays:

* **Score:** The number of correct answers out of the total questions.
* **Percentage:** The percentage of questions answered correctly.
* **Correct answers:** The number of correct responses.
* **Incorrect answers:** The number of incorrect responses.
* **Unanswered questions:** The number of questions left blank.
* **Time taken:** The elapsed time for the test.

Click **Check Answers** to review your responses.

The review screen identifies correct, incorrect, and unanswered questions and shows the correct answer for each question.

Click **Make a New Test** to return to the home screen.

## 11. AI Question Generation

AI question generation is a planned feature and is not currently implemented.

The `Main.py` file contains a placeholder function:

```
generate_questions_with_ai(subject, number_of_questions)
```

This function is reserved for future AI integration.

When implemented, the AI feature could:

* Generate questions for a selected subject.
* Produce four multiple-choice options per question.
* Identify the correct answer.
* Validate the generated questions.
* Save generated questions in JSON format.
* Make generated tests available to the existing application.

The existing test application does not require AI to function.

### Important

If you add an AI service, follow its documentation and security requirements. Do not store private API keys directly in source code or publish them in a public repository.

## 12. Data Analysis

The current application does not require data analysis.

The interface, question loading, timer, navigation, automatic marking, and results calculation work using standard Python functionality.

Additional data analysis may be useful if future versions need to:

* Analyse student performance across multiple tests.
* Identify topics where a student needs more practice.
* Analyse uploaded learning materials.
* Track progress over time.

These features are not currently implemented.

## 13. Troubleshooting

### No tests appear

* Check that the `questions` folder is beside `Main.py`.
* Make sure your question files end in `.json`.
* Click **Refresh Tests**.

### A JSON file cannot be loaded

* Check the JSON syntax.
* Make sure each question has four different options.
* Ensure the correct answer matches an option exactly.
* Remove trailing commas.

### The application will not start

* Confirm that Python is installed.
* Run the command from the project folder.
* Check the error message displayed in the terminal.
* Confirm that Tkinter is available in your Python installation.

### The requested number of questions is unavailable

The application uses all available questions if the requested number exceeds the number of questions in the selected file.

For example, requesting 10 questions from a file containing only 5 questions will produce a 5-question test.

## 14. Limitations

* Questions must currently be provided in JSON files.
* Every question must have exactly four answer options.
* AI question generation has not been implemented.
* Student progress is not permanently stored.
* Results are displayed after a test but are not saved to a database.
* Internet access is not required for the core application.

## 15. Future Improvements

Potential future features include:

* AI-generated questions.
* Importing questions from documents.
* Saving test results.
* Tracking student progress.
* Subject and topic filters.
* Difficulty selection.
* Explanations for correct answers.
* Customizable test settings.
* Exporting results to a file.

## 16. License and Usage

This project is intended as an educational tool and can be modified to suit your needs.

If you distribute the project, ensure that any third-party libraries, AI services, and external learning materials you add are used according to their applicable licenses and terms.

---

**Project:** Student Autotester
**Language:** Python
**Interface:** Tkinter
**Question format:** JSON
**AI integration:** Planned
**Data analysis:** Not required for the current core application
