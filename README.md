# OpenVINO Video Processing

This project demonstrates how to process video files using OpenVINO for object detection, including functionality to blur detected objects. The script allows customization of the input video path, output video path, inference device, detection threshold, and model XML path through command-line arguments.

## Requirements

- Python 3.9+
- OpenCV
- OpenVINO 2024.0.0

## Installation

First, ensure that you have Python 3.9 or newer installed. You can download Python from [python.org](https://www.python.org/).

Next, install the required Python packages using pip:

```bash
pip install opencv-python
pip install openvino==2024.0.0
```

## Usage

To use this script, you need to provide at least the path to the input video. Other parameters such as output video path, device, threshold, and model XML path are optional.

```bash
python faceblur.py --input_video path/to/input.mp4 [--output_video path/to/output.mp4] [--device CPU] [--threshold 0.28] [--model_xml path/to/model.xml]
```

### Arguments

- `--input_video`: Path to the input video file. This argument is required.
- `--output_video`: Path for saving the processed output video file. Default is `output_video.mp4`.
- `--device`: Inference device name, e.g., `CPU`, `GPU`. Default is `CPU`.
- `--threshold`: Confidence threshold for detection. Default is `0.28`.
- `--model_xml`: Path to the OpenVINO model XML file. Default is `model.xml`.

### Example Command

```bash
python video_processing.py --input_video my_video.mp4 --output_video processed_video.mp4 --device CPU --threshold 0.4 --model_xml face-detection-retail-0005.xml
```

### Other models
You may download many face detection model from openvino model zoo or using omz_downloader command. Every models is created for different accuracy and speed requirement.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
