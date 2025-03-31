## `traefik:chaource-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:a32c1e9e611b68904fac15b6e444bfe6f24c10d8dd6ca18b6cb3fdbd6c9acc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `traefik:chaource-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull traefik@sha256:3888e05f43439f0852fe1934f95109c976e966dd3aa0a99ee3948585733089b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325095877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4528b8c7b58790dc163335bbf636520a45bf4bf9c3f58e07da7a7ae0ca8cb560`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 31 Mar 2025 17:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 31 Mar 2025 17:29:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.0-rc1/traefik_v3.4.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 31 Mar 2025 17:29:46 GMT
EXPOSE 80
# Mon, 31 Mar 2025 17:29:47 GMT
ENTRYPOINT ["/traefik"]
# Mon, 31 Mar 2025 17:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa02827d3e91837731186e9349c2051bbb63aede10ab36a77eb00755cefc89`  
		Last Modified: Mon, 31 Mar 2025 17:29:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501927297adfed9d797a18f5bde477f1358dd6791a3190d9ef44b72572168497`  
		Last Modified: Mon, 31 Mar 2025 17:29:59 GMT  
		Size: 55.1 MB (55149583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c065aa52fb4d9b7ba0fc342e3edbaf17308aede8d5b7fd27097c0c70037063d`  
		Last Modified: Mon, 31 Mar 2025 17:29:51 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d3280fab3511a2f2c00228531a5f8bbfeadde566032facb85150a284b9afb3`  
		Last Modified: Mon, 31 Mar 2025 17:29:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1da536e609b51c2e58f5c52015165c351a7aa0f97417a78a3694a374bc048f8`  
		Last Modified: Mon, 31 Mar 2025 17:29:51 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
