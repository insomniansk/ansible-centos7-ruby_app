# ansible-centos7-ruby_app
Развертывание веб-приложения Ruby на сервер с Centos 7.
На хосте с ansible использовались следующие версии ПО:
ansible [core 2.14.6]
python version = 3.10.6
jinja version = 3.1.2 (роль nginxinc.nginx требует Jinja последних версий).

По умолчанию создается база данных app, с пользователем app_user, служба systemd запускается от root.
При необходимости вы можете поменять значения переменных в defaults/main.yml соответствующей роли

Для развертывания приложения достаточно:
1) В hosts.ini добавить ваш сервер (смотрите для примера файла hosts.ini.example)
2) Установить зависимости командой ansible-galaxy install -r requirements.yml
3) Запустить плейбук командой ansible-playbook playbook.yml -i hosts.ini

