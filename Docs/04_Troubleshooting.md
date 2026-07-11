# 04. Troubleshooting

작성일 : 2026-07-11

---

# 개요

Unreal Engine 5.8과 Model Context Protocol(MCP)을 이용하여 Codex와 연결하는 과정에서 여러 문제가 발생하였다.

이번 문서에서는 실습 중 발생한 문제와 해결 과정을 기록하였다.

---

# 문제 1. Unreal MCP 연결 실패

## 증상

Codex에서 Unreal MCP Tool을 실행하려고 하였으나 다음과 같은 오류가 발생하였다.

```
HTTP request failed

Connection refused

http://127.0.0.1:8000/mcp
```

---

## 원인

Unreal Engine에서 MCP Server가 실행되지 않은 상태였다.

Codex는 localhost(127.0.0.1:8000)로 접속을 시도하였지만 MCP Server가 실행되지 않아 연결할 수 없었다.

---

## 해결

Unreal Engine Console(Command)에 다음 명령어를 입력하였다.

```text
ModelContextProtocol.StartServer 8000
```

Output Log에서 다음 메시지를 확인하였다.

```
Starting MCP server on port 8000

Created new HttpListener on 127.0.0.1:8000
```

이후 Codex와 정상적으로 연결되었다.

---

# 문제 2. Tool 실행 권한 요청

## 증상

Codex가 Unreal MCP Tool을 사용할 때마다 권한 요청 창이 반복적으로 나타났다.

```
Allow

Allow for this session

Always allow
```

---

## 원인

보안을 위해 MCP Tool 실행 시 사용자 승인을 요구하는 기능이었다.

---

## 해결

```
Allow for this session
```

을 선택하여 현재 세션에서는 권한을 다시 요청하지 않도록 설정하였다.

---

# 문제 3. Level 저장 중 멈춤

## 증상

새로운 Level을 저장하는 과정에서

```
Saving Packages

0%
```

상태가 지속되며 진행되지 않았다.

---

## 원인

저장 과정에서 Unreal Editor가 정상적으로 응답하지 않는 상태가 발생하였다.

---

## 해결

중요한 작업이 없는 것을 확인한 후 Unreal Editor를 종료하였다.

프로젝트를 다시 실행한 뒤 Level을 다시 저장하여 문제를 해결하였다.

---

# 문제 4. 생성한 Cube가 화면에 보이지 않음

## 증상

Level Designer Agent가 Cube를 생성하였지만 화면에는 아무것도 보이지 않았다.

---

## 원인

Actor는 정상적으로 생성되었지만 Landscape 아래쪽에 생성되어 카메라에서 보이지 않았다.

---

## 해결

Outliner에서 생성된 Actor를 검색하였다.

```
SM_Cube_Center
```

선택 후

```
F
```

키를 이용하여 Focus 기능을 실행하였다.

Actor 위치를 수정한 후 정상적으로 Cube를 확인할 수 있었다.

---

# 문제 5. JSON Warning 발생

## 증상

Output Log에서 다음과 같은 Warning이 반복적으로 출력되었다.

```
LogJson: Warning

Property type ...

Unhandled during Json schema generation
```

---

## 원인

Unreal MCP가 일부 Delegate Property를 JSON Schema로 변환하지 못하여 발생한 Warning이었다.

---

## 해결

Warning 메시지이며 Unreal Engine 실행에는 영향을 주지 않는다는 것을 확인하였다.

실습을 계속 진행하였다.

---

# 문제 6. Agent 동시 실행 제한

## 증상

Agent Team을 실행하는 과정에서 다음과 같은 메시지가 나타났다.

```
Concurrent agent limit reached
```

---

## 원인

Codex에서 동시에 실행 가능한 Agent 수에 제한이 있었기 때문이다.

---

## 해결

Agent가 하나의 작업을 완료한 후 다음 Agent를 실행하도록 순차적으로 진행하였다.

Research Agent, Level Designer Agent, Technical Artist Agent, QA Agent 순으로 작업을 수행하였다.

---

# 문제 7. MCP Tool 권한 확인

## 증상

Tool 실행 시 MCP가 사용자의 승인을 요구하였다.

---

## 원인

외부 프로그램이 Unreal Engine을 직접 수정하기 때문에 보안상 승인이 필요하였다.

---

## 해결

실습 중에는

```
Allow for this session
```

을 선택하여 동일한 세션에서는 반복적인 승인을 생략하였다.

---

# 실습을 통해 배운 점

이번 실습에서는 다양한 오류가 발생하였지만 대부분 원인을 분석하고 단계적으로 해결할 수 있었다.

특히 HTTP 연결 오류와 Actor 위치 문제는 MCP와 Unreal Engine의 동작 방식을 이해하는 데 도움이 되었다.

또한 단순히 오류를 해결하는 것뿐만 아니라 문제의 원인을 분석하는 과정이 중요하다는 점을 확인하였다.

---

# 향후 계획

향후 Easy Waterscape 튜토리얼을 진행하면서 발생하는 문제도 동일한 방식으로 기록할 예정이다.

Troubleshooting 문서를 지속적으로 관리하여 문제 해결 경험을 축적하고 AI 기반 Unreal Engine 개발 환경에 대한 이해를 높일 계획이다.
