# Crop White Backgrounds from Photos

This Python script automatically crops white (or near-white) backgrounds from scanned or photographed images. It handles scanner dust and tiny specks by using a density-based approach, ensuring only the real photo content is kept.

All cropped images are saved into a **`cropped`** folder inside the input folder.

---

## Features

- Crop white/near-white backgrounds from scanned photos.
- Ignores scanner dust and tiny specks.
- Supports batch processing using folders or glob patterns.
- Saves all outputs in a `cropped` folder automatically.
- Adjustable `threshold`, `padding`, and `min-density` parameters.

---

## Requirements

- Python 3.8+
- [Pillow](https://pypi.org/project/Pillow/) ≥ 9.0.0
- [NumPy](https://pypi.org/project/numpy/) ≥ 1.22.0

Install dependencies via pip:

```bash
pip install -r requirements.txt

```

Usage:

```bash

# Crop a single image
python crop_white_background.py photo/image1.jpg

# Crop a single image with custom parameters
python crop_white_background.py photo/image1.jpg --threshold 220 --padding 20 --min-density 30

# Crop all JPEG images in a folder using glob pattern
python crop_white_background.py photo/*.jpg

# Crop all images in a folder using --folder
python crop_white_background.py --folder photo/
