## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
