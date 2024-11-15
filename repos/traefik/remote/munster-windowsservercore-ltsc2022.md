## `traefik:munster-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:109a4db007c6eeb36de335e3e373aaef01e0dfe8768cb724bffe76d9e23e24c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:munster-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:16c3a60767ce7803e17779fb7b4901ecdbb0b1383dd0b00c8bef31d6b22fcc59
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2301142260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978a14a0e279ca813b274a151f3ec40ecf70772a5a0d37cd705e25dcb37d2f72`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:15:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:15:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 14 Nov 2024 20:15:43 GMT
EXPOSE 80
# Thu, 14 Nov 2024 20:15:43 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Nov 2024 20:15:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:02a4725190d6de8cb3f772f91f606584c9decf459034a6c5f02b82a5fde674f0`  
		Last Modified: Thu, 14 Nov 2024 20:15:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b83a6ab40a1d7bd006cda243cb3972414d4800a89ebf0154bb81f6c9b2a927`  
		Last Modified: Thu, 14 Nov 2024 20:15:53 GMT  
		Size: 48.7 MB (48652886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99cb3b9acdcf3f16fd4f2a74bc012c29586e117f0a8a6230657dea6d8953b26`  
		Last Modified: Thu, 14 Nov 2024 20:15:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4ca29718e9185a86cd367e8913e2b29f7ff86dbfdbb02af59c16558a0aea68`  
		Last Modified: Thu, 14 Nov 2024 20:15:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f181a4ce34af391d2a8c8489f436fd92bd585db8e4ab029f713a59024f77ad90`  
		Last Modified: Thu, 14 Nov 2024 20:15:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
