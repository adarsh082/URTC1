# Frontend Instructions (URTC Unity Plugin)

## Project Overview
URTC is a Unity Editor plugin that integrates collaboration features directly into the Unity interface, connecting to the RTC Server backend.

## Tech Stack
- **Engine:** Unity
- **Language:** C#
- **Editor Extension:** `UnityEditor` namespace
- **Git Integration:** `LibGit2Sharp`
- **Networking:** `UnityWebRequest` and WebSockets

## Directory Structure
- `Assets/Editor/`: Contains all editor scripts.
    - `URTC_Panel.cs`: Main UI and logic for the collaboration panel.
    - `URTC_WebSocketClient.cs`: Real-time communication with the backend.
    - `GitHelper.cs`: Wrapper for Git operations.
    - `EditorCoroutineManager.cs`: Utility for running coroutines in the editor.
- `Assets/Assets/`: Binary dependencies like `LibGit2Sharp.dll`.

## Development Workflow
- **Editor UI:** Open the URTC Panel via the Unity Editor menu.
- **Debugging:** Use `Debug.Log` for runtime feedback in the Unity Console.
- **Testing:** Use the Unity Test Runner for editor tests.

## Coding Conventions
- **Editor Safety:** Ensure all editor operations are safe and don't block the main thread unnecessarily.
- **API Communication:** Always use the defined headers (`X-Session-ID`) for protected routes.
- **WebSocket:** Maintain heartbeat/ping-pong to keep connection alive.
- **Git:** Use `GitHelper.cs` for repository management to ensure consistency.
