# Computer Vision: How Computers See the World Around Us

A small set of hands-on demos for an intro-to-computer-vision guest lecture.
Each notebook shows one idea, live in code, using the **same photo** (`demos/demo.jpg`,
a baby and a cat playing with a colorful ball) so you can watch the picture travel
from raw numbers all the way to a conversation about the scene.

The slides that these demos accompany are in `computer-vision-how-computers-see.pdf`.

## The demos

| # | Notebook | Idea | Tools |
|---|----------|------|-------|
| 2 | [`demos/02-image-as-numbers.ipynb`](demos/02-image-as-numbers.ipynb) | An image is just a grid of numbers | OpenCV, NumPy, Matplotlib |
| 3 | [`demos/03-image-classification.ipynb`](demos/03-image-classification.ipynb) | "What is in this image?", one label out | 🤗 Transformers (ResNet-50) |
| 4 | [`demos/04-object-detection.ipynb`](demos/04-object-detection.ipynb) | "What objects, and where?", labelled boxes | RF-DETR + Supervision |
| 5 | [`demos/05-object-segmentation.ipynb`](demos/05-object-segmentation.ipynb) | "Which exact pixels?", masks + background blur | RF-DETR (seg) + Supervision |
| 6 | [`demos/06-image-understanding.ipynb`](demos/06-image-understanding.ipynb) | "What's going on?", ask the image questions | 🤗 Transformers (SmolVLM2-500M) |

Run them in order; each one motivates the next.

## Getting started

This project uses [**uv**](https://docs.astral.sh/uv/) to manage the Python
environment. If you don't have it yet:

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Sync the environment

From the repository root, one command installs the right Python (3.12) and every
dependency into a local `.venv/`:

```bash
uv sync
```

### Run the notebooks

Launch Jupyter through uv so it uses the synced environment:

```bash
uv run jupyter lab
```

Then open any notebook under `demos/` and run the cells top to bottom.
