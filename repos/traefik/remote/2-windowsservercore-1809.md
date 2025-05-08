## `traefik:2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:ea4ea661882fa3e72d24d3ae87971afcb0aef7daea69f5693e67212de62f74e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `traefik:2-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull traefik@sha256:fa8f1c58418c2656b2266f4f99aeb4c65551dcba0f2229346524470ac34c8436
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2219646460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69522ab76301f1ebce94cdd2fb5d6606439d279cc8e06c0cc1ffaf14b21c24f3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 14:02:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 14:02:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.24/traefik_v2.11.24_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 14:02:49 GMT
EXPOSE 80
# Fri, 18 Apr 2025 14:02:50 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 14:02:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cff7303f1306ff2d17b1dc40d6183b7770a21475488f1385ff20a7c6c8c2f8`  
		Last Modified: Fri, 18 Apr 2025 14:02:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c54310975610ff19ae59cf8e3a989ea031982572806f70302795dfebe13492`  
		Last Modified: Fri, 18 Apr 2025 14:03:03 GMT  
		Size: 54.1 MB (54115483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa28db612f0c97e2d2318bfc45dd88501b6d791924fcdab6b483147ba0138ee4`  
		Last Modified: Fri, 18 Apr 2025 14:02:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50f484942e2162b5bb45420774385da9249c4e2f716b8906c848158a926d52d`  
		Last Modified: Fri, 18 Apr 2025 14:02:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2a9df761248d3c4710d1810674e6ede455b18a4a2cda481149cff86811f805`  
		Last Modified: Fri, 18 Apr 2025 14:02:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
