# vaultwarden

Docker Compose stack for vaultwarden. Part of my [home lab](../../README.md).

## Setup
```bash
cp .env.example .env   # then fill in every CHANGE_ME value
docker compose up -d
```

## Ports

- `8085:80     # change if 8085 already in use`
- `3015:3012   # change if 3015 already in use`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
