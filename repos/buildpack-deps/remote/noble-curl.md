## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:0c43ab2c7a0b1f5e69de53aa86bec4704e7fe2dc763d137af43a2270e60b9a2e
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
$ docker pull buildpack-deps@sha256:63858212a20ecf00abee87b6ef9323f4d9d08cb79619371fa0405f67f8eea5bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44143640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2f9c984fc3fe28b7f925bf53d5fb763199bbe2d520448ef4a2004034f9d9e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3fa374d78d6bc1d2cab1e56e050fad206b983d08dd4d05ce017af22c2bb25`  
		Last Modified: Wed, 22 May 2024 23:41:29 GMT  
		Size: 14.4 MB (14441188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:95473b4b84a9ecb58b5f00999164d858b82f209123c313edc3d59ccc17459e12
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40450749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7c54d27f963db7485deaf9d0b0e69078d4395ee7839f208c22b2c3b5dce577`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5898831ca500b9ce4b3ea7cc0a8d9e25e780822eaaa8ad9ffdd70822a7ea67dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43310842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12613c1aaef9307fad8b276fb4bb50a97483461e28825601f1e11a7f88d32fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2afb81653918fa9a91fa586df7601ad7b3319bbca1de65beb077f68feedada9`  
		Last Modified: Wed, 22 May 2024 23:27:43 GMT  
		Size: 14.3 MB (14272172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8427bfb305d7e972fd03e0fc0f799d537170330fa53f119a34b8452e0af5962c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51616381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c7168c2d96a978da33b4a6a45abd17e6f7b5470e186819b7272308b416ad74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0aded05b0749fd5bcf1b632be0ccb7a071c0a03403fe5e218e80cad3030d97f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8702617203377c2d995dd6ddf3bcc5b3af6717281b550a5e33ec66ac1eacf3ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
