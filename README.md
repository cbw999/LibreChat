## npm ci(Continuous Integration, 지속적인 통합)의 약자 명령어로 package-lock.json 또는 npm-shrinkwrap.json 기반의 정확한 버전만 설치
### package-lock.json에 따라 정확하고, 깨끗하며, 일관되게 의존성을 설치하는 명령입니다.
## LibreChat 종속성 설치
```
npm ci
```

### 프론트엔드 빌드
```
npm run frontend
```

### .env 파일을 만드세요. 파일이 없으면 .env.example을 복사해서 설정하세요.

### 도커로 몽고DB 설치
```
docker pull mongo
docker run --name mongo-db -d -p 27017:27017 mongo
```
### 콘솔에 자세한 서버 출력을 표시하려면 .env에서 DEBUG_CONSOLE을 true로 설정하세요.

### 백엔드 시작 (개발용)
```
npm run backend:dev
```
### 백엔드 접속 주소 : http://localhost:3080

### 프론트엔드 시작 (개발용)
```
npm run frontend:dev
```
### 프론트엔드 접속 주소 : http://localhost:3090

### 몽고DB 접속 툴 다운로드
[몽고DB 접속 툴 다운로드](https://www.mongodb.com/try/download/compass)


<p align="center">
  <a href="https://librechat.ai">
    <img src="client/public/assets/logo.svg" height="256">
  </a>
  <h1 align="center">
    <a href="https://librechat.ai">LibreChat</a>
  </h1>
</p>

<p align="center">
  <a href="https://discord.librechat.ai"> 
    <img
      src="https://img.shields.io/discord/1086345563026489514?label=&logo=discord&style=for-the-badge&logoWidth=20&logoColor=white&labelColor=000000&color=blueviolet">
  </a>
  <a href="https://www.youtube.com/@LibreChat"> 
    <img
      src="https://img.shields.io/badge/YOUTUBE-red.svg?style=for-the-badge&logo=youtube&logoColor=white&labelColor=000000&logoWidth=20">
  </a>
  <a href="https://docs.librechat.ai"> 
    <img
      src="https://img.shields.io/badge/DOCS-blue.svg?style=for-the-badge&logo=read-the-docs&logoColor=white&labelColor=000000&logoWidth=20">
  </a>
  <a aria-label="Sponsors" href="https://github.com/sponsors/danny-avila">
    <img
      src="https://img.shields.io/badge/SPONSORS-brightgreen.svg?style=for-the-badge&logo=github-sponsors&logoColor=white&labelColor=000000&logoWidth=20">
  </a>
</p>

<p align="center">
<a href="https://railway.app/template/b5k2mn?referralCode=HI9hWz">
  <img src="https://railway.app/button.svg" alt="Railway에 배포" height="30">
</a>
<a href="https://zeabur.com/templates/0X2ZY8">
  <img src="https://zeabur.com/button.svg" alt="Zeabur에 배포" height="30"/>
</a>
<a href="https://template.cloud.sealos.io/deploy?templateName=librechat">
  <img src="https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg" alt="Sealos에 배포" height="30">
</a>
</p>

<p align="center">
  <a href="https://www.librechat.ai/docs/translation">
    <img 
      src="https://img.shields.io/badge/dynamic/json.svg?style=for-the-badge&color=2096F3&label=locize&query=%24.translatedPercentage&url=https://api.locize.app/badgedata/4cb2598b-ed4d-469c-9b04-2ed531a8cb45&suffix=%+translated" 
      alt="번역 진행률">
  </a>
</p>


# ✨ 주요 기능

- 🖥️ **UI & 경험**: ChatGPT에서 영감을 받은 디자인과 향상된 기능 제공

- 🤖 **AI 모델 선택**:  
  - Anthropic(Claude), AWS Bedrock, OpenAI, Azure OpenAI, Google, Vertex AI, OpenAI Assistants API(포함 Azure)
  - [커스텀 엔드포인트](https://www.librechat.ai/docs/quick_start/custom_endpoints): LibreChat에서 OpenAI 호환 API를 자유롭게 사용, 프록시 불필요
  - [로컬 및 원격 AI 제공자](https://www.librechat.ai/docs/configuration/librechat_yaml/ai_endpoints)와 호환:
    - Ollama, groq, Cohere, Mistral AI, Apple MLX, koboldcpp, together.ai,
    - OpenRouter, Perplexity, ShuttleAI, Deepseek, Qwen 등

- 🔧 **[코드 인터프리터 API](https://www.librechat.ai/docs/features/code_interpreter)**: 
  - Python, Node.js(JS/TS), Go, C/C++, Java, PHP, Rust, Fortran의 안전한 샌드박스 실행
  - 파일 업로드, 처리, 다운로드 지원
  - 완전 격리된 환경으로 개인정보 걱정 없음

- 🔦 **에이전트 & 도구 통합**:  
  - **[LibreChat 에이전트](https://www.librechat.ai/docs/features/agents)**:
    - 노코드 커스텀 어시스턴트: 코딩 없이 AI 기반 도우미 제작  
    - 유연하고 확장 가능: DALL-E-3, 파일 검색, 코드 실행 등 도구 연결  
    - 커스텀 엔드포인트, OpenAI, Azure, Anthropic, AWS Bedrock 등과 호환
    - 도구용 [MCP 지원](https://modelcontextprotocol.io/clients#librechat)
  - LibreChat 에이전트와 OpenAI 어시스턴트에서 파일, 코드 인터프리터, 도구, API 액션 사용

- 🔍 **웹 검색**:  
  - 인터넷 검색 및 관련 정보로 AI 컨텍스트 강화
  - 검색 제공자, 콘텐츠 스크래퍼, 결과 재정렬 기능 결합
  - **[자세히 보기 →](https://www.librechat.ai/docs/features/web_search)**

- 🪄 **코드 아티팩트로 생성형 UI**:  
  - [코드 아티팩트](https://youtu.be/GfTj7O4gmd0?si=WJbdnemZpJzBrJo3)로 채팅에서 React, HTML, Mermaid 다이어그램 생성

- 🎨 **이미지 생성 및 편집**
  - [GPT-Image-1](https://www.librechat.ai/docs/features/image_gen#1--openai-image-tools-recommended)로 텍스트→이미지, 이미지→이미지
  - [DALL-E (3/2)](https://www.librechat.ai/docs/features/image_gen#2--dalle-legacy), [Stable Diffusion](https://www.librechat.ai/docs/features/image_gen#3--stable-diffusion-local), [Flux](https://www.librechat.ai/docs/features/image_gen#4--flux), 기타 [MCP 서버](https://www.librechat.ai/docs/features/image_gen#5--model-context-protocol-mcp) 지원
  - 프롬프트로 멋진 이미지 생성 및 기존 이미지 수정

- 💾 **프리셋 & 컨텍스트 관리**:  
  - 커스텀 프리셋 생성, 저장, 공유  
  - 채팅 중 AI 엔드포인트 및 프리셋 전환
  - 메시지 편집, 재전송, 대화 분기  
  - [메시지/대화 포크](https://www.librechat.ai/docs/features/fork)로 고급 컨텍스트 제어

- 💬 **멀티모달 & 파일 상호작용**:  
  - Claude 3, GPT-4.5, GPT-4o, o1, Llama-Vision, Gemini로 이미지 업로드 및 분석 📸  
  - 커스텀 엔드포인트, OpenAI, Azure, Anthropic, AWS Bedrock, Google로 파일 채팅 🗃️

- 🌎 **다국어 UI**:  
  - 영어, 중국어, 독일어, 스페인어, 프랑스어, 이탈리아어, 폴란드어, 브라질 포르투갈어
  - 러시아어, 일본어, 스웨덴어, 한국어, 베트남어, 번체 중국어, 아랍어, 터키어, 네덜란드어, 히브리어

- 🧠 **추론 UI**:  
  - DeepSeek-R1 등 Chain-of-Thought/Reasoning AI 모델용 동적 추론 UI

- 🎨 **커스터마이즈 가능한 인터페이스**:  
  - 파워유저와 초보자 모두에게 적합한 드롭다운 및 인터페이스 커스터마이즈

- 🗣️ **음성 & 오디오**:  
  - 음성 인식(STT), 음성 합성(TTS)으로 핸즈프리 채팅  
  - 오디오 자동 전송 및 재생  
  - OpenAI, Azure OpenAI, Elevenlabs 지원

- 📥 **대화 가져오기 & 내보내기**:  
  - LibreChat, ChatGPT, Chatbot UI에서 대화 가져오기  
  - 스크린샷, 마크다운, 텍스트, json으로 대화 내보내기

- 🔍 **검색 & 탐색**:  
  - 모든 메시지/대화 검색

- 👥 **멀티유저 & 보안 접근**:
  - OAuth2, LDAP, 이메일 로그인 지원 멀티유저, 보안 인증
  - 내장 모더레이션, 토큰 사용량 도구

- ⚙️ **설정 & 배포**:  
  - 프록시, 리버스 프록시, 도커, 다양한 배포 옵션 지원  
  - 완전 로컬 또는 클라우드 배포 가능

- 📖 **오픈소스 & 커뮤니티**:  
  - 완전 오픈소스, 공개 개발  
  - 커뮤니티 주도 개발, 지원, 피드백

[자세한 기능은 공식 문서에서 확인하세요](https://docs.librechat.ai/) 📚

## 🪶 올인원 AI 대화 LibreChat

LibreChat은 OpenAI ChatGPT의 혁신적인 기술과 다양한 AI 모델 통합 기능을 제공합니다.  
원본 스타일을 계승하면서, 대화/메시지 검색, 프롬프트 템플릿, 플러그인 등 다양한 기능을 강화했습니다.

LibreChat을 사용하면 ChatGPT Plus 없이도 무료 또는 사용량 기반 API로 다양한 AI를 활용할 수 있습니다.  
기여, 클론, 포크 모두 환영합니다!

[![영상 보기](https://raw.githubusercontent.com/LibreChat-AI/librechat.ai/main/public/images/changelog/v0.7.6.gif)](https://www.youtube.com/watch?v=ilfwGQtJNlI)

썸네일을 클릭하면 영상을 볼 수 있습니다☝️

---

## 🌐 리소스

**GitHub 저장소:**
  - **RAG API:** [github.com/danny-avila/rag_api](https://github.com/danny-avila/rag_api)
  - **웹사이트:** [github.com/LibreChat-AI/librechat.ai](https://github.com/LibreChat-AI/librechat.ai)

**기타:**
  - **웹사이트:** [librechat.ai](https://librechat.ai)
  - **문서:** [docs.librechat.ai](https://docs.librechat.ai)
  - **블로그:** [blog.librechat.ai](https://blog.librechat.ai)

---

## 📝 변경 이력

최신 업데이트는 아래에서 확인하세요:
- [릴리즈](https://github.com/danny-avila/LibreChat/releases)
- [변경 이력](https://www.librechat.ai/changelog) 

**⚠️ 업데이트 전 [변경 이력](https://www.librechat.ai/changelog)에서 주요 변경사항을 꼭 확인하세요.**

---

## ⭐ Star 히스토리

<p align="center">
  <a href="https://star-history.com/#danny-avila/LibreChat&Date">
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=danny-avila/LibreChat&type=Date&theme=dark" onerror="this.src='https://api.star-history.com/svg?repos=danny-avila/LibreChat&type=Date'" />
  </a>
</p>
<p align="center">
  <a href="https://trendshift.io/repositories/4685" target="_blank" style="padding: 10px;">
    <img src="https://trendshift.io/api/badge/repositories/4685" alt="danny-avila%2FLibreChat | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/>
  </a>
  <a href="https://runacap.com/ross-index/q1-24/" target="_blank" rel="noopener" style="margin-left: 20px;">
    <img style="width: 260px; height: 56px" src="https://runacap.com/wp-content/uploads/2024/04/ROSS_badge_white_Q1_2024.svg" alt="ROSS Index - Fastest Growing Open-Source Startups in Q1 2024 | Runa Capital" width="260" height="56"/>
  </a>
</p>

---

## ✨ 기여 안내

기여, 제안, 버그 리포트, 수정 모두 환영합니다!

새로운 기능, 컴포넌트, 확장 기능은 이슈를 먼저 열고 논의 후 PR을 보내주세요.

LibreChat의 다국어 번역에 기여하고 싶으시다면 언제든 환영합니다!  
번역 품질 향상은 전 세계 사용자 접근성과 경험을 높입니다.  
[번역 가이드](https://www.librechat.ai/docs/translation)를 참고하세요.

---

## 💖 이 프로젝트는 모든 기여자 덕분에 존재합니다

<a href="https://github.com/danny-avila/LibreChat/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=danny-avila/LibreChat" />
</a>

---

## 🎉 Special Thanks

LibreChat의 다국어 지원을 위해 번역 관리 도구를 제공해준 [Locize](https://locize.com)에 감사드립니다.

<p align="center">
  <a href="https://locize.com" target="_blank" rel="noopener noreferrer">
    <img src="https://github.com/user-attachments/assets/d6b70894-6064-475e-bb65-92a9e23e0077" alt="Locize Logo" height="50">
  </a>
</p>