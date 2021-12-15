## `golang:rc-nanoserver`

```console
$ docker pull golang@sha256:d502fb5a3be5f820d94fe08a3666e44fd3158cac13ec7f367f2cef1cf6961f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `golang:rc-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:91a7f385cceba57d38b573da652c31df8be023b3f6599c6722ee8c64d69484a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269022741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d29434b5c75925e4064155265edcf2458a673eaced4a60b0cb48e648da8ad6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Wed, 15 Dec 2021 01:00:38 GMT
SHELL [cmd /S /C]
# Wed, 15 Dec 2021 01:00:39 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 01:00:40 GMT
USER ContainerAdministrator
# Wed, 15 Dec 2021 01:01:30 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Dec 2021 01:01:31 GMT
USER ContainerUser
# Wed, 15 Dec 2021 01:01:31 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 01:03:58 GMT
COPY dir:abc41c2687fe2e0d7e54b068cc7bb77e17d59bec655dd6e83b05fea7910e798c in C:\Program Files\Go 
# Wed, 15 Dec 2021 01:04:53 GMT
RUN go version
# Wed, 15 Dec 2021 01:04:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e71b7beedb0585e2e2d30a990e4e680f3bfea37d04e5993bcf502b7cc214a0cd`  
		Last Modified: Wed, 15 Dec 2021 01:55:35 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791a8545ff6680119ea879f9675e933cb09d20dabcd8c536774c787a8e232967`  
		Last Modified: Wed, 15 Dec 2021 01:55:35 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cadc4d166f0847e3b29aa9b31c30b8ccb1b7b1c7409f89370f3bc86ac4b9501`  
		Last Modified: Wed, 15 Dec 2021 01:55:35 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4780743ca524a3fe01949a9d2d5db69428f9d02231d90b06a505ad1d1fe9a39`  
		Last Modified: Wed, 15 Dec 2021 01:55:35 GMT  
		Size: 84.6 KB (84609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eadfb74fc8871bb861e5c6ddefbe255eb6a0af0dafaaf93709115ff3bb381e`  
		Last Modified: Wed, 15 Dec 2021 01:55:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd74a55ad0a10af9745c88e4bf9e1073f660a246343bd66bcb75813d41a49cd`  
		Last Modified: Wed, 15 Dec 2021 01:55:33 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d701f42de81d82ee8c021268e479440caed8ba3415ae3ed5a7b968e9b5402eef`  
		Last Modified: Wed, 15 Dec 2021 01:56:08 GMT  
		Size: 151.7 MB (151652104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7f776f88332b88da676a100eb0207e8aae3375556d49ea5c2f7a8c62006091`  
		Last Modified: Wed, 15 Dec 2021 01:55:33 GMT  
		Size: 53.1 KB (53145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010f2d3e3ec081c4a34e4b1bc877752ae5dc6e510053481f0e1937884ad6aaaf`  
		Last Modified: Wed, 15 Dec 2021 01:55:33 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:6dd521b0c5ee99ca08bf0c5dfce8dfb3e3e81237379483ab19efa46e174d8f19
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254723314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2bb278a66a85a47f146ab6687330e2028d4ae131c60ce1cbee481fb54e1ac3`
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
# Wed, 15 Dec 2021 01:05:36 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 01:08:07 GMT
COPY dir:abc41c2687fe2e0d7e54b068cc7bb77e17d59bec655dd6e83b05fea7910e798c in C:\Program Files\Go 
# Wed, 15 Dec 2021 01:08:52 GMT
RUN go version
# Wed, 15 Dec 2021 01:08:53 GMT
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
	-	`sha256:0a66eeb574c994f28af7f7455ffa2d16e80bda3996ac3dea4b5164db6413bece`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db1a5c652b73f1c475f907987272750504bc2b5218f7caecfbb5fe6a56ffa18`  
		Last Modified: Wed, 15 Dec 2021 01:56:54 GMT  
		Size: 151.7 MB (151658015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f6e375c3ce2cba8e643fb90e4e6a61dcf585c9e83e96289b19dee98f7992ca`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 83.4 KB (83430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ced23771c89d0597b1bea64e2c15d4203d91b1674216793458641366bbfd64`  
		Last Modified: Wed, 15 Dec 2021 01:56:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
