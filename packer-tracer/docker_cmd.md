# 🐳 Docker Commands for `packet-tracer`

This file documents all useful commands for building, running, and managing the `packet-tracer:ubuntu22` container.

---

## 1. ✅ Allow X11 Access (Run First)

Before starting the container, run this **on your host** so GUI apps work:

```bash
xhost +local:
```

This allows local Docker containers to connect to your X server.

---

## 2. 🏗️ Build the Image

If you have a `Dockerfile`:

```bash
docker build -t packet-tracer:ubuntu22 .
```

This rebuilds the image with all your changes (aliases, dependencies, etc.).

---

## 3. 🚀 Run as Ephemeral (Fresh Each Time)

If you want a **fresh container every time** (will lose changes):

```bash
docker run -it --rm   --name packet-tracer   --env DISPLAY=$DISPLAY   --volume /tmp/.X11-unix:/tmp/.X11-unix   --privileged   packet-tracer:ubuntu22
```

---

## 4. 🖥️ Run as Persistent (Recommended)

If you want to **keep your changes** (aliases, installed packages, etc.):

### First time (create container):
```bash
docker run -it   --name packet-tracer   --env DISPLAY=$DISPLAY   --volume /tmp/.X11-unix:/tmp/.X11-unix   --privileged   packet-tracer:ubuntu22
```

### Next time (reuse container):
```bash
docker start -ai packet-tracer
```

### Stop when done:
```bash
docker stop packet-tracer
```

### Remove container manually:
```bash
docker rm packet-tracer
```

---

## 5. 🧹 Clean Up

Remove all stopped containers:

```bash
docker container prune
```

Remove unused images:

```bash
docker image prune
```

Remove everything (containers, images, volumes):

```bash
docker system prune -a
```

---

## 6. 🛠️ Quick Alias Setup Inside Container

If using a persistent container, you can add this alias once inside it:

```bash
echo "alias hunyoung='/usr/local/bin/hunyoung/hun-young-prod'" >> ~/.bashrc
source ~/.bashrc
```

Now you can just run:

```bash
hunyoung
```

instead of the full path.

---

✅ **Tip:** Always run `xhost +local:` **before** starting the container if you want GUI support.
