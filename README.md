# Playing Subway Surfers Game using Pose Detection

## Outline

- **Step 1:** Perform Pose Detection
- **Step 2:** Control Starting Mechanism
- **Step 3:** Control Horizontal Movements
- **Step 4:** Control Vertical Movements
- **Step 5:** Control Keyboard and Mouse with PyautoGUI
- **Step 6:** Build the Final Application

### Import the Libraries

```python
import cv2
import pyautogui
from time import time
from math import hypot
import mediapipe as mp
import matplotlib.pyplot as plt
```

### Initialize the Pose Detection Model

```python
# Initialize mediapipe pose class.
mp_pose = mp.solutions.pose

# Setup the Pose function for images.
pose_image = mp_pose.Pose(static_image_mode=True, min_detection_confidence=0.5, model_complexity=1)

# Setup the Pose function for videos.
pose_video = mp_pose.Pose(static_image_mode=False, model_complexity=1, min_detection_confidence=0.7,
                          min_tracking_confidence=0.7)

# Initialize mediapipe drawing class.
mp_drawing = mp.solutions.drawing_utils 
```

### Step 1: Perform Pose Detection

```python
def detectPose(image, pose, draw=False, display=False):
    # Function implementation
```

### Step 2: Control Starting Mechanism

```python
def checkHandsJoined(image, results, draw=False, display=False):
    # Function implementation
```

### Step 3: Control Horizontal Movements

```python
def checkLeftRight(image, results, draw=False, display=False):
    # Function implementation
```

### Step 4: Control Vertical Movements

```python
def checkJumpCrouch(image, results, MID_Y=250, draw=False, display=False):
    # Function implementation
```

### Step 5: Control Keyboard and Mouse with PyautoGUI

```python
# Press the up key.
pyautogui.press(keys='up')

# Press the down key.
pyautogui.press(keys='down')

# Press the mouse right button. It will open up the menu.
pyautogui.click(button='right')
```

### Step 6: Build the Final Application

In the final step, all components will be combined to build the final application. You can use the outputs of the functions created above to control the game character with body movements.

Feel free to play the game [here](https://subway-surfers.me/) using your body gestures and movements.

This project can be found in the following GitHub repository: [Subway-Surfers-Pose-Detection](https://github.com/Tesmin-Varghese/Project).
