## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:00ce9a522e9b96a06cf9c62ed5f886a086452de5fbe729817b22742d97ba27aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2b5869019aea04face8fc1f58ac6e34aad6762c57822fd818b69b060bd4fc7ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44228657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be742ffca4dd43a363aac7275ebf6e97ac5547ed6bda6766fc42e2070e2b249b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc06581ba83c96551e72333478cabe2e3f3e5b95cc6392e1fc088a018c0603`  
		Last Modified: Wed, 02 Oct 2024 02:11:46 GMT  
		Size: 13.6 MB (13617177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eec735e64d7c2150361d844efc23d07624aa56d1a543ca65bf2fc0f9f675b905
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40506514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37404394553903d1b91235398803dd2638432faec207dfee4ba58a7fb09f956`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48dc96ecc6bf69394a6ca52e669cf9d96651adc2fb8de10ea974949a523c3d2`  
		Last Modified: Wed, 02 Oct 2024 01:43:45 GMT  
		Size: 12.8 MB (12774670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e020fee9857b1e24261121e651e2df6156cf76e644e80fb574a4ffc798975a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43405548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b9fe779bce78d95b027b243263b191a3715452165d409c2e1b55fbd47f6528`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eae46c940ffbdc3ac168d6be819cfc19265a43cbbc5748d4bd943f6cfac7ad19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51508806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640e48b20c33f7e1ca056bef068e19aa228353229d915df3c63db96930181b67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:43:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755b52026890c7d432ea6809a1dbb16551ef51fb0b3230bd4bcc77073fff0216`  
		Last Modified: Wed, 02 Oct 2024 01:55:39 GMT  
		Size: 16.0 MB (15990884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:96cca7615cf23168ee927a322ae7d73794d18881edcfaed32a1ecfc82b2bab1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46266072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb9816d3133f9b56df724c02667b50d24d340ed5af45ab422f3ac06a48bf4ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1277e7ab7cd99daec7af1eb3449da0c42fd16778b5e9235a082b3121e4658538`  
		Last Modified: Wed, 02 Oct 2024 02:12:11 GMT  
		Size: 31.9 MB (31945206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6bbfbdb5336912dc7b18069e51e022c68d4491d074d547d4821195766ff6b`  
		Last Modified: Wed, 02 Oct 2024 02:11:59 GMT  
		Size: 14.3 MB (14320866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb95a5db87c595c9980d507e5524a0725155d84f11fdc1a9d79ca26ff3c691a1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45641304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe721fbe62ad193a72dce2096351fc2462cd3129a3257456d227bb4914b5df3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ee2c110cbb81b2fbf7f2ba4af5cca380a129266db2e134961ac4be8f82851`  
		Last Modified: Wed, 02 Oct 2024 01:39:31 GMT  
		Size: 15.0 MB (14975862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
