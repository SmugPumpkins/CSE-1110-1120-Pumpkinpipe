# Pumpkinpipe - Program

## Overview

Create something phenomenal using the Pumpkinpipe library and Python. Your project will need to be planned, tested, and presented to the class to demonstrate your understanding of structured programming. Be sure to focus on using `selection` and `iteration` structures to make your project work.

## Project Criteria

Your task is to:

* Create a project using the Pumpkinpipe library and Python.
* Use values from the hand detection in your project. These inputs might include but are not limited to:
    * Handedness (right or left)
    * Number of hands
    * Hand position (x, y, z)
    * Landmark positions
    * Finger flags / fingers up / fingers down
    * Distance between landmarks
* Create outputs that could come from processing the above input data. This could look like:
    * Rendering shapes / text / lines
    * Adding sounds that play
    * Integrating other libraries to visualize / control other things
    * Creating a simple game loop with score / points

### Record AI Use

Be sure to submit your AI use document as part of your project. Copy and paste all AI use into the document. If no AI was used, paste the following into the document:

```text
NO AI USED IN THE MAKING OF THIS PROJECT
```

### Record External Resources

Be sure to submit your resources document that contains the external resources you used as a part of your project. Paste links to websites, videos, articles, etc. of resources you used when creating your project. If no external resources were used, paste the following into the document:

```text
NO EXTERNAL RESOURCES USED IN THE MAKING OF THIS PROJECT
```

## Submission

* *5% will be deducted for naming files incorrectly.*
* *5% will be deducted for submitting files of the wrong type or missing specified file types.*
* *5% will be deducted for files being located in the wrong folders.*

### Source Code

* **File Type:** `.py`
* **File Name:** `main.py`.
* **File Location:** Root folder.
* **Push your project folder to GitHub Classroom**

### AI Use Document

* **File Type:** `.md`
* **File Name:** `ai use.md`.
* **File Location:** `Project Documents` folder.
* **Push your project folder to GitHub Classroom**

### Resources Document

* **File Type:** `.md`
* **File Name:** `resources.md`.
* **File Location:** `Project Documents` folder.
* **Push your project folder to GitHub Classroom**

## Mastery Rubric

