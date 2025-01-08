## `traefik:munster-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:cf5028a197e361881e3d49ae47c3bb84628687f36a7b4f13c5b44117add4d40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:munster-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:e8c1118ee769b6d67d141db63a3776bbeb538cb2751f35632772f69f2e1b974c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303472651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8b1b1b30021bcff0806c07f31c858ef7ce73066286f761570c62bb6f8f82b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 15:26:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 15:27:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.4/traefik_v3.2.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 06 Jan 2025 15:27:45 GMT
EXPOSE 80
# Mon, 06 Jan 2025 15:27:46 GMT
ENTRYPOINT ["/traefik"]
# Mon, 06 Jan 2025 15:27:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e138cacf55f4d7e7921bf7066c4285d24e17bab504c7dca70b34ea85d8465608`  
		Last Modified: Mon, 06 Jan 2025 15:27:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873451c12cfee51bee6aeb8290ca73819bcf6c9da36aaf4500058490109ff9b5`  
		Last Modified: Mon, 06 Jan 2025 15:27:57 GMT  
		Size: 49.6 MB (49593879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d9dc136bc1c936f806e80c8fd038cd5b888155cccdc303829251e3975179a`  
		Last Modified: Mon, 06 Jan 2025 15:27:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fd4c6878c8a511f8c4c9f4d1e474dd6e0ee121b492a5b7d0779413b26218e`  
		Last Modified: Mon, 06 Jan 2025 15:27:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3d78e390cf55155f7742bca56527fd4ed730414be2810a49678b7fd3112f1`  
		Last Modified: Mon, 06 Jan 2025 15:27:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
