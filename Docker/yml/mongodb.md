

```
version: '3.8'
services:
  mongo:
    image: mongo
    container_name: mongo
    ports:
      - "27017:27017"
    volumes:
      - /home/mongo:/data/db
    environment:
      MONGO_INITDB_ROOT_USERNAME: admin
      MONGO_INITDB_ROOT_PASSWORD: admin

```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA4MzI1NDgzMV19
-->