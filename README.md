# Autovia

Autovia is a web application for semantic segmentation of road scenes using the CityScapes dataset.

## Installation

Install the Python dependencies:

```bash
pip install -r requirements.txt
```

Install the frontend dependencies:

```bash
cd webserver
npm install
```

## Usage

Run both the frontend and backend:

```bash
./run.sh
```

Or run them separately:

```bash
# Backend
python backend.py --model_weights_path ./weights/model-bnet-2.pth

# Frontend (in another terminal)
cd webserver
npm start
```

## Training

To train the model yourself, download the [CityScapes dataset](https://www.cityscapes-dataset.com/) (requires .edu email). You only need these two files:

- `gtFine_trainvaltest.zip` (241MB) - fine annotations for train/val/test sets
- `leftImg8bit_trainvaltest.zip` (11GB) - left 8-bit images for train/val/test sets

Extract both to `~/data/cityscapes/` and run:

```bash
python train.py
```

## Authors

Ramon Asuncion Batista, Santiago Hernandez, Warren Wang

## References

Based on the tutorial code from [talhaanwarch/youtube-tutorials](https://github.com/talhaanwarch/youtube-tutorials/blob/main/cityscape-tutorial.ipynb).
