## `traefik:comte-windowsservercore-1809`

```console
$ docker pull traefik@sha256:e68539faf3d925265afc6d14f3a80347777ff912499284bf00c7e25ef69f5eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `traefik:comte-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull traefik@sha256:fe8e2151f642bcb0656a81c93e69b2c46d9528518f3aeb15f062b4882d49bb47
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1947933394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326ba26f328ade9d6e9ae0cd6d21554ccc3217602eff9eb55a18dd369b455ea3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:08:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:09:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.6/traefik_v3.1.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Oct 2024 23:09:20 GMT
EXPOSE 80
# Wed, 09 Oct 2024 23:09:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Oct 2024 23:09:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d3729c39c7593b15e7dcb75451b5197d9086c7f48df76a39050c8b3dc5a6d4`  
		Last Modified: Wed, 09 Oct 2024 23:09:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb483a3e8234afda44dedbe0bb7864de196a0bd36a31415eca6a30d55ff9ab7a`  
		Last Modified: Wed, 09 Oct 2024 23:09:29 GMT  
		Size: 46.1 MB (46102930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ab7d4d8934a18c7cbb0c5ee47732f2f77d0e9fdfdeb9265e080afccaf4c0d`  
		Last Modified: Wed, 09 Oct 2024 23:09:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b0d0f303020e4028ad2b87b6c8bf560e5904a3689df1b7c02f0bf1090cf213`  
		Last Modified: Wed, 09 Oct 2024 23:09:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be40b912946bb9fa424ca0357afc33ff14826b89bc32a5f7483dcb0ce85f98ed`  
		Last Modified: Wed, 09 Oct 2024 23:09:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
