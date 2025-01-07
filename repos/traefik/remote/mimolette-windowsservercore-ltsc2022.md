## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:ffa58f58ea774f06012252b5155900be9e64ef9314585b6b7dc918695f8b6037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:6999f684a2aebfeb0e0c6698c1a3b17fe144ffe2e098345a7ec015bbe63f1ca7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2300775519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aedbd76a99f7af59fcf708efd2f1327c61901b966c0632ea92e9485defd96d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 06 Jan 2025 15:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 15:28:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.17/traefik_v2.11.17_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 06 Jan 2025 15:28:09 GMT
EXPOSE 80
# Mon, 06 Jan 2025 15:28:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 06 Jan 2025 15:28:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.17 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0eb475c7b4f2daa5a477b09b1468523902fb7a04bd806c0f0c289bb6ad251d2`  
		Last Modified: Mon, 06 Jan 2025 15:28:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5cceaba04e74f4e32a978b903257721ede06ecd6db0767d5c01640aa5739f2`  
		Size: 46.9 MB (46896738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d27978ba4bc94adf7feaffcc88d0f356ba81cbc5ed4bc31897d40884370eeb`  
		Last Modified: Mon, 06 Jan 2025 15:28:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e070b6c78d48136b406334e4e02c98c406d95cddf7a80363f140e9d720abd3c`  
		Last Modified: Mon, 06 Jan 2025 15:28:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dbfd3e60bd9764cd4dbbef55984c14f3fba26b9c650c063f7145b2846cf282`  
		Last Modified: Mon, 06 Jan 2025 15:28:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
