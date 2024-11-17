

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
      MONGO_INITDB_ROOT_USERNAME: db_name
      MONGO_INITDB_ROOT_PASSWORD: db_psd

```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MTc5NjQwNzFdfQ==
-->