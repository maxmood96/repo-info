## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6a8dd62811acb9a6d08ec71df7cb68572d50536c410d369bc9e7f549c10f7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:fc0ad08b09d1869d343026da4245f0047dbd996d74bd7ec8b95fa5c087701987
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206775102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9746f13e341a01170acb968a35cf464b9c816adb02f1c29d52292f9b70ca40f0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 18:21:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 18:21:46 GMT
EXPOSE 80
# Wed, 10 Apr 2024 18:21:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 18:21:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52beb8f2e4b6f071a397fc0bf82e76b4d05e0ef96d461d364e19ae67b572a5b0`  
		Last Modified: Wed, 10 Apr 2024 18:24:01 GMT  
		Size: 42.3 MB (42341499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e749bcf5783f00072b0fed9cb8313de1e08f830f93e14641d10a9cb66d52409`  
		Last Modified: Wed, 10 Apr 2024 18:23:51 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aecb43c4b832031512a026c56830dc52e20eef0de50b9ad9a20e10718ac3256`  
		Last Modified: Wed, 10 Apr 2024 18:23:51 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cde461b4ac8adf63fc4b5f64b935e18bec88fb2ae8f2973521b921bb70c384`  
		Last Modified: Wed, 10 Apr 2024 18:23:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
