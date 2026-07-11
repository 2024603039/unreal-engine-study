# Day1 - Unreal Engine 5.8 MCP Practice

작성일 : 2026-07-11

---

# 1. 실습 목표

오늘 실습에서는 Unreal Engine 5.8과 OpenAI Codex를 Model Context Protocol(MCP)을 통해 연결하고, AI Agent Team을 이용하여 언리얼 엔진을 직접 제어하는 개발 환경을 구축하는 것을 목표로 하였다.

---

# 2. 실습 환경

| 항목 | 내용 |
|------|------|
| Unreal Engine | 5.8 |
| AI | OpenAI Codex (GPT-5.5) |
| MCP | Unreal Model Context Protocol |
| 운영체제 | Windows |
| 개발 환경 | Unreal Editor + Codex |

---

# 3. 실습 과정

## 3.1 Unreal Engine 실행

새로운 프로젝트를 생성하고 Unreal Engine 5.8을 실행하였다.

이후 Model Context Protocol(MCP)을 사용할 수 있도록 플러그인을 활성화하였다.

---

## 3.2 MCP Server 실행

Unreal Editor의 Console(Command) 창에서 MCP Server를 실행하였다.

```
ModelContextProtocol.StartServer 8000
```

실행 후 로그를 통해 다음과 같은 메시지를 확인하였다.

- Starting MCP server on port 8000
- Starting all listeners
- Created new HttpListener on 127.0.0.1:8000

이를 통해 MCP Server가 정상적으로 실행되었음을 확인하였다.

---

## 3.3 Codex 연결

Codex를 실행한 뒤 Unreal MCP Tool을 인식하는지 확인하였다.

초기에는 HTTP Connection Error가 발생하였으나 MCP Server를 실행한 이후 정상적으로 연결되었다.

---

## 3.4 Toolset 확인

Codex에서 Unreal MCP Toolset을 조회하였다.

다양한 Toolset이 정상적으로 표시되었으며 Scene, Actor, Material, Primitive 등 다양한 기능을 사용할 수 있음을 확인하였다.

---

## 3.5 AI Agent Team 구성

이번 실습에서는 역할별 AI Agent를 구성하였다.

구성한 Agent는 다음과 같다.

- Project Manager
- Research Agent
- Level Designer Agent
- Technical Artist Agent
- QA Agent
- Documentation Agent

Project Manager가 전체 작업을 관리하고 각 Agent가 자신의 역할을 수행하도록 구성하였다.

---

## 3.6 Level Designer Agent 실행

Level Designer Agent에게 현재 Level을 조사하도록 요청하였다.

이후 기본 Primitive Cube를 생성하도록 지시하였다.

AI는 언리얼 엔진 내부의 Actor를 생성하고 위치를 설정하였다.

---

## 3.7 생성 결과 확인

처음에는 생성된 Cube가 화면에 보이지 않았다.

Outliner를 이용하여 Actor를 검색한 후 Focus(F) 기능을 이용하여 위치를 확인하였다.

확인 결과 Cube가 Landscape 아래에 생성되어 있었으며 위치를 수정한 뒤 정상적으로 확인할 수 있었다.

---

## 3.8 QA 검증

QA Agent를 이용하여 다음 항목을 검증하였다.

- Actor 생성 여부
- 위치 확인
- 이름 확인
- 중복 생성 여부
- Level 변경 사항

검증 결과 정상적으로 생성되었음을 확인하였다.

---

# 4. 문제 해결 과정

## 문제 1

Codex와 Unreal Engine 연결 실패

### 원인

MCP Server가 실행되지 않은 상태였다.

### 해결

Console에서 MCP Server를 실행한 후 다시 연결하였다.

---

## 문제 2

Actor가 화면에 보이지 않음

### 원인

Landscape 아래에 생성되었다.

### 해결

Outliner에서 Actor를 선택하고 Focus 기능을 이용하여 위치를 확인하였다.

---

## 문제 3

JSON Warning 발생

### 원인

일부 Delegate Property가 JSON Schema로 변환되지 않아 Warning이 발생하였다.

### 해결

Warning 메시지이며 프로젝트 실행에는 영향을 주지 않는다는 것을 확인하고 실습을 계속 진행하였다.

---

# 5. 실습 결과

이번 실습을 통해 Unreal Engine 5.8과 Codex를 성공적으로 연동하였다.

또한 MCP를 이용하여 AI가 언리얼 엔진 내부의 객체를 직접 생성하고 관리할 수 있음을 확인하였다.

AI Agent Team을 이용하여 역할을 분담하는 방식으로 프로젝트를 수행할 수 있음을 확인하였다.

---

# 6. 학습 내용

이번 실습을 통해 다음 내용을 학습하였다.

- Unreal Engine 5.8 MCP 사용 방법
- Codex 연동 방법
- MCP Server 실행 방법
- Toolset 확인 방법
- AI Agent Team 구성 방법
- Unreal Engine 내부 Actor 생성 과정
- QA 기반 검증 절차

---

# 7. 향후 계획

다음 실습에서는 Easy Waterscape 튜토리얼을 AI Agent Team과 함께 수행할 예정이다.

Level Designer, Technical Artist, QA Agent를 활용하여 단계별로 튜토리얼을 구현하고 모든 과정을 Markdown 문서로 기록할 계획이다.

---

# 8. 느낀 점

이번 실습을 통해 MCP를 이용하면 AI가 단순히 코드를 생성하는 수준을 넘어 Unreal Engine과 직접 상호작용할 수 있다는 점을 확인하였다.

또한 여러 Agent가 역할을 분담하여 협업하는 방식은 실제 프로젝트에서도 활용 가능성이 높다고 생각하였다.

앞으로는 다양한 Unreal Engine 프로젝트에 Agent Team을 적용하여 AI 기반 개발 방식을 지속적으로 학습할 계획이다.
