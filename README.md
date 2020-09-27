# flask-react-auth
Микросервисы: внутренняя служба аутентификации с помощью Python, Flask; клиентское приложение, которое использует JavaScript и React

В основі поточного проекту - проект flask_microservice.  
 
 Перевірка роботи базового проекту:  
 - `docker-compose up -d --build`  
 - перегляд API в Swager http://localhost:5001/doc/  
 - взаємодія з OSMX http://localhost:5001/ping
 - сворити базу даних  
 `docker-compose exec users python manage.py recreate_db`
 - заповнити базу даних тестовими даними  
 `docker-compose exec users python manage.py seed_db`  
 - переглянути список тестових даних http://localhost:5001/users  
 - відкрити адмін-панель http://localhost:5001/admin/user/  
 - тестува ти проект  
 `docker-compose exec users python -m pytest "project/tests" -p no:warnings --cov="project"`  
 - зупинити роботу контейнерів  
 `docker-compose stop`
 - вилучити контейнери  
 `docker-compose down` 
 PS: список основних команд в [проекті](https://testdriven.io/courses/auth-flask-react/getting-started/)  
  
 