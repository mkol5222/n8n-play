```bash

docker volume create n8n_data

docker run -it --rm \
 --name n8n \
 -p 5678:5678 \
 -e NODE_ENV="development" \
 -e GENERIC_TIMEZONE="Europe/Prague" \
 -e TZ="Europe/Prague" \
 -e N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true \
 -e N8N_PROXY_HOPS=1 \
 -e N8N_PUSH_BACKEND=sse \
 -v n8n_data:/home/node/.n8n \
 docker.n8n.io/n8nio/n8n

 ```