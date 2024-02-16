## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:9d6f0736498d17ca3578a7d5d9f281e41a2625b61946d8f8f27bb26a9afc2cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:56ffc00ae277d7d43a3616cb6d583a8106f024bf1c30b424ed226bad3b982ae6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44110493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e864e112b75cb0ac68713a0ba92005fa72fb0b6175327b838ca78a95ff2869`
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

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dba95bd984877ea6e48f0eff2327f50d4d1e6013feb4f21b3926c15d1a99b7cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40615828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb78bca00fe6d0b69776790a4569488e0500036dd6ce6b633fdcbe7ee71cc5fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:59 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:59 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:53:02 GMT
ADD file:678218a331e2b831edef68fd454337cb55ed29bb64454ff990a67583493e06fa in / 
# Mon, 12 Feb 2024 04:53:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d82b6d605223cf339149712324b60bc99eb59175bb4d477ffb0fcc34cc97d78`  
		Last Modified: Fri, 16 Feb 2024 07:38:30 GMT  
		Size: 27.6 MB (27566827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860140fea4cdc3e53205a34786b066013a5e82411569c57836e8dcf0f8cfefcf`  
		Last Modified: Fri, 16 Feb 2024 07:38:28 GMT  
		Size: 13.0 MB (13049001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:de14136529f72ed63d43b118fc700fe91f6610071051085c93648c832d1ebd52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43154773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2144bd656086946d08b230b7081ca06e60125b7105e45ce3ad44b9afbff40b12`
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

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eea8c4ccc133de97051f1dd617ce721a14ae172410e189302eeda81dfbefcec4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51258411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba4c7cb1b8213ee23bf1900b4507236bccd3d9e877067bfc27c4cecf6dfb944`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f99e65953eb4c26f66aa6a038cad2127b130e0857531898f0345de4a7c7c967`  
		Last Modified: Fri, 16 Feb 2024 04:14:18 GMT  
		Size: 35.2 MB (35220719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85838c27b62b5d20ff7b908b2b786d1db23180ebd001f5af468413763f01c9c0`  
		Last Modified: Fri, 16 Feb 2024 04:14:12 GMT  
		Size: 16.0 MB (16037692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:88249b29234b01748c7c32377108e130a7bdf18e23eeb9e4fa201e924e9f9419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62482c207e5972a36cfd7c128da5fb0f72f707546c8a49c0bc8864dd03615228`
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
