## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:c0d11ee1d10e1ef6a019dc29034faf452039f43cd1890880199e7585ad775fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:98ca079b978d6a18adfc776f5a47e7454e71a28cfb43cdaa398a2aa383ad2686
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303655703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d9b318d52114f9420bd1bb856e270b6d09b5c23ed64997b9d5bc5006846e44`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 19:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 19:27:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.2/traefik_v3.3.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jan 2025 19:27:59 GMT
EXPOSE 80
# Tue, 14 Jan 2025 19:27:59 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jan 2025 19:28:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a9f034f1de6d94c155a239a5862748f369109bc25d965fc5a0933000a4426`  
		Last Modified: Tue, 14 Jan 2025 19:28:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4db7b36ef409f4e326b5ed8a5b5fa213e83c27417178addf79e0a65d2cb13dc`  
		Last Modified: Tue, 14 Jan 2025 19:28:10 GMT  
		Size: 49.8 MB (49776943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9114375e91d6cd2071f705b2b6aa1f8b8d845658e38ee90591308eea273274aa`  
		Last Modified: Tue, 14 Jan 2025 19:28:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822b4b10bc191baf3cf53da5be3cde3ad7173dc9699cd1dc5aafccf8aa8dbed6`  
		Last Modified: Tue, 14 Jan 2025 19:28:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db69062fb6f5fbd99fd5eaf1c8dd2ae43954d568326efc749b65658296856376`  
		Last Modified: Tue, 14 Jan 2025 19:28:04 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
