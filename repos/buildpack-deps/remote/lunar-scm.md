## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:3b66d545791a7f9331bc8d0ebb978b3925680bb027a90f51653ae0845bd59da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:692d3bda1ca2799b9e43fa06e0b51c86e04ca39de9dcd0a2f297253e055d447c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85710010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489541e75a66b056ee66d97243ec55a2b921d22ae0f60d9e9cd90c825c943b9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:32:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6c6b907db42b6f1b03645d7cd822afa676930182719410e133c9480fede45d4`  
		Last Modified: Wed, 03 May 2023 16:46:32 GMT  
		Size: 27.6 MB (27604112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f85888a90c2a34e30a0c0a9b5fa2d5ec19c9a0971bfdc5c58bad2d07f8c1f`  
		Last Modified: Wed, 17 May 2023 00:42:36 GMT  
		Size: 13.8 MB (13759710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043c1ec00223b167bdf23169d30a48d98f804fc2b3546698981778d404597fa`  
		Last Modified: Wed, 17 May 2023 00:42:50 GMT  
		Size: 44.3 MB (44346188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5748352869b2434ac973efe672183fe843a75f27fcf28133fcb620bb58355f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86803019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8c64e3f8d64c7bbe50aa1caa0163b283e1a7553b418052bb5db06b97c745b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:14:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8f976bcf9a33d090294b25c3fb3430a5833ce92be9f477471addb457c0dc3ac`  
		Last Modified: Wed, 03 May 2023 22:12:58 GMT  
		Size: 25.4 MB (25437887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839eae4aef603ba497d98c83948abc648ed6b000c1d03761b5a774a82f143027`  
		Last Modified: Wed, 17 May 2023 00:26:45 GMT  
		Size: 12.7 MB (12674206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10f2c8c8922fc227111c1003aa483d4fe5d8002ff1f064d1e538e83221d5e86`  
		Last Modified: Wed, 17 May 2023 00:27:03 GMT  
		Size: 48.7 MB (48690926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e3d62086cb295abcc7a6411e6e5530e28e571be4459477586a99ee8b8db975d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84561257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88425b0182105a165f059adb1fc4af6629cca0f08c46b1eb24c070ba5e9a530`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eedec38ef10e1ff872f423ceae12828c5413c8183c216098c34342de77e9e5a3`  
		Last Modified: Wed, 03 May 2023 17:40:37 GMT  
		Size: 27.0 MB (27017867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b19b0b741f1c54f6a360843f1321028128af5d283a1d8f0f5f66bf8beece0a`  
		Last Modified: Tue, 16 May 2023 23:58:57 GMT  
		Size: 13.3 MB (13349536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ede9cbd1d38078a543a2cb21cdb02b9aad695324d7f312340903eed543424da`  
		Last Modified: Tue, 16 May 2023 23:59:11 GMT  
		Size: 44.2 MB (44193854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b298b17eb0ab624162bb4bf11f355ecaaf49d61a6f4ed34631c8a14aeff44184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96892691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5929e4298922b5ef954943aa4598fa77641f4652c7ff3edf8db7c6e1f9e6c43c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:35:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff954998e64505d58ea7cf2bf1a248c9fdc2287c6f6c0f41d3268aa8df574bb`  
		Last Modified: Wed, 03 May 2023 23:42:18 GMT  
		Size: 32.0 MB (31996798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa53d052871f8af1d008e844405fcfee71156e0db99a5f455da388792a32a6`  
		Last Modified: Wed, 17 May 2023 00:52:48 GMT  
		Size: 15.9 MB (15852506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ed1430a2c25c67e1f64d2bd3eaf6caf8695cc10f292170852d6040aa9c4818`  
		Last Modified: Wed, 17 May 2023 00:53:10 GMT  
		Size: 49.0 MB (49043387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:13d466e828964bc26a839bce9d6af7b5be86424794138cfb58cf68de1e44730a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84476595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06548fc41aa53dfdcbacd2708258bdb45a5e9d327b2c27f456638a6c6b26f7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e12ee780e94e13677b8efd3cfc5219f323ee331fab05eb1f1c59218a106122b`  
		Last Modified: Wed, 03 May 2023 22:34:25 GMT  
		Size: 26.2 MB (26236160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc738121c9813521fa4a0fca88e02cb1f66ef200380dff38dd077ab483e2c4b`  
		Last Modified: Tue, 16 May 2023 23:57:26 GMT  
		Size: 14.0 MB (14017600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b0c0328488d708fd92c4400fc82d0ff82947be475b2cec1e956ce34dcb9057`  
		Last Modified: Tue, 16 May 2023 23:57:37 GMT  
		Size: 44.2 MB (44222835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
