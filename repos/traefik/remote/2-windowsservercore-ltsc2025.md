## `traefik:2-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:9e8eb5098f2d2751fbca0258ebf2538c54a6624487942728c4d22ef205ffeebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `traefik:2-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull traefik@sha256:fb048a5aeb96f9536278893c635d7104372aee25dd5f2aca11c826e7b5147a86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2255961192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3315150be0c829d4e0d454036a06780eefda1170a7efa3a09f84ebc61453ab3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:39:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 May 2026 23:39:49 GMT
EXPOSE 80
# Tue, 12 May 2026 23:39:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 May 2026 23:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4498f1426c9298e6d204f6b74e5060c8b3bfb19e1328586b50b0bc0e9976829`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11649ab3697ca0abece8752a18c81c6f3987f1df8dff26ef42a94ee79c7cd6e`  
		Last Modified: Tue, 12 May 2026 23:40:02 GMT  
		Size: 50.0 MB (50014031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876afc80abd3821b184ace312aa1d51d74f587ad7d74a91a9147b4378d4c3ed7`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d0125be8d0aba85037fc6f9f84b9ddddbc842d1a8889773ab96a3bbf68179`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafb1539f6faa8980fe286f06cd550114650295b50dd14c2aff7822e956c5e0f`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
