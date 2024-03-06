## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:2831cd7937395edd7784f7dd23f5626cf17a4902935e9390634a7da22ed155b4
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
$ docker pull buildpack-deps@sha256:fe5c79afc853edbd845ac127d00b186f7df5e3920803a2c5c81bbc469e42173e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92249142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b08e273d8129a14881605da6c8c29203a789693212c0cb0238cc100fc740fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:27735ee07214b2f855072fcd4e72b7ad7424f03fc6e9df5c952927a8fda5a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdee64687fff39f7a4891dd02e5902accecc0de732d5aee169f276d2af04cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:757d42c85cd3bd09dbc38423ed34374377c1efc3a38e7626658e179406ed28ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91339593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaa2591890de58ddef84aa2489d82a3d38063bce37ea4c0ea91fcf1d1770bd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ddf3e3c3a3f4a7084396c5fea9e867258a287407252e406f4a47f9c57c7e768`  
		Last Modified: Fri, 16 Feb 2024 04:50:22 GMT  
		Size: 29.6 MB (29634636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a510494515f4fe176171eb81a58eb13a7d968c4fd55af5da54ea2b1236d850`  
		Last Modified: Fri, 16 Feb 2024 04:50:20 GMT  
		Size: 13.5 MB (13520137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e7554008f9b077a355c6245831eea73ea7b69335b673b117960e3985c652e`  
		Last Modified: Fri, 16 Feb 2024 04:50:36 GMT  
		Size: 48.2 MB (48184820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4abfcbfcbd30feb2b4bfa41fc5fd1b18dc1b0e215977949d3c6a6302f99ef900
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102467463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb035723872aeb49e171babb083d8929637be280313d4c03325efabf9a82b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d6b9c2c0467950293584f6f5f629c50c9b3cbc2f92a09e9642c94a5e742bca72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95266671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10897081722df1674fa655ab9f9f4c99ec007dd87f1d4ae6286777eaddae0c9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:18 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:18 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:21 GMT
ADD file:27ce34bb2abcc5c87cb520dde020b5b78e467380c7f39dcbc302a6f97d8931cd in / 
# Mon, 12 Feb 2024 04:52:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 06:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:047ec5478b188533135ec377aa0ab10cdf96b713e04b75184116e3a8d0e7381a`  
		Last Modified: Fri, 16 Feb 2024 06:34:21 GMT  
		Size: 30.4 MB (30354582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1832ae29896eed72fb184b6254ce4a5f50c804274d01ce56a1c4ae345b45d78`  
		Last Modified: Fri, 16 Feb 2024 06:34:20 GMT  
		Size: 14.9 MB (14946997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404889b91c64925706ad61665db8c07a99ed919566a735134342d7542d1607f2`  
		Last Modified: Fri, 16 Feb 2024 06:34:34 GMT  
		Size: 50.0 MB (49965092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
