# Ansible_course
1. Cоздание роли -
`mkdir roles`
`cd roles`
`cd os_update`
`mkdir defaults files handlers meta templates tasks vars`
 
Либо в папке roles выполнить команду `ansible-galaxy init os_update`

Структура роли `os_update`
- defaults: переменные отсутствуют
- files: статические файлы и файлы сценариев, которые могут быть скопированы на удалённый сервер или выполнены на нём, отсутствуют
- handlers: обработчики отсутствуют
- meta: метаданные роли, которые используются для управления зависимостями - отсутствуют
- templates: шаблоны отсутствуют
- tasks: задачи для выполнения Ansible
- vars: переменные для роли отсутствуют

2. В основной директории создаем файл inventory `hosts.ini` и `playbook2.yml` 
3. В файле inventory `hosts.ini` создаем группу серверов (для начала одного хватит =) )
4. Переходим в `roles/os_update/tasks` и заполняем файл `main.yml` для обновления ОС на сервере (пакет `python` не обновляем)
5. Пишем в основной директории `playbook2.yml` с указанием ролей и хостов
6. Запуск обновления ос (чтобы единожды ввести пароль от сервера вводим команду
`ansible-playbook -i hosts.ini playbook.yml -K`)