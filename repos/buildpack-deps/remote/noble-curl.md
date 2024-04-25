## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:4e2ef35e2a8ecb89fa1bd81d9c17deb4041d625762babc270d859ccd36f3ce84
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
$ docker pull buildpack-deps@sha256:7c3afde1c0e6d014d19fa9b24c5ab5f398730e4697161c2c01190ffd008103cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44005749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136a4aae8506c9ab06db7f10e2b05af87a26c2e754e5f0758a897cfd8c4a8f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5a56530bedea1e0d0c3af3a5d51302f8a7fce497730935921aedc0d30011e`  
		Last Modified: Tue, 16 Apr 2024 03:55:33 GMT  
		Size: 14.3 MB (14299672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ada6bed016d627d35a8ba92ab3342c7dea17d4e386d7167f1fd89a0d9c43fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40264623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139b266328beb8ec86a8f8723f3090098ca2a741f21e58b51b1e49189f863a1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:742a70fdca3d3756e5061f666dde28e7d0a1ba3f3b1b354533743ee38dc188ba`  
		Last Modified: Tue, 16 Apr 2024 02:34:43 GMT  
		Size: 26.9 MB (26941976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cca02843e48d71776b41937e0fd4bf0048507a82e5f363b1d56426b0ded0fd0`  
		Last Modified: Tue, 16 Apr 2024 02:34:41 GMT  
		Size: 13.3 MB (13322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:275f5c5ead5c7ef26ab28a0e7be2358e7ce9eddc80917292673d04ab9a81087d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43144326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f996753ad8c60d6a329cc1e64e8d4a6cacf67b0b87a8e00de9be69e727f7bbd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:210ca002167c3d3a57ad40d06950b6c35055e0f7239ae4a703e86b87f07b7036`  
		Last Modified: Tue, 16 Apr 2024 02:13:06 GMT  
		Size: 29.0 MB (29012773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968c2f4b081a4aee9cd23fc0fc6ed4d4b1355e00c92bcc674f2af81de39846`  
		Last Modified: Tue, 16 Apr 2024 02:13:03 GMT  
		Size: 14.1 MB (14131553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f27e7397f6215e44bac04ded0e89aa69aafba5a4f98efd19e4cc68680d8d2755
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51400158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdae6af20f89e77e9e09d980f92d0d2edd7c3a2e2c933b8e436ef0a482467dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:22:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5717fdb2c5cf6da9438e6e5f41f3cd785febcd2ef3fe59322b2a98bcde0cb94`  
		Last Modified: Tue, 16 Apr 2024 03:34:09 GMT  
		Size: 34.5 MB (34533211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d45733594feda8ec2c8c83b6a7581c528c52f1b682b06b5b676ca990ffab62`  
		Last Modified: Tue, 16 Apr 2024 03:34:02 GMT  
		Size: 16.9 MB (16866947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc831779fb6c27980929aa714f8504f0d9aeb5817683169eee2f40fe529c995d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45501157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fc8603d4bea81767f2180730bc8cf2fccc42f29e89928746e2b4523153a8d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:59 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:01:01 GMT
ADD file:a8f6a75bd4e0f37e8479b0e5c1fd1ab287398559996948607323ac5831f29411 in / 
# Tue, 23 Apr 2024 22:01:01 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09891c72d44d843dec0981794f145f31192710104498499b3283205e955a4699`  
		Last Modified: Thu, 25 Apr 2024 21:00:21 GMT  
		Size: 29.8 MB (29781724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2975750ba9fad7e23fa7d0af87613454caf33ef321c9ac49fa93bf1d2bfe84a`  
		Last Modified: Thu, 25 Apr 2024 21:00:19 GMT  
		Size: 15.7 MB (15719433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
