# Course: PyTorch: Fundamentals - https://www.coursera.org/learn/pytorch-fundamentals/home

# NLP-Pytorch01-Basics — Notebook Summary

This README maps each notebook in `NLP-Pytorch01-Basics` 

- M1-L1 : [Modeling Non-Linear Patterns with Activation Functions](M1-L1/C1_M1_Lab_2_activation_functions.ipynb)
  - Introduces activation functions (ReLU, etc.) and why non-linearity matters.
  - Covers normalization and preparing targets for regression-like tasks.
  - Builds a small neural network, runs a training loop, and visualizes training/predictions.
  > Top heading (from notebook): "Modeling Non-Linear Patterns with Activation Functions"
  - Technical details & techniques: `torch.nn` module usage (`nn.Linear`, activation layers), loss computation with `nn.MSELoss`, optimizer steps (`torch.optim.SGD`/`Adam`), manual training loop (`forward` → `loss.backward()` → `optimizer.step()`), basic plotting of predictions vs targets for diagnostics.

- M1-L2 : [Tensors: The Core of PyTorch](M1-L2/C1_M1_Lab_3_tensors.ipynb)
  - Covers tensor creation, shapes, reshaping and broadcasting rules.
  - Demonstrates indexing, slicing, and basic tensor arithmetic.
  - Shows simple statistics and operations used in model pipelines.
  > Top heading (from notebook): "Tensors: The Core of PyTorch"
  - Technical details & techniques: `torch.tensor` creation and dtypes, tensor device management (`.to(device)`), broadcasting semantics, `view()`/`reshape()` for shape manipulation, in-place vs out-of-place ops, simple use of `torch.autograd` for gradient tracking examples.

- M1-A : [Programming Assignment: Deeper Regression, Smarter Features](M1-A/C1M1_Assignment.ipynb)
  - End-to-end regression assignment using a CSV multi-feature dataset.
  - Focus on feature engineering (e.g., rush-hour features) and data pipeline.
  - Build and train a 2-hidden-layer network; autograder tests verify correctness.
  > Top heading (from notebook): "Programming Assignment: Deeper Regression, Smarter Features"
  - Technical details & techniques: data ingestion with `pandas`, `torch.utils.data.Dataset`/`DataLoader` wrappers for CSV datasets, feature normalization, constructing `nn.Module` models, evaluation metrics (MSE/R2), and using unit-test hooks/autograder compatibility for assignment grading.

- M2-L1 : [Building Your First Image Classifier](M2-L1/C1_M2_Lab_1_mnist_classifier.ipynb)
  - Loads MNIST, applies transforms, and uses DataLoader for batching.
  - Defines a simple nn.Module image classifier and training/evaluation loops.
  - Demonstrates training, validation, and basic model evaluation.
  > Top heading (from notebook): "Building Your First Image Classifier"
  - Technical details & techniques: `torchvision.datasets` & `transforms` pipeline (`ToTensor`, `Normalize`), `DataLoader` batching and `shuffle`, model definition with `nn.Conv2d`/`nn.Linear`, `nn.CrossEntropyLoss`, GPU transfer (`.to(device)`), and basic accuracy computation.

- M2-A : [Programming Assignment: EMNIST Letter Detective](M2-A/C1M2_Assignment.ipynb)
  - Work with the EMNIST Letters split: download, orient, normalize, convert to tensors.
  - Implement `create_emnist_dataloaders`, model initialization, training and evaluation helpers.
  - Includes decoding a secret handwritten message and unit-test/autograder hooks.
  > Top heading (from notebook): "Programming Assignment: EMNIST Letter Detective"
  - Technical details & techniques: dataset transforms for image orientation/normalization, custom `Dataset` wrappers, augmentation for handwritten variants, model initialization patterns, checkpointing and autograder-friendly I/O/testing scaffolding.

- M3-L1 : [Data Management](M3-L1/C1_M3_Lab_data_management.ipynb)
  - Teaches custom `Dataset` classes, transforms, and robust loading patterns.
  - Covers data augmentation, error handling, and monitoring dataset behavior.
  - Shows how to compute dataset statistics (mean/std) required for normalization.
  > Top heading (from notebook): "Data Management"
  - Technical details & techniques: implementing `torch.utils.data.Dataset` and `collate_fn`, deterministic shuffling and seeding, computing dataset mean/std for `Normalize`, augmentation pipelines (`RandomCrop`, `RandomFlip`), and debugging data-loading bottlenecks with `num_workers` and profiling.

- M3-A : [Programming Assignment: Building a Robust Data Pipeline](M3-A/C1M3_Assignment.ipynb)
  - Implement a `PlantsDataset`-style dataset and transformation pipeline.
  - Compute mean/std, design transforms, and implement `get_dataloaders` helpers.
  - Emphasizes reproducible, testable data-loading code for training experiments.
  > Top heading (from notebook): "Programming Assignment: Building a Robust Data Pipeline"
  - Technical details & techniques: packaging data transforms into reusable functions, saving/loading preprocessed shards (optional), deterministic train/val splits, unit-testable `get_dataloaders` signature, and examples of reading/writing Parquet or CSV sources for large datasets.

- M4-L1 : [Building a CNN for Nature Classification](M4-L1/C1_M4_Lab_1_cnn_nature_classifier.ipynb)
  - Introduces a SimpleCNN architecture for a CIFAR-100 subset (nature classes).
  - Demonstrates end-to-end pipeline: data, model, training loop, and metrics.
  - Discusses prototype-first workflow and diagnosing overfitting.
  > Top heading (from notebook): "Building a CNN for Nature Classification"
  - Technical details & techniques: `nn.Conv2d`/`nn.BatchNorm2d`/`nn.MaxPool2d` building blocks, constructing modular CNN blocks, learning rate scheduling (`StepLR`/`ReduceLROnPlateau`), regularization techniques and basic confusion matrix/metric reporting.

- M4-L2 : [Model Debugging, Inspection, and Modularization](M4-L2/C1_M4_Lab_2_debugging.ipynb)
  - Hands-on debugging of a broken CNN: insert prints in `forward` to find shape mismatches.
  - Refactor models using `nn.Sequential` to improve modularity and readability.
  - Inspect activation statistics, count layer types, and analyze parameter distributions (e.g., SqueezeNet).
  > Top heading (from notebook): "Model Debugging, Inspection, and Modularization"
  - Technical details & techniques: debugging strategies (shape assertions, print/log hooks), model introspection (`named_parameters`, `state_dict`), use of `torchsummary`/`summary` for parameter counts, activation histogram inspection and sanity-checking forward passes.

- M4-A : [Programming Assignment - Overcoming Overfitting: Building a Robust CNN](M4-A/C1M4_Assignment.ipynb)
  - Systematic anti-overfitting strategy: stronger augmentation, BatchNorm, Dropout, weight decay.
  - Introduces `CNNBlock` modular design and assembling a `SimpleCNN` from blocks.
  - Implements training/validation loops and best-model selection based on validation accuracy.
  > Top heading (from notebook): "Programming Assignment - Overcoming Overfitting: Building a Robust CNN"
  - Technical details & techniques: augmentation strategies, `nn.Dropout`/`nn.BatchNorm2d`, optimizer weight decay, early stopping & checkpointing best models, reproducible experiment logging (simple CSV or TensorBoard) and evaluation scripts for final model selection.


