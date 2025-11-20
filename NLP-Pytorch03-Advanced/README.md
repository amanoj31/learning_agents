PyTorch Advanced: Topics and Labs - NLP-Pytorch03-Advanced

This README follows the template used in `NLP-Pytorch02-Intermediate/README.md`. Each entry lists the notebook path, top heading (inferred), technical details & techniques, new concepts introduced, and practical outcomes.

- M1-L1 : Siamese Networks — `M1-L1/C3_M1_Lab_1_siamese_network.ipynb`
  - Top heading (from notebook): "Siamese Networks for Similarity Learning"
  - Technical details & techniques:
    - Builds a Siamese twin-network architecture using shared-weight CNN encoders.
    - Implements contrastive loss and/or triplet loss for metric learning.
    - Training loop with pair/triplet sampling strategies and hard-negative mining.
    - Evaluation via ROC/AUC on similarity scores and nearest-neighbor retrieval.
  - New concept introduced:
    - Metric learning paradigms (contrastive/triplet losses) and embedding spaces.
  - By the end of this lab you'll be able to:
    - Implement Siamese architectures and train with contrastive/triplet losses.
    - Build pair/triplet samplers and evaluate embedding quality with retrieval metrics.

- M1-L2 : ResNet Finetuning — `M1-L2/C3_M1_Lab_2_resnet.ipynb`
  - Top heading (from notebook): "Fine-tuning ResNet for Downstream Tasks"
  - Technical details & techniques:
    - Loads pretrained ResNet variants from `torchvision.models` and adapts classifier heads.
    - Shows differential learning rates, layer-wise freezing/unfreezing, and regularization.
    - Integration with `torch.optim.lr_scheduler` and AdamW optimizer for fine-tuning.
    - Uses transfer-learning datasets, data augmentation, and validation curves.
  - New concept introduced:
    - Practical nuances of fine-tuning deep pretrained CNNs for new datasets.
  - By the end of this lab you'll be able to:
    - Replace model heads, freeze backbones, and fine-tune ResNet effectively.
    - Tune optimizers and schedulers for stable transfer-learning training.

- M1-L3 : DenseNet Experiments — `M1-L3/C3_M1_Lab_3_densenet.ipynb`
  - Top heading (from notebook): "DenseNet Architectures and Trade-offs"
  - Technical details & techniques:
    - Constructs DenseNet-based models or loads pretrained DenseNet backbones.
    - Demonstrates growth-rate, compression, and transition layers impact on capacity.
    - Benchmarks DenseNet vs ResNet variants on accuracy, parameter count, and FLOPs.
    - Visualization of feature maps and intermediate activations for diagnostic purposes.
  - New concept introduced:
    - Dense connectivity patterns and how feature reuse affects learning and parameter efficiency.
  - By the end of this lab you'll be able to:
    - Configure DenseNet hyperparameters and compare practical trade-offs to other backbones.
    - Use activation visualizations to debug and interpret model behavior.

- M1-A : Advanced Assignment — `M1-A/C3M1_Assignment.ipynb`
  - Top heading (from notebook): "Advanced Model Assignment: Apply and Evaluate"
  - Technical details & techniques:
    - Combines backbone selection, augmentations, and curriculum-training strategies.
    - Implements evaluation pipelines, per-class metrics, confusion matrices, and deployment checks.
    - Includes unit tests or notebooks cells validating expected outputs and metrics.
  - New concept introduced:
    - Project-level integration: dataset design, model selection, reproducible experiments.
  - By the end of this assignment you'll be able to:
    - Complete an end-to-end model experiment and prepare reproducible reports.

- M2-L1 : Visualizing & Interpreting Models — `M2-L1/C3_M2_Lab_1_visualizing_and_interpreting.ipynb`
  - Top heading (from notebook): "Model Interpretability: Saliency, Grad-CAM, and Visual Tools"
  - Technical details & techniques:
    - Implements saliency maps, Grad-CAM, Integrated Gradients for image explanations.
    - Uses guided backprop, occlusion sensitivity and class-activation mapping to diagnose predictions.
    - Tools for visualizing filters, activation distributions, and embedding projections (t-SNE/PCA).
  - New concept introduced:
    - How to interpret model decisions using gradient- and activation-based attribution methods.
  - By the end of this lab you'll be able to:
    - Generate and compare multiple interpretability visualizations to debug mispredictions.

