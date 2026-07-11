# AGENTS.md

# Unreal Engine 5.8 AI Agent Team

본 프로젝트는 Unreal Engine 5.8의 Model Context Protocol(MCP)을 활용하여 AI Agent Team 기반 개발 환경을 실습하기 위해 구성되었습니다.

각 Agent는 독립적인 역할을 수행하며, Project Manager가 전체 작업을 관리합니다.

---

# Agent Architecture

```
Project Manager
│
├── Research Agent
├── Level Designer Agent
├── Technical Artist Agent
├── QA Agent
└── Documentation Agent
```

---

# 1. Project Manager

## 역할

전체 프로젝트를 관리하는 메인 에이전트입니다.

## 주요 업무

- 프로젝트 목표 설정
- 작업 순서 결정
- 각 Agent에게 작업 분배
- 최종 결과 확인

---

# 2. Research Agent

## 역할

Unreal Engine과 MCP 관련 내용을 조사합니다.

## 주요 업무

- Unreal Engine 5.8 MCP 조사
- Toolset 분석
- 기능 조사
- 개발 방법 제안

## 결과물

- MCP 개념 정리
- Toolset 분석
- 학습 내용 보고서

---

# 3. Level Designer Agent

## 역할

언리얼 엔진 내부 레벨을 구성합니다.

## 주요 업무

- Actor 생성
- Actor 이동
- Actor 이름 변경
- Greybox 제작
- Scene 구성

## 이번 실습

- Floor 생성
- Cube 3개 생성
- 위치 설정
- 레벨 저장

---

# 4. Technical Artist Agent

## 역할

씬의 시각적인 품질을 개선합니다.

## 주요 업무

- 조명 구성
- Material 적용
- 색상 개선
- 환경 개선

## 담당 범위

- Lighting
- Material
- Visual Quality

---

# 5. QA Agent

## 역할

구현 결과를 검증합니다.

## 주요 업무

- Actor 존재 여부 확인
- 이름 확인
- Transform 확인
- Material 확인
- Lighting 확인

## 검증 항목

- 모든 Actor 생성 여부
- 위치 정확성
- 중복 생성 여부
- Unreal 오류 확인

---

# 6. Documentation Agent

## 역할

프로젝트 문서를 작성합니다.

## 주요 업무

- Markdown 작성
- GitHub 문서 작성
- 학습 내용 정리
- 실습 내용 정리

## 생성 문서

- README.md
- Day1_MCP_Study.md
- Day1_Practice.md

---

# Workflow

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

---

# Day 1 Achievement

- Unreal Engine 5.8 설치
- Unreal MCP 연결
- Codex 연결
- Toolset 확인
- AI Agent Team 구축
- AI를 통한 Actor 생성
- QA 검증
- Documentation 작성

---

# Goal

AI Agent Team을 활용하여 Unreal Engine 개발 과정을 자동화하고, MCP 기반 협업 개발 방식을 학습하는 것을 목표로 합니다.
