# Object-detection-and-tracking
Computer Vision Assignment 2 - Track Object and track it

## Dataset Information
train.csv: contains the frame information like video_id, name, frame_id, path to the image
det.txt (Detections): Contains raw object detections for a sequence. This is the output of a model.
gt.txt (Ground Truth): Contains the "true" annotated positions. It includes a persistent ID for each object to define its trajectory over time. It is annotated by hand.

train.csv: contains the frame information like video_id, name, frame_id, path to the image
test_det.txt (Detections): Contains raw object detections for a sequence. This is the output of a model.

| Value | Name | Description |
| :--- | :--- | :--- |
| 1 | Frame | The frame number (starting from 1). |
| 2 | ID | The unique trajectory ID. In det.txt, this is usually -1 (no association yet). |
| 3-4 | Bounding Box Top-Left | The (x, y) coordinates of the top-left corner of the box. |
| 5-6 | Bounding Box Size | The width and height of the bounding box. |
| 7 | Confidence | In det.txt, this is the detection score. In gt.txt, it serves as an "active" flag (1 = active, 0 = ignore). |
| 8-10 | World Coordinates | Used for 3D tracking. For 2D tracking, these are typically set to -1. |

All the above datasets contain video_id and frame_id. And they can be joined on video_id and frame_id.