# NL

There is a code related to the machine learning model that reads text and analyzes emotions that fit that text.

# KoBERT-based Emotion Analysis Model

This project is a fine-tuning of a **emotional classification model that classifies seven emotions based on the KoBERT model for **Real-time Emotion Analysis**, one of the key features of the Sonatale app.

## ✅ Project Overview

- **Objective**: Emotion classification of sentences extracted from fairy tale text and speech using KoBERT
- **Model**: KoBERT (based on HuggingFace) provided by SKT-AI
- **Sorted Appraisal Class**:
- happy (happy)
- Sadness
- Anger (Anger)
- Fear
- Surprise
- Disgust
- Neutral

## 🛠️ Technology of use

- Python 3.8+
- PyTorch
- KoBERT (transformers 기반)
- HuggingFace Datasets, AIhub datasets
- scikit-learn (Evaluation Indicator)

## 📊 Learning Data

- Using Custom Labeled Fairy Tentings Dataset
- 7 emotional classes in total
- **Single classification rather than multiple emotions**
- Text data preprocessing:
- Integrate different emotions into 7 emotions
- Remove unnecessary parts
- Sentence unit emotion mapping
- Class weight is assigned to each class

## 🔧 How to learn

```bash
python train.py \
--epochs 10 \
--batch_size 32 \
--lr 2e-5 \

🎯 Performance
Accuracy: 54.2%
Macro F1 Score: 53.08%

📎 See also
KoBERT: https://github.com/SKTBrain/KoBERT
HuggingFace Transformers: https://huggingface.co/transformers/
AIhub : https://www.aihub.or.kr/
