# Pumpkinpipe - Planning

## Overview

Plan something phenomenal using the Pumpkinpipe library and Python. Your project will need to be planned, tested, and presented to the class to demonstrate your understanding of structured programming. Be sure to focus on using `selection` and `iteration` structures to make your project work.

## Project Criteria

Your task is to:

* Plan a project using the Pumpkinpipe library and Python.
* Identify values that can be used from the hand detection that could be used in your project. These inputs might include but are not limited to:
    * Handedness (right or left)
    * Number of hands
    * Hand position (x, y, z)
    * Landmark positions
    * Finger flags / fingers up / fingers down
    * Distance between landmarks
* Identify outputs that could come from processing the above input data. This could look like:
    * Rendering shapes / text / lines
    * Adding sounds that play
    * Integrating other libraries to visualize / control other things
    * Creating a simple game loop with score / points

Show your planning with the following included in your planning document:

* Overview outlining the idea for your project. The overview should be between 50-75 words.
* Use IPO charts to break down the input, process steps, and output for different modules in your project.
* Use pseudocode or a structured flow chart to communicate the flow of your overall program.

## Submission

* *5% will be deducted for naming files incorrectly.*
* *5% will be deducted for submitting files of the wrong type or missing specified file types.*
* *5% will be deducted for files being located in the wrong folders.*

### Planning Document

* **File Type:** `.md`
* **File Name:** `student planning.md`.
* **File Location:** `Project Documents` folder.
* **Push your project folder to GitHub Classroom**

## Mastery Rubric

*For this project, outcomes are covered from both **CSE 1110 - Structured Programming 1** and **CSE 1120 - Structured Programming 2**. This means that different parts of the rubric will appear in different credits on your gradebook when marking is completed. For each outcome on the rubric, the credit is specified for where the grade will be updated.*

