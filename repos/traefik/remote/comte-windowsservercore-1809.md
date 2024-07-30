## `traefik:comte-windowsservercore-1809`

```console
$ docker pull traefik@sha256:3a966f9f1cba45dd52b58d39e4d4b5d36a3647c6fc4fe2ac7db223649d3c904e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `traefik:comte-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull traefik@sha256:b7999ce84025f7c81f863e9c71331a95dca05f2c99cd48e898a63987262fdc08
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2284449618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94077378dea9ef3d7f693798e0ce76781aba2f036a1f15ba787cc4f362dc2e47`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jul 2024 19:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.1/traefik_v3.1.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 30 Jul 2024 19:18:06 GMT
EXPOSE 80
# Tue, 30 Jul 2024 19:18:07 GMT
ENTRYPOINT ["/traefik"]
# Tue, 30 Jul 2024 19:18:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e1b977f1ec2790de6e1bcdd9b0272d3ab46f70fdbef2ae277b7f99b83d0b3`  
		Last Modified: Wed, 10 Jul 2024 17:26:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b7b26159db436891d1540db5643b1fe52d6fafcf5c11001b929411d4c7fb06`  
		Last Modified: Tue, 30 Jul 2024 19:22:36 GMT  
		Size: 46.0 MB (46014551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddf86da3ffcb3471d6af00c6afd063e5d5314a2e64f0316c9ed776564458f1`  
		Last Modified: Tue, 30 Jul 2024 19:22:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4305c394b5bc577b6bf3d01e88384107c344726dfd932fcf03239e2e7c3116`  
		Last Modified: Tue, 30 Jul 2024 19:22:27 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171071dae99f22ed9c1cfb45e5c394dba168b034e14ced66c8528cb9e3b70da`  
		Last Modified: Tue, 30 Jul 2024 19:22:27 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
