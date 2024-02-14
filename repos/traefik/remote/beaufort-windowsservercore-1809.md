## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:da1c73fee7f37a11819d7670ca346e52932cc576c933fac351011d5764dc47dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull traefik@sha256:eb34084eeccaa84fa67116783e083434e9033008acc9fecbcbb9e21622876d85
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123325321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1273d20399d917cae34e978dd48ba6030fd466e44ded7adcc435145380ce315f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 22:42:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc1/traefik_v3.0.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 22:42:04 GMT
EXPOSE 80
# Wed, 14 Feb 2024 22:42:05 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 22:42:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bbf68049075c21ce6551836efc293b30492223fbd4522ccb55c84873b604dd`  
		Last Modified: Wed, 14 Feb 2024 22:45:34 GMT  
		Size: 42.9 MB (42871200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52580ce83815835febbaacc8c8c0c0450693ed08ce26e2e23dc8e2e21880a6f6`  
		Last Modified: Wed, 14 Feb 2024 22:45:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ea83d02963a04fe7518858bf2835c5db78246dac287166983cf7b4d52ea33`  
		Last Modified: Wed, 14 Feb 2024 22:45:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8754c95d4c635208cf43bb3d9166abb3e034eb4c2f25ecd5f06f7c207fc5a0`  
		Last Modified: Wed, 14 Feb 2024 22:45:25 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
