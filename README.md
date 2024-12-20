# docker-images

Just building container images using continuous integration.

Images:

- [folding@home](https://gitlab.com/hydrargyrum/docker-images/container_registry/6710817): `registry.gitlab.com/hydrargyrum/docker-images/foldingathome`
- [gitolite](https://gitlab.com/hydrargyrum/docker-images/container_registry/6700716): `registry.gitlab.com/hydrargyrum/docker-images/gitolite`
- [syncthing relay](https://gitlab.com/hydrargyrum/docker-images/container_registry/6700854): `registry.gitlab.com/hydrargyrum/docker-images/strelay`

No images are uploaded manually, only from CI based on this repository's sources.

## Tags

Each image is rebuilt on each commit and also rebuilt every month (cron-like), using a recent base image tag (to have the security fixes).

- `latest` on each rebuid
- `<YYYY-mm-dd>T<HH-MM-SS>Z` date of the rebuild
- `<commit hash>` on each rebuild
