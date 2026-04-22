## `traefik:langres-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:f3b8893b69a355f7ff1ab83a78c7b2b32bf3051ee4dfabee17c90450d7c8c1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:langres-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:0e47fc1193dd15ae3acc0aa99966561e4b47a0f55c4898631c68755aefbd2321
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179572211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb630cabe3d6e3adcb7769606d792cdab45c683ac2a4467a1589fa76134ad12`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 22 Apr 2026 17:42:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Apr 2026 17:43:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Apr 2026 17:43:16 GMT
EXPOSE 80
# Wed, 22 Apr 2026 17:43:17 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Apr 2026 17:43:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:09948151efe1cb613efc38c3dedebed9f9b070d442af247ab6a52ff0cf58b617`  
		Last Modified: Wed, 22 Apr 2026 17:43:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a28e373955bb74976e2a7d001a9ad0dd4db86af6635e1e8eda9849888e037`  
		Last Modified: Wed, 22 Apr 2026 17:43:29 GMT  
		Size: 49.6 MB (49580968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433abbd9d2e9b7b7a06e018027f53bb0024f6b013f588607f3b1293b7c16d824`  
		Last Modified: Wed, 22 Apr 2026 17:43:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5765d659b7cbb22dd0881011f1d19df7cf22f0824e4e71959e108a0b010974e2`  
		Last Modified: Wed, 22 Apr 2026 17:43:22 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe4cf2afe003153c543f2f3a6c64052ed2353340f8ae8312f2054a19e2660af`  
		Last Modified: Wed, 22 Apr 2026 17:43:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
