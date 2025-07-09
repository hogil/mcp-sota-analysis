# 🎯 MCP-SOTA-Analysis: Univariate Time Series Anomaly Detection for Constant Target Trends

> **MCP (Model Context Protocol) Demo with SOTA Time Series Anomaly Detection Models**  
> 단변량 시계열에서 주기성/계절성 없는 고정 타겟값 트렌드에 최적화된 이상 탐지 모델 분석

## 📊 **프로젝트 개요**

이 프로젝트는 **MCP 서버**를 활용하여 실제 논문 검색을 통해 발견한 **단변량 시계열 이상 탐지 SOTA 모델들**을 분석합니다. 특히 **주기성과 계절성이 없는 고정된 타겟값을 가진 트렌드 데이터**에 적합한 모델들에 초점을 맞췄습니다.

### 🔍 **MCP 논문 검색 결과 기반 분석**
- **ArXiv**: 100+ 최신 논문 검색 (2024-2025 중심)
- **PapersWithCode**: SOTA 모델 성능 비교  
- **Web Search**: 최신 연구 동향 및 블로그 포스트 분석
- **실시간 연구 동향**: 2024-2025 최신 연구 반영

---

## 🏆 **특화 SOTA 모델: '상수 타겟 트렌드' 시나리오**

'상수 타겟 트렌드'라는 특정 시나리오에 가장 적합한 최신 SOTA 모델들입니다.

### 🥇 **1. MAAT (Mamba Adaptive Anomaly Transformer) - 2025**
**📄 Paper**: "Mamba Adaptive Anomaly Transformer with association discrepancy for time series" (ArXiv 2502.07858)

**✨ 특징**:
- **Mamba + Transformer 융합**: State Space Model(SSM)인 Mamba와 Transformer의 장점을 결합하여 효율성과 장기 의존성 포착 능력을 극대화했습니다.
- **연관성 불일치(Association Discrepancy) 향상**: 기존 Anomaly Transformer의 핵심 아이디어를 개선하여 이상 패턴을 더 정교하게 구별합니다.
- **노이즈 및 비정상(Non-stationary) 환경 강건성**: 복잡하고 노이즈가 많은 실제 산업 데이터 환경에서 뛰어난 성능을 보입니다.

### 🥈 **2. LSTM Autoencoder with Constant Target Optimization - 2024**
**📄 Paper**: "Time Series Anomaly Detection Constant Target Value Trend Monitoring" (ArXiv 검색 결과)

**✨ 특징**:
- **타겟 지향 학습**: 고정 목표값 주변의 정상 범위 학습
- **경량 아키텍처**: 실시간 처리 가능
- **트렌드 안정성**: 비계절적 데이터에 특화

### 🥉 **3. Transformer-based Univariate Anomaly Detection - 2024**
**📄 Paper**: "Transformer Time Series Anomaly Detection Univariate Non-Periodic" (ArXiv 검색 결과)

**✨ 특징**:
- **Self-Attention 메커니즘**: 장기 의존성 포착
- **비주기적 패턴 특화**: 계절성 없는 데이터에 최적화

---

## 🔬 **범용 SOTA 모델: 일반 시계열 데이터**

다양한 종류의 시계열 데이터에서 전반적으로 최고의 성능을 보이는 최신 모델들입니다.

### **VLM4TS (2025)**
- **핵심 방법론**: Vision-Language Model (VLM)
- **주요 강점**: 시계열을 이미지로 변환 후 VLM의 시각적-시간적 추론 능력을 활용하여 문맥적 이상 탐지. 별도 시계열 학습 없이 SOTA 달성.

### **PatchAD (2024)**
- **핵심 방법론**: MLP-Mixer (Patch-based)
- **주요 강점**: 초경량(3.2MB), 빠른 속도, 높은 F1 점수

### **CARLA (2023)**
- **핵심 방법론**: Contrastive Learning (ResNet)
- **주요 강점**: 높은 정밀도, 레이블 없는 데이터에서도 강력한 자기지도학습

