
```
version: '3.8'
services:
	postgres:
		image: postgres
		container_name: postgres
		environment:
			POSTGRES_DB: db_name
			POSTGRES_USER: user_name
			POSTGRES_PASSWORD: psd
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
eyJoaXN0b3J5IjpbLTEwMDg1Mzg2NV19
-->