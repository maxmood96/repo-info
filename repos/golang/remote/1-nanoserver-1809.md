## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:3b0d7a881f790c51a175af79abf024a43d1ef6332e7504738a181eabd5c205cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull golang@sha256:b63266b31c8899c6eb472b648c53312bfb184398ae3b870c0ff31781011171f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190722362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3656342f479eb310d91cf8eadc76f43a50fe5b004ddec7d77f9afdadcfd2efb0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:20:21 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:20:24 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 04:20:25 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:27 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 18 Apr 2025 04:20:28 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:29 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 04:21:31 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Fri, 18 Apr 2025 04:21:35 GMT
RUN go version
# Fri, 18 Apr 2025 04:21:35 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3cbf164b2883f828aceab3ee911c4720163b8b4651c31c6cb93d1f21fceda6`  
		Last Modified: Fri, 18 Apr 2025 04:21:39 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5284ebf1f004993ef3ee7547ca94ac4405db18c28ec27f8fa5fa4c0d9db7d6e`  
		Last Modified: Fri, 18 Apr 2025 04:21:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf57ed8a61edd5d57d1e749b700f9d49cac0377201200dd255e126fa6d444d5b`  
		Last Modified: Fri, 18 Apr 2025 04:21:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db03baab56574eb0c9a52307f7d7a21f3c1be2e61398a1cb4091cdf2b4e86581`  
		Last Modified: Fri, 18 Apr 2025 04:21:39 GMT  
		Size: 69.0 KB (69008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a3eaa0715033ce475ac3ec8f11faf2a67c2c3aeaed3999ec23fa7f7c2d4785`  
		Last Modified: Fri, 18 Apr 2025 04:21:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3638c4c4fc2de37f57bbda0a096ae3679d6d10bc6c5e0c9b2dfb5fdf5daf6a4`  
		Last Modified: Fri, 18 Apr 2025 04:21:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be478da7c477dec31cf78b9008d9a2d98626e908d4eb7bd621f6fc4935b6c24f`  
		Last Modified: Fri, 18 Apr 2025 04:21:51 GMT  
		Size: 81.8 MB (81823768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02119c732901c4a7522fa9c5e61ee710d9aa8178f324a8ac66af5a15901211`  
		Last Modified: Fri, 18 Apr 2025 04:21:38 GMT  
		Size: 70.9 KB (70914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973c920165c2941619a4ed35267951df313a286cd6fc7f5f6c206fc1111b4e00`  
		Last Modified: Fri, 18 Apr 2025 04:21:38 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
