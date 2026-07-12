# AGENTS.md

# Unreal Engine 5.8 AI Agent Team

이번 실습에서는 Unreal Engine 5.8의 MCP(Model Context Protocol)를 이용하여 AI와 함께 작업하는 방법을 공부하였습니다.

AI는 하나만 사용하는 것이 아니라 각각 역할을 나누어 작업할 수 있다는 것을 알게 되었고, 이를 Agent Team이라고 합니다.

---

# Agent Team 구성

```
Project Manager
│
├── Research Agent
├── Level Designer Agent
├── Technical Artist Agent
├── QA Agent
└── Documentation Agent
```

각 Agent는 맡은 역할이 다르며 함께 하나의 프로젝트를 진행합니다.

---

# 1. Project Manager

### 역할

프로젝트 전체를 관리하는 역할입니다.

### 하는 일

- 프로젝트 목표 정하기
- 작업 순서 정하기
- 다른 Agent에게 작업 전달하기
- 최종 결과 확인하기

---

# 2. Research Agent

### 역할

필요한 정보를 찾아주는 역할입니다.

### 하는 일

- Unreal Engine 기능 조사
- MCP 기능 조사
- 필요한 자료 찾기
- 개발 방법 알아보기

---

# 3. Level Designer Agent

### 역할

언리얼 엔진에서 맵을 만드는 역할입니다.

### 하는 일

- Actor 배치
- Floor 만들기
- Cube 생성
- 위치 조정
- 레벨 저장

이번 실습에서는 기본 오브젝트를 배치하고 위치를 변경하는 연습을 하였습니다.

---

# 4. Technical Artist Agent

### 역할

맵을 보기 좋게 꾸미는 역할입니다.

### 하는 일

- 조명 설정
- Material 적용
- 색상 변경
- 환경 꾸미기

이번 실습에서는 기본적인 조명과 화면 구성을 확인하였습니다.

---

# 5. QA Agent

### 역할

작업이 제대로 되었는지 확인하는 역할입니다.

### 하는 일

- Actor가 잘 생성되었는지 확인
- 위치가 맞는지 확인
- 이름이 맞는지 확인
- 오류가 없는지 확인

---

# 6. Documentation Agent

### 역할

실습 내용을 문서로 정리하는 역할입니다.

### 하는 일

- README 작성
- Markdown 문서 작성
- 실습 내용 정리
- 학습 내용 정리

---

# 작업 순서

```
Research Agent
        │
        ▼
Project Manager
        │
        ▼
Level Designer
        │
        ▼
Technical Artist
        │
        ▼
QA Agent
        │
        ▼
Documentation Agent
```

Agent들이 각자의 역할을 수행하면서 하나의 프로젝트를 완성하는 방식입니다.

---

# 이번 실습에서 해본 내용

- Unreal Engine 5.8 설치
- Unreal MCP 연결
- Codex 연결
- MCP Tool 확인
- Agent Team 개념 이해
- AI를 이용한 기본 Actor 생성
- 결과 확인
- GitHub 문서 작성

---

# 느낀 점

이번 실습을 통해 AI와 함께 언리얼 엔진을 사용할 수 있다는 것을 알게 되었습니다.

아직은 MCP와 Agent Team 개념이 어렵지만, 앞으로 언리얼 엔진을 공부하면서 AI를 함께 활용하면 작업을 더 효율적으로 할 수 있을 것이라고 생각합니다.
