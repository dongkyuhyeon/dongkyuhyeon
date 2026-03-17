# Hi, I'm Dongkyuhyeon 👋

컴퓨터공학을 공부하며 LLM Quantization, On-Device AI, Physical AI, and Applied Reinforcement Learning에 관심을 가지고 있습니다.

## Interests
- LLM Quantization
- On-Device AI
- Physical AI
- Applied Reinforcement Learning

## Current Work
- Completed LG Aimers 8
- EXAONE 4.0 quantization experiments
- Ranked 28th out of 628 teams in the LG Aimers 8 EXAONE 4.0 competition
- Understanding Transformer structures and architectures
- Fine-tuning models based on Transformer architectures
- Simple knowledge distillation experiments  
  (using BERT as the teacher model, preprocessing data, fine-tuning DistilBERT, and comparing latency and accuracy)
- Basic QNNX study
- PPO-based asset allocation strategy using reinforcement learning logic

## Tech Stack
- Python
- PyTorch
- Hugging Face
- Transformers
## 최종 코드 설명

최종 제출 코드는 `final_quantize.py`에 정리되어 있다.

주요 흐름은 다음과 같다.

1. `base_model` 경로에서 원본 모델 로드
2. calibration용 JSONL 데이터 생성
3. tokenizer의 chat template 적용
4. `QuantizationModifier`로 `W8A8` 양자화 수행
5. 결과 모델과 tokenizer 저장
6. `generation_config.json` 수정

---

## 실행 흐름

### 1. 기본 폴더 준비

- `base_model/` : 원본 모델 디렉토리
- `submit/model/` : 양자화 결과 저장 경로

### 2. 스크립트 실행

`final_quantize.py`를 실행하면 다음이 순서대로 수행된다.

- calibration 데이터 생성
- 원본 모델 로드
- dataset 변환
- W8A8 양자화
- 결과 저장
- generation_config 수정

---

## 폴더 구조

```text
Lg-aimers-8-exaone4-quantization-competition/
├─ README.md
├─ final_quantize.py
├─ docs/
│  ├─ experiment_log.md
│  └─ paper_review.md
├─ outputs/
│  └─ .gitkeep
└─ submit/
   └─ .gitkeep
>>>>>>> 91e12826bff81b12a443260d477ef46e3583fb17
