# wger

Docker Compose stack for wger. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Ports

- `8090:80`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
