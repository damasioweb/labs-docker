# Módulo 4 — Laboratórios (Docker)

## Lista de Labs

> Cada lab está em um repositório separado.  

### LAB 0 — Namespaces
- Objetivo: comprovar na prática o que é isolamento por namespaces `PID/NET/MOUNT/UTS/USER`.
- Repo: [jvnetobr/lab-namespaces](https://github.com/jvnetobr/lab-namespaces)

### LAB 1 — Dockerfile: Alpine + Nginx + Hello World
- Objetivo: criar **imagem própria**, entender `Dockerfile → build → run → ports → cache`.
- Repo: [jvnetobr/lab-dockerfile](https://github.com/jvnetobr/lab-dockerfile)

### LAB 2 — Inspeção e Troubleshooting (dia a dia)
- Objetivo: investigar “subiu mas não responde” usando `logs`, `exec`, `ps`, `stats`, etc.
- Repo: [jvnetobr/lab-inspect](https://github.com/jvnetobr/lab-inspect)

### LAB 3 — Volumes e Persistência (prática do dia a dia)
- Objetivo: entender persistência com **volume** (sem backup/restore).
- Repo: [jvnetobr/lab-volumes](https://github.com/jvnetobr/lab-volumes)

### LAB 4 — Networking: port mapping, bridge e DNS interno
- Objetivo: entender diferença entre acesso **público (host)** e **interno (rede Docker)**.
- Repo: [jvnetobr/lab-networking](https://github.com/jvnetobr/lab-networking)

### LAB 5 — Docker Compose: multi-container + logs + env + healthcheck introdutório
- Objetivo: subir/derrubar ambiente com 1 comando e depurar por serviço.
- Repo: [jvnetobr/lab-compose](https://github.com/jvnetobr/lab-compose)

---

## Evidências (padrão recomendado)

Para cada lab, **1 evidência por checkpoint** (print ou saída do comando final).  

---

## Padrão de entrega

Vamos padronizar a entrega e facilitar correção:

1) aluno faz **fork** do repo do lab  
2) cria uma branch `aluno/<nome-sobrenome>`  
3) commita apenas o necessário (ex.: Dockerfile, compose.yml, nginx.conf)  
4) abre PR para o **próprio fork**  
5) envia o link do PR como evidência


---

## Cheat sheet (comandos do dia a dia)

```bash
# Imagens
docker images
docker build -t nome:tag .
docker rmi <image>

# Containers
docker ps
docker ps -a
docker run --name app -p 8080:80 -d nginx:alpine
docker logs -f <container>
docker exec -it <container> sh
docker rm -f <container>

# Volumes e redes
docker volume ls
docker network ls

# Compose
docker compose up -d
docker compose ps
docker compose logs -f --tail 50
docker compose down
```
