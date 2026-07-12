# 02. Unreal Engine 5.8 MCP Setup

**작성일 : 2026-07-11**

---

# 1. 실습 목적

이번 실습에서는 Unreal Engine 5.8과 OpenAI Codex를 MCP(Model Context Protocol)를 이용하여 연결하는 방법을 공부하였다.

또한 AI가 언리얼 엔진과 연결되어 프로젝트를 확인하거나 작업을 수행할 수 있는 환경을 직접 구축하는 것을 목표로 하였다.

---

# 2. 개발 환경

| 항목 | 내용 |
|------|------|
| Unreal Engine | 5.8 |
| AI | OpenAI Codex (GPT-5.5) |
| 운영체제 | Windows |
| MCP | Unreal Engine Model Context Protocol |

---

# 3. Unreal Engine 설치

Epic Games Launcher를 이용하여 Unreal Engine 5.8을 설치하였다.

처음에는 HDD에 설치하였지만 설치 시간이 오래 걸려 SSD에 다시 설치하였다.

설치가 완료된 후 새로운 프로젝트를 생성하여 실습을 준비하였다.

---

# 4. MCP Server 실행

Unreal Engine에서 MCP Server를 실행하였다.

실행 후 Output Log를 확인하여 서버가 정상적으로 실행되었는지 확인하였다.

MCP Server가 실행되면 AI와 Unreal Engine이 서로 연결될 수 있는 상태가 된다.

---

# 5. Codex 연결

PowerShell에서 프로젝트 폴더로 이동한 후 Codex를 실행하였다.

Codex에서 `/mcp` 명령을 입력하여 Unreal Engine과 연결되는지 확인하였다.

처음에는 연결되지 않아 오류가 발생하였다.

---

# 6. 오류 해결

처음에는 Codex와 Unreal Engine이 연결되지 않아 오류가 발생하였다.

원인을 확인해 보니 MCP Server가 실행되지 않은 상태였다.

MCP Server를 다시 실행한 후 연결을 다시 시도하였고, 정상적으로 연결되는 것을 확인하였다.

이 과정을 통해 MCP Server가 실행되어 있어야 AI와 Unreal Engine이 통신할 수 있다는 것을 알게 되었다.

---

# 7. MCP 연결 확인

MCP가 정상적으로 연결된 후 `/mcp` 명령을 실행하여 연결 상태를 확인하였다.

또한 Unreal MCP에서 사용할 수 있는 기능들도 확인하였다.

이를 통해 Codex와 Unreal Engine이 정상적으로 연결되었음을 확인하였다.

---

# 8. Tool 확인

MCP에는 여러 기능을 사용할 수 있는 Tool이 있었다.

이번 실습에서는 Tool 목록을 확인하면서 어떤 기능을 사용할 수 있는지 살펴보았다.

앞으로 이러한 Tool을 이용하여 Actor 생성, 프로젝트 확인 등 다양한 작업을 수행할 수 있다는 것을 알게 되었다.

---

# 9. 권한 설정

Codex가 Unreal Engine에서 작업을 수행하려고 할 때 권한을 허용하는 창이 나타났다.

실습에서는 **Allow for this session**을 선택하여 같은 작업을 반복할 때마다 다시 허용하지 않아도 되도록 설정하였다.

---

# 10. 실습 결과

이번 실습에서는 Unreal Engine 5.8과 Codex를 MCP를 이용하여 성공적으로 연결하였다.

또한 MCP가 정상적으로 동작하는 것을 확인하고, 사용할 수 있는 Tool도 확인하였다.

이를 통해 AI와 Unreal Engine을 함께 사용할 수 있는 개발 환경을 구축할 수 있었다.

---

# 11. 느낀 점

이번 실습에서는 MCP를 연결하는 과정에서 여러 오류가 발생하였다.

처음에는 연결되지 않아 어려움을 겪었지만, 하나씩 원인을 찾아 해결하면서 MCP가 어떻게 동작하는지 조금씩 이해할 수 있었다.

직접 Codex와 Unreal Engine을 연결해 보니 AI를 이용하여 언리얼 엔진 작업을 도와줄 수 있다는 점이 신기했고, 앞으로 더 다양한 기능도 사용해 보고 싶다는 생각이 들었다.
