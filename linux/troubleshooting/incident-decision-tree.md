# Linux Incident Decision Tree

Guia de decisão estruturado para diagnóstico inicial de incidentes em hosts Linux.

---

## Sintoma: Aplicação lenta

1. Verificar load:
   - `uptime`
   - load > número de cores? (ex: 8 cores / load 20)

2. Verificar CPU:
   - `top -o %CPU`
   - Processo específico consumindo?

3. Verificar memória:
   - `free -h`
   - Swap ativa?
   - `vmstat 1 5`

4. Verificar I/O:
   - `iostat -xz 1 3`
   - %util > 80%?

5. Verificar rede:
   - `ss -s`
   - `iftop`

---

## Sintoma: Serviço caiu

1. `systemctl status <service>`
2. `journalctl -u <service> -n 100`
3. Verificar:
   - Porta já em uso?
   - Permissão?
   - Disco cheio?
   - Config alterada?

---

## Sintoma: Disco cheio

1. `df -h`
2. `du -sh /* 2>/dev/null | sort -h | tail`
3. Verificar:
   - /var/log
   - backups acumulados
   - arquivos temporários
4. Se for inode:
   - `df -i`

---

## Sintoma: Host instável / travando

1. `dmesg | tail`
2. Verificar OOM Killer
3. Verificar kernel panic logs
4. Verificar saturação contínua

---

## Regra SRE

- Mitigar primeiro.
- Investigar depois.
- Documentar sempre.