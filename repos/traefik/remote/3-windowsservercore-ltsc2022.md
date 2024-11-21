## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6f0e5783e8e26959023bc0f86b42b490fe5b63a367a90659a5e2a155166df133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:bdeec8d8ac650ff774393581757a7fbd4bcdef555acd22b265c4641b3cf2256a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2301902940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2dd979ae888595b424bca135fc7bcdefd3a75a472c7968791cf4a7ab816104`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 20 Nov 2024 23:21:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Nov 2024 23:22:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.1/traefik_v3.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 20 Nov 2024 23:22:52 GMT
EXPOSE 80
# Wed, 20 Nov 2024 23:22:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 20 Nov 2024 23:22:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75ff190998de4bdbb91b8d3ac6bdafdb0ab6f31541fbd701e55e72db13d2be0`  
		Last Modified: Wed, 20 Nov 2024 23:22:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd898f11305e7f2ff947226ca40a12d23c07e7e1f5571d53ff7abce1a02b196`  
		Last Modified: Wed, 20 Nov 2024 23:23:02 GMT  
		Size: 49.4 MB (49413567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2fdb9aac3088c7f907858925f8e916651d10d0ac306b0b671bbcb207afa419`  
		Last Modified: Wed, 20 Nov 2024 23:22:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53269327e7dc7d9c201f3ee857eae026dad18e82ac58148cb6cec765aebfc101`  
		Last Modified: Wed, 20 Nov 2024 23:22:56 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a0369f6c497372a1207114074b3284c811b8b52560f36283a52fa7f92540a`  
		Last Modified: Wed, 20 Nov 2024 23:22:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
