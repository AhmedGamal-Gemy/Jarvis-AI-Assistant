---

## 🧪 From Scratch Model

The `stt-model-from-scratch` folder contains:
- Custom model architectures (e.g., CNN + RNN / Transformer-based ASR)
- Feature extraction and preprocessing scripts
- Training scripts and evaluation notebooks
- Experiment logs and notes

This approach was ultimately set aside due to:
- Limited GPU resources
- Slow convergence on a relatively small dataset
- Better baseline results achievable through transfer learning

---

## 🐋 Fine-tuning Whisper for Egyptian Dialect

The `fine-tuning-whisper-egyptian` folder includes:
- Preprocessing scripts to format data for Whisper
- Fine-tuning scripts using 🤗 Transformers or OpenAI Whisper APIs
- Config files and hyperparameters
- Evaluation and decoding scripts

Whisper, even without fine-tuning, performs reasonably well on Egyptian dialect. Fine-tuning further improves accuracy and robustness on dialect-specific terms and expressions.

---

## ✅ Requirements & Setup

Each folder has its own `requirements.txt` (or equivalent).  
Common setup:
python -m venv venv source venv/bin/activate pip install -r requirements.txt

---

## 📊 Results & Notes

| Approach            | WER (Validation) | Notes                                      |
|--------------------|-----------------:|---------------------------------------------|
| From Scratch       | ~85%             | Converged slowly; overfit on small dataset |
| Fine-tuned Whisper | ~34%             | Better generalization and robustness       |
---

## 🧠 Why We Switched

Training from scratch is often impractical without large datasets and compute.  
Fine-tuning pre-trained models like Whisper leverages transfer learning, requiring fewer resources and achieving better results faster.
