# ALICE-Semantic-Telemetry SaaS

Semantic telemetry event processing API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Semantic-Telemetry |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/events` | テレメトリイベント投入 |
| `GET  /api/v1/alerts` | 異常検知アラート |
| `GET  /api/v1/correlations` | イベント相関分析 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
