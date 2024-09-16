## `traefik:comte-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2f5ea9b188d3833c92570829de6189734d1ba08ba644d7b90ee5faae819ba3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `traefik:comte-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull traefik@sha256:32de57d61c6157e9fd1787975e7141f608f38fda77106016192a74685cc83ef7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766265039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f53168e8a2f90d99dc5febb9afe1fe322a56fa2d5aaf5e61a85257dd18644b5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 19:01:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Sep 2024 19:01:24 GMT
EXPOSE 80
# Mon, 16 Sep 2024 19:01:25 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Sep 2024 19:01:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46e20c7bd1badc3cb97a8f3fd9c19b5530aa47ba807281b28da22bd96e4a52a`  
		Last Modified: Mon, 16 Sep 2024 19:01:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c00d42db6d40fe65713d955eaa74cde669e5c6000abd82a00cc8a0b282e716`  
		Last Modified: Mon, 16 Sep 2024 19:01:36 GMT  
		Size: 46.0 MB (45991511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480250f08d411fcdb7fd03aca864bf5b3722db691fb42ed1fad65e92560697f`  
		Last Modified: Mon, 16 Sep 2024 19:01:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6930ba876873310ab9c407ea48b0debc5bec086b845fcb12c47ebf0867a970ba`  
		Last Modified: Mon, 16 Sep 2024 19:01:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39400d60a03c19269b59fe33a8dde8ca477156f44f2fadf9697d625d0839e0c1`  
		Last Modified: Mon, 16 Sep 2024 19:01:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
