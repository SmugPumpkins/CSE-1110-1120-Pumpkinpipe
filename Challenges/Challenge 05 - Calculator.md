# Challenge 05 - Calculator

The purpose of this challenge is to get used to creating gesture controlled interfaces that are controlled by the hand position relative to the screen.

## Mild 🌶️

Create a program that meets the following criteria:

* A live video feed is captured through a webcam.
* Hands are detected.
* Hands are drawn.
* A number is displayed in the top left corner where the number is the number of fingers on the left hand multiplied by the fingers on the right hand.


## Medium 🌶️🌶️

Create a program that meets the following criteria:

* A live video feed is captured through a webcam.
* Hands are detected.
* Hands are drawn.
* Horizontal lines are drawn to create 4 distinct sections of the screen.
* The left of each section is labeled with an operation (`+`, `-`, `*`, or `/`)
* When both hands have their wrists in the same section, the total is displayed in the top right corner in the form:

```text
(Number of left hand fingers) (operation) (Number of right hand fingers)
```

For example, if I was holding up 4 fingers (left) and 3 fingers (right) and both of my hands were in the `+` layer, the displayed total would be 7 (`4 + 3 = 7`).

## Spicy 🌶️🌶️🌶️

Create a program that meets the following criteria:

* A live video feed is captured through a webcam.
* Hands are detected.
* Hands are drawn.
* Horizontal lines are drawn to create 4 distinct horizontal sections of the screen.
* The left of each section is labeled with an operation (`+`, `-`, `*`, or `/`)
* Vertical lines are drawn to create 4 distinct vertical sections of the screen.
* The top of each vertical section, from left to right is labeled with `1000`, `100`, `10`, `1`.
* The number a hand represents is multiplied by its place value section (for example, a hand with 4 fingers in the `100` column would represent `400`).
* When both hands have their wrists in the same section, the total is displayed in the top right corner in the form:

```text
(Number of left hand fingers) (operation) (Number of right hand fingers)
```

For example, if my hands were in the following quadrants:

|   | 1000 |   100    | 10 |     1     |
|:-:|:----:|:--------:|:--:|:---------:|
| + |      | Left (4) |    | Right (3) |
| - |      |          |    |           |
| * |      |          |    |           |
| / |      |          |    |           |

Then my total would be 403.