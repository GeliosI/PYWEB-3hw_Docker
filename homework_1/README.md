# Сборка образа

```
docker image build --tag=<image_name> .
```

# Запуск контейнера

```
docker run -d --rm -p <host_port>:80 --name <container_name> <image_name>
```

# Проверка

```
curl localhost:<host_port>
```