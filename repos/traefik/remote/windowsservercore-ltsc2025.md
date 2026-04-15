## `traefik:windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:c65479f434909faa9fcee0cbbf682724082e0a70cf74b5074cad8aecb8716cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:248910ec3b9daaad79346e15ce0884d2fa18703fb2deb850e96df000be67d157
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179508310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0056ea3b6eeeabdbf918f47846cb02b8a1af26d942279246e3cf566bb5346f7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.13/traefik_v3.6.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Apr 2026 21:02:57 GMT
EXPOSE 80
# Tue, 14 Apr 2026 21:02:58 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Apr 2026 21:02:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.13 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6381b6627d94a0354f249ec783cecec3a2f7fe084a83b16b2871e14d271640d2`  
		Last Modified: Tue, 14 Apr 2026 21:03:06 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80530590e053d77268d599c8f879a868b5f3480a655cf2f203d6a6f42797f1d0`  
		Last Modified: Tue, 14 Apr 2026 21:03:16 GMT  
		Size: 49.5 MB (49517072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f045944645546c8a29e7aa11f8b46efe0a229d2383cb36911494b58411b182e`  
		Last Modified: Tue, 14 Apr 2026 21:03:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba2a1b737eb093f987381afbc3a105362fb23c03c979db51a29795c070005d0`  
		Last Modified: Tue, 14 Apr 2026 21:03:06 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79695401f3ff195d857ecb9f080824d5578a6b01afd0e390fde3f6008b160d07`  
		Last Modified: Tue, 14 Apr 2026 21:03:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
