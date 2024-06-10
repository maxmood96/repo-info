## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cc0c7b7fdaa584d53394bdf01a18252dfc631ea2776c3386b618176107370a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull traefik@sha256:f499ac45a735be8cf031370e2252a84b7a226052970e2fad998c4f9c8f34efdf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224074670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e716928fdb424786e4f42c3c5fdfa7ee14baa368976f91359540e573a1eec0f4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 19:38:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Jun 2024 22:15:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.4/traefik_v2.11.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 10 Jun 2024 22:15:36 GMT
EXPOSE 80
# Mon, 10 Jun 2024 22:15:37 GMT
ENTRYPOINT ["/traefik"]
# Mon, 10 Jun 2024 22:15:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a2aa6d68dd7a7e7745c65cd54a1e2713d737d3f4fdd07e5e1c2fce38b5d24`  
		Last Modified: Wed, 15 May 2024 20:44:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8b4b853398cc8b67296faa7c1ecec228b3423372873d2a123c66fe5a6ee6af`  
		Last Modified: Mon, 10 Jun 2024 22:18:32 GMT  
		Size: 44.4 MB (44357933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a575f2440c28a6e36eb746d3b589272cf27380d2696c988e29a342b92ee5f69`  
		Last Modified: Mon, 10 Jun 2024 22:18:22 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af4b1ad63a0ddaf8111d864eff6642bb59b6c89fb3d9e1ec951ac6296b6f42d`  
		Last Modified: Mon, 10 Jun 2024 22:18:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20aed781d1b983f781bf59a9c59eb94db3709118761b88d510f782849dbdb2b`  
		Last Modified: Mon, 10 Jun 2024 22:18:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
