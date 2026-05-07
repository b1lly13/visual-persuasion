# visual-persuasion
Official repository containing the evaluation scripts for the paper: "Can MLLMs Reason About Visual Persuasion? Evaluating the Efficacy and Faithfulness of Reasoning."

This repository focuses on our three-dimensional evaluation framework for measuring model-rationale faithfulness: Rationale-to-Decision Consistency, Rationale-to-Image Groundedness, and Rationale-to-Decision Sensitivity.

📊 Evaluation Metrics
The included scripts correspond to the automated evaluation pipelines described in Section 4 of the paper:

Consistency:
run_nli.py: Evaluates whether the predicted persuasiveness decision is derivable from the generated rationale.

Groundedness:
groundedness_calculate.py: Main script for aggregating groundedness metrics.
prompting_metric_groundedness.py: Groundedness evaluation using zero-shot LLM prompting.
atomic_facts_groundedness.py: Groundedness evaluation using the decomposed atomic facts methodology.
clip_metric_groundedness.py: Baseline groundedness calculations using CLIP text/image similarity.

Sensitivity:
analyze_flip_exclusion.py & run_flip_exclusion.sh: Pipeline for measuring rationale-to-decision sensitivity via counterfactual image editing.

🏋️ Training Code
The supervised fine-tuning (Reasoning-SFT) and Group Relative Policy Optimization (GRPO) training codes are not hosted in this repository. Our training environments were built by cloning and adapting the following open-source repositories:

Qwen-2.5-VL Training: 2U1/Qwen-VL-Series-Finetune
Phi-3.5-vision Training: 2U1/Phi3-Vision-Finetune
