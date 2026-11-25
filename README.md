# JWT authentication service

HTTP authentication service that issues and validates **JWT** tokens.

## Features

- TCP/HTTP server on a configurable port (Qt `QTcpServer`)
- User authentication and token issuing
- JWT signed with **HMAC-SHA256** (`QMessageAuthenticationCode`)
- JSON request/response payloads

## Stack

C++17, Qt 5 (Network, Core), qmake, Windows.

## Build

Requirements: Qt 5.15+, MSVC 2019+.

```bash
qmake Authservice.pro
nmake
Authservice.exe
```

The server starts listening on the configured port; tokens are checked on each
protected request.
