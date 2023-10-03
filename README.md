# opencv-inflearn
MacOS 

## Course Info
[Image Processing: OpenCV](https://www.inflearn.com/course/%EB%82%98%EB%8F%84%EC%BD%94%EB%94%A9-%EC%9D%B4%EB%AF%B8%EC%A7%80%EC%B2%98%EB%A6%AC)

## Prerequisite

### Create Virtual Environment (Optional)

```zsh
$ python -m venv <your_venv_name> # e.g. opencv-inflearn
$ source <pwd>/<your_venv_name>/bin/activate
(opencv-inflearn) $
```

### Install Jupyter Notebook (or Jupyter Lab)

```zsh
(opencv-inflearn) $ pip install jupyterlab
(opencv-inflearn) $ jupyter lab
```

### Install Necessary Libraries

- `opencv-python`: OpenCV for python
- `pillow`: PIL (Python Image Library) for python3
- `mediapipe`: On-device ML Library for face detection (and additional features)

```zsh
(opencv-inflearn) $ pip install opencv-python pillow mediapipe
```

### Install Hangul Font

```zsh
$ curl https://www.wfonts.com/download/data/2016/06/13/malgun-gothic/malgun-gothic.zip --output malgun-gothic.zip
$ unzip malgun-gothic.zip
```

## Miscellaenous
In case of using MacOS, you need to additional set `cv2.waitKey(1)` after `cv2.destroyAllWindows()` for preventing infinity loop.

```python
import cv2
img = cv2.imread(<image_dir>)
cv2.imshow('img', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.waitKey(1) # needed in MacOS
``` 
