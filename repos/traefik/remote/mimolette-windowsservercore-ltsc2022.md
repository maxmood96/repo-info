## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7b0bd17d3b20b909962943ee74d1b36965cc550bfedf1acb2bb33c5a2939336a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull traefik@sha256:5d79619d1fc18cf49b6bdb5e08235fc89753af5607cdac55bbd2b6f11ca75924
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2182284499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb0041832e3420fbe9b05f030247d79797b31803259072143369751ed97d343`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:19:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.49/traefik_v2.11.49_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Jun 2026 22:19:59 GMT
EXPOSE 80
# Tue, 09 Jun 2026 22:20:00 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Jun 2026 22:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.49 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8be3d554496e22d6ab17418eea90ce40f29648137b4ace0b0c1a2303574c8`  
		Last Modified: Tue, 09 Jun 2026 22:11:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06a4be622e24a44945085d202d34400b75f725a7d2e989e2db54d66b4edd2a8`  
		Last Modified: Tue, 09 Jun 2026 22:20:14 GMT  
		Size: 50.2 MB (50153772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ec972f1d59cae5b3b79bcbbae195410a8b146b4d4d357d1df607067ebe7c28`  
		Last Modified: Tue, 09 Jun 2026 22:20:07 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451b50b28273fab666863e952ff170895042f9a9f939a157f697d444b4570450`  
		Last Modified: Tue, 09 Jun 2026 22:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfa85e1ff77b478af1f0abcfbf54bf68c84ff6d7649b6ae6e5547ef0adae94f`  
		Last Modified: Tue, 09 Jun 2026 22:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
