docker run -d \
  --name=webtop \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 3000:3000 \
  -p 3001:3001 \
  -v /path/to/data:/config \
  --shm-size="1gb" \
  --restart unless-stopped \
  lscr.io/linuxserver/webtop:ubuntu-kde


  docker run -d -p 3000:8080 -v open-webui:/app/backend/data --name open-webui ghcr.io/open-webui/open-webui:main


curl -LsSf https://astral.sh/uv/install.sh | sh



DATA_DIR=~/.open-webui uvx --python 3.11 open-webui@latest serve
