## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:d72b4964d700d3719a89d7bb5ed1e6c215a01ab7f0ccbb5db28617afd73cebdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull golang@sha256:d5184e2d9593bd614cd2d1c5de6380b6baef333fee999ccbdd516de51fd46f3d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228809948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052d9fcf2c5f08cce1d6348a090caab21aee6643c68c8efddc72bef031ab92a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:39:21 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 01:47:25 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 01:47:26 GMT
ENV GOPATH=C:\go
# Sat, 24 Jun 2023 01:47:27 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 01:47:50 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 24 Jun 2023 01:47:51 GMT
USER ContainerUser
# Tue, 11 Jul 2023 19:09:11 GMT
ENV GOLANG_VERSION=1.20.6
# Tue, 11 Jul 2023 19:11:01 GMT
COPY dir:25ce036b5dae3a52fa31b69c0aadfc7fed5787d8a208e86cf77a591ece610aa2 in C:\Program Files\Go 
# Tue, 11 Jul 2023 19:11:26 GMT
RUN go version
# Tue, 11 Jul 2023 19:11:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:d6e77b89ecdadfdd3ef274e9a235590c9cd4dc832939932eff32f93250571005`  
		Last Modified: Fri, 23 Jun 2023 07:43:32 GMT  
		Size: 120.0 MB (120028254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2deb8649e4dedd9fbe74195175cfdae8176065d0daa61337779d26f0bce93`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e10cc3f3d5c676eb7a8f8b4ed7fe56afe4cf0350369685fa91aa510083aac`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b58becc93557f6a89d8222cf063545afd5a26b68db2507913d2c21195a0b3`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc923d8d9d8150c33f7f6b2a2e36a2f4d74b75729b25a0b8e212b9c4c30b7e01`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 85.8 KB (85779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856c8830a4f06b847fc16b25317f8f7b56b03fb5ccac5d82a17c420b2e5e7385`  
		Last Modified: Sat, 24 Jun 2023 02:17:32 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82a7e76b597683283d31a0c23cc8bfbf6c38bd314752087d50f1b505f43e747`  
		Last Modified: Tue, 11 Jul 2023 19:27:23 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae76cd9b5ba97018e3fb301348600148ffcdcf5554c907fd93bf83ca8dd4134`  
		Last Modified: Tue, 11 Jul 2023 19:27:45 GMT  
		Size: 108.6 MB (108643296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf759d3275019a2eff06210f0b39a1b6080dee9f64fbde1985d07aa4cce90cf`  
		Last Modified: Tue, 11 Jul 2023 19:27:23 GMT  
		Size: 45.5 KB (45546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108c1fc2f001d748d90ab4f437c8ec905cb9576da568462c070dc46ce962d82c`  
		Last Modified: Tue, 11 Jul 2023 19:27:23 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
