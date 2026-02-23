## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
