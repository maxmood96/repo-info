## `traefik:ramequin-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:8ea80f759329fbd76194355c834da32fe696ee8c425c0b9a8d493edf9d4aabee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `traefik:ramequin-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull traefik@sha256:d70e152d145b8aeeef90d2dcb69f99a47b1e0b38290107bf4b9b6dad1d26a2f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2255864379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a1883517888fa1fca49e5ed460d3db92ccd2f461cb5c51372ce08a703b514d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.17/traefik_v3.6.17_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 May 2026 23:39:55 GMT
EXPOSE 80
# Tue, 12 May 2026 23:39:55 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 May 2026 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.17 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:73dab9e350fc730aed7db6c5533fb3137169005dbb3d03e7ec95809aba0cb46c`  
		Last Modified: Tue, 12 May 2026 23:40:03 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb900177ff152cdd061e255a702ee171b47c6a68e71be596acba5a859b3fcd83`  
		Last Modified: Tue, 12 May 2026 23:40:11 GMT  
		Size: 49.9 MB (49917169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9eb4467b0156414502aa836e476bf35f66897c311bef260d75ff06e3ef2dfe`  
		Last Modified: Tue, 12 May 2026 23:40:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e988d666be8c878cf09acfb20b7442cf4cc9b8f6c418705cca33700416620ebb`  
		Last Modified: Tue, 12 May 2026 23:40:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80d8053f346e24c4d398538bf905484e8109118603abb8ed35ab962d165f328`  
		Last Modified: Tue, 12 May 2026 23:40:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
