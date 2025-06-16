# NL

There is a code related to the machine learning model that reads text and analyzes emotions that fit that text.

---

<br>

# KoBERT-based Emotion Analysis Model

This project is a fine-tuning of a **emotional classification model that classifies seven emotions based on the KoBERT model for **Real-time Emotion Analysis**, one of the key features of the Sonatale app.

---

<br>

## ✅ Project Overview

- **Objective**: Emotion classification of sentences extracted from fairy tale text and speech using KoBERT or other large-scale transformers
- **Model**: 
  - KoBERT (SKT-AI 제공) for 7 basic emotion classes
  - [searle-j/kote_for_easygoing_people](https://huggingface.co/searle-j/kote_for_easygoing_people) for 43 fine-grained emotions
- **Emotion Classes**:
  - 7-label (Single-label classification):
    - Happy, Sadness, Anger, Fear, Surprise, Disgust, Neutral
  - 43-label (Multi-label classification):
    - 감탄, 감정없음, 걱정, 공감, 관심, 기대, 기쁨, 농담, 당황, 답답, 두려움, 마음아픔, 미안함, 반가움, 분노, 불안, 부담, 불쾌함, 상처, 사과, 슬픔, 신뢰, 실망, 실수, 심각, 안타까움, 애정, 어이없음, 억울, 열등감, 외로움, 우울, 응원, 의욕, 자랑, 좌절, 죄책감, 질투, 창피, 후회, 흥미, 희망, 힘듦 등

---

<br>

## 🛠️ Technology of use

- Python 3.8+
- PyTorch
- KoBERT (transformers 기반)
- HuggingFace Datasets, AIhub datasets
- scikit-learn (Evaluation Indicator)
- pandas, openpyxl
  
---

<br>

## 📊 Learning Data

- Custom labeled fairy tale text dataset
- 7 emotional classes for single-label
- 43 emotional labels for multi-label
- Preprocessing:
  - Sentence-level emotion mapping
  - Removal of noise
  - Mapping & thresholding for multi-label

---

<br>

## 🔧 How to learn

bash
python train.py \
--epochs 10 \
--batch_size 32 \
--lr 2e-5 \

---

<br>

## 🎯 Performance

| Model                                   | Task Type     | Accuracy | Macro F1 |
|----------------------------------------|---------------|----------|-----------|
| KoBERT                                  | Single-label  | 54.2%    | 53.08%    |
| searle-j/kote_for_easygoing_people     | Multi-label   | 79.7% (top-1 accuracy) | - |

---

<br>

## 📎 See also
- [KoBERT GitHub](https://github.com/SKTBrain/KoBERT)
- [HuggingFace Transformers](https://huggingface.co/transformers/)
- [searle-j/kote_for_easygoing_people](https://huggingface.co/searle-j/kote_for_easygoing_people)
- [AIhub Emotion Dataset](https://www.aihub.or.kr/)