| Outcome                                                                  | **5 – Mastery of Skill**                                                                                                                                                  | **4 – Excellence in Skill**                                                                                       | **3 – Proficiency in Skill**                                      | **2 – Attempting Skill**                               | **1 – Starting to Attempt Skill**                  | **0 – Refusal to Engage with Skill**         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------|----------------------------------------------------|----------------------------------------------|
| **2.1 Maintain a clear IPO structure in the program**                    | Program clearly follows a real-time pipeline (camera input → hand detection → processing → output) and is structured for easy expansion, debugging, and feature addition. | Program is clearly organized around IPO with hand input, processing, and outputs logically separated.             | IPO structure is present and mostly consistent.                   | IPO structure is attempted but inconsistently applied. | IPO structure is unclear or incorrect.             | No identifiable IPO structure.               |
| **2.2 Include appropriate internal and external documentation**          | Code and documents clearly explain how and why hand data is used; planning, AI use, and resources documents are complete and directly reflected in the program.           | Code is well-commented and documentation clearly explains how the program works; required documents are complete. | Code includes useful comments and required documents are present. | Limited comments or incomplete documentation.          | Minimal or ineffective documentation.              | No documentation or required files provided. |
| **2.3 Use data types correctly**                                         | Data types are chosen intentionally for hand data (e.g., lists, tuples, Booleans) and used correctly across all features including gestures and calculations.             | Data types are used correctly and consistently throughout the program.                                            | Data types are mostly used correctly.                             | Frequent confusion between data types causes issues.   | Data types are largely incorrect or misunderstood. | No meaningful use of data types.             |
| **2.4 Use variables and constants to store data correctly**              | Variables are clearly named and organized (e.g., hand data, game state, settings) to support readability and future expansion.                                            | Variables are meaningful and consistently used; constants are used where appropriate.                             | Variables are used correctly with minor issues.                   | Variables are inconsistently used or poorly named.     | Limited or incorrect use of variables.             | No meaningful use of variables.              |
| **2.5 Use literals and external input to provide data for processing**   | Hand detection inputs (e.g., finger states, positions, distances) are used creatively to control dynamic and interactive features.                                        | Program effectively uses hand input data to control behavior and outputs.                                         | Hand input is used correctly with clear purpose.                  | Limited or repetitive use of hand input.               | Minimal or ineffective use of input.               | No input or interaction used.                |
| **2.6 Use operators to work with data correctly**                        | Operators are used precisely for gesture detection, comparisons, and calculations; logic is clean and efficient.                                                          | Operators are used correctly and effectively throughout the program.                                              | Operators are mostly used correctly.                              | Operator errors affect behavior.                       | Major misunderstandings of operators.              | No meaningful operator use.                  |
| **2.7 Use common algorithm patterns when needed**                        | Algorithm patterns (e.g., counting fingers, comparing landmark distances, tracking state) are used strategically to create complex interactions.                          | Algorithm patterns are used effectively to process hand data.                                                     | Appropriate patterns are used correctly.                          | Patterns are attempted but poorly implemented.         | Little evidence of algorithmic thinking.           | No algorithm patterns used.                  |
| **2.8 Use selection and iteration structures**                           | Loops and conditionals are used fluently (e.g., looping through hands, gesture conditions, nested logic) to create responsive and efficient interaction.                  | Selection and iteration are used effectively, including nested structures where needed.                           | Selection and loops are used correctly.                           | Limited or incorrect use of selection or loops.        | Minimal or incorrect use of control structures.    | No selection or iteration used.              |
| **2.9 Use output commands to display results clearly**                   | Output is dynamic and responsive (e.g., drawings, animations, feedback, game elements) and clearly reflects hand interactions in real time.                               | Output is clear, meaningful, and directly tied to hand input.                                                     | Output communicates results clearly.                              | Output is inconsistent or unclear.                     | Output is minimal or ineffective.                  | No output produced.                          |
| **3.1 Use suitable test data to ensure the program works as intended**   | Program is tested with a wide range of hand inputs (gestures, positions, multiple hands); testing results improve functionality and reliability.                          | Program is tested with varied hand inputs and improvements are made.                                              | Program is tested with multiple inputs.                           | Limited testing; issues remain.                        | Minimal or ineffective testing.                    | No testing evident.                          |
| **3.1.1 Use debugging techniques to correct run-time and syntax errors** | Independently diagnoses and fixes errors efficiently using testing, debugging tools, and iteration; prevents future errors through design.                                | Independently identifies and fixes most syntax and run-time errors.                                               | Fixes most errors with minimal guidance.                          | Struggles to identify or fix errors.                   | Rarely attempts to debug.                          | Makes no attempt to debug.                   |
| **3.1.2 Use debugging techniques to correct logic errors**               | Effectively identifies and resolves complex logic issues in gesture handling, control flow, and interaction design through testing and reasoning.                         | Identifies and fixes logic errors through testing and revision.                                                   | Fixes most logic errors with guidance.                            | Has difficulty identifying logic errors.               | Does not meaningfully address logic errors.        | Makes no attempt to debug logic errors.      |


## Outcome Criteria

* **2 Demonstrate the ability to take an algorithm and convert it to a programming language. Run the program and see the results.**
    * **2.1** Maintain a clear input–process–output (IPO) structure in the algorithm.
    * **2.2** Include appropriate internal and external documentation. This can include comments in your code that explain how it works and planning you’ve done previously.
    * **2.3** Use basic data types correctly (integer, real/float, character, string, Boolean).
    * **2.4** Use variables and constants appropriately to store data.
    * **2.5** Use literals (setting values manually or assigning them to variables in the code) and input commands (allowing the user to set values through input or interaction) to supply data for processing.
    * **2.6** Use the appropriate operators to work with data (for example, assigning values, doing math, comparing values, combining text, or inserting values into strings, etc.) whenever the task requires it.
    * **2.7** Use common algorithm patterns when needed, such as accumulation or finding maximum/minimum values.
    * **2.8** Use suitable selection and looping structures to avoid unconditional jumps, including:
        * **2.8.1** nested conditional blocks
        * **2.8.2** nested loops
    * **2.9** Use output commands (methods or operators) to display results in a clear, formatted way.
* **3 Run the program. Determine if there are any errors and fix them so that the program runs as expected.**
    * **3.1** Use suitable test data to check the program. This can include user inputs or literals that you manually program to check if things work as expected.
        * **3.1.1** Use debugging techniques to track and correct run-time or syntax errors. These are errors that occur when a program will not run at all until the code is correct.
        * **3.1.2** Use debugging techniques to find and fix logic errors. These are errors where the code does run, but produces an unexpected result due to the logic used in the program.
