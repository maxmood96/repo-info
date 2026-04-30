## `traefik:windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:85514a34fc6fe79fc89898f00435b4728466e932ce86d377743dd4c1bc16b8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:2a5e046904f5844081556f6b67ee354b9c673bf88d1e18724e6eb768b55c62cc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179830494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fded3313749a5ea9eba4e7e6366b08d1658d02f2eab6cb73812be12ad18dde03`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 29 Apr 2026 23:18:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 23:20:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.15/traefik_v3.6.15_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Apr 2026 23:20:15 GMT
EXPOSE 80
# Wed, 29 Apr 2026 23:20:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Apr 2026 23:20:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.15 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562d928de810bf1009ba0e114e47d9d09174ba37d51627ac810e43398c105eed`  
		Last Modified: Wed, 29 Apr 2026 23:20:30 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a529f85b87ebdf23a86c356dd204f772453c511f5080a6a75f2603afdbceca2`  
		Last Modified: Wed, 29 Apr 2026 23:20:38 GMT  
		Size: 49.8 MB (49839235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40ab465f9ddd5b35c02715c46d31f3c39a469932a8ba7b3ac21bda21220dce1`  
		Last Modified: Wed, 29 Apr 2026 23:20:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622a3e48ba31d1bc6f7845d511b4e31481c073f38a01301d56e69962bbfe5134`  
		Last Modified: Wed, 29 Apr 2026 23:20:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1c9aad070bfcc28c5bf536852da6b51bcc0e9cf6d6b38348ed352aa330419f`  
		Last Modified: Wed, 29 Apr 2026 23:20:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
