# Consistent image generation using Stable diffusion XL.

This repository contains unofficial PyTorch code for the paper [The Chosen One: Consistent Characters in Text-to-Image Diffusion Models](https://arxiv.org/abs/2311.10093), implemented using the Diffuser framework. The goal of this project is to enhance the existing pipeline and leverage lightweight models for more efficient image generation.

## TODO List
- [x] Code release.
- [ ] Release models
- [x] Training instructions.
- [x] Inference instructions.
- [ ] Replace text to image model with lightweight and efficient models.
- [ ] Change the euclidean distance to cosine similarity.
- [ ] Replace the DINO V2 model with state of the art models.

## Getting Started

### Installation and Prerequisites
Install diffuser `0.24.0.dev0`:
```
git clone https://github.com/huggingface/diffusers
cd diffusers
pip install .
```

Clone the repository and install the required packages:
```
https://github.com/chinmayembedded/consistent_image_generation.git
cd consistent_image_generation
pip install -r requirements.txt
```
You also need to modify your configuration file in `config/theChosenOne.yaml` to fit your local environment.

### Data backup folder preparation
You need to create a backup data folder to store the initial images generated in the first loop for faster training start up next time if you want to train on the same character again.
This is set up in the configuration file as follows:
``` 
backup_data_dir_root: Your absolute path to the data folder
```

## Run the codes
### Training
```
python main.py
```

### Inference
Simply run:
```
python inference.py
```
The script will load the model you designated in the `inference.py` and your config file.


### Citing the paper
Please always remember to respect the authors and cite their work properly. 🫡
```
@article{avrahami2023chosen,
  title={The Chosen One: Consistent Characters in Text-to-Image Diffusion Models},
  author={Avrahami, Omri and Hertz, Amir and Vinker, Yael and Arar, Moab and Fruchter, Shlomi and Fried, Ohad and Cohen-Or, Daniel and Lischinski, Dani},
  journal={arXiv preprint arXiv:2311.10093},
  year={2023}
}
```
