# Сборка образа

```
docker image build --tag=<image_name> .
```

# Запуск контейнера

```
docker run -d --rm -p <host_port>:8000 --name <container_name> <image_name>
```

Также дополнительно можно указать свои переменные окружения (`SECRET_KEY`, `DEBUG`, `ALLOWED_HOSTS`):

```
docker run -d --rm -p <host_port>:8000 -e SECRET_KEY=<secret_key> -e DEBUG=<debug> -e ALLOWED_HOSTS=<allowed_hosts> --name <container_name> <image_name>
```

# Проверка

```
curl localhost:8888
```