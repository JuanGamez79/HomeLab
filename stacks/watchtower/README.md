# watchtower

Docker Compose stack for watchtower. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
