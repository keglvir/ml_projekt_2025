# Tiled Diffusion Self-Tiling

A demo using [tiled-diffusion](https://github.com/madaror/tiled-diffusion) to generate self-tiled images with Stable Diffusion. Includes example notebooks and images, and supports CPU-only execution.

---

## Project Structure

```
.
├── dpt_large_huggingface_flattening.ipynb        # Optional additional demo (not required for tiling)
├── tiled_diffusion_self_tiling.ipynb             # ✅ Main notebook to run
├── example_images/
│   ├── input.jpg
│   ├── self_tile_result.png
│   └── sample_640x426.jpeg
├── README.md
└── requirements.txt
```

---

## Setup Instructions
### 1. (Recommended) Create a virtual environment
```
```bash
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Make sure your PyTorch and Diffusers versions are compatible — the ones listed in the notebook were:

```text
torch==2.0.1
diffusers==0.20.2
transformers==4.31.0
xformers==0.0.20
```

> You may need to pin `huggingface_hub==0.16.4` and `accelerate==0.21.0` as well.

---

### 3. Clone the Tiled Diffusion repo

```bash
git clone https://github.com/madaror/tiled-diffusion.git
cd tiled-diffusion
```

---

## How to Run

Use the notebook:

> `tiled_diffusion_self_tiling.ipynb`

Follow the steps inside to:

* Load and resize your input image
* Run the self-tiling generation
* Save and view the resulting tile

For creating a flattened image, better for self tiling if contains texture on 3D surface, use notebook:

> `dpt_large_huggingface_flattening.ipynb`

and use it's output for self-tiling.

---

## Notes

* Running on **CPU** is supported, but very slow.
* For Colab users, switch to **GPU runtime** via `Runtime > Change runtime type > GPU`.
* Compatible with Python 3.9–3.11.

---

## 📄 License

This project integrates with [`tiled-diffusion`](https://github.com/madaror/tiled-diffusion), which is under its own license. Refer to that repo for licensing details.

