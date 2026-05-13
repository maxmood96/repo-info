## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b5f65378ca53705f0adaebf1bb35a4e01adafbd52ad265b318257af66e1e6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull traefik@sha256:8d82bff86a5dc4dde6f2077babc808ddc7faef4235bdad69b5db739c8b82e9cf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172572517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124c3972eeb239657dba2e330f363f8ad6fa6d909b4af1a1dc38c65692a7002`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:47:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 May 2026 23:47:42 GMT
EXPOSE 80
# Tue, 12 May 2026 23:47:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 May 2026 23:47:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2e44e55275db5068cf0d4475ab7d854551417c468de6c97ae46ab66ae1067`  
		Last Modified: Tue, 12 May 2026 23:39:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d026fbb71e35ea8646d0844327994b01f0b58bf75db5e3e95d3b3d62a58dab`  
		Last Modified: Tue, 12 May 2026 23:47:54 GMT  
		Size: 50.1 MB (50146653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046dd614d5184d9e11becf13973cf74fdea6205c01ad626b8efd9918aefac0cb`  
		Last Modified: Tue, 12 May 2026 23:47:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099177e7a4d1fab60ae398d6847176cf7da4896530024b5fd85338f5f98bfc3`  
		Last Modified: Tue, 12 May 2026 23:47:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dba34439795041720fa42a6f88182b7c6fa845141efdd9eaed684f05de29c0`  
		Last Modified: Tue, 12 May 2026 23:47:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
