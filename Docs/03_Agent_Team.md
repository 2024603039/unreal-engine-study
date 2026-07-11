# 03. AI Agent Team

작성일 : 2026-07-11

---

# 1. 실습 목적

이번 실습에서는 Unreal Engine 5.8 MCP 환경에서 여러 AI Agent가 각각의 역할을 수행하는 Agent Team을 구성하고, 실제 Unreal Engine 프로젝트에 적용하는 것을 목표로 하였다.

단일 AI에게 모든 작업을 맡기는 것이 아니라, 역할을 분리하여 프로젝트를 수행하는 방식을 학습하였다.

---

# 2. Agent Team이란?

Agent Team은 여러 AI Agent가 각각의 역할을 수행하며 하나의 프로젝트를 협업하는 개발 방식이다.

기존에는 하나의 AI가 모든 작업을 수행하였다.

하지만 프로젝트 규모가 커질수록 하나의 AI가 모든 작업을 수행하기에는 한계가 있다.

따라서 프로젝트 관리, 조사, 레벨 제작, 시각적 개선, 검증, 문서 작성 등을 각각의 Agent가 담당하도록 구성하였다.

---

# 3. Agent Team 구조

이번 실습에서는 다음과 같은 구조로 Agent Team을 구성하였다.

```
Project Manager
│
├── Research Agent
├── Level Designer Agent
├── Technical Artist Agent
├── QA Agent
└── Documentation Agent
```

Project Manager가 전체 프로젝트를 관리하고, 각 Agent는 자신의 역할에 따라 작업을 수행하도록 구성하였다.

---

# 4. Project Manager

Project Manager는 전체 프로젝트를 관리하는 역할을 수행하였다.

주요 업무는 다음과 같다.

- 프로젝트 목표 설정
- 작업 순서 결정
- Agent에게 작업 분배
- 작업 결과 확인
- 최종 승인

모든 Agent는 Project Manager의 계획에 따라 작업을 수행하였다.

---

# 5. Research Agent

Research Agent는 Unreal Engine 5.8 MCP를 조사하는 역할을 수행하였다.

주요 업무는 다음과 같다.

- Unreal Engine 5.8 MCP 조사
- Toolset 분석
- MCP 활용 방법 조사
- Markdown 보고서 작성

Research Agent는 실제 Unreal Engine을 수정하지 않고 정보를 수집하는 역할만 수행하였다.

---

# 6. Level Designer Agent

Level Designer Agent는 Unreal Engine 내부의 레벨을 구성하는 역할을 수행하였다.

이번 실습에서는 다음 작업을 수행하였다.

- 현재 Level 조사
- Actor 확인
- Primitive Cube 생성
- Actor 위치 수정
- Level 저장

생성된 Cube는 처음에는 Landscape 아래에 생성되어 화면에 보이지 않았다.

Outliner에서 Actor를 검색하고 Focus(F) 기능을 이용하여 위치를 확인한 뒤 위치를 수정하여 정상적으로 확인하였다.

---

# 7. Technical Artist Agent

Technical Artist Agent는 프로젝트의 시각적인 품질을 개선하는 역할을 수행하였다.

이번 실습에서는 실제 변경을 수행하지는 않았지만 다음과 같은 개선 계획을 수립하였다.

- Material 적용
- Lighting 개선
- Scene 시각적 개선
- 색상 구분

향후 Easy Waterscape 실습에서도 Technical Artist Agent를 활용하여 조명과 머티리얼을 개선할 예정이다.

---

# 8. QA Agent

QA Agent는 구현 결과를 검증하는 역할을 수행하였다.

검증 항목은 다음과 같다.

- Actor 생성 여부
- Actor 이름 확인
- Transform 확인
- 중복 생성 여부
- Scene 변경 사항 확인

QA Agent를 통해 생성된 Actor가 정상적으로 존재하는 것을 확인하였다.

---

# 9. Documentation Agent

Documentation Agent는 프로젝트 문서를 작성하는 역할을 수행하였다.

이번 실습에서는 다음 문서를 작성하였다.

- README.md
- AGENTS.md
- 01_MCP_Study.md
- 02_MCP_Setup.md
- 03_Agent_Team.md

향후 실습에서도 모든 작업을 Markdown 문서로 기록할 예정이다.

---

# 10. Agent Team 실습 과정

이번 실습은 다음 순서로 진행하였다.

1. Project Manager가 전체 작업 계획을 수립하였다.
2. Research Agent가 Unreal Engine 5.8 MCP를 조사하였다.
3. Level Designer Agent가 현재 Level을 조사하였다.
4. Primitive Cube를 생성하였다.
5. QA Agent가 생성 결과를 검증하였다.
6. Documentation Agent가 결과를 Markdown으로 정리하였다.

각 Agent는 자신의 역할만 수행하며 다른 Agent의 역할에는 관여하지 않도록 구성하였다.

---

# 11. 실습 결과

이번 실습을 통해 AI Agent Team을 성공적으로 구성하였다.

또한 Unreal Engine 5.8 MCP를 이용하여 AI가 실제 Unreal Engine 내부를 제어하고 Actor를 생성하는 과정을 확인하였다.

Agent Team 구조를 이용하면 프로젝트를 역할별로 분리하여 효율적으로 관리할 수 있다는 점을 확인하였다.

---

# 12. 향후 계획

향후 실습에서는 Easy Waterscape 튜토리얼을 동일한 Agent Team 구조를 이용하여 수행할 예정이다.

각 Agent가 자신의 역할을 수행하고 Documentation Agent가 모든 과정을 Markdown 문서로 기록하는 방식으로 프로젝트를 진행할 계획이다.

---

# 13. 느낀 점

이번 실습을 통해 하나의 AI에게 모든 작업을 맡기는 것보다 역할을 분리하여 협업하는 방식이 더욱 체계적이라는 점을 확인하였다.

특히 Project Manager를 중심으로 각 Agent가 자신의 역할만 수행하도록 구성하였기 때문에 작업을 명확하게 구분할 수 있었다.

앞으로는 Blueprint, Material, Animation, Easy Waterscape 등 다양한 Unreal Engine 프로젝트에도 Agent Team 방식을 적용하여 AI 기반 개발 환경을 지속적으로 학습할 계획이다.
