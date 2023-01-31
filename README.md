# beigam-databases
Databases 

Создаем Dockerfile
```agsl
FROM postgres
ENV POSTGRES_PASSWORD docker
ENV POSTGRES_DB beigam
COPY init_db.sql /docker-entrypoint-initdb.d/
```
где init_db.sql это возможный дамп существующей базы

Создаем образ с тегом _my-postgres-db_
```
docker build -t my-postgres-db ./
```

Чтобы посмотреть существующие образы
```
docker images -a
```

Отлично, теперь у нас есть собственный образ под названием my-postgres-db. Мы можем запустить его как контейнер, выполнив следующие действия:
```
docker run -d --name my-postgresdb-container -p 5432:5432 my-postgres-db
```
Теперь вы можете подключиться к этой базе данных, используя данные для входа, указанные в файле Dockerfile.

Если вы хотите удалить изображения, вы можете запустить эту команду:
```
docker image rm 'nameOfTheImage'
```