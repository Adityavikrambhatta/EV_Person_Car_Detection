# Object Detection for People and Cars

This project implements an object detection model using YOLOv5 to detect people and cars in images. It's designed to work with the COCO dataset format.

## Project Structure

```
project_root/
│
├── data/
│   ├── annotations/
│   │   └── bbox-annotations.json
│   └── images/
│          ├── image_000000001.jpg
│          ├── image_000000002.jpg
│          └── ...
├── src/
│   ├── __init__.py
│   ├── config.py
│   ├── dataset.py
│   ├── model.py
│   ├── train.py
│   ├── evaluate.py
│   └── utils.py
│
├── notebooks/
│   └── exploratory_data_analysis.ipynb
│
├── tests/
│   ├── __init__.py
│   ├── test_dataset.py
│   └── test_model.py
│
├── requirements.txt
├── README.md
└── main.py
```

## Setup

1. Clone this repository:
   ```
   git clone https://github.com/Adityavikrambhatta/Assessment-YoloV8/tree/develop/V1/src
   cd object-detection-people-cars/V1
   ```

2. Create a virtual environment and activate it:
   ```
    conda create --name myenv python=3.x
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Download the dataset and place it in the `data_set/` directory.

## Usage

To train the model:
```
python main.py --mode train --config config.yaml
```

To evaluate the model:
```
python main.py --mode evaluate --config config.yaml
```

To run inference on a single image:
```
python main.py --mode inference --config config.yaml --image_path path/to/your/image.jpg
```

## Configuration

You can modify the `config.yaml` file to change various parameters such as batch size, learning rate, etc.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

- This project uses the YOLOv8 model implemented by Ultralytics.
- The dataset is derived from OpenImages, with annotations licensed under CC BY 4.0 and images under CC BY 2.0.
