# 02. Unreal Engine 5.8 MCP Setup

작성일 : 2026-07-11

---

# 1. 실습 목적

이번 실습에서는 Unreal Engine 5.8과 OpenAI Codex를 Model Context Protocol(MCP)을 이용하여 연결하고, AI가 Unreal Engine을 직접 제어할 수 있는 개발 환경을 구축하는 것을 목표로 하였다.

---

# 2. 개발 환경

| 항목 | 내용 |
|------|------|
| Unreal Engine | 5.8 |
| AI | OpenAI Codex (GPT-5.5) |
| 운영체제 | Windows |
| MCP | Unreal Engine Model Context Protocol |
| 연결 방식 | localhost (127.0.0.1:8000) |

---

# 3. Unreal Engine 설치

Epic Games Launcher를 이용하여 Unreal Engine 5.8을 설치하였다.

설치 과정에서는 SSD를 설치 경로로 지정하였다.

설치 완료 후 새로운 프로젝트를 생성하여 MCP 실습 환경을 준비하였다.

---

# 4. MCP Plugin 활성화

Unreal Engine에서 MCP Plugin이 활성화되어 있는지 확인하였다.

Plugin 활성화 이후 Unreal Editor를 재실행하였다.

Plugin이 정상적으로 로드된 것을 확인하였다.

---

# 5. MCP Server 실행

Unreal Engine Console(Command)에서 다음 명령어를 입력하였다.

```text
ModelContextProtocol.StartServer 8000
```

실행 후 Output Log에서 다음과 같은 메시지를 확인하였다.

```
Starting MCP server on port 8000

Created new HttpListener on 127.0.0.1:8000
```

이를 통해 MCP Server가 정상적으로 실행되었음을 확인하였다.

---

# 6. Codex 실행

PowerShell에서 프로젝트 폴더로 이동한 후 Codex를 실행하였다.

```text
cd 프로젝트폴더

codex
```

Codex 실행 후 /mcp 명령을 이용하여 MCP Tool을 확인하였다.

처음에는 Tool 호출이 실패하였다.

```
HTTP request failed

Connection refused

127.0.0.1:8000
```

오류가 발생하였다.

---

# 7. 오류 해결

HTTP Error가 발생한 원인은 Unreal Engine에서 MCP Server가 실행되지 않았기 때문이었다.

Console에서

```text
ModelContextProtocol.StartServer 8000
```

명령을 다시 실행한 후 Codex에서 MCP를 다시 확인하였다.

정상적으로 연결되었다.

---

# 8. MCP Tool 확인

Codex에서

```text
/mcp
```

명령을 이용하여 연결 상태를 확인하였다.

다음과 같이 Unreal MCP가 정상적으로 인식되는 것을 확인하였다.

```
unreal-mcp

call_tool

list_toolsets

describe_toolset
```

이를 통해 Unreal Engine과 Codex가 성공적으로 연결되었음을 확인하였다.

---

# 9. Toolset 확인

다음으로 Toolset을 조회하였다.

```
list_toolsets
```

명령을 이용하여 Unreal Engine에서 제공하는 Toolset 목록을 확인하였다.

이를 통해 AI가 Unreal Engine 내부 기능을 사용할 수 있음을 확인하였다.

---

# 10. 권한 승인

Codex가 Unreal MCP Tool을 실행할 때 다음과 같은 권한 요청 창이 나타났다.

```
Allow

Allow for this session

Always allow
```

실습에서는 **Allow for this session**을 선택하여 동일한 작업을 반복 수행할 때마다 권한을 다시 요청하지 않도록 설정하였다.

---

# 11. 연결 확인

MCP 연결 이후 AI가 Unreal Engine과 정상적으로 통신하는 것을 확인하였다.

현재 Level을 조회하고 Actor 정보를 확인하는 기능이 정상적으로 수행되었다.

이를 통해 MCP 환경 구축이 성공적으로 완료되었음을 확인하였다.

---

# 12. 실습 결과

이번 실습을 통해 Unreal Engine 5.8과 Codex를 MCP를 이용하여 성공적으로 연결하였다.

또한 Toolset 조회와 Actor 정보 확인을 수행하면서 AI가 Unreal Engine과 직접 상호작용할 수 있는 환경을 구축하였다.

이후 Agent Team을 구성하여 실제 Level 제작 실습을 진행할 수 있는 기반을 마련하였다.

---

# 13. 느낀 점

처음에는 MCP 연결 과정에서 여러 오류가 발생하였다.

특히 HTTP Connection Error와 MCP Server 실행 문제로 인해 연결에 어려움을 겪었다.

하지만 원인을 하나씩 분석하며 해결하는 과정을 통해 MCP의 동작 원리를 이해할 수 있었다.

이번 실습을 통해 AI와 Unreal Engine을 직접 연결하는 환경을 구축할 수 있었으며, 이후 Agent Team 기반 개발 실습을 진행할 준비를 마칠 수 있었다.
