# wger

Docker Compose stack for wger. Part of my [home lab](../../README.md).

## Setup
```bash
docker compose up -d
```

## Ports

- `8090:80`

## Notes

- Volume paths in the compose file are specific to my host. Adjust them for yours.
- The `config/` folder is not in this repo (git-ignored). Recreate it before starting the stack.
