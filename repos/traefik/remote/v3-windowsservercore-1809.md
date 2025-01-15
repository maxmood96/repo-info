## `traefik:v3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:e670ffd861b95b21944e9982c724ee5f9481fe67f2b75e01e0980f75f4977c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `traefik:v3-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull traefik@sha256:9eefa2e0bdac9ceac10f55f7a1c5098cd477d80713d873278eb531ca9b75f34b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2064083133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9484dbe04e0130768bf9325a3b2fc3987a4cf00fb87ba0c73819ae0bf434fa8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 19:27:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 19:29:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.2/traefik_v3.3.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jan 2025 19:29:11 GMT
EXPOSE 80
# Tue, 14 Jan 2025 19:29:12 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jan 2025 19:29:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064fc46cfe1cff3b6971a89cb9f044b9a133574c7bcba5935de857af55312bd9`  
		Last Modified: Tue, 14 Jan 2025 19:29:15 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6351b407c675c5765bab74621339c678d54093ce0c6401c11eadaba5ee0d0bb1`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 49.9 MB (49907729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa592b93a681517d7a0a31533064ad6a0237b20c9bcbfbf4c43fe56da432f8d`  
		Last Modified: Tue, 14 Jan 2025 20:33:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b695be1399efc9dc951db0f708c11d0c56c2e4feffffbc43b6c3d54fd6f25c1`  
		Last Modified: Tue, 14 Jan 2025 20:33:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c187f80d37f6bdf0265111075313fa444e95e4ebbd750594d96d633c1c2f83c1`  
		Last Modified: Tue, 14 Jan 2025 19:29:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
