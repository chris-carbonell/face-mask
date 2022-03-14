# Face Mask

With <b>Face Mask</b>, you can steal someone's likeness from a <b>static image</b> of their face, create a <b>3-D mask</b> from it, don it virtually, and <b>stream</b> it to your favorite video chatting platform!

# Quickstart

Run with the following:<br>
<code>python -m face_mask</code>

If using <b>UnityCapture</b> as your virtual camera, "Unity Video Capture" will be available as a camera option in your video chatting platform (e.g., Zoom, MS Teams).

# Example

![demo](docs/demo.gif)<br>
\* The frame rate dropped due to capturing the screen through FFmpeg and converting that video to a GIF.

# Installation

1. Install <b>UnityCapture</b>. See the links below for installation instructions.
    * This will serve as the virtual camera we use with <code>pyvirtualcam</code>.
    * There are other options for virtual cameras available here:<br>
    [https://pypi.org/project/pyvirtualcam/](https://pypi.org/project/pyvirtualcam/)

2. Install the required Python dependencies:<br>
<code>python -m pip install -r requirements.txt</code>
    * I'd recommend running this all in a virtual environment or a Docker container.

# Overview

<code>face_mask.py</code> accomplishes the following:
* detects faces - in the input image and the webcam stream - using MediaPipe's Face Mesh model
* creates a virtual mask from the input image by creating triangles between facial landmarks
* maps that virtual mask to the webcam's face

# Building Environment

To build this repo, I used the following:
* Microsoft Windows 10 Home (64-bit)
* Python 3.9.7
* FFmpeg (2022-03-07)
* OpenShot (v2.6.1)

# Resources

* MediaPipe Face Swap<br>
[https://github.com/uelordi01/mediapipe_faceswap/blob/main/media_pipe_sample.py](https://github.com/uelordi01/mediapipe_faceswap/blob/main/media_pipe_sample.py)
    * mouth not cut out
* pyvirtualcam<br>
[https://pypi.org/project/pyvirtualcam/](https://pypi.org/project/pyvirtualcam/)
    * UnityCapture<br>
    [https://github.com/schellingb/UnityCapture](https://github.com/schellingb/UnityCapture)