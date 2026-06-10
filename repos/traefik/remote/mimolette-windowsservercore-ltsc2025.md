## `traefik:mimolette-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:925507367f22179b93a912c8c4d9b944e83ec86470003a433738a2ed5f27333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `traefik:mimolette-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull traefik@sha256:76d9a58defa17dd1c1936c0d49a46de764d98897ba0b9fc57befddddec1907f8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329208306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13f516362260dc24697ffdbab4d2c5185d98815ca1d892043facf5da46ea640`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:14:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.49/traefik_v2.11.49_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Jun 2026 22:14:17 GMT
EXPOSE 80
# Tue, 09 Jun 2026 22:14:18 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Jun 2026 22:14:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.49 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:0f5da0ca79e35ac4e85e4f31bcc8903c02e8ea435b81b7a831f2be05314fbdfd`  
		Last Modified: Tue, 09 Jun 2026 22:14:25 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93be08df00b9c6645a6ed2218fa777684d9c22538f6d341da3c0631c151ad8b7`  
		Last Modified: Tue, 09 Jun 2026 22:14:38 GMT  
		Size: 50.1 MB (50060121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aafb1ea7847939e559b71ff23a015a08d677081e88ac74fa823d3742d3ac562`  
		Last Modified: Tue, 09 Jun 2026 22:14:25 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e43276a5cdc0d6b7cedbb561f808d0209abf7e052219db5b9d1eb7103fd6212`  
		Last Modified: Tue, 09 Jun 2026 22:14:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42db8be4655652312e1d3b67e9861d704ed762ed7594702e24c38a8b538fdea6`  
		Last Modified: Tue, 09 Jun 2026 22:14:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
