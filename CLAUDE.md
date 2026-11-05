# base-components

Shared local infrastructure for Vivid Pay (docker compose: Postgres today; brokers, identity and
observability later). Local development only: the credentials here are not secrets.

**Product context lives in the `platform` repo** (`../platform`, https://github.com/vivid-pay/platform): `VISION.md`,
`ROADMAP.md` and the working agreements. Read `../wallet-service/CLAUDE.md` for the branching model,
commit and PR conventions, which apply here too (`feature/VPAY-<n>-<name>` from `develop`, PR into `develop`,
squash-merge, owner approves in chat).

## Rules for this repo
- Add a service here when an application needs it locally; document it in `README.md` (service table).
- Never put real secrets or production credentials in the compose file.
- Each application gets its own database/role inside shared services, not its own container.
- Start only what you need: `docker compose up -d <service>`.
