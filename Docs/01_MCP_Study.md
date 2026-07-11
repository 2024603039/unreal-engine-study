# 01. Unreal Engine 5.8 MCP Study

작성일 : 2026-07-11

---

# 1. 실습 목적

이번 실습의 목적은 Unreal Engine 5.8에서 제공하는 Model Context Protocol(MCP)의 개념을 이해하고, AI와 언리얼 엔진을 연동하여 개발 환경을 구축하는 것이다.

또한 MCP를 활용하여 AI가 언리얼 엔진을 직접 제어하는 과정을 학습하고, Agent Team 기반 개발 방식이 실제 프로젝트에서 어떻게 활용될 수 있는지 확인하는 것을 목표로 하였다.

---

# 2. Model Context Protocol(MCP)이란?

Model Context Protocol(MCP)은 AI 모델과 외부 프로그램을 연결하기 위한 표준 프로토콜이다.

기존의 생성형 AI는 코드 생성이나 문서 작성과 같은 작업에 주로 활용되었다. 그러나 MCP를 사용하면 AI가 외부 프로그램과 직접 연결되어 현재 상태를 조회하거나 필요한 작업을 수행할 수 있다.

즉, AI는 단순히 코드를 작성하는 도구가 아니라 실제 프로그램과 상호작용하는 Agent로 동작하게 된다.

---

# 3. Unreal Engine 5.8에서의 MCP

Unreal Engine 5.8에서는 Model Context Protocol Plugin을 통해 AI가 Unreal Editor와 직접 연결될 수 있다.

MCP를 이용하면 AI는 현재 열려 있는 프로젝트의 정보를 읽고 필요한 작업을 수행할 수 있다.

예를 들어 다음과 같은 작업이 가능하다.

- 현재 레벨 조회
- Actor 생성 및 삭제
- Actor 이동
- Material 생성
- Asset 검색
- Scene 분석
- Toolset 조회

---

# 4. MCP의 동작 구조

이번 실습에서는 다음과 같은 구조로 MCP를 사용하였다.

```
Codex

↓

Model Context Protocol

↓

Unreal Engine 5.8
```

Codex가 사용자의 요청을 분석한 후 MCP를 통해 Unreal Engine으로 명령을 전달하며, Unreal Engine은 수행 결과를 다시 Codex에 전달한다.

---

# 5. MCP Toolset

MCP는 다양한 Toolset을 제공한다.

이번 실습에서 확인한 Toolset에는 다음과 같은 기능이 포함되어 있었다.

- Scene Tool
- Actor Tool
- Primitive Tool
- Material Tool
- Animation Tool
- Data Asset Tool
- Behavior Tree Tool

Toolset을 통해 Unreal Engine의 다양한 기능을 AI가 사용할 수 있음을 확인하였다.

---

# 6. MCP의 장점

MCP를 사용하면 다음과 같은 장점이 있다.

- Unreal Engine과 AI를 직접 연결할 수 있다.
- 반복적인 작업을 자동화할 수 있다.
- 프로젝트 구조를 AI가 이해할 수 있다.
- 여러 AI Agent가 협업하는 개발 환경을 구축할 수 있다.
- 실시간으로 Unreal Engine 상태를 조회할 수 있다.

---

# 7. 이번 실습에서 확인한 내용

이번 실습에서는 Unreal Engine 5.8과 Codex를 MCP를 통해 성공적으로 연결하였다.

또한 Toolset을 조회하고 AI가 Unreal Engine 내부의 객체를 생성할 수 있음을 확인하였다.

이를 통해 MCP가 단순한 코드 생성 기능이 아니라 실제 Unreal Engine 개발을 지원하는 인터페이스라는 점을 확인하였다.

---

# 8. 느낀 점

기존에는 AI가 코드를 작성하는 수준에서만 활용된다고 생각하였다.

하지만 MCP를 활용하면 AI가 Unreal Engine과 직접 상호작용하여 프로젝트를 분석하고 필요한 작업을 수행할 수 있다는 점이 매우 인상적이었다.

특히 여러 Agent가 역할을 분담하여 하나의 프로젝트를 수행하는 방식은 향후 게임 개발에서도 충분히 활용될 수 있을 것으로 생각된다.

앞으로는 다양한 Unreal Engine 프로젝트에 MCP와 AI Agent Team을 적용하여 보다 효율적인 개발 방식을 학습할 계획이다.
