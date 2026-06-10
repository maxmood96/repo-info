## `traefik:ramequin-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:869040565a8ad3b07f6b88c9a90e2eb0e4602a3617bef2ed69a91391c725a41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `traefik:ramequin-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull traefik@sha256:c1fce70791046ae4af65fbf46966ec24756441fba834c53c90f00de27c5a211f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329089477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bd3f8d50c149b95dfe74a3d4f17d15c38748d788a278b1e86099d8c544839a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:14:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Jun 2026 22:14:36 GMT
EXPOSE 80
# Tue, 09 Jun 2026 22:14:37 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Jun 2026 22:14:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:566cdf18a17bdab7820302b130023f73a19298c31c1cd48a5d18a27f6ebb1b7d`  
		Last Modified: Tue, 09 Jun 2026 22:14:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7451ac6e19b1c0f13bb0d14e5b57bd60132810904c5fa5ad10fb2a9f02748b`  
		Last Modified: Tue, 09 Jun 2026 22:15:08 GMT  
		Size: 49.9 MB (49941288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5892bbaa2fa696dde6f2fac88755f1017950220aadf5fd7655d36dbb06b9987`  
		Last Modified: Tue, 09 Jun 2026 22:14:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b96f1b23e5ad45177136440104648532f1b9ecf7a4225631eaaa475b21b8cd`  
		Last Modified: Tue, 09 Jun 2026 22:14:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72c2b7304571382856331af5008062c2653c2816855583fec68a854a089a5a1`  
		Last Modified: Tue, 09 Jun 2026 22:14:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
