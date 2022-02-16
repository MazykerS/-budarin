Для работы данного yml файлы для начала нужно указать хосты в /etc/ansible/hosts
[test]
10.0.2.11
10.0.2.12
10.0.2.13

После чего создать и раздать ключи машинам
ssh-keygen (пробел пробел пробел)
ssh-copy-id root@10.0.2.11
ssh-copy-id root@10.0.2.12
ssh-copy-id root@10.0.2.13

Затем нужно установить зависимости для ANSIBLE
ansible-galaxy collection install community.general

Все файлы Jeniston 14 я выгрузил с помощью git clone в папку /gitfiles

После чего можно запсукать скрипт
ansible-playbook "путь к файлу"
ansible playbook /etc/ansible/playbooks/main.yml
