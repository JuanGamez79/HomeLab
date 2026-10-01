# vpn

Docker Compose stack for vpn. Part of my [home lab](../../README.md).

## Setup
```bash
cp .env.example .env   # then fill in every CHANGE_ME value
docker compose up -d
```

## Ports

- `9091:9091`
- `6789:6789      `
- `8989:8989`
- `7878:7878`
- `9696:9696`
- `8191:8191`
- `11011:11011`

## Notes

- Secrets are not stored in the compose file; they come from `.env`, which is git-ignored.
- Volume paths in the compose file are specific to my host. Adjust them for yours.
