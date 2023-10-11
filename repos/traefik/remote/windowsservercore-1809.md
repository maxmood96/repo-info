## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:e48ea53ba59577bef28d3ceb8dd82d512802fc92bba0ea8730217ca65bb7a400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull traefik@sha256:6ddb17d74fd90ba6dd250de9179642d6b9578d6d56be82327b31f0817eb5f195
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2072188607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781a8b280451eba384580300e40e1a90f21b2bce4bebedde69d5c87b66476b17`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 17:53:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.5/traefik_v2.10.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Oct 2023 17:53:26 GMT
EXPOSE 80
# Wed, 11 Oct 2023 17:53:27 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Oct 2023 17:53:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f15241f4df03f5eed76e4442d2b3f7a498d9144f1297714e03b04a513bddc8c`  
		Last Modified: Wed, 11 Oct 2023 17:53:58 GMT  
		Size: 40.6 MB (40592559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40acdeea4d8136d5f835b8e319e6a7d4bc818c64267537a59a2076fb38cd0a8`  
		Last Modified: Wed, 11 Oct 2023 17:53:49 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289c14de3f4bf9beef5623344f1de08243e9ed0e48c8293aad5c67e937f006b1`  
		Last Modified: Wed, 11 Oct 2023 17:53:49 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a066414845489fe46ce720ac765d0b3b8ad3727c9c622c21223676eed2a8906`  
		Last Modified: Wed, 11 Oct 2023 17:53:49 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
