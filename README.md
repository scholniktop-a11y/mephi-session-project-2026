MEPHI Session Project 2026

Настройка базовых средств защиты ОС GNU/Linux (РЕД ОС 8.0.3, Server Minimal).

Студент: 372929
Хост: mephi-2026.domain.local

Разделы проекта

| Раздел | Файлы | Что проверяется |
|--------|-------|----------------|
| 1. Установка | hostnamectl.out, ip.out, ping.out | Имя хоста, сеть, связность |
| 2. Управление ПО | dnf.out | Обновление, установка пакетов, RPM |
| 3. Файловые системы | fstab, stat.out | ext4 MEPHI_WEB, монтирование |
| 4. Сервисы | journalctl.out | Nginx, автозапуск |
| 5.1. DAC | stat.out, getfacl | user1/2/3, curator1/2, ACL |
| 5.2. Capabilities | getcap.out | tcpdump cap_net_admin,cap_net_raw |
| 5.3. SELinux | getenforce.out, stat.out | Enforcing, httpd_sys_content_t |
| 6.1. Вход | pam-login, denied_users, curator-blocked.out | Запрет кураторам |
| 6.2. Пароли | shadow, pwquality.conf | 90 дней, minlen=12 |
| 7. Тестирование | curl.out, mephi-screenshot.png | Hello from Student: 372929 |
| 8. Публикация | history.out | История команд |

Основные настройки

- Hostname: mephi-2026.domain.local
- Second disk: /dev/sdb1, ext4, LABEL=MEPHI_WEB, монтируется в /mephi-web
- Web: nginx отдаёт /mephi-web/index.html
- Разработчики: user1 (5501), user2 (5502), user3 (5503), группа developers
- Кураторы: curator1 (5504), curator2 (5505), группа curators (4444)
- Директория проекта: /data/mephi-2026, права 2770 + ACL
- tcpdump: без set-UID, capability cap_net_admin,cap_net_raw
- SELinux: Enforcing
- Пароли: 90 дней, minlen = 12
