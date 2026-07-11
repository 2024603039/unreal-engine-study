# Day1 - Unreal Engine 5.8 MCP Study

작성일 : 2026-07-11

---

# 1. 실습 목적

이번 실습의 목적은 Unreal Engine 5.8에서 새롭게 제공하는 Model Context Protocol(MCP)을 이해하고, AI(Codex)와 연동하여 언리얼 엔진을 직접 제어하는 개발 환경을 구축하는 것이다.

또한 단순히 AI에게 명령을 수행하도록 하는 것이 아니라 여러 AI Agent가 각각 역할을 분담하는 Agent Team을 구성하여 실제 프로젝트에 적용하는 방법을 학습하는 것을 목표로 하였다.

---

# 2. Model Context Protocol(MCP)란?

Model Context Protocol(MCP)은 AI와 외부 프로그램을 연결하기 위한 표준 프로토콜이다.

기존에는 AI가 단순히 코드만 생성하였다면, MCP를 이용하면 AI가 실제 프로그램과 연결되어 프로그램 내부를 읽거나 수정하는 것이 가능하다.

Unreal Engine 5.8에서는 MCP Plugin을 통해 AI가 언리얼 에디터 내부를 직접 제어할 수 있도록 지원한다.

이를 통해 AI는 다음과 같은 작업을 수행할 수 있다.

- Actor 생성
- Actor 삭제
- Actor 이동
- Material 생성
- Scene 조사
- Asset 조사
- Blueprint 관련 작업
- 프로젝트 구조 분석

즉, AI가 단순한 코드 생성기를 넘어 실제 개발을 수행하는 Agent 역할을 수행할 수 있게 된다.

---

# 3. Unreal Engine 5.8 MCP

이번 실습에서는 Unreal Engine 5.8에서 제공하는 MCP 기능을 사용하였다.

MCP Server를 실행한 후 Codex와 연결하여 Unreal Engine 내부 Toolset을 사용할 수 있도록 설정하였다.

연결 구조는 다음과 같다.

```
Codex

↓

Unreal MCP

↓

Unreal Engine 5.8
```

MCP Server는 Localhost(127.0.0.1:8000)에서 실행하였다.

---

# 4. 개발 환경

| 항목 | 내용 |
|------|------|
| 운영체제 | Windows |
| Unreal Engine | 5.8 |
| AI | Codex |
| Protocol | Unreal MCP |
| MCP Server | localhost:8000 |

---

# 5. Unreal MCP 연결 과정

실습 과정은 다음 순서로 진행하였다.

① Unreal Engine 실행

↓

② MCP Plugin 활성화

↓

③ MCP Server 실행

↓

④ Codex 실행

↓

⑤ Toolset 확인

↓

⑥ AI와 Unreal Engine 연결

연결 이후 Codex에서 Unreal MCP Toolset을 정상적으로 인식하는 것을 확인하였다.

---

# 6. Toolset 확인

Codex를 이용하여 Unreal MCP에서 제공하는 Toolset을 확인하였다.

확인된 Toolset에는 다음과 같은 기능이 포함되어 있었다.

- Scene Tool
- Object Tool
- Material Tool
- Primitive Tool
- Animation Tool
- Behavior Tree Tool
- Data Asset Tool

이를 통해 Unreal Engine 대부분의 기능을 AI가 제어할 수 있음을 확인하였다.

---

# 7. AI Agent Team 구축

이번 실습에서는 여러 AI Agent가 각각 역할을 수행하도록 Agent Team을 구성하였다.

구성한 Agent는 다음과 같다.

- Project Manager
- Research Agent
- Level Designer Agent
- Technical Artist Agent
- QA Agent
- Documentation Agent

각 Agent는 서로 다른 역할을 담당하였다.

Project Manager는 전체 프로젝트를 관리하고, Research Agent는 MCP를 조사하였다.

Level Designer는 레벨 제작을 담당하였으며 Technical Artist는 시각적인 개선을 담당하였다.

QA Agent는 결과를 검증하였고 Documentation Agent는 Markdown 문서를 작성하도록 구성하였다.

---

# 8. 실습 내용

Level Designer Agent를 이용하여 현재 Level을 조사하였다.

이후 AI에게 Primitive Cube를 생성하도록 지시하였다.

생성된 Cube는 처음에는 지형 아래에 생성되어 화면에 보이지 않았다.

Outliner에서 Actor를 검색한 후 Focus(F) 기능을 이용하여 위치를 확인하였다.

이후 AI를 이용하여 Actor 위치를 수정하면서 정상적으로 Cube가 생성되는 것을 확인하였다.

이를 통해 AI가 Unreal Engine 내부를 실제로 제어하고 있음을 확인할 수 있었다.

---

# 9. 문제 발생 및 해결

## 문제 1

MCP 연결 실패

### 원인

MCP Server가 실행되지 않은 상태에서 Codex가 연결을 시도하였다.

### 해결

ModelContextProtocol.StartServer 8000 명령어를 이용하여 MCP Server를 실행하였다.

---

## 문제 2

Cube가 보이지 않음

### 원인

Landscape 아래에 생성되었기 때문이었다.

### 해결

Outliner에서 Actor를 검색한 후 Focus 기능을 이용하여 위치를 확인하였다.

Actor의 위치를 수정하여 정상적으로 확인하였다.

---

## 문제 3

JSON Warning 발생

### 원인

Unreal MCP가 일부 Delegate Property를 JSON Schema로 변환하지 못하여 발생한 Warning이었다.

### 해결

치명적인 오류가 아닌 Warning임을 확인하고 계속 진행하였다.

---

# 10. 실습 결과

이번 실습을 통해 Unreal Engine 5.8과 Codex를 성공적으로 연결하였다.

또한 MCP를 이용하여 Unreal Engine 내부 Toolset을 사용할 수 있었으며 AI Agent Team을 구성하여 실제 Unreal Engine을 제어하는 실습을 진행하였다.

AI가 생성한 Actor를 직접 확인함으로써 MCP 기반 개발 환경이 정상적으로 동작함을 확인하였다.

---

# 11. 느낀 점

기존에는 AI가 코드만 작성해 주는 도구라고 생각하였다.

하지만 MCP를 이용하면 AI가 실제 Unreal Engine을 직접 조작할 수 있다는 점이 매우 인상적이었다.

또한 여러 Agent가 역할을 나누어 협업하는 방식은 향후 대규모 프로젝트에서도 활용 가능성이 높다고 생각하였다.

앞으로는 Easy Waterscape 튜토리얼과 같은 실제 프로젝트에 Agent Team을 적용하여 AI 기반 개발 방식을 더욱 심화하여 학습할 예정이다.

---
