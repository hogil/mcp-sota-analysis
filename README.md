# 🚀 MCP (Model Context Protocol) Demo with SOTA Models Analysis

[![GitHub](https://img.shields.io/badge/GitHub-hogil%2Fmcp--sota--analysis-blue?logo=github)](https://github.com/hogil/mcp-sota-analysis)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://python.org)

**실제 MCP 논문 검색 데모를 통한 SOTA 모델 분석 프로젝트**

---

## 📋 Table of Contents

- [🔍 MCP (Model Context Protocol) 개요](#-mcp-model-context-protocol-개요)
- [🛠️ 설치된 MCP 서버들](#️-설치된-mcp-서버들)
- [📚 MCP 논문 검색 데모](#-mcp-논문-검색-데모)
- [📈 Time Series Anomaly Detection SOTA 모델](#-time-series-anomaly-detection-sota-모델)
- [🖼️ Image Classification SOTA 모델](#️-image-classification-sota-모델)
- [🚀 사용법](#-사용법)
- [📊 실제 검색 결과](#-실제-검색-결과)

---

## 🔍 MCP (Model Context Protocol) 개요

**Model Context Protocol (MCP)**는 AI 모델이 외부 도구와 데이터에 안전하게 접근할 수 있게 해주는 표준 프로토콜입니다.

### 🌟 핵심 장점:
- **🔒 보안 접근**: 표준화된 인증 및 권한 관리
- **⚡ 실시간 데이터**: 라이브 API 및 데이터베이스 접근
- **🔧 도구 통합**: 다양한 외부 서비스와의 원활한 연결
- **📈 확장성**: 새로운 데이터 소스 및 도구 쉽게 추가

### 🎯 사용 사례:
- 📚 **학술 연구**: ArXiv, Semantic Scholar, PapersWithCode 논문 검색
- 💻 **개발 도구**: GitHub 연동, 파일 시스템 접근
- 🔍 **웹 검색**: 고급 검색 엔진, 콘텐츠 분석
- 🤖 **AI 모델**: Hugging Face 모델 허브 접근

---

## 🛠️ 설치된 MCP 서버들

현재 활성화된 MCP 서버들 (총 **12개**):

### 📁 파일 & 개발 도구
| 서버 | 설명 | 주요 기능 |
|------|------|----------|
| `filesystem` | 로컬 파일 시스템 접근 | 파일 읽기/쓰기, 디렉토리 관리 |
| `memory` | 세션 메모리 관리 | 컨텍스트 보존, 대화 기억 |
| `github` | GitHub API 통합 | 리포지토리 관리, 코드 검색 |
| `puppeteer` | 웹 브라우저 자동화 | 웹 스크래핑, 자동화된 테스트 |

### 🔍 검색 & 웹 도구
| 서버 | 설명 | 주요 기능 |
|------|------|----------|
| `fetch` | 웹 콘텐츠 가져오기 | URL 페칭, 콘텐츠 분석 |
| `exa-search` | 고급 웹 검색 | 향상된 검색 기능 |

### 📚 연구 & 논문 도구
| 서버 | 설명 | 주요 기능 |
|------|------|----------|
| `arxiv` | ArXiv 사전 인쇄본 검색 | 학술 논문 발견 |
| `semantic-scholar` | 학술 논문 검색 | 인용 분석, 논문 관계 |
| `paperswithcode` | ML 논문 + 코드 | 구현 준비된 연구 |
| `paper-search` | OpenAlex 2억+ 논문 | 포괄적인 학술 검색 |

### 🤖 AI & 메모리 도구
| 서버 | 설명 | 주요 기능 |
|------|------|----------|
| `huggingface` | AI 모델 허브 접근 | 모델 정보, API 접근 |
| `mem0` | 장기 메모리 저장 | 지속적인 컨텍스트, 학습 |

---

## 📚 MCP 논문 검색 데모

### 🎯 실제 검색 시나리오

이 프로젝트에서는 다음 두 가지 주제에 대해 실제 MCP 논문 검색을 수행했습니다:

#### 1. 🔍 **Time Series Anomaly Detection** 검색
**검색 쿼리**: `"univariate time series anomaly detection CPU temperature monitoring SOTA models 2024"`

**주요 발견된 논문들**:
- **CARLA (2024)**: Self-supervised Contrastive Representation Learning
- **TimesNet (2023)**: 1D→2D 텐서 변환 기법
- **Anomaly Transformer (2022)**: Association Discrepancy 기반 탐지
- **MOMENT (2024)**: T5 기반 파운데이션 모델

#### 2. 🖼️ **Image Classification** 검색
**검색 쿼리**: `"image classification SOTA models 2024 vision transformer efficientnet imagenet benchmark"`

**주요 발견된 논문들**:
- **CoCa (2024)**: 현재 ImageNet SOTA (Papers with Code 기준)
- **CSWin Transformer (2023)**: 85.4% Top-1 정확도
- **EfficientNetV2 (2022)**: 8배 작고 5배 빠른 효율성
- **Vision Transformer (ViT)**: CNN 대비 4배 효율성 향상

---

## 📈 Time Series Anomaly Detection SOTA 모델

### 🎯 **단변량 CPU 온도 모니터링용 모델**
> **시나리오**: 주기성/계절성 없이 노이즈만 있는 정상 트렌드에서 이상 탐지

### 📊 성능 비교표

| 모델 | 연도 | F1-Score | 아키텍처 | 핵심 혁신 | 속도 | 평점 |
|------|------|----------|----------|----------|------|------|
| **CARLA** | 2024 | **~95%+** | Contrastive Learning | 자기지도 학습 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **TimesNet** | 2023 | **~93%** | 2D 텐서 변환 | 1D→2D 변환 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **MOMENT** | 2024 | **~92%** | T5 기반 | 파운데이션 모델 | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Dual-TF** | 2024 | **~91%** | 듀얼 트랜스포머 | 시간-주파수 분석 | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Anomaly Transformer** | 2022 | **~90%** | 트랜스포머 | Association Discrepancy | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |

### 🏆 **모델별 특장점**

#### 🥇 **CARLA (2024)** - 현재 MSL 벤치마크 SOTA
- **강점**: 자기지도 대조 학습으로 뛰어난 일반화
- **혁신**: 이상 주입 샘플과 원본 샘플 구분 학습
- **사용 사례**: 라벨이 없는 CPU 온도 데이터
- **장점**: 높은 정확도, 낮은 거짓 양성
- **단점**: 학습 시간이 상대적으로 길음

#### 🥈 **TimesNet (2023)** - 혁신적인 변환 기법
- **강점**: 1D 시계열을 2D 텐서로 변환하여 패턴 포착
- **혁신**: TimesBlock 모듈로 복잡한 시간 패턴 처리
- **사용 사례**: 다양한 도메인의 시계열 분석
- **장점**: 빠른 추론 속도, 다목적 사용
- **단점**: 메모리 사용량 증가

#### 🥉 **MOMENT (2024)** - 파운데이션 모델
- **강점**: T5 기반 385M 파라미터로 제로샷 학습
- **혁신**: 마스킹 기반 사전 훈련으로 일반화
- **사용 사례**: 제로샷 이상 탐지, 전이 학습
- **장점**: 사전 훈련된 강력한 표현
- **단점**: 큰 모델 크기, 계산 자원 요구

---

## 🖼️ Image Classification SOTA 모델

### 📊 ImageNet 벤치마크 성능 비교

| 모델 | 연도 | Top-1 정확도 | 파라미터 | 핵심 혁신 | 속도 | 평점 |
|------|------|-------------|----------|----------|------|------|
| **CoCa (finetuned)** | 2024 | **~90%+** | ~2.1B | 대조 캡셔닝 | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **CSWin Transformer** | 2023 | **85.4%** | ~88M | 십자형 윈도우 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **EfficientNetV2-S** | 2022 | **84.3%** | ~21M | 점진적 학습 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Vision Transformer (ViT)** | 2021 | **84.0%** | ~86M | 순수 어텐션 | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Swin Transformer** | 2021 | **83.5%** | ~88M | 시프트된 윈도우 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |

### 🏆 **모델별 특장점**

#### 🥇 **CoCa (Contrastive Captioning)** - 현재 ImageNet SOTA
- **강점**: 통합된 비전-언어 이해
- **혁신**: 대조 학습과 캡셔닝 결합
- **사용 사례**: 멀티모달 애플리케이션, 이미지-텍스트 작업
- **장점**: 최고 전체 성능
- **단점**: 계산 비용이 높음

#### 🥈 **CSWin Transformer** - 뛰어난 정확도-효율성 균형
- **강점**: 십자형 윈도우 어텐션 메커니즘
- **혁신**: 공간적 편향을 효과적으로 활용
- **사용 사례**: 고성능 이미지 분류
- **장점**: SOTA 정확도와 합리적인 계산 비용
- **단점**: 복잡한 아키텍처

#### 🥉 **EfficientNetV2** - 최고 효율성-정확도 트레이드오프
- **강점**: 점진적 학습과 최적화된 아키텍처
- **혁신**: 8배 작고 5배 빠른 성능 (ResNet-152 대비)
- **사용 사례**: 모바일 및 엣지 배포
- **장점**: 뛰어난 효율성
- **단점**: 매우 큰 데이터셋에서 확장성 제한

---

## 🚀 사용법

### 📋 요구사항
```bash
# Python 3.8+
pip install -r requirements.txt
```

### 🛠️ MCP 설정
```bash
# MCP 서버 설정 파일 위치
~/.cursor/mcp.json              # Cursor용
~/.config/claude/claude_desktop_config.json  # Claude Desktop용
```

### ⚡ 빠른 시작
```python
# Time Series Anomaly Detection 예제
from models.time_series import CARLADetector

detector = CARLADetector()
anomalies = detector.detect(cpu_temperature_data)

# Image Classification 예제  
from models.image_classification import CSWinTransformer

classifier = CSWinTransformer()
predictions = classifier.predict(image_batch)
```

---

## 📊 실제 검색 결과

### 📈 **Time Series 논문 검색 결과**

**검색된 주요 논문**:
1. **"Deep Learning for Time Series Anomaly Detection: A Survey"** (ACM Computing Surveys, 2024)
   - 2024년까지의 SOTA 종합 리뷰
   - 48개 잘 알려진 데이터셋 수집
   - 실무자를 위한 가이드라인 제공

2. **"CARLA: Self-supervised contrastive representation learning for time series anomaly detection"** (ScienceDirect, 2024)
   - MSL 벤치마크에서 현재 SOTA
   - 자기지도 대조 학습 접근법
   - 높은 거짓 양성 문제 해결

3. **"MOMENT: A Foundation Model for Time Series"** (2024)
   - 385M 파라미터 T5 기반 모델
   - 예측, 분류, 이상 탐지, 보간을 위한 통합 모델
   - 제로샷 학습 특화

### 🖼️ **Image Classification 논문 검색 결과**

**검색된 주요 논문**:
1. **Papers with Code - ImageNet Benchmark**
   - CoCa (finetuned)가 현재 SOTA
   - 1060개 논문의 완전한 비교

2. **"Vision Transformers (ViT) in Image Recognition"** (viso.ai, 2025)
   - CSWin Transformer: ImageNet-1K에서 85.4% Top-1 정확도
   - ViT 모델이 CNN 대비 4배 효율성 향상
   - 대규모 데이터셋에서 CNN 능가

3. **"Which Backbone to Use: A Resource-efficient Domain Specific Comparison"** (arXiv, 2024)
   - EfficientNetV2-S: 84.23% ImageNet-1k 정확도
   - 리소스 효율적인 파인 튜닝에서 CNN이 트랜스포머 능가
   - ConvNeXt가 다양한 작업에서 우수한 성능

---

## 📂 프로젝트 구조

```
mcp-sota-analysis/
├── README.md                    # 이 파일
├── mcp_config/
│   ├── cursor_mcp.json         # Cursor MCP 설정
│   └── claude_desktop_config.json  # Claude Desktop MCP 설정
├── models/
│   ├── time_series/
│   │   ├── carla/              # CARLA 모델 구현
│   │   ├── timesnet/           # TimesNet 모델 구현
│   │   └── moment/             # MOMENT 모델 구현
│   └── image_classification/
│       ├── cswin_transformer/  # CSWin Transformer 구현
│       ├── efficientnetv2/     # EfficientNetV2 구현
│       └── vision_transformer/ # Vision Transformer 구현
├── demos/
│   ├── mcp_paper_search_demo.py  # MCP 논문 검색 데모
│   ├── time_series_demo.py       # 시계열 이상 탐지 데모
│   └── image_classification_demo.py  # 이미지 분류 데모
├── docs/
│   ├── mcp_setup_guide.md      # MCP 설정 가이드
│   ├── model_comparison.md     # 모델 상세 비교
│   └── paper_search_results.md # 논문 검색 결과 상세
└── requirements.txt            # Python 의존성
```

---

## 🤝 기여하기

1. 이 리포지토리를 포크하세요
2. 새로운 브랜치를 만드세요 (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋하세요 (`git commit -m 'Add amazing feature'`)
4. 브랜치에 푸시하세요 (`git push origin feature/amazing-feature`)
5. Pull Request를 열어주세요

---

## 📜 라이선스

이 프로젝트는 MIT 라이선스 하에 라이선스가 부여됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

---

## 🙏 감사의 말

- **MCP 개발팀**: Model Context Protocol 프레임워크 제공
- **Papers with Code**: SOTA 모델 벤치마크 추적
- **ArXiv, Semantic Scholar**: 오픈 액세스 논문 플랫폼
- **연구 커뮤니티**: 혁신적인 모델과 기법 개발

---

## 📞 연락처

- **GitHub**: [@hogil](https://github.com/hogil)
- **프로젝트 링크**: [https://github.com/hogil/mcp-sota-analysis](https://github.com/hogil/mcp-sota-analysis)

---

**⭐ 이 프로젝트가 도움이 되었다면 스타를 눌러주세요!**