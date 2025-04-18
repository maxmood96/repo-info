## `traefik:chaource-windowsservercore-1809`

```console
$ docker pull traefik@sha256:9c762522397791ab16e4a59bf9f656ab6bd020ab392107dad236a329536b9b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `traefik:chaource-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull traefik@sha256:70e3ec771c7329b57ce8b5977df31f9a329aa020941ffbb64b0660421edaacad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220673496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eb9302ac80bd6bfd567e897644baf87e99b4f6e9789904d5bc33ec3537d0d1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:17:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:18:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.0-rc1/traefik_v3.4.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 03:18:06 GMT
EXPOSE 80
# Fri, 18 Apr 2025 03:18:07 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 03:18:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e58dde985a6c144f557e9f1887c33aeee31d4f48e03a5a98d8a90e71aab2b85`  
		Last Modified: Fri, 18 Apr 2025 03:18:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560931281544ebf3663c837ccabe6ba386e8e5d22d7c447d5e48548d818ed7c5`  
		Last Modified: Fri, 18 Apr 2025 03:18:17 GMT  
		Size: 55.1 MB (55142512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcbe38b94df50767ed7ec9116de0a29bb4454a04f9fd0040b8423d22939ea6`  
		Last Modified: Fri, 18 Apr 2025 03:18:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aa202082a8ae4cb7c79ba073a348781daf665f15579e41b2812b06aa13fa60`  
		Last Modified: Fri, 18 Apr 2025 03:18:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea63c1ea4c6db67c1c7876b6f9321968e36e3f6bbee00b5236e7100ae8a2dc4`  
		Last Modified: Fri, 18 Apr 2025 03:18:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
