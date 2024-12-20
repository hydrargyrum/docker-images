# gitolite

Imported from <https://github.com/jgiannuzzi/docker-gitolite> but with [up to date](https://endoflife.date/alpine) Alpine base image.

## Volumes

- `/etc/ssh/keys`: ssh keys for gitolite access
- `/var/lib/git`: git repositories

## Ports

- 22

## Example

```
docker run \
    --rm \
    -v gitolite-sshkeys:/etc/ssh/keys \
    -v gitolite-git:/var/lib/git \
    -p 22222:22 \
    registry.gitlab.com/hydrargyrum/docker-images/gitolite:latest
```
