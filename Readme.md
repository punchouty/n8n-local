# Learn n8n 

> based on https://github.com/n8n-io/self-hosted-ai-starter-kit 
> Removed dependency on ollama. Ollama need to installed natively

## Local Setup

> for clean up ./data folder completely. All n8n, postgres, pgadmin, quadrant data is stored here


```bash
docker compose up -d
```

Start following containers

1. n8n
2. postgres - store n8n data
3. pgadmin - ui for postgres
4. quadrant - vector db


### Username and Password

#### Pgadmin

> Look at pgadmin service in docker-compose.yaml (Line 94 and 95)

* Url : http://localhost:8888/
* User Name : punchouty
* User Email : punchouty@gmail.com
* Password : strong-P@ssw0rd

#### Postgres (Access it via PgAdmin)

After login to pgadmin click on **Add Server**

* General Tab > Name : local
* Connection Tab > 

1. Host name/address : postgres
2. User Name : punchouty
3. Password : strong-P@ssw0rd

#### n8n

* Url : http://localhost:5678/ & Sign up
* Email : punchouty@gmail.com
* First Name : Rajan
* Last Name : Punchouty
* Password : strong-P@ssw0rd

#### Qdrant

* Web UI : lhttp://ocalhost:6333/dashboard
* Rest API : http://localhost:6333
* GRPC API: http://localhost:6334

### Setup Ollama (Optional)

1. Head to http://localhost:5678/home/credentials
2. Click on "Local Ollama service"
3. Change the base URL to "http://host.docker.internal:11434/"
