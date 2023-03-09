# test_devops
Test task for DevOps work

Для запуска плейбука необходимо:

1) Скачать проект на свой компьютер

2) Установить последнюю версию ansible, если он еще не установлен

3) В inventory файл [hosts] внести свой список серверов, заранее настроив доступ к ним по методу Identity/Pubkey

4) Выполнить команду:

ansible-playbook playbook.yml --extra-vars "ansible_user=root ansible_ssh_private_key_file=~/.ssh/id_ed25519_test"

* где переменная ansible_ssh_private_key_file=~/.ssh/id_ed25519 указывает на расположение вашего приватного ssh ключа
ansible_user=root пользователь на удаленном сервере, который будет запускать процессы, пользователь должен обладать правами root или sudo без пароля, так как многие процессы требуют такого уровня доступа