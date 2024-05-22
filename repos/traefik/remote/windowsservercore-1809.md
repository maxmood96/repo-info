## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:061ec54542154d9b3f7a3536a51bded22d3be875e6509088719ad855aa779d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull traefik@sha256:933adda121b8cce0f3625e2f4043489fc1a8f001f9a6d5f85000b0154c405e6c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2222799114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f243895030efff25c9dc47dd22a6628d40032f9a5af966649f818e270981a142`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 19:38:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 18:19:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.1/traefik_v3.0.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 May 2024 18:19:45 GMT
EXPOSE 80
# Wed, 22 May 2024 18:19:46 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 May 2024 18:19:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:416f48199344f03d6754410434c5ec27819f03b68a093259a449abf96cdfaff8`  
		Last Modified: Wed, 22 May 2024 18:21:36 GMT  
		Size: 43.1 MB (43082035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b442a1f7b8af9119996bcd7ac1784b7ebcb176ce51ee52ee1d4b5185ef74e4ad`  
		Last Modified: Wed, 22 May 2024 18:21:27 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728d734c20c96b60ab688972eced7a90e3ba915093e9e7e802d9761e6a03dc2b`  
		Last Modified: Wed, 22 May 2024 18:21:27 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc9f0299e304227247e338457939c4633ef89862aed77ddd80d29f8c6a706c`  
		Last Modified: Wed, 22 May 2024 18:21:27 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
