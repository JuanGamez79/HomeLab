# portainer

Docker Compose stack for portainer. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Ports

- `9000:9000   # Web UI`
- `8000:8000   # Edge agent tunnel (optional)`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