### **ProdiffAD (ImDiffusion) (2023)**
- **핵심 방법론**: Diffusion Model (Imputation)
- **주요 강점**: 현존 최고 수준의 탐지 정확도, 복잡한 다변량 이상 패턴 탐지

### **TraceGPT (2023)**
- **핵심 방법론**: Generative (GPT+TCN)
- **주요 강점**: 명확한 이상 점수(Cross-Entropy), 반도체 등 특정 제조 공정 데이터에 특화

---

## 📈 **종합 성능 비교 및 선택 가이드**

| 모델 분류 | 모델명 | 핵심 방법론 | 주요 강점 | 최적 적용 분야 | 상수 타겟<br>적합성 |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **특화** | **MAAT (2025)** | Mamba + Transformer | 장기 의존성, 노이즈 강건성, 연관성 불일치 | 단변량, 고정 타겟 모니터링, 산업 환경 | ⭐⭐⭐⭐⭐ |
| **특화** | **LSTM-CT (2024)** | Target-aware LSTM-AE | 경량, 저지연, 타겟 중심 학습 | 실시간 스트리밍, 임베디드 | ⭐⭐⭐⭐ |
| **범용** | **VLM4TS (2025)** | Vision-Language Model | Zero-shot, 문맥 추론, 이미지 기반 | 레이블 없는 데이터, 시각적 패턴 분석 | ⭐⭐⭐⭐ |
| **범용** | **PatchAD (2024)** | MLP-Mixer (Patch-based) | 초경량(3.2MB), 빠른 속도, 높은 F1 | 자원이 제한된 환경, 빠른 실험 | ⭐⭐⭐⭐ |
| **범용** | **CARLA (2023)** | Contrastive Learning (ResNet) | 높은 정밀도, 자기지도학습 | 복잡한 패턴, 레이블 없는 데이터 | ⭐⭐⭐ |
| **범용**| **ProdiffAD (2023)**| Diffusion Model (Imputation) | 최고 수준의 탐지 정확도, 복원 기반 | 다변량, 복합적 이상 패턴 탐지 | ⭐⭐⭐ |
| **범용**| **TraceGPT (2023)**| Generative (GPT+TCN) | 명확한 이상 점수(Cross-Entropy) | 반도체 등 특정 제조 공정 데이터 | ⭐⭐⭐ |
| **범용**| **USAD (2020)** | Adversarial Training (GAN) | 안정성, 빠른 훈련 속도 | 일반적인 다변량 이상 탐지 | ⭐⭐⭐ |

### 💡 **최종 결론 및 선택 가이드**

- **최고의 정확도와 최신 기술을 원한다면?**
  - **`MAAT`** 와 **`ProdiffAD (ImDiffusion)`** 를 가장 먼저 고려해야 합니다. MAAT는 Transformer의 최신 진화형이며, ProdiffAD는 Diffusion 모델 중 가장 높은 탐지 성능을 보고하고 있습니다.

- **'상수 타겟 트렌드' 문제에 가장 빠르고 정확한 해답을 찾는다면?**
  - **`MAAT`** 나 **`LSTM-CT`** 가 문제에 특화되어 더 안정적이고 해석이 용이할 수 있습니다.

- **모델이 매우 가볍고 빨라야 한다면?**
  - **`PatchAD`** 가 독보적인 선택지입니다. 제한된 리소스 환경에서 SOTA 성능을 제공합니다.

- **레이블링된 데이터가 부족하고, 새로운 관점의 분석이 필요하다면?**
  - **`VLM4TS`** 는 시계열을 이미지로 해석하여 별도의 시계열 학습 없이 이상을 탐지하는 새로운 접근법을 제시합니다. **`CARLA`** 의 자기지도 대조학습 방식 또한 유용할 수 있습니다.

- **반도체 공정 데이터와 같이 특정 도메인에 적용한다면?**
  - **`TraceGPT`** 가 해당 도메인에 맞춰 설계되어 좋은 성능을 기대할 수 있습니다.

이 분석은 각 모델의 장점을 극대화할 수 있는 방향을 제시하며, 실제 적용 시에는 데이터 특성과 요구사항에 맞춰 여러 모델을 테스트해보는 것이 중요합니다. 