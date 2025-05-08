## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:81209fe390582304d7a9175a1ea8930493418330294b4729f06bf1cf5a25f150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull traefik@sha256:bf140cb718732927898798f5dd7541d0c42acafbb236e8f0ebf508409b64cb7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329417293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29c81a8a33a1df4e06163023129237b29046bd0e59d750dc7be4fc3e73d18cb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 05 May 2025 17:22:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 May 2025 17:23:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.0/traefik_v3.4.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 05 May 2025 17:24:02 GMT
EXPOSE 80
# Mon, 05 May 2025 17:24:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 05 May 2025 17:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc5aecfc807b8057929efc7933cbe06ab83f91e79f0edbde109f6f2014f1144`  
		Last Modified: Mon, 05 May 2025 17:24:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6261fdcdbf8184739efbbea2bd70162a77692dbfd0b79b26bcfc2b55e6f31`  
		Last Modified: Mon, 05 May 2025 17:24:15 GMT  
		Size: 55.8 MB (55829613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dd541af258ae6c952d6a5887deb6024ef26e324d934391f04bbd09bc25fa3e`  
		Last Modified: Mon, 05 May 2025 17:24:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384bdc2691b80f276b7b563a9e3be7ac8402fe629917ec65f1d5cc53e50201a2`  
		Last Modified: Mon, 05 May 2025 17:24:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80cf4d04142031481a5066785df7078fc72e39086ac4a5b4f87307baf135403`  
		Last Modified: Mon, 05 May 2025 17:24:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
