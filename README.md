# yolov7-object-tracking

### New Features
- Added Label for Every Track
- Code can run on Both (CPU & GPU)
- Video/WebCam/External Camera/IP Stream Supported

### Coming Soon
- Development of streamlit dashboard for Object Tracking

### Ready to Use Google Colab
- https://colab.research.google.com/drive/1xrB76UQ_LaVaBAxfTi8-a9dIcazmxD5b?usp=sharing
### Steps to run Code
1. Clone the repository.
    ```bash
    git clone https://github.com/RizwanMunawar/yolov7-object-tracking.git
    ```
2. Goto the cloned folder.
    ```bash
    cd yolov7-object-tracking
    ```
3. Create a virtual envirnoment (Recommended, If you dont want to disturb python packages)

    #### For Anaconda
    ```bash
    # Create the virtural envirnment
    conda create -n yolov7objtracking python=3.10

    # Activate the virtural envirnment
    conda activate yolov7objtracking
    ```

    #### For Linux Users
    ```bash
    # Create the virtural envirnment
    python3 -m venv yolov7objtracking

    # Activate the virtural envirnment
    source yolov7objtracking/bin/activate
    ```

    #### For Window Users
    ```bash
    # Create the virtural envirnment
    python3 -m venv yolov7objtracking

    # Activate the virtural envirnment
    cd yolov7objtracking
    cd Scripts
    activate
    cd ..
    cd ..
    ```

4. Update pip and install libraries
    ```bash
    # Upgrade pip with mentioned command below.
    pip install --upgrade pip

    # Install requirements with mentioned command below.
    pip install -r requirements.txt
    ```

5. Run the script
   
    Select the appropirate command from the following list of command according to your need.
    (by default, pretrained [yolov7](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt) weights will be automatically downloaded into the working directory if they don't already exist).

    ```bash
    # for detection only
    python detect.py --weights yolov7.pt --source "your video.mp4"

    #if you want to change source file
    python detect_and_track.py --weights yolov7.pt --source "your video.mp4"

    #for WebCam
    python detect_and_track.py --weights yolov7.pt --source 0

    #for External Camera
    python detect_and_track.py --weights yolov7.pt --source 1

    #For LiveStream (Ip Stream URL Format i.e "rtsp://username:pass@ipaddress:portno/video/video.amp")
    python detect_and_track.py --source "your IP Camera Stream URL" --device 0

    #for specific class (person)
    python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --classes 0

    #for colored tracks 
    python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --colored-trk

    #for saving tracks centroid, track id and bbox coordinates
    python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --save-txt --save-bbox-dim
    ```

6. Output file will be created in the `working-dir/runs/detect/obj-tracking` with original filename.


### Results



 ### References
 - https://github.com/WongKinYiu/yolov7
 - https://github.com/abewley/sort

