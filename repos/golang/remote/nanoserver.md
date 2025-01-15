## `golang:nanoserver`

```console
$ docker pull golang@sha256:e0a7d06844bf212a2af1874027d569d24070bdd0a78f34caa8da0c3ee1345f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `golang:nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:97790716ac4d039da44a5a1195cac48f8241ddeb2729bdf7a01fa3276a1847a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197786779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0b3461f5d739d4a56b9f66502248d1161aa95d69a05067a5a7d49a309a82eb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:14:18 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:14:19 GMT
ENV GOPATH=C:\go
# Wed, 15 Jan 2025 18:14:19 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:14:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Jan 2025 18:14:22 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:14:23 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 15 Jan 2025 18:16:19 GMT
COPY dir:c57def00df00b8073b50c57c8023ceae4d144aedef00a4df4374a7bdf40392c4 in C:\Program Files\Go 
# Wed, 15 Jan 2025 18:16:22 GMT
RUN go version
# Wed, 15 Jan 2025 18:16:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c3bb441f37d3fbc45f0844a9d2e1bc1b7c1e9f566291b346f7d29e3eea46ee`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef33c3275e4d5878f48b1b9f0aca43082d160a9b1babbbf1e6d10cfd23ea54e`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19808a7b95c38731d9c0bbd02a9babdce1a450668dabf034c61a5ca34c7f4303`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed1327b7c47c430b6c7bfe3b02ea0751273d3fc5a2142e9996f98d9086bd6da`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 75.7 KB (75672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653a33260bf10f25ef8775ad06a179d71e6c10de4f27b21739f394f4d3eb8e34`  
		Last Modified: Wed, 15 Jan 2025 18:16:25 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df024a2d8536b6e9a77ab98042a07ea0c36c649785cf7e786ea9cea146d0c096`  
		Last Modified: Wed, 15 Jan 2025 18:16:25 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c487ca3fa941df51872cefa56a2ad8acfce4edeaf0fdd7c4daa5e4c40c848e3`  
		Last Modified: Wed, 15 Jan 2025 18:16:36 GMT  
		Size: 77.0 MB (76950598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a304752d81c91585242c32ee5619dcece38ca217cff22c0302c0d2db5784ec34`  
		Last Modified: Wed, 15 Jan 2025 18:16:25 GMT  
		Size: 92.3 KB (92315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc8cc00fafee190201ac1e36a620b28feb19416dd9a7ea36b1a09c76f1c1eeb`  
		Last Modified: Wed, 15 Jan 2025 18:16:25 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:2e9eeac347bc26f10496a54cc75c5e29779cd76f485a9f0c00cbe9aebd6854e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97476e2649bd26db040b70cd4e2bf3503bfb1e00667d46db91fa80e61950d41`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:54 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:02:55 GMT
ENV GOPATH=C:\go
# Wed, 15 Jan 2025 18:02:55 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:57 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Jan 2025 18:02:58 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:59 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 15 Jan 2025 18:03:57 GMT
COPY dir:c57def00df00b8073b50c57c8023ceae4d144aedef00a4df4374a7bdf40392c4 in C:\Program Files\Go 
# Wed, 15 Jan 2025 18:04:00 GMT
RUN go version
# Wed, 15 Jan 2025 18:04:01 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289835f94628689f4f4163843f138789e40e0cadd9cdda2dbe7356216ba5e7ad`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8baf4e5644f71c977dab1d900be8235d0e5daa7d4f4fe8bbf1d70add2b7ef5e`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1f13b5f349a328d58a1a61f4559024534b981502e5096853468c3559277dbc`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722ae0a3e311a418cc049d63bcbd8298fa3ea955111e8adab2293a7022c5a51c`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 74.1 KB (74079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210119b3631b411512c40e76314cae4a2dc29d6cc24f41a7e9c26b1df5dc8a67`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab75551faa32f909db6677df0ff9d08f682c7a89abec6d5b75a2b5240811ec4`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc9ff4d86c42b350f08f4bdb47adfe93c647d3e7864f2b4a27947cf6a4bdfc`  
		Last Modified: Wed, 15 Jan 2025 18:04:17 GMT  
		Size: 76.9 MB (76948663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22efaaf02302cd9ba7efd17eb7f88ade8ad9b7b17553e58eba285bbac68bd48b`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 71.9 KB (71899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d604df50c984c997a36b581d85b9fd52677f1dd15e2149aa1ed867c615e48c6`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
