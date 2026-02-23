## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
