<div style="height: 90pt;"></div>
<div style="flex: 0 0 16%; margin-top: -10pt;">
<img src="https://avatars.githubusercontent.com/u/26833451?s=200&v=4" width="100px">
</div>
<div style="flex: 0 0 65%; text-align: center;">
<h1 style="margin-bottom: 10pt;">Demo: YoloV5</h1>
<h2>A demo of YoloV5 model using Lightning App</h2>
</div>
<div style="flex: 1">
    <div style="display: flex; align-items: center;">
        <img style="height: 20pt; width: 20pt; margin: 5pt;" src="icons/fontawesome/brands/github.svg">
        <div style="font-size: 0.9rem; margin-right: 5pt;"><a href="https://github.com/ultralytics/">Ultralytics</a></div>
    </div>
    <div style="display: flex; align-items: center;">
        <img style="height: 20pt; width: 20pt; margin: 5pt;" src="icons/fontawesome/brands/twitter.svg">
        <div style="font-size: 0.9rem;"><a href="https://twitter.com/ultralytics">@ultralytics</a></div>
    </div>
</div>

--split--

# YoloV5

## YOLOv5 in PyTorch > ONNX > CoreML > TFLite

This app is a research poster demo of YoloV5 Object Detection model by Ultralytics. It showcases a notebook, a blog, and
a model demo where you can upload photos to get a bounding box visualized output image.

> Thanks to [Ultralytics](https://github.com/ultralytics/yolov5) for open-sourcing this fantastic library.


To create a research poster for your work please
use [Lightning Research Template app](https://github.com/Lightning-AI/lightning-template-research-app).
You can fork this app and edit to customize according to your need.


<img src="https://github.com/ultralytics/yolov5/releases/download/v1.0/splash.jpg">

YOLOv5 🚀 is a family of object detection architectures and models pretrained on the COCO dataset, and represents
Ultralytics open-source research into future vision AI methods, incorporating lessons learned and best practices evolved
over thousands of hours of research and development.

--split--

# Lightning Apps

## Lightning Apps can be built for any AI use case, including AI research, fault-tolerant production-ready pipelines, and everything in between.

!!! abstract "Key Features"

    - **Easy to use-** Lightning apps follow the Lightning philosophy- easy to read, modular, intuitive, pythonic and highly composable interface that allows you to focus on what's important for you, and automate the rest.
    - **Easy to scale**- Lightning provides a common experience locally and in the cloud. The Lightning.ai cloud platform abstracts the infrastructure, so you can run your apps at any scale. The modular and composable framework allows for simpler testing and debugging.
    - **Leverage the power of the community-** Lightning.ai offers a variety of apps for any use case you can use as is or build upon. By following the best MLOps practices provided through the apps and documentation you can deploy state-of-the-art ML applications in days, not months.

```mermaid
graph LR
    A[local ML]
    A --> B{<b>Lightning Apps</b><br>Effortless GPU distributed compute}
    B -->|Frontend| C[Lightning Work 1]
    B -->|DB integration| D[Lightning Work 2]
    B -->|User auth| E[Lightning Work 3]
```

### Available at : `Lightning-AI/lightning-template-research-app/app.py`

```python
import lightning as L

poster_dir = "resources"
blog = "https://ultralytics.com/yolov5"
github = "https://github.com/ultralytics/yolov5"
training_logs = (
    "https://wandb.ai/glenn-jocher/yolov5_tutorial/reports/"
    "YOLOv5-COCO128-Tutorial-Results--VmlldzozMDI5OTY?galleryTag=intermediate"
)
tabs = ["Notebook Viewer", "Poster", "training logs", "Blog", "Model Demo"]

app = L.LightningApp(
    ResearchApp(
        poster_dir=poster_dir,
        blog=blog,
        github=github,
        notebook_path="resources/demo.ipynb",
        training_log_url=training_logs,
        launch_gradio=True,
        tab_order=tabs,
        launch_jupyter_lab=False,  # don't launch for public app, can expose to security vulnerability
    )
)
```

### Citation

```bibtex

@article{YourName,
  title={Your Title},
  author={Your team},
  journal={Location},
  year={Year}
}

```
