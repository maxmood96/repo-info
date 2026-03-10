## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
