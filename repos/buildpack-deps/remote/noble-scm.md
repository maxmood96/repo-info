## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:47ebb9de9a029d0381efc89f2e05553c403d2850569cb88b6482057160efc3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d0ada0fd87383898793527a2108364d125434776d8996380fb18e85fc48e0dd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89579571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fb010e9d8362e64239fc46b0f1845b95190c39c075a5f62eb5ea602f4ac12e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3fa374d78d6bc1d2cab1e56e050fad206b983d08dd4d05ce017af22c2bb25`  
		Last Modified: Wed, 22 May 2024 23:41:29 GMT  
		Size: 14.4 MB (14441188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad31eb17b1c35f2639c2ad85926af055e59d35a801e6a53297275981850f09e`  
		Last Modified: Wed, 22 May 2024 23:41:45 GMT  
		Size: 45.4 MB (45435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c8361c2f22d82113df3ab9c0d9d3598cbe6f52392b2678836904baffef6812cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89397466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef57cc2c25e599bf59398ec7a3b8a688a145716b68ce2faca3c270ef5d07ac7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 17:03:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 17:03:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 17:03:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 17:03:38 GMT
ADD file:7b9ebeed2b8df3ae6b4ff0b90cb86423ff21019cca623cd8f5ffaeedebc50bef in / 
# Mon, 29 Apr 2024 17:03:38 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:11:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:65b0f107a3b2a3765c847470cc1b37265cdb4ec78f1b5b17b6936546f15e2381`  
		Last Modified: Thu, 02 May 2024 02:12:18 GMT  
		Size: 27.0 MB (26956922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341026a43066edba3891759cc2046c69c99f7276f495e01f0c11ebb123a0c4a6`  
		Last Modified: Wed, 22 May 2024 23:18:14 GMT  
		Size: 13.5 MB (13462659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79c7665cb15132f5e9fdf1c155d6655289164bb1cc11ceab600dddbd579fdd`  
		Last Modified: Wed, 22 May 2024 23:18:29 GMT  
		Size: 49.0 MB (48977885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dd7c125037938cf0033d1801675a3e9b97a05820056808b7f678879022b284be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88710081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf721d51fc43f52663c4076a822935af6d8124a27c821c8ea7845c75f391e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2afb81653918fa9a91fa586df7601ad7b3319bbca1de65beb077f68feedada9`  
		Last Modified: Wed, 22 May 2024 23:27:43 GMT  
		Size: 14.3 MB (14272172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb103266013103b27f23e5331700e3f47c0d81dfb6cc077477879bc345690da4`  
		Last Modified: Wed, 22 May 2024 23:27:57 GMT  
		Size: 45.4 MB (45399239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47647f9af2878ca9efbc2a530ff60408af1b786ebdce4739d89aa723dbd7a0c7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102236196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df2ee5e3435332bb73e4d3941bee46519534a471e13553323516e8aed17b1cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:36:39 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:36:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:36:42 GMT
ADD file:c915ac180ad59faba89e9e3f73473adedd3ac5b7024bea2fe61b266b3efc1267 in / 
# Mon, 29 Apr 2024 16:36:42 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:22:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bcb8c42b2752babcd7ef1c98e380f22f0fe7f25521a416951d4cd54bb4cb300`  
		Last Modified: Thu, 02 May 2024 02:33:48 GMT  
		Size: 34.6 MB (34579045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3454492f91b9cbefc2b39d3778f8e7438fe49ad93238457b280d4a2ff725bca9`  
		Last Modified: Wed, 22 May 2024 23:30:04 GMT  
		Size: 17.0 MB (17006808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbd8c45886bd3fcccfaef22c71a6bfdc3ed9d116a6895a61a882314d5333409`  
		Last Modified: Wed, 22 May 2024 23:30:21 GMT  
		Size: 50.7 MB (50650343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:347ec9f8908fbfd52725d228eb0df842231f907bf728abf9fcacb9565c6d4cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92723005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a453fa11fa1069726192c869c0f802c31efc1a3dcde77c484cc8290c0f9db6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 22:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 22:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:68e0be12c8304c831d669224097b6db6b2c5123796652f8911f2245c0f955227`  
		Last Modified: Thu, 02 May 2024 01:35:40 GMT  
		Size: 29.8 MB (29782463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc6aab162b5b621207fc955e7e0f2eb5814a8f0e8ea50c9758912808a622956`  
		Last Modified: Wed, 22 May 2024 22:53:58 GMT  
		Size: 15.9 MB (15859108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62dfb49284bd5744f51b3d45e6eb0607119e2baf55223aa79a3cb688a47fc9`  
		Last Modified: Wed, 22 May 2024 22:54:11 GMT  
		Size: 47.1 MB (47081434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
