# AGENTS.md

# Unreal Engine 5.8 AI Agent Team

이번 프로젝트에서는 Unreal Engine 5.8과 MCP(Model Context Protocol)를 이용하여 AI와 함께 개발하는 환경을 공부하였습니다.

처음에는 AI 하나가 모든 작업을 하는 줄 알았지만, 여러 AI가 각각 역할을 나누어 작업하는 Agent Team 방식도 사용할 수 있다는 것을 알게 되었습니다.

이번 실습에서는 기본적인 Agent Team을 구성하여 각 역할이 어떤 일을 하는지 확인해 보았습니다.

---

# Agent Team 구조

```
                    Project Manager
                           │
 ┌────────────┬────────────┼────────────┬────────────┐
 │            │            │            │            │
Research   Level      Lighting     QA      Documentation
 Agent     Designer     Agent      Agent      Agent
```

Project Manager가 전체 작업을 관리하고, 각 Agent는 맡은 역할에 따라 작업을 수행합니다.

이번 실습에서는 Agent Team의 기본 구조를 이해하는 것을 목표로 하였습니다.

---

# Project Manager

프로젝트 전체를 관리하는 역할입니다.

### 담당 작업

- 프로젝트 목표 정하기
- 작업 계획 세우기
- 각 Agent에게 작업 분배
- 작업 진행 상황 확인
- 최종 결과 확인

Project Manager는 직접 작업하기보다는 전체 진행 상황을 관리하는 역할을 합니다.

---

# Research Agent

필요한 자료를 조사하는 역할입니다.

### 담당 작업

- Unreal Engine 기능 조사
- MCP 기능 조사
- Tool 사용법 조사
- 필요한 자료 찾기

이번 실습에서는 Unreal Engine 5.8과 MCP에 대해 조사하였습니다.

---

# Level Designer Agent

언리얼 엔진에서 맵을 만드는 역할입니다.

### 담당 작업

- Actor 배치
- Cube 생성
- Floor 생성
- 오브젝트 위치 수정
- 레벨 저장

이번 실습에서는 기본 오브젝트를 배치하고 위치를 변경하는 연습을 하였습니다.

---

# Lighting Agent

씬의 조명과 분위기를 만드는 역할입니다.

이번 실습에서는 직접 작업하지는 않았지만 앞으로 학습하면서 사용할 예정입니다.

### 담당 작업

- Directional Light
- Sky Light
- Environment Light
- Post Process

---

# QA Agent

작업 결과를 확인하는 역할입니다.

### 담당 작업

- Actor 생성 확인
- 위치 확인
- 이름 확인
- 오류 확인
- 레벨 정상 저장 여부 확인

---

# Documentation Agent

실습 내용을 문서로 정리하는 역할입니다.

### 담당 작업

- README 작성
- Markdown 문서 작성
- 실습 내용 정리
- 학습 내용 정리

---

# 이번 실습에서 수행한 내용

- Unreal Engine 5.8 설치
- MCP 연결
- Codex 연결
- AI Agent Team 구성
- 기본 Actor 생성
- GitHub 문서 작성

---

# 앞으로의 계획

교수님께서 말씀해 주신 것처럼 앞으로는 Agent를 더 세분화하여 사용할 계획입니다.

예를 들어

- Camera Agent
- Material Agent
- Animation Agent
- Physics Agent

등으로 역할을 나누어 더 효율적으로 프로젝트를 진행해 보고자 합니다.

---

# 느낀 점

처음에는 Agent Team이라는 개념이 조금 어려웠지만, 역할을 나누어 생각하니 각각의 AI가 어떤 일을 하는지 이해하기 쉬웠습니다.

아직은 기본적인 구조만 사용해 보았지만 앞으로 언리얼 엔진을 더 공부하면서 다양한 Agent를 활용해 보고 싶습니다.
