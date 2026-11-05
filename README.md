# base-components

Part of **Vivid Pay**; see the [platform](https://github.com/vivid-pay/platform) repo for the vision and roadmap.

Shared local infrastructure (databases, brokers, identity, observability) used by
the applications in this directory. Local development only: the credentials here
are not secrets.

## Usage
```bash
cd ~/Projects/base-components
docker compose up -d            # start everything
docker compose up -d postgres   # start just one service
docker compose down             # stop (data kept in volumes)
docker compose down -v          # stop and wipe data
```

## Services
| Service  | Port | Used by |
|----------|------|---------|
| postgres | 5432 | wallet  |
