## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:4cb5154e97d5f30ba19cd4072113c151cbd8aa83a72a8576db4838cabcf3e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull golang@sha256:2ff2bd24b657f1232a89419fd1be7802612d4d97f17bbcebcc731314732dd60c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269049268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfa6354e939b740fe8a67e8ddca674dd7251fe5d7afb48481ae7978f03badb2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:15:05 GMT
SHELL [cmd /S /C]
# Tue, 14 Apr 2026 22:15:05 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 22:15:06 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:15:08 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 14 Apr 2026 22:15:08 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:15:09 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 22:16:31 GMT
COPY dir:67fc335d5ed530085681f1943ca37084f1abf3c9dd644604da00d33121190fa6 in C:\Program Files\Go 
# Tue, 14 Apr 2026 22:16:33 GMT
RUN go version
# Tue, 14 Apr 2026 22:16:34 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b72946700875900955019084fbc5ba8eeb559fba8f57a4c1a197c2a1832df6`  
		Last Modified: Tue, 14 Apr 2026 22:16:51 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b09f561bbd01ffd854703ccc8bc8721b6d744df7520061d63fe9f33e02eb60`  
		Last Modified: Tue, 14 Apr 2026 22:16:51 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4858a0f3feee74860a0adb3f7e34cdf16acae3689ab221ea700671a307a01bb`  
		Last Modified: Tue, 14 Apr 2026 22:16:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551e02c1d5dcb16bca77f1a9cf8b5fcc47128dc10786dc9d94322f4c7677c6d`  
		Last Modified: Tue, 14 Apr 2026 22:16:51 GMT  
		Size: 72.9 KB (72887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4eb0555a0516eaf428143404691996d398a194f7d2d3d2f6513e75bd7533df`  
		Last Modified: Tue, 14 Apr 2026 22:16:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a00674930bd7d52fc83b042f3ca5dbe90122114d6951d164795f00e6dba901`  
		Last Modified: Tue, 14 Apr 2026 22:16:49 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c6a93db0604ab05aa4bf861c3358c7527719ab26e9552d72b866dd45b2cec0`  
		Last Modified: Tue, 14 Apr 2026 22:17:01 GMT  
		Size: 69.2 MB (69169039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a94e9f0faefcdc8b8c8556d24105a3ac6b8ce7285c271f074cf3da02c75e4ff`  
		Last Modified: Tue, 14 Apr 2026 22:16:49 GMT  
		Size: 83.6 KB (83622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4f358559cba0ad3a5a96a3a373b0ef1ad5eb162f92d41a8b586a609a06c85f`  
		Last Modified: Tue, 14 Apr 2026 22:16:49 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
