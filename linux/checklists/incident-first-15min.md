# Primeiros 15 minutos de incidente (Linux)

## 1. Entendimento
- O que falhou?
- Escopo: isolado ou geral?
- Mudança recente?

## 2. Coleta rápida
- `uptime`
- `top`
- `free -h`
- `df -h`
- `ss -tulpn`

## 3. Logs
- `systemctl status <servico>`
- `journalctl -u <servico> -n 100`

## 4. Ação
- Mitigar
- Comunicar
- Registrar timeline