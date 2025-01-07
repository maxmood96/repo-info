## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:4814e769bda142f2ea2a60d2a65dbe0b3166ebea421b9608bdf1a22d7a2eb7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull golang@sha256:462437086922039a684099af661363e116db23899d3872ba547b03cb8380eaf6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232326712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcc3770c02ee147527fb774b65c2b2c9d401c6b709ec01ab5aab65a8b5e2c10`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:46:44 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:46:45 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 21:46:46 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:46:48 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 11 Dec 2024 21:46:48 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:46:49 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 21:47:48 GMT
COPY dir:c57def00df00b8073b50c57c8023ceae4d144aedef00a4df4374a7bdf40392c4 in C:\Program Files\Go 
# Wed, 11 Dec 2024 21:47:51 GMT
RUN go version
# Wed, 11 Dec 2024 21:47:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10a906d5cec7932283ffd73e8a8bbd50777586f8b72b876739ecc44f3fa5cc9`  
		Last Modified: Wed, 11 Dec 2024 21:47:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a7ccf2bb3194a837b5c0f7b76649d8069bb09e6c1a135452abdaef820e850`  
		Last Modified: Wed, 11 Dec 2024 21:47:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3289da10e68b05ada5998e355227e4111361cd6163ba1cdbd53b5ae982076d5f`  
		Last Modified: Wed, 11 Dec 2024 21:47:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9f89d75dad44358058fb924a3fe3c80f9e3de3b5fab6f9533762ece824bc8c`  
		Last Modified: Wed, 11 Dec 2024 21:47:57 GMT  
		Size: 69.3 KB (69251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f90597a72a30c7e676d733f67e269d69df2958dee1a00c47f221a15b88c9740`  
		Last Modified: Wed, 11 Dec 2024 21:47:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a9585c9f3fe965a8278c8cfffcda989d690d0579ed05dfd488ea17eaa7d9e0`  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3689e47dd7448c87c5bbeffd4ad3a548a094a3a8a7ff510561d2b29df85d2d3`  
		Last Modified: Wed, 11 Dec 2024 21:48:07 GMT  
		Size: 76.9 MB (76949923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980fbe2e82201a5704af6ea2f1ab6597060f1f23a5a5ea679b3ec9700c77d3a4`  
		Last Modified: Wed, 11 Dec 2024 21:47:56 GMT  
		Size: 69.5 KB (69485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ff3ad76b237b65125442fe54c35ea92c8fa1c7992ac0b263ad8dfe001ab0d7`  
		Last Modified: Wed, 11 Dec 2024 21:47:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
