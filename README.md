# Sandbox server

Simple server for GUI playground

## Docker

### Build this image

```bash
docker build . -t hpf-sandbox-server
```

### Run this image

#### Using local storage

```bash
docker run -it --rm \
       -p 4800:4800 \
       -e HPF_PORT=4800 \
       -e HPF_HOSTNAME=domain.com \
       --name hpf-sandbox-server \
       hapify/sandbox-server
```

#### Using remote storage

```bash
docker run -it --rm \
       -p 4800:4800 \
       -e HPF_KEY=XXXXXXXXXXXXXXXXXXXXX \
       -e HPF_PROJECT=XXXXXXXXXXXXXXXXXXXXX \
       -e HPF_PORT=4800 \
       -e HPF_HOSTNAME=domain.com \
       -e HPF_API_URL=https://api.hapify.io/v1 \
       --name hpf-sandbox-server \
       hapify/sandbox-server
```
