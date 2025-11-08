## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:937c3780cfe52f24b2f79a8a96d5c81457aa629399e259c4c1c275c3e1855ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:d7176df6bc8e00a4fe0befeaedb893737a14c7ec5865ae03a360dc64e93be7f4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1626244321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a125b36abc9d91e864056a5832b51c8d81192c78b3e900a801ac346a00159c0d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Sat, 08 Nov 2025 17:50:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Nov 2025 17:52:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Sat, 08 Nov 2025 17:52:01 GMT
EXPOSE 80
# Sat, 08 Nov 2025 17:52:02 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Nov 2025 17:52:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e9059525ffdb388ecb5e55bce62b363c192756a62a419a4006c0933aca5393`  
		Last Modified: Sat, 08 Nov 2025 17:59:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad99f4d97c938fedc1c5841e029ae40af5753e36fcb764743eb1c1ef1a002c`  
		Last Modified: Sat, 08 Nov 2025 17:59:33 GMT  
		Size: 49.0 MB (49046129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5634a6732c3deebdf05e4859e4f3df2901c7f62985b4db6cca73d142a69355a`  
		Last Modified: Sat, 08 Nov 2025 17:59:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86b82888e75447a08c2ec98988629cc4ffb2d5f5c289f34d30f76ed86657a1`  
		Last Modified: Sat, 08 Nov 2025 17:59:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3e2bcefa3670c2268fdc4dfa45788e59826cfab2e0f65366187b2c15f1ddc`  
		Last Modified: Sat, 08 Nov 2025 17:59:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
