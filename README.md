# beigam-databases
Databases

Mongo DB

Запускам docker compose
```agsl
docker-compose up -d
```

Для удаления используем команду
```agsl
docker-compose down
```

Для запуска с инициализацией конфигурации используйте 
`startdb.sh`

Для создания пользователя заходим в ssh
```
docker exec -it mongo1 mongosh
```

Затем создаем пользователя
```agsl
db.createUser(
    {
        user: "test",
        pwd: "test",
        roles: [
            {
                role: "readWrite",
                db: "test"
            }
        ]
    }
);
```