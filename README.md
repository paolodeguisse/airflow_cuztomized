Change your user password and login as you want. By default it is login: admin, password: admin.
```bash

    git clone https://github.com/xnuinside/airflow_in_docker_compose
    cd airflow_in_docker_compose
    docker-compose -f docker-compose-with-celery-executor.yml up --build
```

Typical errors:
in case of permissions denied make 
```
/usr/local/airflow/ instead of /opt/
```
in case 5432 port is not available make 
```bash
sudo lsof -i -P -n | grep 5432
pkill -f postgres
```