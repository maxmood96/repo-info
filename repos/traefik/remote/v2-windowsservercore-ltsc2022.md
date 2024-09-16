## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:68e4d728e9b217e24e5dc7c8b2912426f2300795853915f0a5f06c1f168788c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:d3d04749ce18696d0b6b689be6f0f4fcf57c3118c12330a7368d4e263a05984a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1506617381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f412f805df1ab86e3dd8df09d7914c2ccbccfc09519a98e2e3e5f1db624e6e0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Mon, 16 Sep 2024 18:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 18:58:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.9/traefik_v2.11.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Sep 2024 18:58:51 GMT
EXPOSE 80
# Mon, 16 Sep 2024 18:58:52 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Sep 2024 18:58:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4744f040026f9b6a0ac190555e6ac2c076dfbe57c65bef3675bd7e01175e16ab`  
		Last Modified: Mon, 16 Sep 2024 18:58:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d9f7e8915b78111d5ff1eb1a5744276d0e7bbf86f19bbc857937b9a93c1b60`  
		Last Modified: Mon, 16 Sep 2024 18:59:01 GMT  
		Size: 44.4 MB (44419844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f90656f199236c12336390b736018d38f390bc235bf4e6101fe17ffcbf9454a`  
		Last Modified: Mon, 16 Sep 2024 18:58:56 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea027321c937eb1c5db8e280c2b1645f9491202faa48a4ff336de480bd4aeb1`  
		Last Modified: Mon, 16 Sep 2024 18:58:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7e846c0ce229511793f4dfe1227b6554c27469b614c50cf7aa1cd5ae812866`  
		Last Modified: Mon, 16 Sep 2024 18:58:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
