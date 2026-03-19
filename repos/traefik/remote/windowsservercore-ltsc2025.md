## `traefik:windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:13ebe023e283f4ca3536cc1a6e57506a23e972e96e0f326d26a4ffbefd2e4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `traefik:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull traefik@sha256:58893d470883c7431bfaa7c224e9a0a5820e96f9f3bc9faab1abbf5814d7bcc9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130683396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfd36069c02831d5e70fcf91f5138d585c44c41edac2642aa47d201bec2cda3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Thu, 19 Mar 2026 19:12:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2026 19:13:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2026 19:13:19 GMT
EXPOSE 80
# Thu, 19 Mar 2026 19:13:20 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2026 19:13:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c91ff25be764a7787bd32943fd90e96f3b5532f73159d65f78ebdf46c05b33`  
		Last Modified: Thu, 19 Mar 2026 19:13:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f29621a876538ba2d5c1b6d08934ea73ee62e5979f30926c5179d3fa5407d`  
		Last Modified: Thu, 19 Mar 2026 19:13:34 GMT  
		Size: 49.5 MB (49482123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b057f6d245710dfd5c864e3b2c1c215398da96ec6a657ce41a6712815b084391`  
		Last Modified: Thu, 19 Mar 2026 19:13:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a515d8fddae1bbaa003699ce68047c309b3c1e67c1747b550f924a3498bb5a6e`  
		Last Modified: Thu, 19 Mar 2026 19:13:26 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3b69d75d2edc87472bf23673dad74cb4404c09c9267c6f519f1c938910635`  
		Last Modified: Thu, 19 Mar 2026 19:13:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
