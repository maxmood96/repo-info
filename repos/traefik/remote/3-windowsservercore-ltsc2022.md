## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:58d1e87db2fe0450ae3868325944fce791ee62d03fe7654d7a0fa539d679cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:6141b79c11f1676e157e1ba4fb54e219f2eb2544d21c1b606cb726239ce4c1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2120122206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b54f4905ab1ac794a71b24692b45700b84eecebd462b3cd58164b88b0e3aa9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Wed, 22 Apr 2026 17:50:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Apr 2026 18:07:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Apr 2026 18:07:34 GMT
EXPOSE 80
# Wed, 22 Apr 2026 18:07:34 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Apr 2026 18:07:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e0933917d0d20c53809f0ba325797897336435fa87c6b609e86b09cb1d8e8`  
		Last Modified: Wed, 22 Apr 2026 17:51:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25ef34113ae7238e57483f077f7f2a317b7b47fe7b443282572beae13cb3640`  
		Last Modified: Wed, 22 Apr 2026 18:07:46 GMT  
		Size: 49.9 MB (49905719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a589e4255ec7027b1ed32a383fc21361771286d7bc8c429d1e20b201cb3ca7fe`  
		Last Modified: Wed, 22 Apr 2026 18:07:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df46076a794ccb2ba86c6cd03eeb22503eb1e71cd1c299f7d23326fe9afad7da`  
		Last Modified: Wed, 22 Apr 2026 18:07:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45502dbe2cd802dfa30995e045adeaaaad957f78036d6a1550e87129835f0e98`  
		Last Modified: Wed, 22 Apr 2026 18:07:39 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
