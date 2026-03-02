# PostgreSQL — Backup & Restore (conceitual + comandos)

## Backup lógico (pg_dump)
- Backup de 1 banco:
  - `pg_dump -Fc -f backup.dump -d <db>`
- Restore:
  - `pg_restore -d <db> -c backup.dump`

## Backup do cluster (pg_dumpall)
- `pg_dumpall > all.sql`

## Boas práticas
- Testar restore periodicamente.
- Armazenar backups em local diferente do host.
- Versionar scripts de backup (não os backups).
- Definir retenção (ex: diários 7d, semanais 4s, mensais 6m).