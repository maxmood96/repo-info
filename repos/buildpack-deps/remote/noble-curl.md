## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:7907c3085d9754feafccd77db7e8a27b693dfb43c998dfe1b29cb90cb94565fe
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
$ docker pull buildpack-deps@sha256:ee6619518234d5405ba8f94421cf0080c2c2e5951fe4e4b94bf2e6b5ef53dd93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44007564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e663bb54ee5c1f72bf54c4d90d616ceea2a986638d02a9ac69f807c6725c956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
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
$ docker pull buildpack-deps@sha256:1a3525c19b4f6e3ec470584da100af08a4cc90e81c46fd9f96fa2120689c22c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45449176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88c57696396911c2c93788e10f30a9ba39aaac13d5a7820d336de3ba6350a79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f8b3814528d1a4f48050c53a434c342d156d2c17e42c4995b43378d312b9a0d`  
		Last Modified: Tue, 16 Apr 2024 01:38:44 GMT  
		Size: 29.7 MB (29730630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7301652c4369a1a4573103c28643b88888a84fa00e1a3d3502ff8a7254d2ba7`  
		Last Modified: Tue, 16 Apr 2024 01:38:41 GMT  
		Size: 15.7 MB (15718546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
