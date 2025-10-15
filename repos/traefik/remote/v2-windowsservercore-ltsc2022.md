## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:27a1bbf086489d00336f75516abab425145a8a479ae93202a1ee7358ee45ca19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull traefik@sha256:383adf02248b08702a3c52cec23f83667ec2e068c32274b25de4b6b04479d727
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1534898170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3713d2d72990779334c54f03ae609446815f34b0ea5a8aec30679ee02ed3ec6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:46:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Oct 2025 20:46:35 GMT
EXPOSE 80
# Tue, 14 Oct 2025 20:46:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Oct 2025 20:46:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10c5840f5ac53b165a8d97a8c18f54d6b441ff098b8e78dd29ffb6558d77165`  
		Last Modified: Tue, 14 Oct 2025 20:47:17 GMT  
		Size: 45.9 MB (45873831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cfe06237c3967c39e35983c57ed6103fea93f6220431eab3a321c480d52f76`  
		Last Modified: Tue, 14 Oct 2025 20:47:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da6f9e2a14a7f736645c81bc6863577686e2dbe79c637aaedaf4c83475d356c`  
		Last Modified: Tue, 14 Oct 2025 20:47:11 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3e295b719ed2bbc7d877dc07d80622efbcde4b6dec9b43280299d31d95f1c7`  
		Last Modified: Tue, 14 Oct 2025 20:47:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
