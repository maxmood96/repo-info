## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:e73bfbf948ed37609531dcd7890e69efba62f352258ed12f1073b32c339dbf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:56c5bcd827df60dfce4e8681ff3007a48e46d2460ec1e5014d1d872c510fb754
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268383150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fbb938599093ae01a04327ec9b358f438cd66110f3ec9ba9b526a6fa94ddf7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 21:44:36 GMT
SHELL [cmd /S /C]
# Tue, 10 Feb 2026 21:44:37 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 21:44:38 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 21:44:47 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Feb 2026 21:44:48 GMT
USER ContainerUser
# Tue, 10 Feb 2026 21:44:48 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:47:02 GMT
COPY dir:e78f50a609fea5ca46e1d1addc58169ec10f3d2953a55005b52ef7e0adbd1c09 in C:\Program Files\Go 
# Tue, 10 Feb 2026 21:47:05 GMT
RUN go version
# Tue, 10 Feb 2026 21:47:06 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bab89a6a66a202f5b1e3b0da2a9b2e2e1f27ae465393caa4609832e69e0238`  
		Last Modified: Tue, 10 Feb 2026 21:47:15 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fde7432bd3e13c937fe844e3aa845423fc28e07ba060bacf7e2087de5225055`  
		Last Modified: Tue, 10 Feb 2026 21:47:15 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14168d99c7b4da06fbcbb5affb1f6df05a2334737a279d24703d3fd5a4af3573`  
		Last Modified: Tue, 10 Feb 2026 21:47:15 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca61e143f32ad48e7183e8a5e07da11505a0b52334a9c8fcefb6bf0957930ec`  
		Last Modified: Tue, 10 Feb 2026 21:47:15 GMT  
		Size: 90.5 KB (90470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd17ffcfc74086c50f082b6e044829c9218928521bd51a9fd0a15c8d23f179`  
		Last Modified: Tue, 10 Feb 2026 21:47:14 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91758a8c6801dfabec2edd9992cc8997a99173d54d17ff49a0729e61454f3d4c`  
		Last Modified: Tue, 10 Feb 2026 21:47:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3198d18c756924426ee65712fd685ec499f3631ff88fe39d5ef587af7ae434`  
		Last Modified: Tue, 10 Feb 2026 21:47:24 GMT  
		Size: 69.1 MB (69119773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12494c3349aba4332e07cb259d13a89aae9cd22fbd6be72d05b1c86ef61c72fe`  
		Last Modified: Tue, 10 Feb 2026 21:47:14 GMT  
		Size: 89.8 KB (89824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15420d652f7a21b4e3e66fe97acdc77c42e1656f922c2d2958580cf5b31abc8`  
		Last Modified: Tue, 10 Feb 2026 21:47:13 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:3c7976249f173fc1c3f70fd3d8a8ae5bb46724a2cf5d86f8b0d4c23042a5e074
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195985118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9058a50e156f8b6eeedef93a4368f4acc6627c8638ca40b0eb6984975638f7a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 10 Feb 2026 21:13:44 GMT
SHELL [cmd /S /C]
# Tue, 10 Feb 2026 21:44:36 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 21:44:37 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 21:44:40 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Feb 2026 21:44:41 GMT
USER ContainerUser
# Tue, 10 Feb 2026 21:44:42 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:47:52 GMT
COPY dir:e78f50a609fea5ca46e1d1addc58169ec10f3d2953a55005b52ef7e0adbd1c09 in C:\Program Files\Go 
# Tue, 10 Feb 2026 21:47:55 GMT
RUN go version
# Tue, 10 Feb 2026 21:47:57 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4acba92e930621aa066243dc804cb79601d3950ee96d913d0b2138d82a8db70`  
		Last Modified: Tue, 10 Feb 2026 21:16:09 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d97665fdaf9c43e79c850fb30334c8fafe94df8465e7b006813ef7b964b740`  
		Last Modified: Tue, 10 Feb 2026 21:48:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74311b2bd92143cdb9c2853f5cf82e0aebb837be6a4d61e9e33bd9254b71ab4c`  
		Last Modified: Tue, 10 Feb 2026 21:48:09 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9daab90393696b4895d90d05feab9bae92ebcd8caa0e39f6345353a2acb7a6`  
		Last Modified: Tue, 10 Feb 2026 21:48:09 GMT  
		Size: 76.9 KB (76890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee760acdabdc624a0701daa5a3e4615b5dd1cc8dc483409a700dd605987350`  
		Last Modified: Tue, 10 Feb 2026 21:48:07 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117ce7ab71a3c29283b9c7efa5cb0fb9268c2b63909d5957f24f8b90b11a72b4`  
		Last Modified: Tue, 10 Feb 2026 21:48:07 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4195a1180cf1ea3d9bcff2e159790407d50756efc5f0810c6e58b0f31f0df2`  
		Last Modified: Tue, 10 Feb 2026 21:48:18 GMT  
		Size: 69.1 MB (69118240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1414dfa8ff732cd556dcb4eb2153335de05afe22fb8f2f7bebdb7211648c3df`  
		Last Modified: Tue, 10 Feb 2026 21:48:07 GMT  
		Size: 86.7 KB (86668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c170604e6bcdd2aa19bc58329caf64617b30889d356d9fe7427f0bc145ba8b6`  
		Last Modified: Tue, 10 Feb 2026 21:48:07 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
