## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:4b7a1f82c6efd11e785a321096fc02cf5bff81d0905ddcbc7f434992fca2047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:827ea20bb3d72c4ed19241bbecfdd967ce4706f07fb08d6de76f116bd514f26e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288331233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfcab0ad9f6f54d0ab799aeb9bef54af3e38c56fb86ba19ad10873b6ac6ca8a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:38 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 19:17:39 GMT
ENV GOPATH=C:\go
# Wed, 12 Mar 2025 19:17:41 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:45 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Mar 2025 19:17:45 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:47 GMT
ENV GOLANG_VERSION=1.24.1
# Wed, 12 Mar 2025 19:18:51 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Wed, 12 Mar 2025 19:18:55 GMT
RUN go version
# Wed, 12 Mar 2025 19:18:56 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366a9eff47ff5992506e4485a05b5fa057cb1e4e9e4cfe1613c46999ea0c46a0`  
		Last Modified: Wed, 12 Mar 2025 19:19:00 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978a9c35947af3df7656b615297979c5a7e7a9b3121a93120ffe1efe0aac14be`  
		Last Modified: Wed, 12 Mar 2025 19:19:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d1fbcb26ad837c6478428b5951b8b43cd4b9821942957fce50921b8703ec1a`  
		Last Modified: Wed, 12 Mar 2025 19:19:00 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87658b1286582ded25fc8265ad1b50b1027e459a9822893263674e0f46372d6e`  
		Last Modified: Wed, 12 Mar 2025 19:19:00 GMT  
		Size: 76.2 KB (76199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b2784c7af1e97a91b7e7a2bb4824a83531337b821168c4470eff2b29d876c`  
		Last Modified: Wed, 12 Mar 2025 19:18:59 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252f671a4c4928c6ca222d81c34fe8ddf87fc77b34a5f53042c57ab367267f28`  
		Last Modified: Wed, 12 Mar 2025 19:18:59 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f5474d476bbe56551e41db37c8fbb6380e4827ad47b908c0fe556768fdd8d1`  
		Last Modified: Wed, 12 Mar 2025 19:19:12 GMT  
		Size: 81.9 MB (81858388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d0d76842af9c19c862a115c5826e7531d6029baba634a906ec3dd019659a11`  
		Last Modified: Wed, 12 Mar 2025 19:18:59 GMT  
		Size: 87.9 KB (87857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1624edec8cc5f66c5621c7eca6f533fab3d3fb0ecee5507d797286700e92d118`  
		Last Modified: Wed, 12 Mar 2025 19:18:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
