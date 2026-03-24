# Lesson 02 - Overview of OpenCV and Mediapipe

## Overview

OpenCV is the computer vision engine behind pumpkinpipe and handles opening and viewing images, processing images, and the live feed from the camera. Mediapipe handles the hand recognition from previously trained machine learning algorithms. Pumpkinpipe is a helper library I created to minimize the boilerplate required to set up projects.

## Importing OpenCV

This section shows how to import the OpenCV library so its functions can be used in your program.

* `import cv2`: Loads the OpenCV library so you can access its functions.
* `cv2`: The namespace used to call OpenCV methods.

```python
# Import the OpenCV library
import cv2
```

## Using a Live Camera Feed

This section explains how to access and work with a webcam feed using OpenCV.

* `cv2.VideoCapture(0)`: Connects to the default webcam (device index 0).
* `cap`: A variable that stores the camera object.
* The camera object is used to read frames continuously.

```python
# Connect to the default webcam
cap = cv2.VideoCapture(0)
```

### Reading the Camera Feed

This section shows how to capture individual frames from the webcam.

* `cap.read()`: Captures a single frame from the camera.
* `success`: A boolean indicating if the frame was captured successfully.
* `frame`: The actual image captured from the camera.

```python
# Read a frame from the camera
success, frame = cap.read()
```

### Displaying the Camera Feed

This section shows how to display frames in a window.

* `cv2.imshow()`: Displays an image in a window.
* `"Camera Feed"`: The title of the display window.
* `frame`: The image being displayed.

```python
# Display the frame in a window
cv2.imshow("Camera Feed", frame)
```

## Drawing on Frames

This section introduces how to draw shapes and text directly onto image frames.

### Line

This section shows how to draw a straight line on an image.

* `cv2.line()`: Draws a line on the image.
* `frame`: The image being drawn on.
* `(0, 0)` and `(100, 100)`: Start and end coordinates.
* `(255, 0, 0)`: Color in BGR format (blue).
* `2`: Thickness of the line.

```python
# Draw a blue line from top-left to a point
cv2.line(
    frame,        # Image to draw on
    (0, 0),       # Start coordinates
    (100, 100),   # End coordinates
    (255, 0, 0),  # Color in BRG format
    2             # Line thickness
    )
```

### Rectangle

This section shows how to draw a rectangle.

* `cv2.rectangle()`: Draws a rectangle on the image.
* `(50, 50)` and `(200, 200)`: Opposite corners of the rectangle.
* `(0, 255, 0)`: Green color.
* `2`: Border thickness.

```python
# Draw a green rectangle
cv2.rectangle(
    frame,        # Image to draw on
    (50, 50),     # Top left corner of the rectangle
    (200, 200),   # Bottom right corner of rectangle
    (0, 255, 0),  # Color in BGR format
    2             # Outline thickness (-1 fills the shape)
    )
```

### Circle

This section shows how to draw a circle.

* `cv2.circle()`: Draws a circle.
* `(150, 150)`: Center point.
* `50`: Radius.
* `(0, 0, 255)`: Red color.
* `2`: Thickness.

```python
# Draw a red circle
cv2.circle(
    frame,        # Image to draw on
    (150, 150),   # Center point of circle
    50,           # Radius
    (0, 0, 255),  # Color in BGR format
    2             # Outline thickness (-1 fills the shape)
    )
```

### Ellipse

This section shows how to draw an ellipse.

* `cv2.ellipse()`: Draws an ellipse.
* `(150, 150)`: Center point.
* `(100, 50)`: Width and height of ellipse.
* `0`: Rotation angle.
* `0, 360`: Start and end angles.
* `(255, 255, 0)`: Color.

```python
# Draw an ellipse
cv2.ellipse(
    frame,          # Image to draw on
    (150, 150),     # Center point of ellipse
    (100, 50),      # Width, height
    0,              # Rotation angle (rotates the ellipse)
    0,              # Start of arc (partial arc will look Pac-Man)
    360,            # End of arc (partial arc will look Pac-Man)
    (255, 255, 0),  # Color in BGR format
    2               # Outline thickness (-1 fills the shape)
    )
```

### Polygon

This section shows how to draw a polygon using multiple points.

* `points`: A list of coordinates defining the shape.
* `cv2.polylines()`: Draws connected lines between points.
* `True`: Closes the shape.
* `(255, 0, 255)`: Color.

```python
# Define points for the polygon
points = [(100, 100), (200, 100), (150, 200)]

# Draw the polygon
cv2.polylines(
    frame,          # Image to draw on
    [points],       # List of points
    True,           # Connect the firt and last point automatically
    (255, 0, 255),  # Color in BGR format
    2               # Outline thickness (-1 fills the shape)
    )
```

