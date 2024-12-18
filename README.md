# Towards Unifying Evaluation of Counterfactual Explanations: Leveraging Large Language Models for Human-Centric Assessments

This repository is the official implementation and supplementary materials for the paper:  
**"Towards Unifying Evaluation of Counterfactual Explanations: Leveraging Large Language Models for Human-Centric Assessments"**  
by **Marharyta Domnich, Julius Valja, Rasmus Moorits Veski, Giacomo Magnifico, Kadi Tulver, Eduard Barbu, and Raul Vicente.**

---

## 🤔 Introduction

Counterfactual explanations play a vital role in Explainable AI (XAI) by providing actionable insights on how to change inputs to achieve a desired model outcome. Despite their importance, evaluating counterfactual explanations is often fragmented, with metrics and methods lacking grounding in human perspectives. 
![Diagram from the paper](cf_evaluation_diagram.png)


To address this gap, our work introduces:  
1. **CounterEval Dataset**: A human-evaluated dataset of 30 counterfactual scenarios rated by 206 participants across eight explanatory quality metrics, including Feasibility, Consistency, Completeness, Trust, and Overall Satisfaction. (Dataset is available in https://huggingface.co/datasets/anitera/CounterEval)  
2. **LLM-based Evaluation Models**: Large Language Models fine-tuned on CounterEval to predict average and individual human judgments, enabling scalable evaluation of counterfactual explanation frameworks.

Our results show that fine-tuned LLMs achieve **up to 85% accuracy** in mimicking human evaluations and outperform current zero-shot approaches. This advancement sets the stage for more consistent and human-aligned XAI evaluation.

---

## 🚀 Main Results

### Highlights from Our Findings
1. **Accuracy of Fine-Tuned LLMs**:
   - Zero-shot evaluations: **63% accuracy**.
   - Fine-tuned evaluations: **85% accuracy** for predicting human ratings.

2. **CounterEval Dataset**:
   - 30 diverse counterfactual scenarios spanning multiple domains.
   - Human evaluations across eight metrics, providing insights into explanatory quality.

## 📦 Model Weights

We provide **fine-tuned LLaMA 3.1 8B model weights** trained on the CounterEval dataset to predict human evaluations of counterfactual explanations.

### Files Included:
| File                     | Description                                                 |
|--------------------------|-------------------------------------------------------------|
| `adapter_config.json`    | Configuration file for the adapter.                         |
| `adapter_model.safetensors` | Fine-tuned model weights in `safetensors` format.          |
| `tokenizer.json`         | Tokenizer for the LLaMA model.                              |
| `tokenizer_config.json`  | Tokenizer configuration file.                               |
| `special_tokens_map.json`| Special tokens mapping used during training.                |
| `training_args.bin`      | Training arguments saved for reproducibility.               |
| `README.md`              | Instructions and documentation for model usage.             |

---

### ⬇️ Downloading the Model Weights
The model weights can be downloaded directly from this repository under the **`models`** directory or via Hugging Face:

```bash
git clone https://github.com/your_username/countereval.git
