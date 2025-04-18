## `traefik:v3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:c147966597f19f7c0e031b64c9fb0d6181304bc6875f8a880e7755e13a1dd954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `traefik:v3-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull traefik@sha256:679d5841498e9946700b468f18a8fc34d2c64c8c089ce93e364281670b895e0b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221318850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ea58ba41fb37f09965c52fd144ff5efb004a93d6cb9fb0ea145c3ef61ff6c3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 14:08:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 14:09:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.6/traefik_v3.3.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 14:09:05 GMT
EXPOSE 80
# Fri, 18 Apr 2025 14:09:06 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 14:09:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a6253943ebe1c887b98e57661c371197e2b1dbc0f12f276a5652e53262c98c`  
		Last Modified: Fri, 18 Apr 2025 14:09:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521df65ebfc1d628af743af4bb2990594eca330b4977706780253b68c1724827`  
		Last Modified: Fri, 18 Apr 2025 14:09:17 GMT  
		Size: 55.8 MB (55787883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45db03ed533a436d68a248f7348cf2db43482333d7146f86d52f15a5c7f54e69`  
		Last Modified: Fri, 18 Apr 2025 14:09:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb9dec753d317abbc028187a633ea883caa2e509ddef3d39bb880a4b58c45ad`  
		Last Modified: Fri, 18 Apr 2025 14:09:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afcd891ef9e6440da168ddc0657b6e5cf87febda3cb5d4a9cf4866b04d3b12`  
		Last Modified: Fri, 18 Apr 2025 14:09:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
