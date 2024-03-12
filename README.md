<a name="readme"></a>

<!-- [![Contributors][contributors-shield]][contributors-url] -->
<!-- ![Python][python-shield] -->
![Python 3.8](https://img.shields.io/badge/Python-3.8-blue.svg)



<!-- GETTING STARTED -->

# MediaPipe Pose to OpenPose JSON Generator
## Info

Mediapipe pose extraction and exporting to OpenPose format but Mediapipe has 33 keypoints as output as compared to 25 from Openpose. The keypoints also have a different order.
The code in this repository has three scripts:
- `mediapipe_JSON.py` :  extracts the keypoints from all images in a folder and exports them as an Openpose JSON format with 25 keypoints. The JSON is compaitble with SMPLify-X for 3D shape extraction.
- `plot_json.py` : plots the OpenPose keypoints and saves the image.
- `gui.py` : GUI (made in [CustomTkinter](https://customtkinter.tomschimansky.com)) for the above two scripts, that displays the Mediapipe keypoints on the loaded image as well as the generated OpenPose keypoints. **Note that each of the scripts can be run independently and the GUI is not required to be run.** But running the GUI simplifies the process of running the scripts.
- `test-path.py`: script to test if the path in the config file is correct.  If [] there are no files with the extensions available, otherwise, test_img_path in the config.yaml is correct


![Rofi](./src//GUI.png "GUI Window" )

## Other features:
- Uses Hydra.cc for config
- Supports only 1 person per frame (Mediapipe limitation)
- Supports multiple image extensions in folder (PNG, JPG, JPEG etc)
- Each script can be run separately, gui is optional

## Requirements
To install all the required packages: `pip install -r requirements.txt`

Ensure correct version of tkinter:
Ubuntu/Debian:
    For system wide:  sudo apt install python3-tk -y  
    For venv:  sudo apt-get install python3.8-tk
        where 3.8 is the version to install 

## ToDo:
- [ ] Image overlay for OpenPose JSON plot
- [ ] Better GUI scaling for different screen sizes and images

<!--Reference to the original repo-->
This is a copy of the the repo found here <a href="https://github.com/Atif-Anwer/Mediapipe-to-OpenPose-JSON">Mediapipe-to-OpenPose-JSON</a> but uses python 3.8
