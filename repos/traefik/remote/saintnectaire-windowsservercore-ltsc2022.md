## `traefik:saintnectaire-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:ae6ab256683acb57c1c35e5a8965ec4bd883ad47fe75b0656bbc453ca4d99b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:saintnectaire-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:239b4490bd30e2e910fd5b27daf08dfd35f46e121f30b881c68eec7e8dd8b9ea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303656697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1063ce4e3e14afd9bfa9d27704f8cc461b2b5bfa4b4ac391b42b69f983a708cb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 15:26:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 15:28:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 06 Jan 2025 15:28:17 GMT
EXPOSE 80
# Mon, 06 Jan 2025 15:28:18 GMT
ENTRYPOINT ["/traefik"]
# Mon, 06 Jan 2025 15:28:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a7a27d65978b8e7d33f522fc143d49a0b4a08fb776592ae16d2cf5076c117239`  
		Last Modified: Mon, 06 Jan 2025 15:28:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacc4346d17e8f746d28f00991fb80205cdee48d6ec345a0608c5b139f3513c1`  
		Last Modified: Mon, 06 Jan 2025 15:28:28 GMT  
		Size: 49.8 MB (49777923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d102f1d1acdb76ecc4d190639bb1fe0b99812da077a12e280ff661d0f5101646`  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ee31500e1db58a0912768f555787e6f045bfb5a5830b5d2ceb222cd47c32b`  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8f880e1b2a0ef40954b445a2c732a9f53bd6966b9bcfb23396527f455d81ec`  
		Last Modified: Mon, 06 Jan 2025 15:28:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
