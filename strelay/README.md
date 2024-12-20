# syncthing relay

https://docs.syncthing.net/users/relaying.html

## Env

- `STRELAY_GLOBAL_RATE`: see https://docs.syncthing.net/users/strelaysrv.html#cmdoption-global-rate
- `STRELAY_SESSION_RATE`: see https://docs.syncthing.net/users/strelaysrv.html#cmdoption-per-session-rate
- `STRELAY_OWNER`: see https://docs.syncthing.net/users/strelaysrv.html#cmdoption-provided-by

## Ports

- Protocol port: 22067
- Status port: 22070

## Volumes

- `/strelay`: keys

## Example

```
docker run \
    --rm \
    --name=strelay \
    -e STRELAY_OWNER=me \
    -v strelay-keys:/strelay \
    --publish=22067:22067 \
    --publish=22070:22070 \
    registry.gitlab.com/hydrargyrum/docker-images/strelay:latest
```
