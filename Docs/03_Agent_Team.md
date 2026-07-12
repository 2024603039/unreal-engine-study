# 03. AI Agent Team

**작성일 : 2026-07-11**

---

# 1. 실습 목적

이번 실습에서는 Unreal Engine 5.8의 MCP를 이용하여 여러 AI가 각각 역할을 나누어 작업하는 Agent Team에 대해 공부하였다.

또한 Codex를 이용하여 AI가 어떤 역할을 맡을 수 있는지 확인하고, 역할을 나누어 작업하는 방식이 어떻게 진행되는지 알아보는 것을 목표로 하였다.

---

# 2. Agent Team이란?

Agent Team은 하나의 AI가 모든 작업을 하는 것이 아니라 여러 AI가 각각 역할을 나누어 함께 작업하는 방식이다.

예를 들어 자료를 조사하는 AI, 맵을 만드는 AI, 결과를 확인하는 AI처럼 역할을 나누어 프로젝트를 진행할 수 있다.

이번 실습에서는 Agent Team의 개념을 이해하고 각 Agent의 역할을 확인하였다.

---

# 3. Agent Team 구성

이번 실습에서는 다음과 같은 Agent를 사용하였다.

```
Project Manager
│
├── Research Agent
├── Level Designer Agent
├── Technical Artist Agent
├── QA Agent
└── Documentation Agent
```

각 Agent는 맡은 역할에 따라 작업을 진행하며, Project Manager가 전체 작업을 관리하는 구조이다.

---

# 4. Project Manager

Project Manager는 전체 프로젝트를 관리하는 역할이다.

주요 역할은 다음과 같다.

- 작업 계획 세우기
- 작업 순서 정하기
- 다른 Agent에게 역할 나누기
- 작업 결과 확인하기

---

# 5. Research Agent

Research Agent는 필요한 자료를 조사하는 역할이다.

이번 실습에서는 다음 내용을 확인하였다.

- Unreal Engine 5.8 MCP 조사
- MCP 기능 확인
- 사용할 수 있는 Tool 확인

---

# 6. Level Designer Agent

Level Designer Agent는 언리얼 엔진 안에서 레벨을 구성하는 역할이다.

이번 실습에서는

- 현재 레벨 확인
- Actor 확인
- Cube 생성
- 위치 이동
- 레벨 저장

등의 작업을 수행하였다.

처음에는 생성한 Cube가 보이지 않았지만 Outliner에서 Actor를 찾고 **F 키**를 이용하여 위치를 확인한 뒤 정상적으로 배치할 수 있었다.

---

# 7. Technical Artist Agent

Technical Artist Agent는 화면을 보기 좋게 만드는 역할이다.

이번 실습에서는 직접 작업하지는 않았지만 앞으로 다음과 같은 작업을 진행할 예정이다.

- 조명 설정
- Material 적용
- 환경 꾸미기
- 화면 색상 조정

---

# 8. QA Agent

QA Agent는 작업 결과를 확인하는 역할이다.

이번 실습에서는

- Actor가 정상적으로 생성되었는지
- 위치가 올바른지
- 오류가 없는지

확인하는 과정을 진행하였다.

---

# 9. Documentation Agent

Documentation Agent는 실습 내용을 문서로 정리하는 역할이다.

이번 실습에서는 다음 문서를 작성하였다.

- README.md
- AGENTS.md
- 01_MCP_Study.md
- 02_MCP_Setup.md
- 03_Agent_Team.md

---

# 10. 실습 과정

이번 실습은 다음 순서로 진행하였다.

1. Unreal Engine과 Codex를 연결하였다.
2. Agent Team 구성을 확인하였다.
3. Research Agent가 필요한 내용을 조사하였다.
4. Level Designer Agent가 레벨을 확인하고 Cube를 생성하였다.
5. QA Agent가 결과를 확인하였다.
6. Documentation Agent가 실습 내용을 정리하였다.

---

# 11. 실습 결과

이번 실습을 통해 Agent Team의 개념을 이해할 수 있었다.

또한 하나의 AI가 모든 작업을 하는 것이 아니라 역할을 나누어 작업할 수 있다는 점을 알게 되었고, Codex를 이용하여 언리얼 엔진에서 기본적인 작업도 수행해 보았다.

---

# 12. 앞으로 해보고 싶은 것

앞으로는 이번에 공부한 Agent Team을 활용하여 다양한 언리얼 엔진 실습을 진행해 보고 싶다.

특히 Easy Waterscape와 같은 환경 제작 실습에서도 AI를 함께 활용하면서 작업 과정을 익혀볼 계획이다.

---

# 13. 느낀 점

처음에는 Agent Team이라는 개념이 어렵게 느껴졌지만, 역할을 나누어 생각해 보니 각각의 AI가 어떤 일을 하는지 이해하기 쉬웠다.

이번 실습을 통해 AI를 언리얼 엔진과 함께 사용할 수 있다는 점이 흥미로웠고, 앞으로 Blueprint, Material, Lighting 등 다양한 기능도 AI와 함께 공부해 보고 싶다.
