## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:1dd8789d7c487eb31dc2371bfba1fdb16e2ced7923bf9294241be5ec5a7879c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:96b3f85d40336bff5092581c55b041c299813fad47489c74dbc5664b8c7c9663
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329445718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3598d8c0bbcbc5b50155e8fc5090edcd58b0924e8a0abf98b4b8da2bb5cdec18`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:53:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:53:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.0/traefik_v3.4.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 May 2025 20:53:54 GMT
EXPOSE 80
# Wed, 14 May 2025 20:53:54 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 May 2025 20:53:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1c4f0e1accf550e8a1e634f553b65d565236311f3e1ab5ac30f6573b459c20`  
		Last Modified: Wed, 14 May 2025 20:53:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10642fae349afab8f6789bfa737cbad745326e9f52e57ebd18cf54797b6435d6`  
		Last Modified: Wed, 14 May 2025 20:54:06 GMT  
		Size: 55.8 MB (55812460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae64f6163ddb588e57ef9a416bec9751f2db6c10186ba3d7e306e87bfaa326`  
		Last Modified: Wed, 14 May 2025 20:53:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3844a5146362a690a4726e442e6aafd4b59b6cfa9867f50cfdf672aeb4a806e0`  
		Last Modified: Wed, 14 May 2025 20:53:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafeacba51742b885930089bf45447945212499d0a6410d9bfc4a6b9d307ad0`  
		Last Modified: Wed, 14 May 2025 20:53:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
