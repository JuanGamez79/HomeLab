# crafty

Docker Compose stack for crafty. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Ports

- `8443:8443          # Web UI (HTTPS)`
- `8124:8124          # Dynmap`
- `19132:19132/udp    # Bedrock`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
