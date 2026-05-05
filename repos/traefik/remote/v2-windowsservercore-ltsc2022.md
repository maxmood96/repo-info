## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:218ec7985a335f7442432826960857f3f7f5768173078ace7ee75c96d0589471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:e1bf31cae2fda28a9e656c639380ae1a06ddd20a70f631c36659885d7af525c7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2120302885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03dbfb7a954ae6318d717bc18aff795756cd38d924f8ae3d9015e1ce897c38c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 05 May 2026 19:13:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 19:30:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 05 May 2026 19:30:02 GMT
EXPOSE 80
# Tue, 05 May 2026 19:30:03 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 May 2026 19:30:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db82a2d531a598d9a508a8aa7112fb7d6b2fd2763cee34f01e502d4df7ae5440`  
		Last Modified: Tue, 05 May 2026 19:15:03 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c67866e5af7989ab850f817a88b2448de641a8a99c38007b12a8c239e10d5`  
		Last Modified: Tue, 05 May 2026 19:30:14 GMT  
		Size: 50.1 MB (50086402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cd562353a13be86cfa301734678692d1bf68d24ba3cbf67db9b117303e6881`  
		Last Modified: Tue, 05 May 2026 19:30:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9a3b812068ba887cb7586b5a4673b4b547431be9c06b474c1008518a4f6768`  
		Last Modified: Tue, 05 May 2026 19:30:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c37b778eb56086b04168589de222fc3a42c513e56405c36e28b0654fe5b380`  
		Last Modified: Tue, 05 May 2026 19:30:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
