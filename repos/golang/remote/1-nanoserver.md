## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:5b3e65463f424a4883fae7b12b63304ccbaa117edf857b8cb5daf61cbd3102c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.1787; amd64

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

### `golang:1-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull golang@sha256:e847def62af33c08fb0af27f8b0f9b74b75c4916773b73187cf9806ac6fa4296
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213192119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d7b90a09ced27e5ae2e80cf0deec56dbb09a471c4677009c8ea2ebb69d9a76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 01:50:24 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 01:50:24 GMT
ENV GOPATH=C:\go
# Sat, 24 Jun 2023 01:50:25 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 01:50:35 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 24 Jun 2023 01:50:35 GMT
USER ContainerUser
# Tue, 11 Jul 2023 19:11:40 GMT
ENV GOLANG_VERSION=1.20.6
# Tue, 11 Jul 2023 19:13:30 GMT
COPY dir:25ce036b5dae3a52fa31b69c0aadfc7fed5787d8a208e86cf77a591ece610aa2 in C:\Program Files\Go 
# Tue, 11 Jul 2023 19:13:49 GMT
RUN go version
# Tue, 11 Jul 2023 19:13:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0712dde7e721d063ebcbe80a9968c96e3b3af1f54a33928786e0d37335da4cd`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1bb56d03326ca5e79924c6352857c51196cf8f928048b26c00fa80a312117`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d00feabe0d4e83beb6838d3847aece194f2c8d80d0d9089ad4a3e32ed7374b`  
		Last Modified: Sat, 24 Jun 2023 02:18:03 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672e56f0ebd8522585806f001623bbcab66fb0dcc669e9bb559c2a7a66422281`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 68.0 KB (67956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20802e580a6d2822dae3e7f795d2622374b998505f92dc584dd6afa325251223`  
		Last Modified: Sat, 24 Jun 2023 02:18:01 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d42fa2499d29f6c4f4a177135bfb3b5d94b5a8a32d476f1f0ee67d079541bb`  
		Last Modified: Tue, 11 Jul 2023 19:28:00 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2668fc29e208f0def54feefe47d9207bedce7722b4149555cc747cf26db38ab`  
		Last Modified: Tue, 11 Jul 2023 19:28:22 GMT  
		Size: 108.6 MB (108641089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bb2aab1dfb03a09643a889fed5736689810412406841a4d475461725c10b70`  
		Last Modified: Tue, 11 Jul 2023 19:28:00 GMT  
		Size: 75.0 KB (75048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff564005f8e49bc2280888ffb040b5a56e66d042a7662b3db5d144dc314f8aac`  
		Last Modified: Tue, 11 Jul 2023 19:28:00 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
