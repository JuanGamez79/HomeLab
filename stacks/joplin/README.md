# joplin

Docker Compose stack for joplin. Part of my [home lab](../../README.md).

## Setup
```bash
cp .env.example .env   # then fill in every CHANGE_ME value
docker compose up -d
```

## Ports

- `5432:5432`
- `22300:22300`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
