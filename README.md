# Ansible LEMP Stack

Развёртывание LEMP-стека (Nginx + PHP-FPM + MariaDB) с помощью Ansible.

## Структура

- `site.yml` — главный плейбук
- `roles/` — роли: nginx, php-fpm, mariadb, lemp-app
- `group_vars/all/vault.yml` — зашифрованные секреты (пароли)

## Запуск

```bash
ansible-playbook -i hosts.ini site.yml --ask-vault-pass
# или с файлом пароля
ansible-playbook -i hosts.ini site.yml --vault-password-file ~/.vault_pass
