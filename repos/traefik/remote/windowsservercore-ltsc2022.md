## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
