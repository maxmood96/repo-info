## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:df5d297fd3e44de7b2507935eb663208ba4e35ab90acd05ea0624d3a84a8fe13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:265f67ddcb51514970c3d8bdaa32d2ae491a4152f20c456aacb548c2543c1fec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303281727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5dc419689ba51e0e32d61d9af99aad87baa8407a08ef307d46fef5813d260`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.2/traefik_v3.2.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Dec 2024 20:39:06 GMT
EXPOSE 80
# Wed, 11 Dec 2024 20:39:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Dec 2024 20:39:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685fe9b2086ef55eda355bb197008c8461fff2173663f1bdf94b7128583bc04b`  
		Last Modified: Wed, 11 Dec 2024 20:39:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2642b912410c55ded2990f766d5e480d2d9e79c71f9a2fd87a66013d03da5fec`  
		Last Modified: Wed, 11 Dec 2024 20:39:16 GMT  
		Size: 49.4 MB (49402953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ce891a9178b68cf648d99d6a0e576ba1f2d4b2a543d3b57d7285d01f11912b`  
		Last Modified: Wed, 11 Dec 2024 20:39:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc56cd986a1af696cc554d149e540724772adc6ff812ff047da4d327b05e80f7`  
		Last Modified: Wed, 11 Dec 2024 20:39:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a1174cfc8f1f4911cac74c906eae87e833262cba95a1608a215c6c5fe33184`  
		Last Modified: Wed, 11 Dec 2024 20:39:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
