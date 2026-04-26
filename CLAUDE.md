# WebSlides Vanilla Server

## Running the Server

Use `reloadserver` with HTTPS (self-signed certificate) for development:

```bash
reloadserver 8444 --certificate reference/server.pem
```

**Why reloadserver:** Provides auto-watch and hot-reload when editing HTML/CSS/JS files.

**Certificate:** `/home/lee/Downloads/webslides/vanilla-webslides-server/reference/server.pem`

**Port:** 8444 (8443 may be in use)

**Access:** https://localhost:8444/demos/
