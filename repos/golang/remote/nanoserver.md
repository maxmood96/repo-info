## `golang:nanoserver`

```console
$ docker pull golang@sha256:8a0802bff553cf5c618cb22599fc373d8db702b2017927ea8177e820b3575f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `golang:nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull golang@sha256:7d240c50e1983f64736cb6c7cfc5798bba026e402b5473c6c0bd16d6c2092835
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272186767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111629d12315f483b29afbae07b1107f7cdc693ecef672bfc6d2237e0f9f71fb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:15:26 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:15:28 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 04:15:29 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:33 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 18 Apr 2025 04:15:35 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:36 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 04:16:40 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Fri, 18 Apr 2025 04:16:44 GMT
RUN go version
# Fri, 18 Apr 2025 04:16:46 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b535a6f5c2ac5a5a3eb6c22d947519dfbbd4939786e13b9bed36b1cc83391ab`  
		Last Modified: Fri, 18 Apr 2025 04:16:51 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee5269a6a73616ca31567d74efbe74ea0119e8e8baefe507f6b1ffbad70ed7`  
		Last Modified: Fri, 18 Apr 2025 04:16:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf4b3b914b1e8267046989fc0727cdc39187815f48993f66cc0d1add41a43e8`  
		Last Modified: Fri, 18 Apr 2025 04:16:51 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21d947b0c10e7e1d23a64c1a42815974ffc32dce102f3aa68b97b9087377691`  
		Last Modified: Fri, 18 Apr 2025 04:16:51 GMT  
		Size: 76.2 KB (76230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a9e7184f566b1016b3a288357231cd1ae28f640939b25134400480a90bf95e`  
		Last Modified: Fri, 18 Apr 2025 04:16:50 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2e708b23254762679ed58b53c27302946663435e865b09dd0541f21c020402`  
		Last Modified: Fri, 18 Apr 2025 04:16:50 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de6c7b0f61ab90430a2fa869dc8c4f52edc6149b9511817b86cfe314b125a36`  
		Last Modified: Fri, 18 Apr 2025 04:17:02 GMT  
		Size: 81.9 MB (81873071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736ca52bc532d2423a046b9cdd0bc1257eb4e5a09f294a66d200a19c24672e9`  
		Last Modified: Fri, 18 Apr 2025 04:16:50 GMT  
		Size: 88.9 KB (88940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280aa38cf9a25d4123219a5a296b3546d2f4aa5050a1967fbdefd0ebc8eddd9d`  
		Last Modified: Fri, 18 Apr 2025 04:16:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull golang@sha256:5fb1f102305a43435c16a6e109c99393cb35f423ba46fd92e56c7628f75b5527
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204539753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee0bf25dd1b72d75a79266ebef0ac35a4491eb0f997e09c12b9904d749af9c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:19:27 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:19:28 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 04:19:28 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:19:31 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 18 Apr 2025 04:19:32 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:19:33 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 04:21:28 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Fri, 18 Apr 2025 04:21:32 GMT
RUN go version
# Fri, 18 Apr 2025 04:21:33 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e132a0cab38b238e0161170e6c371719830bb20e459d1d14d69a6d2f0597a6`  
		Last Modified: Fri, 18 Apr 2025 04:21:37 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2581cb463477029201cf975e6523a4ae46c880b3d607f51a50c23c029539eb`  
		Last Modified: Fri, 18 Apr 2025 04:21:36 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672d5a8362d128c539d5623318cc4e599c4d154bfaa09a7ede803b79a51f60f`  
		Last Modified: Fri, 18 Apr 2025 04:21:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ecc4b3f4f6c21729f8cf4cafe161b31743148eb227283713450f27a8055e8`  
		Last Modified: Fri, 18 Apr 2025 04:21:36 GMT  
		Size: 77.5 KB (77507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253c6c5ce36f40540461c7e4cd8b0fa4e5c5d91f6e89005a87c3dbff7dafeac`  
		Last Modified: Fri, 18 Apr 2025 04:21:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fca72f3ec0f04bdcc4a5cbb4fe6b3f38849107bd04524f816f52a1518959338`  
		Last Modified: Fri, 18 Apr 2025 04:21:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2085763ca6b6737912deecb91e926386437c437e10d6c1f4f140a434bd86ade`  
		Last Modified: Fri, 18 Apr 2025 04:21:47 GMT  
		Size: 81.8 MB (81831596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87839bc0957918a6cdfd8e62795e326d32e01f7555870de8bad4d3eb078acca0`  
		Last Modified: Fri, 18 Apr 2025 04:21:35 GMT  
		Size: 85.1 KB (85093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206001f66ad277b05ce3ef0fddad47eb55949b457988efe3bb04079a4cff4b54`  
		Last Modified: Fri, 18 Apr 2025 04:21:35 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.7249; amd64

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