- M2-L2 : Saliency & Class Maps — `M2-L2/C3_M2_Lab_2_saliency_and_class_map.ipynb`
  - Top heading (from notebook): "Saliency Maps and Class Activation Visualizations"
  - Technical details & techniques:
    - Computes class-conditional saliency and overlays heatmaps on input images.
    - Quantifies explanation fidelity and sparsity; compares methods across layers.
    - Automates batch visualization and logging to TensorBoard or Matplotlib exports.
  - New concept introduced:
    - Practical differences between saliency methods and how to measure their usefulness.
  - By the end of this lab you'll be able to:
    - Produce reproducible saliency visualizations and integrate them into model debugging workflows.

- M2-L3 : Stable Diffusion Utilities — `M2-L3/C3_M2_Lab_3_stable_diffusion.ipynb`
  - Top heading (from notebook): "Interfacing with Stable Diffusion and Diffusion Models"
  - Technical details & techniques:
    - Demonstrates running diffusion-based generation pipelines and conditioning mechanisms.
    - Shows prompt engineering, classifier-free guidance, and sampling schedule parameters.
    - Exports and post-processes generated images; discusses safety and model artifacts.
  - New concept introduced:
    - The diffusion sampling loop, noise schedules, and guidance techniques for conditional generation.
  - By the end of this lab you'll be able to:
    - Run stable-diffusion inference pipelines and tune sampling + guidance hyperparameters.

- M2-A : Advanced Transfer Assignment — `M2-A/C3M2_Assignment.ipynb`
  - Top heading (from notebook): "Assignment: Transfer + Interpretation"
  - Technical details & techniques:
    - Mixes transfer-learning with interpretability checks and model compression probes.
    - Exercises include head replacement, partial freezing, and model-size/perf trade-off reporting.
    - Reproducible reporting with plots, metric tables, and exportable artifacts.
  - New concept introduced:
    - Combining transfer learning with downstream validation and interpretability constraints.
  - By the end of this assignment you'll be able to:
    - Deliver a fine-tuned model plus interpretability artifacts and performance trade-offs.

- M3-L1 : Attention Mechanisms — `M3-L1/C3M3_Lab_1_attention.ipynb`
  - Top heading (from notebook): "Attention: Scaled Dot-Product and Variants"
  - Technical details & techniques:
    - Builds scaled dot-product attention from scratch and compares to `nn.MultiheadAttention`.
    - Visualizes attention maps, computes attention heads’ importance, and examines sparsity.
    - Shows positional encodings, masking for causal/structured attention, and complexity analysis.
  - New concept introduced:
    - How attention computes context, multi-head decomposition, and masking strategies.
  - By the end of this lab you'll be able to:
    - Implement attention modules and inspect their behavior on sequence inputs.

- M3-L2 : Encoder Architectures — `M3-L2/C3M3_Lab_2_encoder.ipynb`
  - Top heading (from notebook): "Encoder Blocks and Transformer Encoders"
  - Technical details & techniques:
    - Implements transformer encoder layer stack: attention → add&norm → feedforward → add&norm.
    - Covers layer normalization vs batch norm, residual connections, and initialization effects.
    - Benchmarks encoder depth/width trade-offs and studies training stability techniques (LR warmup, AdamW).
  - New concept introduced:
    - The encoder-only modeling paradigm and its application to classification/representation learning.
  - By the end of this lab you'll be able to:
    - Build and train encoder stacks and apply them to classification or embedding tasks.

- M3-L3 : Decoder Architectures — `M3-L3/C3M3_Lab_3_decoder.ipynb`
  - Top heading (from notebook): "Decoder Blocks, Masking and Autoregressive Generation"
  - Technical details & techniques:
    - Implements causal attention, autoregressive masking, and cross-attention for encoder-decoder setups.
    - Demonstrates teacher-forcing, scheduled sampling, and decoding strategies (greedy, beam search).
    - Measures perplexity and generation quality; inspects exposure bias and mitigation techniques.
  - New concept introduced:
    - Autoregressive decoding mechanics, masking, and practical decoding algorithms.
  - By the end of this lab you'll be able to:
    - Implement decoder blocks and run autoregressive generation with beam search and temperature control.

