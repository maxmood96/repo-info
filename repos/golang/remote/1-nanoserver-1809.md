## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:6edca792339bb8b475692ef9f845f1c38fbadf7ea8f88a6cad4b5ec86199c7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:8b566af8a7ebf74faae2b358a3a4d379b909387ffb088878802550d169fb5690
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248132451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2741fb3ae764fb003f9331aead15ac6879c2070dae0d9afc2838dabf39b2ff2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Wed, 15 Dec 2021 01:05:08 GMT
SHELL [cmd /S /C]
# Wed, 15 Dec 2021 01:05:10 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 01:05:11 GMT
USER ContainerAdministrator
# Wed, 15 Dec 2021 01:05:35 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Dec 2021 01:05:35 GMT
USER ContainerUser
# Wed, 15 Dec 2021 01:25:00 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:27:08 GMT
COPY dir:4c99dbbc4d53a915cdc29ae9417d812da5b5217c7296fe04ef7fdf708c4a960d in C:\Program Files\Go 
# Wed, 15 Dec 2021 01:27:52 GMT
RUN go version
# Wed, 15 Dec 2021 01:27:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6e2c96db2bf5f7145097ec413d670382424bdefcc277e5a2fc8226ab4fe949`  
		Last Modified: Wed, 15 Dec 2021 01:56:22 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f891f84ddd60832c4b29ece068492db0be44693d884f38408d2dda2a55dd43`  
		Last Modified: Wed, 15 Dec 2021 01:56:22 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01532dba2d359c6d6d0acbd787b3e509dfc8aae8306343c0406a301c57fdab25`  
		Last Modified: Wed, 15 Dec 2021 01:56:21 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc4a9978971608524735fe0bed920bb9046e2609ceb7dddc5c86ed6a199611`  
		Last Modified: Wed, 15 Dec 2021 01:56:21 GMT  
		Size: 70.7 KB (70700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b255b2f880492b8241cd7b4a6b151a9ca9065d34321b683d84c37206a0f4a552`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831bc5da37486cc0a2c567a4cf2035ed9cb5b712a7ec577998331b7c017cc0d1`  
		Last Modified: Wed, 15 Dec 2021 02:00:27 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b039108609ed24635eb361597edcd5b1c17fb3e9687c72bd97476dc143e669e`  
		Last Modified: Wed, 15 Dec 2021 02:01:02 GMT  
		Size: 145.1 MB (145075119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efd3d17f920dbdf1554fc26b403dc172d216848d493f7a10c89e4c681556554`  
		Last Modified: Wed, 15 Dec 2021 02:00:27 GMT  
		Size: 75.5 KB (75450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d279b0ab45fcf6f725bf6ba78ce147d4a669e65ae9b44f946e00b4b5b3afe60`  
		Last Modified: Wed, 15 Dec 2021 02:00:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
