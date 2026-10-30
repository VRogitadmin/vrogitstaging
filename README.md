# PayGate

Manual payment-collection platform (Admin · Partners · Branches).

Stack: Laravel 13 · PHP 8.5 (FrankenPHP) · PostgreSQL 18 · Redis 8 + Horizon · React/TypeScript via Inertia.

Live: https://a27pay.tech. Deploy a new version with `bash ~a27pay_tech/public_html/a27pay.tech/scripts/deploy-live.sh`.

## Local development (Docker)

The Docker stack (`compose.yaml`, `Makefile`, `docker/`) and the project documents (`Document/`) are kept
on the developer's machine only and are not in this repository.

```bash
sudo sh -c 'echo "127.0.0.1 a27pay.local api.a27pay.local pay.a27pay.local" >> /etc/hosts'
make setup
```

| URL                         | What               | Login                                     |
| --------------------------- | ------------------ | ----------------------------------------- |
| http://a27pay.local         | Portals            | `admin@a27pay.local` / `password`         |
| http://localhost:8080       | Adminer (database) | `paygate` / `secret`, database `paygate`  |
| http://localhost:8025       | Mailpit (emails)   | none                                      |
| http://a27pay.local/horizon | Queues             | none (local)                              |

`make help` lists all commands.
