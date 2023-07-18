## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:e637201ce903e9176ba769b0ca6feb98a106673a788691e0057e6837ce7efabc
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
$ docker pull buildpack-deps@sha256:85d72857fea95aeb6d112513da095e1878f6e1efa45f440f9dcdee9d9a0b5370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86321874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7b8afe3427bf251dbae8dba5b9d858cdb087aeed3dc518427671aa5aea9ea4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:50:42 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:50:44 GMT
ADD file:592c8f21973a80f096ca38aaf5ef478d80f666517a169bc638ebb325f5ae07f4 in / 
# Wed, 12 Jul 2023 04:50:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c57e6f7e53eccd34261640d6f245ad38a4ff7cc54ead279536b568d836363ae4`  
		Last Modified: Tue, 18 Jul 2023 01:49:46 GMT  
		Size: 27.8 MB (27758391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70262639a4fd505c867f716c40dd85135752950cc1aa365725b9e2967d66175a`  
		Last Modified: Tue, 18 Jul 2023 01:49:45 GMT  
		Size: 13.8 MB (13781000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade5aed8da7a4eb9b7d6f71f11a953d3491588e96cb6cd244876de5a69a96cea`  
		Last Modified: Tue, 18 Jul 2023 01:50:01 GMT  
		Size: 44.8 MB (44782483 bytes)  
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
$ docker pull buildpack-deps@sha256:29540c8fb7fe2cbff1c5b2ebbe79377102298bb93e3176b97416e36008ebef3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85116674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d4533597e76b8d10fc71998896d25f47ab73decd47de07630f4cbb9c0e52e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:54:30 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:54:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:54:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:54:31 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:54:38 GMT
ADD file:6eb08bb754e74bd297a54d5c56c7622fe3945c0e013d8a48b8d85b09f1818099 in / 
# Wed, 12 Jul 2023 04:54:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:46:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f4369a81c2a2103bb37c89ff5ddb71caf0eefa6abc6ace3a6312b114b1b43f4`  
		Last Modified: Tue, 18 Jul 2023 01:51:33 GMT  
		Size: 27.1 MB (27116407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9605105b68496ddcb5871d9313b51b49ff984efaf7993f0d2e84539e1fd35b1d`  
		Last Modified: Tue, 18 Jul 2023 01:51:32 GMT  
		Size: 13.4 MB (13364288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7138fb2464b9037662e225fd640c60489c9bdfc93091ead842a55da631876df`  
		Last Modified: Tue, 18 Jul 2023 01:51:47 GMT  
		Size: 44.6 MB (44635979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5427d53e2a0f36be11ddee624b8c2282efb28ea974220e842386fef4566bb3ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97390756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490ac353d73761f55f94aaa4b8e908f4e3c1ecdff0aeef98c7eb21967229e66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:53:28 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:53:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:53:31 GMT
ADD file:7028e8b5bb04424a3fa537fa5b5a311cfcaf1c8b6f321b414b40ee0388d0f9e0 in / 
# Wed, 12 Jul 2023 04:53:31 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jul 2023 01:54:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaefff58e8d715237ca48dbc24624ab97d73780134b6abfa9397a3fb107c7847`  
		Last Modified: Tue, 18 Jul 2023 02:02:03 GMT  
		Size: 32.0 MB (31995451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3142716ff35072c411419b141a83ce524bc1af91e86195277f4ca49673988b19`  
		Last Modified: Tue, 18 Jul 2023 02:01:59 GMT  
		Size: 15.9 MB (15880046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5986d60cc2d030634cd4d91824fd3926b4c50f5ff1bed4d038671c930e6dc5`  
		Last Modified: Tue, 18 Jul 2023 02:02:28 GMT  
		Size: 49.5 MB (49515259 bytes)  
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
