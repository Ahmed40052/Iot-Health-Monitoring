# Smart, Life-Aware IoT Health Monitoring

An AI-optimized communication architecture for local body-area patient monitoring.

ESP32 wearable node -> Gateway (ESP-NOW) -> FastAPI backend + SQLite -> live dashboard.

## Repository layout

| Folder | Layer | Owner |
|---|---|---|
| `firmware/sensor_node/` | Layer 1: sensing (MAX30102, AD8232, MPU6050) | Embedded |
| `firmware/gateway/` | Gateway: ESP-NOW receiver, controller, channel scan | Embedded |
| `ai/` | Layer 2: patient state model (Model 1) | AI and Database |
| `backend/` | Layer 4: FastAPI API + SQLite | Backend |
| `frontend/` | Layer 5: dashboard | Front-end |
| `shared/` | Agreed JSON packet format and constants | Everyone |
| `docs/` | Work plan, report, diagrams | Everyone |

## Branching

- `main`: always working. No direct pushes.
- One branch per task: `embedded/<task>`, `ai/<task>`, `backend/<task>`, `frontend/<task>`.
- Open a pull request into `main`; at least one teammate reviews it.

## Getting started

Each folder will get its own setup notes in its README as it is built.
