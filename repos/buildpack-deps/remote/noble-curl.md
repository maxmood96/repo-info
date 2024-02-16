## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:a20b2bdc2290d9c196b723981370a8d6ff7212b3ef7756091e0ca05b22434740
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
$ docker pull buildpack-deps@sha256:cc36a047bedb9cc2d55e5df5c556fea75120543f367636d278c86916503d230f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40634194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185cd3292d981b14a4a9da76e47837fc33c43a4f484df3f411d01accdf05ea73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
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