### Text

This section shows how to draw text on an image.

* `cv2.putText()`: Draws text on an image.
* `"Hello"`: The text string.
* `(50, 50)`: Position of the text.
* `cv2.FONT_HERSHEY_SIMPLEX`: Font style.
* `1`: Font scale (size).
* `(255, 255, 255)`: White color.
* `2`: Thickness.

```python
# Draw text on the frame
cv2.putText(
    frame,                     # Image to draw on
    "Hello",                   # Text to write
    (50, 50),                  # Position of the text
    cv2.FONT_HERSHEY_SIMPLEX,  # Font to render text as 
    1,                         # Scale (size)
    (255, 255, 255),           # Color in BGR format
    2                          # Line thickness
    )
```

#### Fonts

| Code                              | Description                                    |
|-----------------------------------|------------------------------------------------|
| `cv2.FONT_HERSHEY_SIMPLEX`        | Simple, clean sans-serif font.                 |
| `cv2.FONT_HERSHEY_PLAIN`          | Small sans-serif font with minimal styling.    |
| `cv2.FONT_HERSHEY_DUPLEX`         | Slightly thicker sans-serif font.              |
| `cv2.FONT_HERSHEY_COMPLEX`        | Serif-style font with more detail.             |
| `cv2.FONT_HERSHEY_TRIPLEX`        | More detailed serif font with thicker strokes. |
| `cv2.FONT_HERSHEY_COMPLEX_SMALL`  | Smaller version of `FONT_HERSHEY_COMPLEX`.     |
| `cv2.FONT_HERSHEY_SCRIPT_SIMPLEX` | Simple handwriting-style font.                 |
| `cv2.FONT_HERSHEY_SCRIPT_COMPLEX` | More detailed handwriting-style font.          |
| `cv2.FONT_ITALIC`                 | Modifier flag that applies italics.            |

#### Line Types

| Code          | Description                                                 |
|---------------|-------------------------------------------------------------|
| `cv2.FILLED`  | Fills the shape completely with color.                      |
| `cv2.LINE_4`  | Line drawn using 4-connected pixels (blocky edges).         |
| `cv2.LINE_8`  | Line drawn using 8-connected pixels (smoother than LINE_4). |
| `cv2.LINE_AA` | Anti-aliased line for smooth edges.                         |

## Example - Live Camera Feed and Display

This example opens the webcam and continuously displays the live camera feed in a window.

```python
import cv2

# Connect to the webcam
cap = cv2.VideoCapture(0)

while True:
    # Read a frame from the camera
    success, frame = cap.read()

    # Display the frame
    cv2.imshow("Camera Feed", frame)

    # Exit if the 'q' key is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

    # Exit if the window is manually closed
    if cv2.getWindowProperty("Camera Feed", cv2.WND_PROP_VISIBLE) < 1:
        break

# Release webcam resources
cap.release()

# Close all OpenCV windows
cv2.destroyAllWindows()
```

## Example - Live Camera Feed with Drawing

This example displays the webcam feed and draws shapes on each frame in real time.

```python
import cv2

# Connect to the webcam
cap = cv2.VideoCapture(0)

while True:
    # Read a frame from the camera
    success, frame = cap.read()

    # Draw shapes on the frame
    cv2.rectangle(frame, (50, 50), (200, 200), (0, 255, 0), 2)
    cv2.circle(frame, (300, 150), 50, (255, 0, 0), 2)

    # Display the frame
    cv2.imshow("Camera Feed with Drawing", frame)

    # Exit if the 'q' key is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

    # Exit if the window is manually closed
    if cv2.getWindowProperty("Camera Feed with Drawing", cv2.WND_PROP_VISIBLE) < 1:
        break

# Release webcam resources
cap.release()

# Close all OpenCV windows
cv2.destroyAllWindows()
```

## Example - Live Camera Feed with Text

This example displays the webcam feed and overlays text on each frame.

```python
import cv2

# Connect to the webcam
cap = cv2.VideoCapture(0)

while True:
    # Read a frame from the camera
    success, frame = cap.read()

    # Add text to the frame
    cv2.putText(frame, "Live Feed", (50, 50), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 2)

    # Display the frame
    cv2.imshow("Camera Feed with Text", frame)

    # Exit if the 'q' key is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

    # Exit if the window is manually closed
    if cv2.getWindowProperty("Camera Feed with Text", cv2.WND_PROP_VISIBLE) < 1:
        break

# Release webcam resources
cap.release()

# Close all OpenCV windows
cv2.destroyAllWindows()
```
