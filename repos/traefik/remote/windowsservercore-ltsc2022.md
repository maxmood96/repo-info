## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:5b5a5159625d4efefe139d62f6de0586a8951645bd1a495ee0315bd8e14ecf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull traefik@sha256:d619e73e0da67e676b734d9c7c24bc25b32c5a659b4f57db1069024a37fd6b7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319736296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5a07ad5aaedc228be9c8a0e842b18386b4ed65988558c1f78d47c604601133`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:59:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:59:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.4/traefik_v3.3.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 12 Mar 2025 18:59:28 GMT
EXPOSE 80
# Wed, 12 Mar 2025 18:59:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Mar 2025 18:59:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bed800fc8c9f528bc55135163d4850c84696578d9763374fcd7fdacb405a258`  
		Last Modified: Wed, 12 Mar 2025 18:59:32 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d9032742521f5b90c6f5377274a9badd375fbac1a6c34b39c80f0733789c7`  
		Last Modified: Wed, 12 Mar 2025 18:59:38 GMT  
		Size: 49.8 MB (49789948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7faeb8df64c4ed3b8e22bcddbd7f0b2ba7dc637ef25e49277af6b743819bab7`  
		Last Modified: Wed, 12 Mar 2025 18:59:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f91794960931540cb3a0fd0e885d1cc7df2a09064ffe797d16030b837e7d437`  
		Last Modified: Wed, 12 Mar 2025 18:59:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28f835fc5884f34e19bf813d8392d489d732de037c9c345dc28e9eb17903eab`  
		Last Modified: Wed, 12 Mar 2025 18:59:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
