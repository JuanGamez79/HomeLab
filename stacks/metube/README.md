# metube

Docker Compose stack for metube. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Ports

- `8089:8081`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
