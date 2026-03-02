# Host Health Check (Linux) — checklist rápido

## CPU / Load
- `uptime`
- `top -o %CPU`
- `ps aux --sort=-%cpu | head`

## Memória
- `free -h`
- `vmstat 1 5`

## Disco / Storage
- `df -h`
- `lsblk`
- `du -sh /var/* 2>/dev/null | sort -h | tail`

## Rede
- `ip a`
- `ip r`
- `ss -tulpn`
- `ping -c 3 1.1.1.1`

## Logs
- `journalctl -p 3 -n 50 --no-pager`
- `dmesg --level=err,warn | tail -n 50`