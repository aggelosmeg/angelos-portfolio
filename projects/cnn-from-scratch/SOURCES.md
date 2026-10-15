# Sources – cnn-from-scratch (not published)

Built 2026-10-11 from the old-laptop hand-off `website-handoff/cnn-from-scratch/`
(original folder: `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\Angelos Mengoudis Data Science Projects\B4-CNN`).
The full hand-off notes are copied below; they map every fact and image to its source file.

## Used on the page
- Images (from `images/individual/`): galaxy-elliptical-01, galaxy-cigar-shaped-03 (also card cover),
  inversion-kernel-sizes, classifier-two-layer-loss, kernel-two-layer-first, kernel-two-layer-second,
  galaxy-saved-misclassification.
- The confusion-matrix numbers are shown as a table instead of the redrawn image.
- Year 2025: from Angelos's CV ("CNN from scratch (Python) – 2025").
- Validation losses rounded to 2 decimals (0.641542, 0.331755, 0.480683).

## Still placeholders / open questions
- Exact course credit (and whether to credit the assignment author).
- Galaxy dataset name, credit and licence.
- Code: publish on GitHub? Link.
- Featured on homepage? (it already appears there from the brief's list; currently linked).
- May the figures and description be public?

---

---
title: "Convolutional Neural Network from Scratch"
slug: "cnn-from-scratch"
kind: project
year: null
status: completed
category: "Programming & Computational Methods"
tags: [Python, NumPy, CNN, Backpropagation, Galaxy classification]
summary: "I built a convolutional neural network from scratch in Python and NumPy to understand how image models learn. I tested image inversion and binary galaxy classification, comparing model depth, kernels, and learning rates."
featured: false
cover_image: images/individual/galaxy-cigar-shaped-03.png
source_folder: "C:\\Users\\Aggelos\\Desktop\\1st Semester\\Astrophysics & Data Science\\Angelos Mengoudis Data Science Projects\\B4-CNN"
---

## Overview
I wanted to understand how a convolutional neural network learns, from the convolution operation to the parameter updates. I built the model from scratch with NumPy, then used it to invert images and distinguish elliptical from cigar-shaped galaxies.

## Context
Astrophysics & Data Science coursework. Angelos identified `Angelos Mengoudis Data Science Projects/B4-CNN` as the likely final submission folder after assignment changes; it is the primary source for this handoff. The earlier `Convolution/` folder contains the handwritten-digit work and assignment handouts. The galaxy handout is credited to Yannick Eyholzer and dated December 2, 2025. The completion year remains unconfirmed.

## My role
I implemented the project from scratch, including the convolution and padding operations, model structure, forward pass, activation functions and derivatives, loss functions, backpropagation, parameter updates, and training loops. I also prepared the images and compared model configurations. Angelos confirmed in this conversation that he did essentially all the implementation; the assignment supplied the task and theoretical framework.

## Methods and tools
- Python and NumPy for the numerical implementation; Jupyter notebooks for experiments; Matplotlib for figures and pandas for displaying confusion matrices.
- A configurable `Model2D` class, with kernels and padding specified per layer.
- Identity, ReLU, sigmoid, and hard-tanh activations; mean squared error for inversion and binary cross-entropy for classification.
- Galaxy images from the supplied `galaxymnist31RGB.npz` archive. I selected classes 0 and 1, leaving 3,987 images of 31 x 31 RGB pixels, normalized each image with a z-score, and converted it to greyscale.
- A shuffled split of 3,189 training images and 798 validation images. Classification runs sampled 1,000 training images and 500 validation images per epoch. The selected inversion comparisons used 200 and 50 respectively.

## Process
I first explored the operations and sanity checks with handwritten-digit images. In the later galaxy experiments, I tested the mapping from each image to its negative, varying learning rate, kernel size, and layer count. I then adapted the model for binary classification: a final convolution without padding reduced the image to one scalar, followed by a sigmoid activation. I compared one-, two-, and three-layer classifiers and inspected their learned kernels and misclassified examples.

## Results and visuals
For inversion, the saved notes report that a simple linear model was sufficient and that larger models did not improve this task in the tested configurations. One saved one-layer, 3 x 3 run reached a validation mean squared error of approximately 0.000023 after five epochs (learning rate 0.1, 200 training and 50 validation samples per epoch).

For galaxy classification, the final saved confusion matrices give the following accuracies. These are derived from predictions made on training samples during the last epoch, while parameters were still being updated. They are not held-out validation accuracies. Each matrix contains 1,000 predictions.

| Layers | Epochs | Correct training predictions | Accuracy during last training epoch | Last sampled validation cross-entropy |
|---|---|---|---|---|
| 1 | 100 | 386 + 400 | 78.6% | 0.641542 |
| 2 | 50 | 453 + 434 | 88.7% | 0.331755 |
| 3 | 15 | 424 + 404 | 82.8% | 0.480683 |

I monitored validation loss separately. The final one-layer curve shows a gap between training and validation loss, while the final two-layer run ends with similar training and validation losses. These runs used different epoch counts and sampled subsets, so the table does not establish a controlled ranking of architectures. No fixed-model held-out classification accuracy is recorded in the selected notebooks.

The visuals below lead with the objects and operations, then show the measured results. The digit graphic illustrates convolution; the final classification task uses galaxy images. A saved two-layer prediction shows a galaxy labelled elliptical being predicted as cigar-shaped. I did not retrain the model to manufacture additional predictions.

- `images/cover.png` - Six real galaxy inputs, with elliptical and cigar-shaped dataset labels and a simple processing diagram. Alt text: "Two rows of galaxy images show elliptical and elongated examples beside the steps image, convolution, and class score." These are dataset labels, not individual model predictions.
- `images/digit-convolution.png` - The same handwritten 0 and 2 examples used in the earlier notebooks, shown with an illustrative 3 x 3 filter and its computed response. Alt text: "Each digit is followed by a filter with columns minus one, zero, and one, and a coloured map showing the convolution response." This is a new explanatory calculation using the project's convolution function and a fixed filter; it does not depict learned weights or digit classification results.
- `images/learned-kernels.png` - The final two-layer classifier's saved 3 x 3 first-layer kernel and 31 x 31 output kernel, side by side. Alt text: "A small kernel with contrasting weights sits beside a larger heatmap concentrated near its centre." These are the original embedded kernel plots, not reconstructed numerical weights.
- `images/classification-example.png` - A saved misclassification with its input image, dataset label elliptical, and printed prediction cigar-shaped. Alt text: "A compact galaxy image is labelled elliptical, while the two-layer classifier's saved prediction is cigar-shaped."
- `images/classification-confusion.png` - The final two-layer training-epoch confusion matrix, redrawn with class names. Alt text: "A two-by-two matrix has counts 453, 72, 41, and 434, with predicted labels in rows and dataset labels in columns." It records 887 correct predictions out of 1,000 during training, not validation accuracy.
- `images/classification-two-layer-loss.png` - The final two-layer classifier's saved loss curves over 50 epochs. Alt text: "Training and validation cross-entropy decrease together to about one third."
- `images/inversion-kernel-comparison.png` - The final inversion notebook's saved comparison of 1 x 1, 3 x 3, 5 x 5, and 7 x 7 kernels. Alt text: "Five-epoch logarithmic loss curves show the one-by-one kernel reaching the lowest plotted loss."

## Individual images (preferred)
Angelos prefers individual images over collages. Use the files in `images/individual/` as the primary visual selection. The earlier composed graphics remain optional alternatives.

- `galaxy-elliptical-01.png` to `galaxy-elliptical-03.png`: individual elliptical galaxy inputs.
- `galaxy-cigar-shaped-01.png` to `galaxy-cigar-shaped-03.png`: individual cigar-shaped galaxy inputs.
- `digit-0.png`, `digit-1.png`, `digit-2.png`: individual handwritten digits from the earlier work.
- `kernel-one-layer.png`, `kernel-two-layer-first.png`, `kernel-two-layer-second.png`, and the three `kernel-three-layer-*.png` files: original saved kernel plots, one per file.
- `galaxy-saved-misclassification.png`: original saved image figure, with its original true-label title. The corresponding notebook prints predicted label 1 (cigar-shaped), while the displayed true label is 0 (elliptical).
- Remaining files are individual original notebook plots, including loss curves and inversion comparisons.

Raw input exports contain only the image pixels, with no titles, borders, or added text. Dataset class labels in filenames are annotations, not new predictions. The notebook plots retain their original axes and titles. `images/individual/SOURCES.md` maps every file to its source.

## Files and links
- Code remains in the primary `B4-CNN` source folder. PLACEHOLDER - public repository URL and permission to publish the code. No code folders, notebooks, datasets, or caches are copied.
- No final report PDF is present in that folder. The older PDFs are instructor-authored assignment handouts and are not packaged.
- The earlier `Answers.docx` remains referenced locally and is not copied; its values describe older experiments.
- Angelos requested the digit, kernel, and classification visuals for this local handoff. Dataset licence/credit details and final publication approval remain open; nothing has been uploaded.
- `ASSET_SOURCES.md` records the exact source cells, dataset selections, and explanatory-filter calculation for the new graphics.

## Source map
Paths without a prefix below are relative to the primary `source_folder`. `Earlier/` means the full earlier folder `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\Convolution`. Notebook cell numbers are zero-based.

| Fact or image | Came from (file path) |
|---|---|
| Personal implementation and preferred final folder | Angelos, this conversation, 2026-10-11 |
| Assignment author/date and class names | `Earlier/B4) Convolutional Network from scratch-20251217/instruction.pdf`, pp. 1, 10 |
| Early MNIST work and sanity checks | `Earlier/conv notebook.ipynb`, cells 3-9, 43-55; `Earlier/convolution_functions.py` |
| Model, forward/backward passes, and training | `model.py`, `convolution.py`, `activations.py`, `loss.py` |
| Dataset preparation, counts, and split | `3.classification.ipynb`, cells 5, 7-8 |
| Inversion configuration, saved loss, and interpretations | `2.inversion.ipynb`, cells 9, 11-12, 16, 20, 24 |
| Final classification runs and saved validation losses | `3.classification.ipynb`, cells 9, 13, 18 |
| Training confusion matrices | `3.classification.ipynb`, cells 11, 16, 22; `model.py`, `train_model_classification` |
| Cover input images | `galaxymnist31RGB.npz`; shuffle/filter from `3.classification.ipynb`, cells 5, 7; selected indices in `ASSET_SOURCES.md` |
| Digit examples and convolution calculation | `Earlier/MNIST10sample.npz`; shuffle 42 and position 10 from `Earlier/conv notebook.ipynb`, cells 4-5; position 5 from `Earlier/playing.ipynb`, cells 4-5; final `convolution.py`, functions `conv2d` and `padding` |
| Learned kernels | `3.classification.ipynb`, cells 14-15, embedded PNGs |
| Actual saved input and prediction | `3.classification.ipynb`, cell 23, embedded PNG titled true label 0 and printed prediction 1 |
| Confusion graphic | `3.classification.ipynb`, cell 16, counts `[[453, 72], [41, 434]]`; 88.7% derived as `(453 + 434) / 1000` |
| Two-layer loss figure | `3.classification.ipynb`, cell 13, embedded PNG |
| Inversion kernel-size figure | `2.inversion.ipynb`, cells 18-19, embedded PNG in cell 19 |

## Placeholders
- PLACEHOLDER - completion year; `year: null` until confirmed.
- PLACEHOLDER - homepage feature choice; `featured: false` until Angelos requests otherwise.
- PLACEHOLDER - publication approval and public code link.
- PLACEHOLDER - final report availability and exact formal course/institution attribution.

## Questions for Angelos
- What completion year should be displayed?
- Is any material private, and may the selected figures and project description be published? What dataset credits/licence text should be included?
- Should this project be featured on the homepage?
- Is there a final report or presentation beyond the files in this folder, and may it be published?
- Do you want to publish the code, and is there already a repository link?
- What is the exact course/institution credit you want displayed?

---

## Revision 2026-10-11 (simpler, idea-first page)
Angelos asked for a simpler page: show that he built it from scratch, explain the idea and the components, no metrics.
- Source re-checked directly: `website-handoff/semester 1/B4-CNN/` (model.py, convolution.py, activations.py, loss.py, 1.CNN.ipynb, 2.inversion.ipynb, 3.classification.ipynb).
- Final task confirmed as galaxy classification (elliptical = class 0, cigar-shaped = class 1). Digits were only early sanity checks in a separate folder.
- Pipeline diagram = the 2-layer model in 3.classification.ipynb cell 13: kernels [3, 31], padding [1, 0], ReLU then sigmoid.
- Component cards: convolution.py (conv2d, padding), activations.py, model.py (Model2D, backward, training loops), loss.py; hand derivations in 1.CNN.ipynb cells 14–23; learning-rate tuning in 2.inversion.ipynb cells 13–16.
- Kernel captions: 3.classification.ipynb cell 17 notes. Failure causes (small/ambiguous galaxies): cell 24.
- Personal note: Angelos's own words in conversation ("a good project where I learned how to do something difficult, that was out of my reach").
- Removed from the page: results table, loss curve, inversion kernel-size plot.

## Revision 2 – 2026-10-11 (Angelos's own story)
Text now based on Angelos's answers in conversation:
- Hardest project offered in the data science course; chose it after enjoying 3Blue1Brown (convolution) and "Sebastian …" (neural networks) videos – surname "Lague" is Claude's guess, marked to confirm.
- First time coding something this complete; breaking it into steps made it make sense.
- Backpropagation was the moment it clicked ("why am I doing this exactly?").
- Looking back: "build something with your own hands"; would do the math and plan on pen and paper first.
- Learned coding skills incl. classes – verified: `Model2D` class in model.py.
- Ten-second takeaway → page summary line.
- No code on the page, no GitHub link (his choice). Assignment credit to Yannick Eyholzer approved.
- Equation δ^{l-1} = δ_p^l ∗ rot180(K^l): heading of 1.CNN.ipynb cell 16.
- Removed the eight icon cards (felt AI-made); replaced with a plain list.
