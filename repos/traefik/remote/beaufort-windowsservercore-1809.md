## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:0c7d6ff039135cc176f9e0830375aeaff5a42c837e169cf0415bc0efa2261e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull traefik@sha256:fa4a6677b0221d984fb164870d59b2c638e21344dee3a5e2e0213b89865eca48
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123286315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dbe728abf001b6eaf2b1a15f74b8d6bff7247e6593d36114861d9b0d92f207`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Mar 2024 17:17:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc2/traefik_v3.0.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Mar 2024 17:17:50 GMT
EXPOSE 80
# Tue, 12 Mar 2024 17:17:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Mar 2024 17:17:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:69f171c1363d8b45186afdcd3d579278910a8857253b3c2f949911a637b973fb`  
		Last Modified: Tue, 12 Mar 2024 17:19:12 GMT  
		Size: 42.8 MB (42832200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d887cf0d3507c6728ef64fb3cebd6638cf2e80cbe4f0daf700d3ff7fa4c10e2`  
		Last Modified: Tue, 12 Mar 2024 17:19:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62199ac041ff293ab0d2e40dd1ab22777b0af362e9cc60bb67568fcec78dffce`  
		Last Modified: Tue, 12 Mar 2024 17:19:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f9a8f9456166b3bbf111eb687351026c33fbf2a27890565acad317adac98f8`  
		Last Modified: Tue, 12 Mar 2024 17:19:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
