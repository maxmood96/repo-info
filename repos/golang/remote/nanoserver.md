## `golang:nanoserver`

```console
$ docker pull golang@sha256:449585add1f97e72c279c5cdfc7247f4f2a4098db1ff3234d5081ff520a1f401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `golang:nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull golang@sha256:51bf7719dd2b245cbe9ff23c9780e5757780c30b621433cd24e1d0463c936b94
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268735301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b87c950c202a7b0686fbe4990b7d2f8b2690bb6ca7b8ed191c0abfc71bf6253`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 07 Apr 2026 21:57:55 GMT
SHELL [cmd /S /C]
# Tue, 07 Apr 2026 21:57:56 GMT
ENV GOPATH=C:\go
# Tue, 07 Apr 2026 21:57:56 GMT
USER ContainerAdministrator
# Tue, 07 Apr 2026 21:58:08 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 07 Apr 2026 21:58:09 GMT
USER ContainerUser
# Tue, 07 Apr 2026 21:58:10 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 22:00:50 GMT
COPY dir:67fc335d5ed530085681f1943ca37084f1abf3c9dd644604da00d33121190fa6 in C:\Program Files\Go 
# Tue, 07 Apr 2026 22:00:52 GMT
RUN go version
# Tue, 07 Apr 2026 22:00:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff39316d7ed38cca276635aaf0cddad70becc05593f9a1978bd07974ec7815b`  
		Last Modified: Tue, 07 Apr 2026 22:01:08 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d6c050fd2614e8f35f44ff810bdbfa2f65d9bdf51cd21889564d6e7bc7da5e`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f676ac91c1d7fdf325024edcae69aaf6358b81b2e3000e1d9bf2e60d2c21a1`  
		Last Modified: Tue, 07 Apr 2026 22:01:08 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f62a7f89ed56876373d62a8f930e94ae2fda29f31a8cec5ae906618110d5bd`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 69.9 KB (69878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbed30d38d6bf0319b94ecf37ec485650a73d378e14b856d8f0c1d03557323a1`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c424dc3dc8d2403cdba22f1a7953ddf277a27a9c85d0b217d4e65decda5e3a5`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaef163da3710587aa500927e003e9449f2b92ec373ae17d721924fa26469ec1`  
		Last Modified: Tue, 07 Apr 2026 22:01:16 GMT  
		Size: 69.2 MB (69170670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7416ed4445fa690b18b75a43d22c1a3d912b27a4ec1cfb0b045a1e72cf57cce9`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 78.8 KB (78791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e354edab508450f5dcf41c251fe64b02c2e2206508ba44d5b8dfe9ed52ea620`  
		Last Modified: Tue, 07 Apr 2026 22:01:06 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull golang@sha256:b044947f062d0a01ff678ac5b250d6afb91a00ebb81ec68a48b49d872cd02b6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195988422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb92c0bb0f77922cab19fb69d5ec99ba5eb29408f249ae6b793ca16e3e346ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 07 Apr 2026 21:58:43 GMT
SHELL [cmd /S /C]
# Tue, 07 Apr 2026 21:58:44 GMT
ENV GOPATH=C:\go
# Tue, 07 Apr 2026 21:58:45 GMT
USER ContainerAdministrator
# Tue, 07 Apr 2026 21:58:53 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 07 Apr 2026 21:58:54 GMT
USER ContainerUser
# Tue, 07 Apr 2026 21:58:54 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 22:00:45 GMT
COPY dir:67fc335d5ed530085681f1943ca37084f1abf3c9dd644604da00d33121190fa6 in C:\Program Files\Go 
# Tue, 07 Apr 2026 22:00:49 GMT
RUN go version
# Tue, 07 Apr 2026 22:00:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f216241facf4bba1cc03d1ec55fdf125abb561d7f3a568a3ffe678888b92f2`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da6bb8d7c1d4117737148054e412319c7d99fb56863457a6a24f7c69ec72e01`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4529d7130569fb746783a303f6abb4168223c24d7390b990fc29781eea77ef8`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f386751e503d44d894ca77516fbabd191a6907b6bee6d003087c91f5fa56e`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 80.8 KB (80775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d628fc173a698b9cecd00506d8d138898e4ab7b1b37ddba0f1750ba8f95a98`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d884941654cb343034a810782e4394437ea9794039cf3a5cb7cdc8b3511c89`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa5fed408a1d0c911eca62d232dc4e6e2716fb04b71038e13c11e38dca71b4b`  
		Last Modified: Tue, 07 Apr 2026 22:01:16 GMT  
		Size: 69.2 MB (69170893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b011e5d0af76eb6651b003c8d6e325ce9ba9569df969beee1add2e2db78b96`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 79.6 KB (79609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9e347e2d411dd96c9dd9186c97a8836996138ace6c13178b1cc6a29771f2f`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