- M3-A : Transformer Assignment — `M3-A/C3M3_Assignment.ipynb`
  - Top heading (from notebook): "Assignment: Build and Train a Small Transformer"
  - Technical details & techniques:
    - End-to-end dataset preparation, tokenizer use, positional encodings, and model training loop.
    - Exercises include partial-freezing, gradient accumulation, and mixed-precision training experiments.
    - Includes evaluation: BLEU/ROUGE for generation, accuracy/F1 for classification variants.
  - New concept introduced:
    - Holistic transformer training: data, model, optimization, and evaluation trade-offs.
  - By the end of this assignment you'll be able to:
    - Train a small transformer and evaluate it on both generation and classification tasks.

- M4-L1 : MLflow Integration — `M4-L1/C3_M4_Lab_1_mlflow.ipynb`
  - Top heading (from notebook): "Experiment Tracking with MLflow"
  - Technical details & techniques:
    - Demonstrates MLflow tracking API for parameters, metrics, artifacts, and model registry.
    - Shows how to log models, serialize artifacts (plots/checkpoints), and reproduce experiments.
    - Integration examples with training loops and hyperparameter sweeps.
  - New concept introduced:
    - Experiment management and model lifecycle (tracking → registry → deployment artifacts).
  - By the end of this lab you'll be able to:
    - Instrument training code to log experiments and register best models using MLflow.

- M4-L2 : ONNX Export & Inference — `M4-L2/C3_M4_Lab_2_onnx.ipynb`
  - Top heading (from notebook): "Exporting Models to ONNX and Running Inference"
  - Technical details & techniques:
    - Exports PyTorch models to ONNX, inspects ONNX graph, and validates numeric parity.
    - Demonstrates runtime inference with `onnxruntime`, optimizations (graph optimization, quantization-ready export).
    - Shows common pitfalls (dynamic axes, ops not supported, input shapes) and how to debug.
  - New concept introduced:
    - Model portability via ONNX and considerations for production inference runtimes.
  - By the end of this lab you'll be able to:
    - Export models safely to ONNX and run/benchmark inference using `onnxruntime`.

- M4-L3 : Pruning Techniques — `M4-L3/C3_M4_Lab_3_pruning.ipynb`
  - Top heading (from notebook): "Model Pruning: Structured and Unstructured Approaches"
  - Technical details & techniques:
    - Exercises in magnitude-based weight pruning, iterative pruning schedules, and fine-tuning after prune.
    - Compares unstructured vs structured pruning and measures latency/accuracy trade-offs.
    - Integrates pruning with sparsity-aware training and checkpointing for recovery.
  - New concept introduced:
    - How pruning reduces parameter count and inference cost, and the recovery fine-tuning steps required.
  - By the end of this lab you'll be able to:
    - Apply pruning workflows and evaluate their effect on model size and performance.

- M4-L4 : Quantization — `M4-L4/C3_M4_Lab_4_quantization.ipynb`
  - Top heading (from notebook): "Quantization: Post-Training and Quant-Aware Training"
  - Technical details & techniques:
    - Demonstrates post-training static/dynamic quantization and quantization-aware training (QAT).
    - Benchmarks int8 models for size, latency, and accuracy; discusses calibration datasets and observers.
    - Shows integration with `torch.quantization` and `torch.ao.quantization` tooling.
  - New concept introduced:
    - Quantization techniques and how they affect numerical precision and deployment performance.
  - By the end of this lab you'll be able to:
    - Convert PyTorch models to quantized variants and measure deployment improvements.

- M4-A : Deployment Assignment — `M4-A/C3M4_Assignment.ipynb`
  - Top heading (from notebook): "Assignment: Prepare Models for Production"
  - Technical details & techniques:
    - End-to-end deployment checklist: export (ONNX/TorchScript), compress (prune/quantize), and test inference.
    - Includes monitoring hooks, simple API wrappers, and performance regression tests.
    - Creates reproducible artifact bundles for deployment (model + preprocessing + sample inputs).
  - New concept introduced:
    - Production-readiness considerations: portability, monitoring, and regression testing.
  - By the end of this assignment you'll be able to:
    - Package a model for deployment and validate it through inference and performance checks.

