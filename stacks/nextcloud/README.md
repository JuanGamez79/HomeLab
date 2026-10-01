# nextcloud

Docker Compose stack for nextcloud. Part of my [home lab](../../README.md).

## Setup
```bash
cp .env.example .env   # then fill in every CHANGE_ME value
docker compose up -d
```

## Ports

- `8086:80   # change/remove if you use a reverse proxy`
- `8087:80   # change/remove if you use a reverse proxy`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