| Outcome                                                                                                                                                  | **5 – Mastery of Skill**                                                                                                                                  | **4 – Excellence in Skill**                                                              | **3 – Proficiency in Skill**                                                            | **2 – Attempting Skill**                                                  | **1 – Starting to Attempt Skill**              | **0 – Refusal to Engage with Skill** |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|------------------------------------------------|--------------------------------------|
| **CSE 1110**<br>*1.1-1.5*<br>Input, processing, and output are correctly identified and placed into IPO charts.                                          | IPO charts are complete, accurate, and clearly show how specific hand detection inputs are transformed into meaningful outputs across multiple modules.   | IPO charts clearly represent how inputs are processed into outputs with minor gaps.      | IPO charts correctly identify input, process, and output for the project.               | IPO charts are partially correct but show misunderstandings.              | IPO structure is unclear or mostly incorrect.  | No IPO charts.                       |
| **CSE 1110**<br>*1.7*<br>Use pseudocode to write a clear algorithm. Follow the standardized styles for pseudocode.                                       | Pseudocode is complete, correctly formatted (START/END, structure), and clearly represents the full program flow including interaction and control logic. | Pseudocode is clear, mostly complete, and follows standard formatting with minor issues. | Pseudocode represents the main logic but may be incomplete or inconsistently formatted. | Pseudocode is attempted but lacks clarity, structure, or correctness.     | Minimal pseudocode with major issues.          | No pseudocode.                       |
| **CSE 1110**<br>*1.6, 1.6.1*<br>Pseudocode algorithm is structured such that processing only occurs after all required input is available.               | Algorithm clearly ensures all required hand input data is gathered before any processing; sequencing is precise and consistent across modules.            | Algorithm correctly sequences input before processing with minor issues.                 | Input generally occurs before processing, with some inconsistencies.                    | Sequencing is partially incorrect or unclear.                             | Sequencing is mostly incorrect.                | No logical sequencing.               |
| **CSE 1110**<br>*1.6, 1.6.2*<br>Pseudocode algorithm is structured such that output only occurs after processing is complete.                            | Algorithm clearly ensures all processing is completed before outputs (visuals, sounds, interactions) occur across all modules.                            | Output follows processing correctly with minor inconsistencies.                          | Output generally follows processing, with some issues.                                  | Output sequencing is inconsistent or partially incorrect.                 | Output sequencing is mostly incorrect.         | No logical sequencing.               |
| **CSE 1120**<br>*1.1-1.4*<br>Input is clearly defined, including how the data is being provided and what the data represents.                            | All inputs (hand data, states, variables) are clearly identified, categorized, and explained in context of the planned project.                           | Inputs are clearly identified and mostly well described.                                 | Inputs are identified but lack detail or clarity.                                       | Inputs are partially identified or confused.                              | Minimal or incorrect identification of inputs. | No inputs identified.                |
| **CSE 1120**<br>*1.1-1.3, 1.5-1.6*<br>Process is clearly defined, including steps correctly using sequence, selection, and iteration control structures. | Processing steps are detailed, logically ordered, and clearly use selection and iteration to support interaction or game logic.                           | Processing steps are clear and correctly use control structures with minor issues.       | Processing steps are present and use basic control structures.                          | Processing steps are incomplete or inconsistently use control structures. | Processing steps are minimal or incorrect.     | No processing defined.               |
| **CSE 1120**<br>*1.1-1.3, 1.7*<br>Output is clearly defined, including whether it is used by the program or displayed to the user.                       | Outputs are clearly defined, meaningful, and directly tied to processing results (e.g., visuals, sounds, feedback, game state).                           | Outputs are clearly defined and connected to the program.                                | Outputs are identified but lack detail or clarity.                                      | Outputs are incomplete or inconsistently defined.                         | Outputs are unclear or incorrect.              | No outputs identified.               |
| **CSE 1120**<br>*1.8-1.9*<br>Use pseudocode to write a clear algorithm. Follow the standardized styles for pseudocode.                                   | Full algorithm is logically ordered (input → process → output), modularized, and ready for implementation; flow is clear and complete.                    | Algorithm is logically ordered and mostly complete with minor issues.                    | Algorithm shows logical order but may be incomplete.                                    | Algorithm order is inconsistent or unclear.                               | Algorithm is mostly incorrect or incomplete.   | No algorithm provided.               |


## Outcome Criteria

### CSE 1110

* **1 Demonstrate introductory structured programming skills by planning and writing sequential algorithms.**
  * **1.1** Explain what an algorithm is and why it is used.
  * **1.2** Analyze simple algorithms and describe the task or tasks they perform.
  * **1.3** Determine whether a problem can be solved using an input–process–output (IPO) approach.
  * **1.4** Break a problem into input, processing, and output components.
  * **1.5** Identify which data is already available to the program and which data must be provided as input.
  * **1.6** Arrange inputs, processing steps, and outputs in the correct order so that:
    * **1.6.1** processing occurs only after all required input is available
    * **1.6.2** output occurs only after processing is complete
  * **1.7** Write algorithms in a clear, standard format.

### CSE 1120

* **1 Demonstrate the ability to plan for structured programming challenges that incorporate selection and iteration structures**
    * **1.1** Determine whether a problem can be solved with an algorithm using the input–process–output (IPO) model.
    * **1.2** Decide if the problem contains more than one IPO module.
    * **1.3** Break the problem into smaller modules and identify the input, processing, and output for each.
    * **1.4** Identify what data the program already has, what data the user must provide, and group those inputs logically using suitable control structures.
    * **1.5** Identify the processing steps needed for the solution and group them logically using suitable control structures.
    * **1.6** Use common algorithm patterns when needed, such as accumulation or finding maximum/minimum values.
    * **1.7** Identify the required outputs and group them logically using suitable control structures.
    * **1.8** Arrange all inputs, processes, and outputs in a logical order so that processing only happens when all needed data is available, and output only happens after processing is complete.
    * **1.9** Write the final algorithm in a clear, standard format (e.g., pseudocode or a structured chart).

