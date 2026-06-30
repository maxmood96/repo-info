## `traefik:ramequin-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:e82c664c9cfd452a38631e6d9aba3a20679dc013b32303d3b88ce49df95947f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `traefik:ramequin-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull traefik@sha256:bcadf8f394a040d3cb7fe3da91c4d586f3a42d19df257a1b396e373fe81a750b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329860447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8570a73c576d2793b350e0950e31e3099a1a3e0b576ee76ac766e57db3e79b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 30 Jun 2026 20:41:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jun 2026 20:42:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.22/traefik_v3.6.22_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 30 Jun 2026 20:42:24 GMT
EXPOSE 80
# Tue, 30 Jun 2026 20:42:25 GMT
ENTRYPOINT ["/traefik"]
# Tue, 30 Jun 2026 20:42:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72265e600cee36cf36338fa1112590247f5d2eed6fbacd1b8998dd3e98a28b1`  
		Last Modified: Tue, 30 Jun 2026 20:42:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562d761db4ca8dd33dfabecdddb1e77219eed60e5a72ad6237abe226e8bb841c`  
		Last Modified: Tue, 30 Jun 2026 20:42:44 GMT  
		Size: 50.7 MB (50712235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b02bc7252ec0769b4dcf5fa976825f079f41f14f25e062bc3b1ea8eb2153712`  
		Last Modified: Tue, 30 Jun 2026 20:42:36 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f321f8f478c591881ba457322c61bbc68a3a43b11ceec4a24163f86c3cb2b`  
		Last Modified: Tue, 30 Jun 2026 20:42:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6353aeaea9a1d79fa6b104486786826debc62f1f96407fd4a795f6e444c31bf1`  
		Last Modified: Tue, 30 Jun 2026 20:42:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
