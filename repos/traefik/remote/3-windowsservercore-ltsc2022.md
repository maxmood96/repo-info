## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9cd5ba31b5d7d6afbc702968b420f89eaaf00d45088134a08ece62fd4680d0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull traefik@sha256:cf075e8cd72185465fcbdcccade36db8c21b69416b5840de43b974e3432b93eb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1535761311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d519c4202c8d5733624ab3b37fbc3841fe26d5d2faedc266b21caf1e563358ec`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:40:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:46:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Oct 2025 20:46:30 GMT
EXPOSE 80
# Tue, 14 Oct 2025 20:46:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Oct 2025 20:46:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fbaa2338b5f21199cd9a50079b2aa9af297c6a713f9ac529a66776518157d9`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae8d4eabb67458e457685840c3747e332a9581599e7cb1b86f768466f71889`  
		Last Modified: Tue, 14 Oct 2025 21:12:04 GMT  
		Size: 46.7 MB (46736968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74b67313050ee1e9cd1df819a679fa03d1aa1d782291f95a2c90d04adfe168`  
		Last Modified: Tue, 14 Oct 2025 21:12:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e2e1dcc355dcecb69756f7fba350d47f5030778b22381c46b75c0570b51346`  
		Last Modified: Tue, 14 Oct 2025 21:12:03 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa581b891479f869d8f41e1e095f879c55002e3867e1234a050067bfc3b8cc6`  
		Last Modified: Tue, 14 Oct 2025 21:12:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
