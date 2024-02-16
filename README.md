# Docker container management with Traefik v2 and Portainer

A Simple HTML Deployment set-up for a Traefik v2 reverse proxy along with Portainer and Docker Compose.

This set-up makes container management & deployment a breeze and the reverse proxy allows for running multiple applications on one Docker host. Traefik will route all the incoming traffic to the appropriate docker containers and through the open-source app Portainer you can speed up software deployments, troubleshoot problems and simplify migrations.

Detailed explanation how to use this in this blog post:
[Docker container management with Traefik v2 and Portainer](https://rafrasenberg.com/docker-compose-traefik-v2/)

## Run it

Change on `docker-compose.yml` file:

```yml
labels:
  - "traefik.http.routers.simple-html-secure.rule=Host(`simple-html.yourdomain.com`)"
```

```yml
`simple-html.yourdomain.com` for the desired domain pointing to server
```

```bash
git clone https://github.com/MADLABCG/simple-html.git ./simple-html
cd simple-html
docker-compose up -d
```
