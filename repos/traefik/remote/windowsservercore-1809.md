## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:0b0a610e536ac61689df170e6e71da555338f3eead188e5adbcd30cfcb3088b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull traefik@sha256:d030f6bfbe50cab183344e0da8f9467590a3a236600e550a2120c56672688f99
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122695518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e5d0086a7d7255835185fb8f2547d54753730e84ac5b77e434f880eaea7802`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 22:44:20 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Feb 2024 22:44:21 GMT
EXPOSE 80
# Wed, 14 Feb 2024 22:44:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Feb 2024 22:44:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5dc2c4d4ded9903c14c59a09986b84eaf65706d973ce36622ad710244feebd15`  
		Last Modified: Wed, 14 Feb 2024 22:46:24 GMT  
		Size: 42.2 MB (42241398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d258da5300854c4ef321cae83a94d013bccb8d6c9fcb59ad6030b6cb68065b2`  
		Last Modified: Wed, 14 Feb 2024 22:46:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc391b65d1fc55a98c51f741207be28a31c5a0ed72b5428c8bf07b1061662ca`  
		Last Modified: Wed, 14 Feb 2024 22:46:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0ba9cec0564645d60f00f7ba1850e58d08d1ffce53d8b2633bd3c18f60aa94`  
		Last Modified: Wed, 14 Feb 2024 22:46:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
