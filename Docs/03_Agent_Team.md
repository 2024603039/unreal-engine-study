# 03. AI Agent Team

**작성일 : 2026-07-11**

---

# 1. 실습 목적

이번 실습에서는 Unreal Engine 5.8의 MCP를 이용하여 AI Agent Team이 어떻게 구성되는지 공부하였다.

또한 하나의 AI가 모든 작업을 수행하는 것이 아니라 여러 AI가 각각 역할을 나누어 프로젝트를 진행하는 방식을 이해하는 것을 목표로 하였다.

---

# 2. Agent Team이란?

Agent Team은 여러 AI가 각각 역할을 맡아 하나의 프로젝트를 함께 진행하는 방식이다.

예를 들어 자료를 조사하는 AI, 레벨을 만드는 AI, 결과를 확인하는 AI처럼 역할을 나누어 작업할 수 있다.

이번 실습에서는 Agent Team의 기본적인 구조를 이해하는 데 중점을 두었다.

---

# 3. Agent Team 구성

이번 실습에서는 다음과 같은 구조로 Agent Team을 구성하였다.

```
                    Project Manager
                           │
 ┌────────────┬────────────┼────────────┬────────────┐
 │            │            │            │            │
Research   Level      Lighting     QA      Documentation
 Agent     Designer     Agent      Agent      Agent
```

Project Manager가 전체 작업을 관리하고, 각 Agent는 자신의 역할에 맞는 작업을 수행하는 방식이다.

---

# 4. Project Manager

Project Manager는 프로젝트 전체를 관리하는 역할이다.

주요 역할은 다음과 같다.

- 프로젝트 목표 설정
- 작업 계획 관리
- 각 Agent에게 역할 분배
- 작업 진행 상황 확인
- 최종 결과 확인

---

# 5. Research Agent

Research Agent는 필요한 자료를 조사하는 역할이다.

이번 실습에서는

- Unreal Engine 5.8 조사
- MCP 기능 조사
- Tool 사용 방법 조사

등을 진행하였다.

---

# 6. Level Designer Agent

Level Designer Agent는 언리얼 엔진에서 레벨을 구성하는 역할이다.

이번 실습에서는

- 레벨 확인
- Actor 생성
- Actor 위치 수정
- 레벨 저장

등의 작업을 수행하였다.

생성한 Actor가 화면에 보이지 않는 문제도 있었지만 Outliner와 Focus(F) 기능을 이용하여 위치를 확인할 수 있었다.

---

# 7. Lighting Agent

Lighting Agent는 조명과 화면 분위기를 담당하는 역할이다.

이번 실습에서는 직접 조명을 수정하지는 않았지만 앞으로 다음 내용을 공부할 예정이다.

- Directional Light
- Sky Light
- Environment Light
- Post Process

교수님께서 말씀해 주신 것처럼 앞으로는 그래픽스가 어떻게 연결되는지 이해하는 데 집중하면서 조명도 함께 공부할 계획이다.

---

# 8. QA Agent

QA Agent는 작업 결과를 확인하는 역할이다.

이번 실습에서는

- Actor가 정상적으로 생성되었는지
- 위치가 올바른지
- 레벨이 정상적으로 저장되었는지

등을 확인하였다.

---

# 9. Documentation Agent

Documentation Agent는 실습 내용을 문서로 정리하는 역할이다.

이번 실습에서는

- README.md
- AGENTS.md
- MCP Study
- MCP Setup
- AI Agent Team
- Troubleshooting

문서를 작성하였다.

교수님께서 말씀해 주신 것처럼 AI가 작성한 내용을 그대로 사용하는 것이 아니라 직접 읽어보고 수정하면서 문서를 작성하였다.

---

# 10. 이번 실습에서 배운 점

이번 실습에서는 AI Agent Team의 기본적인 구조를 이해할 수 있었다.

또한 역할을 나누어 작업하면 프로젝트를 더 체계적으로 관리할 수 있다는 점도 알게 되었다.

아직은 기본적인 Agent만 사용하였지만 앞으로 언리얼 엔진을 더 공부하면서 필요한 Agent를 추가하여 활용해 보고 싶다.

---

# 11. 앞으로의 계획

이번에는 기본적인 Agent Team만 구성하였다.

앞으로는 교수님께서 말씀해 주신 것처럼

- Camera Agent
- Material Agent
- Animation Agent
- Physics Agent

등 역할을 더욱 세분화하여 프로젝트를 진행해 보고자 한다.

또한 Easy Waterscape와 같은 실습에서도 AI를 활용하면서 그래픽스 파이프라인을 이해하는 데 집중할 계획이다.

---

# 12. 느낀 점

처음에는 Agent Team이라는 개념이 조금 어렵게 느껴졌지만 역할을 하나씩 나누어 생각해 보니 이해하기 쉬웠다.

특히 하나의 AI가 모든 작업을 수행하는 것이 아니라 필요한 역할을 나누어 사용할 수 있다는 점이 인상적이었다.

이번 실습을 통해 AI를 언리얼 엔진과 함께 활용하는 방법을 배울 수 있었고, 앞으로 그래픽스와 언리얼 엔진을 공부하면서 더 다양한 Agent를 활용해 보고 싶다.
