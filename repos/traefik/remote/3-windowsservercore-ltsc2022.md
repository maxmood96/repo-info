## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
