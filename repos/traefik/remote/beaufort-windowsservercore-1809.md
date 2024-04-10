## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d53161e4866ab11c032ece229059098add56f3e974c98fd5b2fd6425fe2b4d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:0bd3554e9bb2357ed6a5ca7162ae92ba0c332c8fe52c898d332566207bab1c48
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207341911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd17647bb0a044bc0c9259b00aa6968f5b778de0c0b76e6d802d4f631a4d8c6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 18:18:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc4/traefik_v3.0.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 18:18:56 GMT
EXPOSE 80
# Wed, 10 Apr 2024 18:18:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 18:18:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0815eb841bd00e8a83a7b6b0eb3ad8962c90ae4ce340b47991e3693a581e1ca`  
		Last Modified: Wed, 10 Apr 2024 18:23:06 GMT  
		Size: 42.9 MB (42908671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f8989204c597f85ad13782bc30ab8404ff55477442bf0e66cc2813e2b9990c`  
		Last Modified: Wed, 10 Apr 2024 18:22:56 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c0886d63af681abb1513d239eef7cd0da2d5b151ff5941eaba015deec4698`  
		Last Modified: Wed, 10 Apr 2024 18:22:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a71f52525a7fafdd39a7f54ebb64840765855aedc3cb3fc4b21fb1b5d44ba5`  
		Last Modified: Wed, 10 Apr 2024 18:22:56 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
