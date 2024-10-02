## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:9a6b2c87e868774dc2360c45a1f43f9f8d2a53f2ca7ab02272f976cc82e538b9
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
$ docker pull buildpack-deps@sha256:5ca2897281b063ee5aee00397d461cd1c5fc63a7385b596758176a2d8c37c369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46628635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0999cd855bf065bf57ef39f3fc4175a91e117a598a2cd9acfb4622289c560f77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7378fd8b9079c627cbf64e65e2cc05f4434545bbee435a0392ce6e61d3173d11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42292534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106e99ee95aefcfa2630c3d9ba65a826d8685c1c826d3d3dc2c3175b9b81aa9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
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
$ docker pull buildpack-deps@sha256:ad6152b94fdc26d3243e31944ad6bf88f2fe0e2bc487a198202cc02a68b1d1e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8850ca23b16189c702035ca8031796c2fd0330fa6314e0a1a29dc8af2004306`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a3718ec79f151ea424a0e2237cd6e1074348ed31dbc2fd83ada601b1997e0111
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48372793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb46e4e0a703fd6d8d1d23976dfd0072e7242a7b3fb99daf90da3d103a2d7ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:00ba728c2bdaa3c28520c2f2f3e309ace3751a0d290526d178071175db6debec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47734264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2bd27d12d23454fcb655a1b0d44b1033f1ac6ee97c980f48820646bbfd18c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
