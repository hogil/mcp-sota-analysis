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

## 🤖 **MCP (Model Context Protocol)란?**
MCP는 '모델 컨텍스트 프로토콜(Model Context Protocol)'의 약자입니다. AI 모델(LLM)이 단순히 텍스트만 생성하는 것을 넘어, **다양한 외부 도구(Tools)와 실시간 정보에 접근**하고, **파일 시스템을 읽고 쓰거나 코드를 실행**하는 등 복잡한 작업을 수행할 수 있도록 만든 개방형 프로토콜입니다.

쉽게 말해, AI가 사람처럼 컴퓨터를 사용하여 정보를 찾고, 분석하고, 결과를 만들어내는 능동적인 '에이전트'가 되도록 돕는 규약입니다.

### 🔧 **MCP 설정 및 연결 방법**

#### **1. Claude Desktop에서 MCP 설정**
Claude Desktop 앱을 사용하는 경우:

1. **설정 파일 위치**: `%APPDATA%\Claude\claude_desktop_config.json` (Windows)
2. **기본 설정 예시**:
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-filesystem", "/path/to/allowed/files"]
    },
    "web-search": {
      "command": "npx", 
      "args": ["@modelcontextprotocol/server-web-search"]
    },
    "youtube": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-youtube"]
    }
  }
}
```

#### **2. Cursor에서 MCP 설정**
Cursor 에디터를 사용하는 경우:

1. **설정 파일 위치**: 프로젝트 루트의 `mcp_config/cursor_mcp.json`
2. **설정 예시**:
```json
{
  "servers": {
    "filesystem": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-filesystem", "D:\\project"]
    },
    "web-search": {
      "command": "npx", 
      "args": ["@modelcontextprotocol/server-web-search"]
    }
  }
}
```

#### **3. 주요 MCP 서버 설치**
```bash
# 파일 시스템 접근
npm install -g @modelcontextprotocol/server-filesystem

# 웹 검색 기능
npm install -g @modelcontextprotocol/server-web-search

# 유튜브 데이터 접근
npm install -g @modelcontextprotocol/server-youtube
```

### 🎯 **MCP를 사용하는 이유**

#### **기존 AI의 한계**
- ❌ **정적 지식**: 훈련 데이터 시점까지의 정보만 알고 있음
- ❌ **실시간 정보 부족**: 최신 논문, 뉴스, 트렌드를 모름
- ❌ **도구 사용 불가**: 파일 읽기/쓰기, 코드 실행, 웹 검색 등 불가능
- ❌ **단발성 응답**: 지속적인 작업 관리나 업데이트 불가능

#### **MCP 활용 시 가능한 것들**
- ✅ **실시간 정보 수집**: 최신 논문, 뉴스, 기술 동향 실시간 검색
- ✅ **파일 시스템 조작**: 코드 작성, 문서 생성, 프로젝트 관리
- ✅ **지속적인 업데이트**: Git 커밋, 자동 문서화, 버전 관리
- ✅ **복합 작업 수행**: 데이터 수집 → 분석 → 문서화 → 배포까지 자동화
- ✅ **다양한 도구 연동**: API 호출, 데이터베이스 접근, 클라우드 서비스 연결

### 💡 **이 프로젝트에서의 MCP 활용 사례**

#### **실제 수행된 작업들**
1. **📚 논문 검색 및 분석**
   - `web_search` 도구로 ArXiv에서 최신 SOTA 논문 검색
   - 각 논문의 핵심 내용, 성능 지표, 방법론 자동 추출

2. **📝 문서 생성 및 편집**
   - `filesystem` 도구로 README.md 파일 읽기/쓰기
   - 분석 결과를 구조화된 마크다운 문서로 자동 변환

3. **🔄 버전 관리**
   - `terminal` 도구로 Git 명령어 실행
   - 변경사항 자동 커밋 및 GitHub 푸시

4. **📊 비교 분석표 생성**
   - 수집된 데이터를 바탕으로 모델 성능 비교표 자동 생성
   - 각 모델의 특징과 적용 분야 매핑

#### **전통적인 방법 vs MCP 활용**
| 구분 | 전통적인 방법 | MCP 활용 |
|------|---------------|----------|
| 정보 수집 | 수동으로 논문 검색 및 읽기 | 자동 논문 검색 및 핵심 내용 추출 |
| 문서 작성 | 수동으로 내용 정리 및 작성 | 분석 결과 자동 문서화 |
| 업데이트 | 새로운 정보 발견 시 수동 수정 | 실시간 최신 정보 반영 |
| 버전 관리 | 수동 Git 명령어 실행 | 자동 커밋 및 푸시 |
| 소요 시간 | 수 시간 ~ 수 일 | 수 분 ~ 수십 분 |

### 🤔 **이 프로젝트에서 MCP는 어떻게 사용되었나요?**
이 프로젝트의 `README.md`는 **사람이 직접 작성한 것이 아니라, MCP를 기반으로 동작하는 AI 에이전트가 생성하고 업데이트**한 결과물입니다.

AI 에이전트는 다음과 같은 작업을 MCP를 통해 자율적으로 수행했습니다.
1. **논문 검색**: `web_search`, `arxiv` 등 도구를 사용하여 '시계열 이상 탐지' 관련 최신 SOTA 논문을 수십 편 검색하고 분석했습니다.
2. **핵심 내용 추출 및 요약**: 검색된 논문과 자료를 읽고, 각 모델의 핵심 방법론, 장단점, 특징을 추출하여 요약했습니다.
3. **콘텐츠 생성**: 분석한 내용을 바탕으로 `README.md` 파일의 비교 분석표와 선택 가이드 등 전체 콘텐츠를 직접 작성했습니다.
4. **지속적인 업데이트**: 사용자의 "최신 정보로 업데이트해줘"라는 새로운 요구에 따라, 다시 최신 논문을 검색하고 기존 `README.md` 파일을 읽어 **스스로 수정하고 Git에 Push**했습니다.

결론적으로 이 프로젝트는 MCP가 어떻게 AI의 능력을 확장하여 **최신 기술 동향을 실시간으로 분석하고, 그 결과를 문서화하며, 지속적으로 관리**할 수 있는지 보여주는 실제 사례(Live Demo)입니다.

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