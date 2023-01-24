<h1 align='center'>Установка PostgreSQL - сервера и настройка удалённого доступа на CentOS:</h1>
<p>
    <strong>Шаг 1. </strong> Создание playbook для запуска роли
</p>
<p><i>Пример:</i></p>

    ---
    - name: Deploy Postgresql server
      hosts: db01
      become: true 

      roles:
        - ansible-role-postgresql

<p>
    <strong>Шаг 2. </strong> Склонировать роль в дирректорию с playbook:
</p>

  <pre>git clone https://github.com/NewErr0r/ansible-role-postgresql.git</pre>
  
 <p>
    <strong>Шаг 3.</strong> Запустить playbook для развёртывания postgresql - сервера и настройки адалённого доступа:
</p>
  
  <pre>ansible-playbook -i inventory/db/hosts playbook.yml</pre>
