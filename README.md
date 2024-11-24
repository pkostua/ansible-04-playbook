
#### Описание playbook'a

Этот playbook предназначен для установки и настройки Clickhouse, Vector и Lighthouse. Он включает в себя следующие задачи:

* Установка Clickhouse с помощью RPM-пакетов.
* Создание базы данных в Clickhouse.
* Установка и настройка Vector.
* Создание каталога конфигурации Vector.
* Создание файла конфигурации Vector из шаблона.
* Запуск Vector в фоне.
* Установка статических файлов Lighthouse
* Установка веб сервера nginx
* Hастройка nginx для работы с Lighthouse

#### Требования

* Ansible 2.9.
* AlexeySetevoi/ansible-clickhouse 1.13
* pkostua/vector-role 0.0.0
* pkostua/lighthouse-role 0.0.0


#### Управление playbook'ом

Чтобы управлять playbook'ом, используйте следующие команды:

Используйте тэг vector для установки Vector
```
ansible-playbook site.yml -i inventory/prod.yml --tags="vector"
```

Используйте тэг clickhouse для установки Clickhouse
```
ansible-playbook site.yml -i inventory/prod.yml --tags="clickhouse"
```

Используйте тэг lighthouse для установки Lighthouse
```
ansible-playbook site.yml -i inventory/prod.yml --tags="lighthouse"
```

Запустите без тегов для установки Vector, Lighthouse и Clickhouse
```
ansible-playbook site.yml -i inventory/prod.yml 
```


### Источники

* [Clickhouse documentation](https://github.com/AlexeySetevoi/ansible-clickhouse)
* [Vector documentation](https://github.com/pkostua/vector-role)
* [Lighthouse documentation](https://github.com/pkostua/lighthouse-role)