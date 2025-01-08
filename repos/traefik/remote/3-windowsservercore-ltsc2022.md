## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3c560849b33b2ad9a461131e5cfc495982ae97b4bb4be4b93565b7bfc46abde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:2856e000541e12c4ed955ed7aa4e7e17dad1098b9197f69ba4897f04787a6bbd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303648155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e2a5572d478c35b7b8e2b4c095a66db6da3504f0ceb62e3286cf9c424b5e3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 07 Jan 2025 22:27:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Jan 2025 22:27:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.1/traefik_v3.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 07 Jan 2025 22:27:47 GMT
EXPOSE 80
# Tue, 07 Jan 2025 22:27:48 GMT
ENTRYPOINT ["/traefik"]
# Tue, 07 Jan 2025 22:27:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97347a8f032dc608046258505897cd3cf8475203fd370ed37d88bc64fc5b379`  
		Last Modified: Tue, 07 Jan 2025 22:27:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071939c32284de0ad61c36b4f84656564567512c6d41aa963362dca00db4251`  
		Last Modified: Tue, 07 Jan 2025 22:27:59 GMT  
		Size: 49.8 MB (49769356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8333ec492bc5210204526b5621ed3c9dca00228e34798563b4a35dbdf1293b9`  
		Last Modified: Tue, 07 Jan 2025 22:27:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d098f00a5d771a0cc6d245ceae19171774febdead51859bf14d7e662c811af79`  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f929255c186fb724b2b03ae394043ab1e047cf7453cc27fd11de91b4fdd59`  
		Last Modified: Tue, 07 Jan 2025 22:27:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
