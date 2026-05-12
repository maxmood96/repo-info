## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6dab4c5e68d071a8cfde200d2d9b9ff21ed60f6043d52687f246360b1144caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:9613246bd881091dac65fb51cd7fe543342eb4f6ae2ce7ffe9121974acc51db8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2120366108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1525992eb3cba5ae99bb3af12733ba4fd3d7f888fe5768ebf7675867271590bf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 11 May 2026 21:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 May 2026 22:02:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 May 2026 22:02:44 GMT
EXPOSE 80
# Mon, 11 May 2026 22:02:45 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 May 2026 22:02:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:59bce1e29b114db5563fcd892d2c84957519a6bbaa25acd04961c7db9af87fd3`  
		Last Modified: Mon, 11 May 2026 21:47:39 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a2f2f3a344cdb7077e4e62a03d3ffdd39671bd206568aab00be8706d5bff1`  
		Last Modified: Mon, 11 May 2026 22:02:57 GMT  
		Size: 50.1 MB (50149598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64e6b95688023abbd2751991c94774b41dbaf9af319cf3504aa7611f3d06717`  
		Last Modified: Mon, 11 May 2026 22:02:49 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bb2229c1cd7cba62c848670efbf682ee6bd3780352fb33f458bb908d793d3b`  
		Last Modified: Mon, 11 May 2026 22:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa722ff4e9846f154f3f9036152beff8df2d9a67b6988395bd9ce3c604156eb7`  
		Last Modified: Mon, 11 May 2026 22:02:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
