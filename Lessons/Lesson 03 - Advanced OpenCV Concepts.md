# Lesson 03 - Advanced OpenCV Concepts

## Overview
This lesson is completely optional, but provides some brief outlines on additional ways that OpenCV can be used!

This document covers core OpenCV concepts including image loading, drawing, pixel operations, and image processing techniques used in real-world computer vision workflows.

## Loading Images

This section explains how to load images from disk into memory.

* `cv2.imread()`: Reads an image file into a NumPy array.
* `"image.png"`: The file path to the image.
* The result is stored as an array representing pixel data.
* If loading fails, the result will be `None`.

```python
# Load an image from file
img = cv2.imread("image.png")
```

## Saving Images

This section shows how to save images back to disk.

* `cv2.imwrite()`: Writes an image to a file.
* `"output.png"`: The output file name.
* `img`: The image data to save.
* Existing files will be overwritten.

```python
# Save the image to a new file
cv2.imwrite("output.png", img)
```

## Displaying Images

This section shows how to display images in a window.

* `cv2.imshow()`: Displays an image in a window.
* `"Window"`: The name of the window.
* `img`: The image to display.
* `cv2.waitKey(0)`: Waits indefinitely for a key press.
* `cv2.destroyAllWindows()`: Closes all windows.

```python
# Show the image in a window
cv2.imshow("Window", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Image Properties

This section shows how to inspect image information.

* `img.shape`: Returns `(height, width, channels)`.
* `img.size`: Total number of values in the image.
* `img.dtype`: Data type (usually `uint8`).

```python
# Print image properties
print(img.shape)
print(img.size)
print(img.dtype)
```

## Accessing Pixels

This section shows how to read pixel values.

* `img[y, x]`: Accesses a pixel at row `y`, column `x`.
* Returns `[B, G, R]` values.
* Each value ranges from `0` to `255`.

```python
# Get pixel value at (100, 100)
pixel = img[100, 100]
```

## Modifying Pixels

This section shows how to change pixel values.

* `img[y, x] = [B, G, R]`: Sets a pixel color.
* `[255, 0, 0]`: Blue in BGR format.
* Direct modification updates the image instantly.

```python
# Set pixel to blue
img[100, 100] = [255, 0, 0]
```

## Region of Interest (ROI)

This section shows how to work with sections of an image.

* `img[y1:y2, x1:x2]`: Slices a region.
* Regions can be copied and pasted.
* Source and destination must be the same size.

```python
# Copy a region and paste it elsewhere
roi = img[50:100, 50:100]
img[150:200, 150:200] = roi
```

## Splitting Channels

This section shows how to separate color channels.

* `cv2.split()`: Splits into blue, green, red channels.
* Each channel becomes a grayscale image.
* Useful for analyzing colors separately.

```python
# Split into channels
b, g, r = cv2.split(img)
```

## Merging Channels

This section shows how to recombine channels.

* `cv2.merge()`: Combines channels into one image.
* Channels must be in BGR order.
* Used after modifying channels.

```python
# Merge channels back
img = cv2.merge((b, g, r))
```

## Adding Images

This section shows how to combine images.

* `cv2.add()`: Adds pixel values safely (clipped at 255).
* Both images must be same size.
* Prevents overflow issues.

```python
# Add two images
result = cv2.add(img, img)
```

## Blending Images

This section shows how to mix images using weights.

* `cv2.addWeighted()`: Blends two images.
* `0.5, 0.5`: Equal contribution.
* `0`: No brightness offset.

```python
# Blend two images
blend = cv2.addWeighted(img, 0.5, img, 0.5, 0)
```

## Drawing Shapes

This section shows how to draw basic shapes.

* `cv2.line()`: Draws a line.
* `cv2.rectangle()`: Draws a rectangle.
* `cv2.circle()`: Draws a circle.
* Coordinates use `(x, y)` format.
* Colors use BGR format.

```python
# Draw shapes
cv2.line(img, (0, 0), (100, 100), (255, 0, 0), 2)
cv2.rectangle(img, (50, 50), (150, 150), (0, 255, 0), 2)
cv2.circle(img, (200, 200), 50, (0, 0, 255), 2)
```

## Drawing Text

This section shows how to overlay text on images.

* `cv2.putText()`: Draws text.
* `"Text"`: The string to display.
* `(x, y)`: Position of text.
* Font and size control appearance.

```python
# Add text
cv2.putText(img, "Hello", (50, 50), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 2)
```

## Color Space Conversion

This section shows how to change how color is represented.

* `cv2.cvtColor()`: Converts color spaces.
* `cv2.COLOR_BGR2GRAY`: Converts to grayscale.
* Used for simplifying image processing.

```python
# Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

## Resizing Images

This section shows how to scale images.

* `cv2.resize()`: Changes image size.
* `(width, height)`: New dimensions.
* Used for standardizing image size.

```python
# Resize image
small = cv2.resize(img, (100, 100))
```

## Translating Images

This section shows how to move images.

* `cv2.warpAffine()`: Applies transformation.
* Matrix controls movement.
* Moves image in x and y directions.

```python
# Move image right and down
matrix = np.float32([[1, 0, 50], [0, 1, 50]])
moved = cv2.warpAffine(img, matrix, (img.shape[1], img.shape[0]))
```

## Rotating Images

This section shows how to rotate images.

* `cv2.getRotationMatrix2D()`: Creates rotation matrix.
* `cv2.warpAffine()`: Applies rotation.
* Rotation is around a center point.

```python
# Rotate image
center = (img.shape[1] // 2, img.shape[0] // 2)
matrix = cv2.getRotationMatrix2D(center, 45, 1)
rotated = cv2.warpAffine(img, matrix, (img.shape[1], img.shape[0]))
```

## Thresholding

This section shows how to create binary images.

* `cv2.threshold()`: Applies threshold.
* Pixels become black or white.
* Works on grayscale images.

```python
# Apply threshold
_, thresh = cv2.threshold(gray, 127, 255, cv2.THRESH_BINARY)
```

## Edge Detection

This section shows how to detect edges in images.

* `cv2.Canny()`: Detects edges.
* `100, 200`: Threshold values.
* Outputs a binary edge image.

```python
# Detect edges
edges = cv2.Canny(gray, 100, 200)
```

## Example - Image Load, Modify, and Display

This example loads an image, modifies it, and displays the result.

```python
import cv2
import numpy as np

# Load image
img = cv2.imread("image.png")

# Draw a rectangle
cv2.rectangle(img, (50, 50), (200, 200), (0, 255, 0), 2)

# Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Display result
cv2.imshow("Window Name", gray)

# Wait for key press or window close
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Example - Image Blending

This example blends two images together.

```python
import cv2

# Load images
img1 = cv2.imread("image1.png")
img2 = cv2.imread("image2.png")

# Blend images
blend = cv2.addWeighted(img1, 0.5, img2, 0.5, 0)

# Display result
cv2.imshow("Window Name", blend)

# Wait for key press or window close
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Example - Edge Detection Pipeline

This example converts an image to grayscale and detects edges.

```python
import cv2

# Load image
img = cv2.imread("image.png")

# Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect edges
edges = cv2.Canny(gray, 100, 200)

# Display result
cv2.imshow("Window Name", edges)

# Wait for key press or window close
cv2.waitKey(0)
cv2.destroyAllWindows()
```
