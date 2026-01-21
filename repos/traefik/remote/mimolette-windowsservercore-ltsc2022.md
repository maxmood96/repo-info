## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:15:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:15:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
