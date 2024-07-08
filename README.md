# Podman Quadlets for Paperless-ngx

Setup Paperless-ngx on a server using Podman Quadlets only, to run on Fedora
CoreOS for example.

Based on the
[official container images](https://docs.paperless-ngx.com/setup/#installation)
and the [Docker compose](https://github.com/paperless-ngx/paperless-ngx/tree/dev/docker/compose)
configs.

For the full documentation for Quadlet support in Podman, see
[podman-systemd.unit](https://docs.podman.io/en/latest/markdown/podman-systemd.unit.5.html).

## Notable changes

- Use [Valkey](https://valkey.io/) instead of Redis
- Use Caddy to setup HTTPS automatically using Let's Encrypt
- All container images run:
  - under a non root user by default
  - without any capabilities
  - with NoNewPrivileges set
  - with the filesystem set as read only
  - with auto update enabled

## License

[MIT][LICENSE] or [CC0](https://creativecommons.org/public-domain/cc0/).
