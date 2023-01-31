# beigam-databases
Databases

Redis

Запуск

```
docker run --name my-redis-db -d redis
```

Запуск с сохранением на диск каждые 60 сек
```agsl
docker run --name my-redis-db -d redis redis-server --save 60 1 --loglevel warning
```