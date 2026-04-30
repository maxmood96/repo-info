## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3b4a34c15b0b4876b45e0caab15c6ebe4dd43c392ff7c24b662da92c5c81c91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:687439d7435d04e4b1e700b9be23b6e290689e9c0041b9f4de5ee7f87b819e55
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2120140420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dc9dba1c39658abc01fef6bfde2c86e85dbb08e4e16fd01edc2b41e0cd0c8d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Wed, 29 Apr 2026 22:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 23:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.44/traefik_v2.11.44_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Apr 2026 23:20:18 GMT
EXPOSE 80
# Wed, 29 Apr 2026 23:20:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Apr 2026 23:20:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.44 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:881adac9baa303e4738660f9fd178c83fa652492d7841586a9540b0b9e48a059`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7f3de33a85c75d8fa28ea6e8adb4ecb0bc62130dd3ba6c2d3f55582484078e`  
		Last Modified: Wed, 29 Apr 2026 23:20:30 GMT  
		Size: 49.9 MB (49923959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875d9d0ed7e0bbcf71e81e9253ab538e80fab890e83e211ce3899ba2aaf87dd1`  
		Last Modified: Wed, 29 Apr 2026 23:20:23 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cccf7f626786d522f2e7e8584d65caf884c0ece610e71f1aca886fe76ed642`  
		Last Modified: Wed, 29 Apr 2026 23:20:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947558eb59de314e5a6214f56cfbe1bb5362f3048db9126fe549d4f95f3f8e5a`  
		Last Modified: Wed, 29 Apr 2026 23:20:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
