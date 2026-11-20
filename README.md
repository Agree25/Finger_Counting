# Finger Counting with OpenCV

A webcam-based experiment estimating finger counts through **HSV thresholding, contours, convex hulls, and convexity defects**.

## Run

Use Python with a webcam and desktop display:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python HandGesture-Based-Finger-Counting-using-OpenCV-and-Python-main/code.py
```

The script selects camera index `0` with the **Windows DirectShow backend** (`cv2.CAP_DSHOW`). On macOS/Linux, change that line to `cv2.VideoCapture(0)` or a suitable platform backend. Camera/GUI behavior has not been verified across platforms.

## Usage

Place your hand in the displayed region of interest. Adjust the lower/upper HSV thresholds and `Thresh` slider in **Color Adjustments** to separate the hand from the background. Press **Escape** in the active window to exit.

The script finds a hand contour and convex hull, counts qualifying defects, and overlays an estimate. Lighting, background, threshold settings, and hand orientation affect results. This classical computer-vision demonstration does not use a trained hand-landmark model.

The [original nested README](HandGesture-Based-Finger-Counting-using-OpenCV-and-Python-main/README.md) is preserved with the source.
