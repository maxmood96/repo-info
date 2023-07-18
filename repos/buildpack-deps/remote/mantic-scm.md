## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:527f222a41e4936de72f0e69e0ff06f1349311d08fd5c58d1b5b0178bba16cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9f970f1776038a66f4b75044c41dafba6089e4ec7db6709eb484303684963a47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86109654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82309d805ca626013980144be9e47ab97fba4af8543f5d772705a8d5a0c7ceac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:47:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:48:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f87743a51ebd3c3339057ac4b3ec85dc6978d0b2810c7e52fbb67db0710e9b8c`  
		Last Modified: Tue, 04 Jul 2023 03:57:50 GMT  
		Size: 27.7 MB (27723058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d294972834df62fa5155c9ab227aa39a4ee9d4ff010b19bc7f855b772262f2d`  
		Last Modified: Tue, 04 Jul 2023 03:57:48 GMT  
		Size: 13.8 MB (13766640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b6edf84d2734ddc13188542334cb7491b5163fce6d690d663129665b1037f5`  
		Last Modified: Tue, 04 Jul 2023 03:58:04 GMT  
		Size: 44.6 MB (44619956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3050efa4991929ec39def062f5afb330bb9fb65cf98def03962ddd04f22dc105
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86721999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1d23305027d3f4a15bd18676f44d0057f6fd47fff74ec1f7f66dc3556bdee1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:41 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 09:16:48 GMT
ADD file:53ef0e936c198583128a468b64a8223b792a28cbd74935a7aaa5fa145b4053b4 in / 
# Wed, 28 Jun 2023 09:16:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20af62948d2ad360ef116fe2eef1820df7f5aeee326beae2e81efcc6e366f665`  
		Last Modified: Tue, 04 Jul 2023 06:25:22 GMT  
		Size: 25.3 MB (25270588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ac3606f55aa9aea708e379f37c263f56752be04b8642f50a6f4c8046333a8`  
		Last Modified: Tue, 04 Jul 2023 06:25:19 GMT  
		Size: 12.7 MB (12682677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad2008a4cd1ae83435a1e4de359cd60f53b9915ddb8ab1af207bb42c8151c1`  
		Last Modified: Tue, 04 Jul 2023 06:25:39 GMT  
		Size: 48.8 MB (48768734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bee8e35384ddf35f421ef7381a89a824144c9ac486473cc4f20372cd0cad7a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84888650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3a45fdfb9ffcc2cf174abea921bdd6d649eaaf5646ebc258a27ea3ab2f3e58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a79642e11e4017a06f5c62b8100430987499aaec88e4faace4d954add4f7c0c3`  
		Last Modified: Tue, 04 Jul 2023 06:26:33 GMT  
		Size: 27.1 MB (27075337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809bd1eb3409186f408adf9b158ad6ea72d1135884bdac11ef3a66c1d5758d38`  
		Last Modified: Tue, 04 Jul 2023 06:26:30 GMT  
		Size: 13.3 MB (13349478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9c06373fcaa28267ef4034fdf86623a4cdf64765b1eb01bb141a1bfacb89d2`  
		Last Modified: Tue, 04 Jul 2023 06:26:46 GMT  
		Size: 44.5 MB (44463835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f555e748d57936a1893ce800414d2691b397e629dc4cc217584d9b599d454f0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97161131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08d5140e79cd7a53ef9cada9b9fb0a5bfe876f6f17eefa9b7c9e077edcfcc75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:23:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:add2cbebe3a583002ff52a300bd69d6b961b4a7735c4612e8030bd26ad555288`  
		Last Modified: Tue, 04 Jul 2023 04:45:56 GMT  
		Size: 32.0 MB (31951571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de6196fb1fff1ebdd9bca2afdccb736f7418000536393564f88be29d3b0c74`  
		Last Modified: Tue, 04 Jul 2023 04:45:52 GMT  
		Size: 15.9 MB (15859335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce64e4b1ebabc1c300d88412d9b3c89e46389306d0ece236088cc4721eea35b`  
		Last Modified: Tue, 04 Jul 2023 04:46:21 GMT  
		Size: 49.4 MB (49350225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0701a87a39ba7a5b13f5af26dd438551eae62de80cfb8e120b20da4016b92148
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85005805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8e32e1c8a0607953bad4aa48adfe5b58e9641c89ddaa7c104660b0848cd95d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:53:32 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:53:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:53:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:53:32 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:53:34 GMT
ADD file:878995fa3a12c9df0a99fc88605932ffefec3e772a3c4ca89fe0c0aaa7dee67d in / 
# Wed, 12 Jul 2023 04:53:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2b8f6b9cb3947ae25987d6e3685dc9709178b596bd7bf0d7a84ceeba23a2073`  
		Last Modified: Tue, 18 Jul 2023 01:18:14 GMT  
		Size: 26.3 MB (26322139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b736a5889ac0138557b62eaa679858540efdff47fa4079b2d261d5d981a0b7`  
		Last Modified: Tue, 18 Jul 2023 01:18:13 GMT  
		Size: 14.0 MB (14037874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d33eaf6ee65a8ded43a590675151bb6e283880b75995e7651a1b22700ecbe`  
		Last Modified: Tue, 18 Jul 2023 01:18:27 GMT  
		Size: 44.6 MB (44645792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
