# folding@home

Inspired from <https://github.com/heichblatt/dockerfiles/blob/master/foldingathome/Dockerfile>

## Volumes

- `/var/lib/fahclient`: work unit data
- `/etc/fahclient`: F@H config

## Example

```
docker run \
    --rm \
    -v foldingathome-config:/etc/fahclient \
    -v foldingathome-workunit:/var/lib/fahclient \
    registry.gitlab.com/hydrargyrum/docker-images/foldingathome
```

