## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 27 May 2025 14:53:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 27 May 2025 14:53:57 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 27 May 2025 14:53:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 27 May 2025 14:53:48 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 27 May 2025 14:53:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
