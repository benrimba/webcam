# Membuat Aplikasi WebCam dari Python
## Disini saya OS Linux Ubuntu 19.10 dan menggunakan Python3 dan pip3 
### Buka terminal linux dengan menekan tombol Ctrl+Alt+T 
### 1. Instal pip3
#### # sudo apt update
#### # sudo apt install pip3
### 2. Install OpenCV-Python 
#### # pip3 install opencv-python
# Source Code 
```py
import requests
import cv2
import numpy as np

url = "Alamat IP dari hp/shot.jpg"
while True:
    img_resp = requests.get(url)
    img_arr = np.array(bytearray(img_resp.content),dtype=np.uint8)
    img = cv2.imdecode(img_arr,-1)
    cv2.imshow("Gl-Tech Lab",cv2.resize(img,(600,300)))
    if cv2.waitKey(1)==27:
        break
```
