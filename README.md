# Sofa vs Table Image Classifier

A small deep learning project that tells whether a photo shows a **sofa** or a **table**. Built while following lesson 1 of [Practical Deep Learning for Coders](https://course.fast.ai/) (fast.ai), with my own classes and images.

## Results

- Validation error rate: **0.154** (about 85% accuracy)
- Three new test photos were all classified correctly:

| Test image | Model answer | Probability of "sofa" |
|---|---|---|
| sofa.jpg | sofa | 0.6929 |
| sofa2.jpg (different sofa) | sofa | 0.8252 |
| table1.jpg | table | 0.1165 |

## How it works

1. Download images for each class from DuckDuckGo and remove broken files.
2. Fine-tune a pretrained `resnet18` model with `fastai` (80% training / 20% validation).
3. Test the model on new photos.

**Tech:** Python, fastai, PyTorch, Jupyter notebook, Kaggle (free GPU).

## How to run

Import the notebook into [Kaggle](https://www.kaggle.com/) (or Google Colab), turn on Internet and GPU in the settings, and run all cells. If the image download fails because of rate limits, wait a few minutes and try again.

## Limitations

- Very small dataset: 33 images per class, so the validation set has only ~13 images and results change between runs.
- Only two classes: a photo of a chair or a bed will still be labeled "sofa" or "table".
- Only three test photos were checked by hand, and all of them were clean, easy images.

## What I learned

- How a full image classification pipeline works: data collection, cleaning, training and testing.
- Fine-tuning a pretrained model gives usable results with very little data.
- A high predicted probability does not always mean a correct answer.

## Next steps

Collect more images and add more classes (for example chair and bed).
