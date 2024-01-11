## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:53a60637c1c1b7718cb2b22bbbb3b94bee811564f7d88bffdad67bc72d08fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull traefik@sha256:2e248ba9e658c4794d540927f750878dfc3bb8b100dfa7b8c3d8367994b17bc5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1941142321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e0f1a3a4cde740e20c131b19a2b00701ec8daddceed934e883bcebb2c10a76`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:57:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0-rc1/traefik_v2.11.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Jan 2024 02:57:35 GMT
EXPOSE 80
# Thu, 11 Jan 2024 02:57:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Jan 2024 02:57:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9a96a6376415b2707898cdc296fc6f3ee7d8156e8739b1f9c25d0b6d6af286`  
		Last Modified: Thu, 11 Jan 2024 03:02:52 GMT  
		Size: 40.9 MB (40924205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b1e05bba14697f719803f20a9789b420f49a9eb9b52ee9d396941653eb2272`  
		Last Modified: Thu, 11 Jan 2024 03:02:40 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c3e007a71f79fdad0e408d500124c5d8015b1f988d9105a8a727f1dc65ba9`  
		Last Modified: Thu, 11 Jan 2024 03:02:40 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e3d74cbcb1daa1ef4acea987e656c09099eb6d136495bd9ff33c7671d83f00`  
		Last Modified: Thu, 11 Jan 2024 03:02:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
