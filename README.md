# 🚀 Agentic Terminal Coder (ATC)
> **"Terminal-based Agentic Coding Assistant powered by Multi-LLM Rotation"**

ATC는 터미널(TUI) 환경에서 작동하는 자율 코딩 에이전트입니다. Google Gemini API와 GitHub Models API를 지능적으로 로테이션하여 **API 호출 제한 없이 24/7 개발을 지원**하며, 스킬(Skill) 기반의 반복적인 개선 루프를 통해 개발자의 생산성을 극대화합니다.

---

## 🛠 주요 특징 (Key Features)

* **🤖 Autonomous Agentic Loop:** 생각(Thought) → 행동(Action) → 관찰(Observation) 패턴으로 복잡한 코딩 과업을 스스로 해결합니다.
* **🔄 Intelligent Model Rotation:** Google Gemini(Gemma 4)를 메인 두뇌로, GitHub Models(GPT-4o-mini 등)를 백업으로 사용하는 **LiteLLM 기반 무중단 API 아키텍처**를 적용했습니다.
* **🏗 Skill-Creator Workflow:** 단순히 코드를 짜는 것을 넘어, 개발한 코드를 스스로 평가(Eval)하고 개선하는 반복적인 최적화 루프를 포함합니다.
* **🛡 Safety First:** 모든 터미널 명령어 실행은 사용자의 명시적인 승인(`Human-in-the-loop`) 없이는 작동하지 않습니다.
* **⚡ Ultra-Fast TUI:** `Rich` 및 `Textual`을 활용하여 터미널에서도 아름답고 직관적인 개발 경험을 제공합니다.

---

## 🏗 아키텍처 (Architecture)

```mermaid
graph TD
    User[Developer] --> TUI[TUI Interface]
    TUI --> Agent[Coding Agent]
    Agent --> LiteLLM[LiteLLM Router]
    LiteLLM --> Google[Google Gemini API]
    LiteLLM --> GitHub[GitHub Models API]
    Agent --> Tools[File System / Bash Tools]
    Agent --> Evals[Skill Creator Eval Loop]
