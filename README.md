# Netshoot

The `netshoot` container has a set of powerful networking troubleshooting tools that can be used to troubleshoot Docker networking issues. Along with these tools come a set of use-cases that show how this container can be used in real-world scenarios.

## Usage

```bash
# local build
docker build -t netshoot .
docker run netshoot

# container net namespace
docker run -it --net container:<container_name> moabukar/netshoot


# normal

docker run -it --name netshoot-container moabukar/netshoot /bin/sh
```

## netshoot with k8s

```bash
# if you want to spin up a throw away pod for debugging.
kubectl run tmp-shell --rm -i --tty --image moabukar/netshoot

```
