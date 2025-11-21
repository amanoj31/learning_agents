Generative AI Engineering and Fine-Tuning Transformers - https://www.coursera.org/learn/generative-ai-engineering-and-fine-tuning-transformers/home/module/1



- L1 : Loading Models and Inference with Hugging Face — `L1/Loading Models and Inference with Hugging Face.ipynb`
  - Top heading (inferred): "Loading Pretrained Models and Running Inference with Hugging Face"
  - Technical details & techniques:
    - Loading models via `transformers.AutoModel` / `AutoTokenizer` and sending inputs through the pipeline.
    - Tokenization details (special tokens, padding/truncation, attention masks) and batching for inference.
    - Using `pipeline` for zero-shot tasks and low-effort inference wrappers.
    - Device placement (`cpu`/`cuda`), mixed precision inference, and memory considerations for large models.
  - New concept introduced:
    - Hugging Face model-loading ergonomics and practical inference tips for throughput and memory.
  - By the end of this lab you'll be able to:
    - Load models and tokenizers, run batched inference, and tune inference settings for speed/memory.

- L2 : Optional Pre-training LLMs with Hugging Face — `L2/Optional Pre-training LLMs with Hugging Face.ipynb`
  - Top heading (inferred): "Pre-training Basics and Optional Continuation Training"
  - Technical details & techniques:
    - Data pipeline for pre-training: dataset creation, sharding, and TFRecords/JSONL workflows.
    - Masked Language Modeling (MLM) vs. Causal Language Modeling (CLM) objectives and when to use each.
    - Training loops for large-batch pretraining, gradient accumulation, and checkpointing best practices.
    - Tokenizer training (BPE/WordPiece/Unigram) and vocabulary considerations for new domains.
  - New concept introduced:
    - Pre-training objectives, data scaling, and how tokenizer choices affect downstream performance.
  - By the end of this lab you'll be able to:
    - Prepare datasets and training scripts for optional pre-training or domain-adaptive continuation training.

- L3 : Pre-Training and Fine-Tuning with PyTorch — `L3/Pre-Training and Fine-Tuning with PyTorch.ipynb`
  - Top heading (inferred): "From Pre-Training to Fine-Tuning: Transfer and Best Practices"
  - Technical details & techniques:
    - Fine-tuning loops for classification, token-level tasks, and conditional generation using `Trainer` or custom loops.
    - Optimization best-practices: AdamW, LR schedules, warmup steps, weight decay, and gradient clipping.
    - Dataset formatting for supervised fine-tuning and prompt/response formatting for generation tasks.
    - Evaluation metrics: perplexity, BLEU/ROUGE, accuracy/F1 for classification, and human-centric checks.
  - New concept introduced:
    - Fine-tuning strategies and pitfalls such as catastrophic forgetting and overfitting on small datasets.
  - By the end of this lab you'll be able to:
    - Fine-tune a pretrained transformer for a downstream task and evaluate with appropriate metrics.

- L4 : Fine-Tuning Transformers with PyTorch and Hugging Face — `L4/Fine-Tuning Transformers with PyTorch and Hugging Face.ipynb`
  - Top heading (inferred): "Hands-on Fine-Tuning with `transformers` and PyTorch"
  - Technical details & techniques:
    - Using `Trainer`/`TrainingArguments` and also implementing custom `train()` loops for more control.
    - Handling mixed-precision (AMP), gradient accumulation, multi-GPU training, and distributed strategies.
    - Checkpointing, resuming training, and robust logging of metrics/artifacts (TensorBoard/MLflow).
  - New concept introduced:
    - Production-aware training pipelines and how to scale fine-tuning from single-GPU to multi-node setups.
  - By the end of this lab you'll be able to:
    - Run fine-tuning experiments with reproducible configs and evaluate/compare runs reliably.

- L5 : Adapters in PyTorch — `L5/Adapters in PyTorch.ipynb`
  - Top heading (inferred): "Parameter-Efficient Fine-Tuning with Adapters"
  - Technical details & techniques:
    - Introduces adapter modules (small bottleneck layers) and how they integrate into transformer blocks.
    - Training only adapter parameters while freezing the backbone to drastically reduce trainable parameters.
    - Comparison to other parameter-efficient methods (LoRA, prefix-tuning, prompt-tuning) in compute and accuracy.
    - Practical tips for adapter placement, bottleneck dimension, and multi-task adapter strategies.
  - New concept introduced:
    - Parameter-efficient transfer learning and modular adapter design for multi-domain adaptation.
  - By the end of this lab you'll be able to:
    - Add adapters to a transformer and run efficient fine-tuning experiments with low GPU/CPU cost.

- L6 : LoRA with PyTorch — `L6/LoRA with Pytorch.ipynb`
  - Top heading (inferred): "Low-Rank Adaptation (LoRA) for Efficient Fine-Tuning"
  - Technical details & techniques:
    - Implements LoRA layers that inject low-rank updates into attention/query/value projections.
    - Training procedure: freezing base weights, optimizing low-rank adapters, and merging weights for inference.
    - Memory and compute trade-offs compared to full fine-tuning and training recipes for different model sizes.
    - Tips for rank selection, scaling factors, and merging/unmerging modules for deployment.
  - New concept introduced:
    - Low-rank updates as a practical alternative for parameter-efficient fine-tuning at scale.
  - By the end of this lab you'll be able to:
    - Apply LoRA to transformer models and measure parameter savings and task performance.

- L7 : QLoRA with Hugging Face — `L7/QLoRA with Hugging Face.ipynb`
  - Top heading (inferred): "Quantized LoRA (QLoRA): Combine Quantization + LoRA for LLM Finetuning"
  - Technical details & techniques:
    - Workflow for quantizing models (4-bit or 8-bit) and applying LoRA adapters on top for finetuning.
    - Practical usage of `bitsandbytes` or similar libs for quantized training and memory-efficient optimizer choices.
    - Calibration, tokenizer behavior under quantization, and preserving numeric stability during training.
  - New concept introduced:
    - Combining quantization with parameter-efficient adapters to run finetuning on commodity hardware.
  - By the end of this lab you'll be able to:
    - Run QLoRA-style finetuning and fit large models on limited GPU memory while preserving performance.

Notes:
- These summaries follow the same structure as the `NLP-Pytorch02-Intermediate` README. I inferred headings and technical bullets from notebook filenames and common LLM finetuning practices.
- If you'd like exact first-paragraph headings and live code highlights, I can open each notebook and extract the real top-level text and a brief code excerpt.
- I can also create per-folder `README.md` files (e.g., `L1/README.md`, `L2/README.md`, ...) or commit this aggregated README to the repo. Tell me which you prefer.
