# StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks

This repository provides an implementation of StackGAN, a model for text-to-image synthesis using stacked generative adversarial networks. The implementation is based on the paper [StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks](https://arxiv.org/pdf/1612.03242v1.pdf) by Han Zhang et al.

![Framework](examples/framework.jpg)

## Dependencies

- Python 2.7
- TensorFlow 0.12

The following optional dependencies are needed if you want to use additional features:
- Torch (for pre-trained char-CNN-RNN text encoder)
- skip-thought (for skip-thought text encoder)

To install the required packages, add the project folder to your PYTHONPATH and use pip to install the following packages:
- prettytensor
- progressbar
- python-dateutil
- easydict
- pandas
- torchfile

## Dataset

To create the dataset for training, follow these steps:

1. Download the preprocessed char-CNN-RNN text embeddings for birds and flowers and save them to the `Data/` directory. You can download them from the following links:
   - [Birds Text Embeddings](https://drive.google.com/open?id=0B3y_msrWZaXLT1BZdVdycDY5TEE)
   - [Flowers Text Embeddings](https://drive.google.com/open?id=0B3y_msrWZaXLaUc0UXpmcnhaVmM)

2. Download the bird and flower image datasets and extract them to the `Data/birds/` and `Data/flowers/` directories, respectively. You can find the download links in the original paper.

3. Preprocess the images using the provided scripts:
   - For birds: `python misc/preprocess_birds.py`
   - For flowers: `python misc/preprocess_flowers.py`

## Training

To train the StackGAN model, follow these steps:

1. Train the Stage-I GAN for the desired number of epochs:
2. Train the Stage-II GAN for the desired number of epochs:
3. 
You can adjust the configuration file (`*.yml`) to train the model on different datasets or with different settings.

## Pretrained Model

Pretrained models are available for both birds and flowers. Download the models from the following links and save them to the `models/` directory:
- [StackGAN for birds](https://drive.google.com/open?id=0B3y_msrWZaXLNUNKa3BaRjAyTzQ)
- [StackGAN for flowers](https://drive.google.com/open?id=0B3y_msrWZaXLX01FMC1JQW9vaFk)

Additionally, a StackGAN model trained on skip-thought text embeddings for birds is also available. Download it from the following link and save it to the `models/` directory:
- [StackGAN for birds (skip-thought)](https://drive.google.com/open?id=0B3y_msrWZaXLZVNRNFg4d055Q1E)

Please note that the skip-thought model uses the same settings as the char-CNN-RNN model.

## Running Demos

To generate image samples from sentences, you can use the provided demo scripts:

- Flowers Demo: `sh demo/flowers_demo.sh`
- Birds Demo: `sh demo/birds_demo.sh`
- Birds Skip-Thought Demo: `python demo/birds_skip_thought_demo.py --cfg demo/cfg/birds-skip-thought-demo.yml --gpu 2`

Please make sure to download the necessary text encoders and follow the instructions provided in the respective demo scripts.

## Examples

Here are some examples of images generated by the StackGAN models:

Birds (char-CNN-RNN embeddings):
![Bird Example 1](examples/bird1.jpg)
![Bird Example 2](examples/bird2.jpg)
![Bird Example 3](examples/bird3.jpg)
![Bird Example 4](examples/bird4.jpg)

Flowers (char-CNN-RNN embeddings):
![Flower Example 1](examples/flower1.jpg)
![Flower Example 2](examples/flower2.jpg)
![Flower Example 3](examples/flower3.jpg)
![Flower Example 4](examples/flower4.jpg)

Feel free to save your favorite pictures generated by our models!

## Citing StackGAN

If you find StackGAN useful in your research, please consider citing the original paper:



