
```

  

version: '3.8'

services:
postgres:
image: postgres

container_name: postgres

environment:

POSTGRES_DB: db

POSTGRES_USER: charles

POSTGRES_PASSWORD: charles

volumes:

- postgres_data:/var/lib/postgresql/data

ports:

- "5432:5432"

restart: unless-stopped

  

volumes:

postgres_data:

name: postgres_data
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTIxOTkyMjA5XX0=
-->