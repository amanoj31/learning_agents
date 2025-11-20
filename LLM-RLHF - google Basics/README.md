Course: Reinforcement Learning from Human Feedback
DeepLearning.AI - https://www.coursera.org/learn/reinforcement-learning-from-human-feedback-project/home/welcome

**Course**: Reinforcement Learning from Human Feedback (RLHF)

- **L2**: Datasets For Reinforcement Learning Training : `L2/L2_explore_data.ipynb`
  - **Top heading**: Lesson 2: Datasets For Reinforcement Learning Training
  - **Summary**: Introduces the two core dataset types used for RLHF — the preference dataset (prompt, two candidate completions, human choice) and the prompt dataset (prompts only). Shows how to load and inspect JSONL samples and why both datasets must come from the same distribution.
  - **Technical details & techniques**: JSONL sample files (`sample_preference.jsonl`, `sample_prompt.jsonl`), simple exploration helpers (`print_d`), dataset schema keys (`input_text`, `candidate_0`, `candidate_1`, `choice`). Emphasizes distribution matching for preference vs prompt data.

- **L3**: Tune an LLM with RLHF : `L3/L3_tune_llm.ipynb`
  - **Top heading**: Lesson 3: Tune an LLM with RLHF
  - **Summary**: Walks through compiling and preparing an RLHF pipeline (KubeFlow / Vertex AI). Defines `parameter_values` (paths to preference/prompt/eval datasets, model reference, training steps and hyperparameters), shows how to compute reward and RL training steps from dataset size and batch size, and describes creating/running a `PipelineJob` on Vertex AI.
  - **Technical details & techniques**: Uses `google_cloud_pipeline_components.preview.llm.rlhf_pipeline`, `kfp.compiler` to generate a YAML pipeline, GCS dataset paths (gs://...), example hyperparameters (`reward_model_train_steps`, `reinforcement_learning_train_steps`, `kl_coeff`), formulas for converting epochs → steps, and precautions about reward hacking and tuning scales.

- **L4**: Evaluate the Tuned Model : `L4/L4_evaluate_model.ipynb`
  - **Top heading**: Lesson 4: Evaluate the Tuned Model
  - **Summary**: Shows evaluation workflow comparing tuned vs untuned models: read `eval_results_tuned.jsonl` and `eval_results_untuned.jsonl`, inspect entries, visualize training logs with TensorBoard, and assemble a side-by-side dataframe of prompts, base-model completions and tuned-model completions for inspection.
  - **Technical details & techniques**: JSONL evaluation format, TensorBoard for log visualization (`reward-logs`, `reinforcer-logs`), pandas dataframe aggregation of `prompt`, `base_model` and `tuned_model` columns for manual inspection and qualitative comparison.

**Notes & next steps**:
- The lesson set here covers dataset preparation, pipeline compilation and cloud-run RLHF tuning, then evaluation. The repository also contains sample JSONL files and log directories used for local exploration (`sample_preference.jsonl`, `sample_prompt.jsonl`, `reward-logs/`, etc.).
