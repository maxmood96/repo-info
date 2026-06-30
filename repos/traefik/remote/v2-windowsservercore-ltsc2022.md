## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:484d0a700e2103888012c5f923184513676cde7767266ea595f6c7a7cf1b56fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull traefik@sha256:ed6e261eea8907156a8cec771db664cd94461927f355ce5a0e2e29a3744ae302
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2182509031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e593b984262ae15e36c3348ae17e69aabf734e8f1a4a5417f3cba509955eaedc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 30 Jun 2026 20:44:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jun 2026 20:45:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.51/traefik_v2.11.51_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 30 Jun 2026 20:45:03 GMT
EXPOSE 80
# Tue, 30 Jun 2026 20:45:03 GMT
ENTRYPOINT ["/traefik"]
# Tue, 30 Jun 2026 20:45:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.51 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cea9fe23a1a650e35e2a78f8919d62bcc48747a6061160aedb4ab2db520a286`  
		Last Modified: Tue, 30 Jun 2026 20:45:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af831c018fd07b16da804a59867ca6ea94a3033d2d00af858f0f927544ed396`  
		Last Modified: Tue, 30 Jun 2026 20:45:24 GMT  
		Size: 50.4 MB (50378278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad521703ae59e9bc0cf449d8cacd8a093e995a4ea1c5e65bf47baad8194f175`  
		Last Modified: Tue, 30 Jun 2026 20:45:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5a130139cb002ff137e4a19e54b84a9a1577c4a95e35f67181e328de9be3cd`  
		Last Modified: Tue, 30 Jun 2026 20:45:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d030fa8595b290d808c66cbab893ef7de80a88399311f1b9467b5ed363117af9`  
		Last Modified: Tue, 30 Jun 2026 20:45:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
