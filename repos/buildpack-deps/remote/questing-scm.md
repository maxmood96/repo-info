## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:1adf07c01e3b0b6ec54d9f9fa430e85d71fccff3ea10f5496490f14421967588
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4562a10c54d9ad7003b35faef17b37b06e4e3b71a54223dc1b3c948ccdc9caec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96189274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9394f5b3fe876da424a1b4181c75bc282aba398e634e229f0193a3b2368602f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:a74a840d4eedf15a85cf6d55ff2e2efce2562bb735481008b7b05feab3e31a41 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17bdd67b6aa5856e02c1b36cec4ec29df1dacb071c5f6279c9aea0a311ee1058`  
		Last Modified: Sat, 16 Aug 2025 00:41:51 GMT  
		Size: 29.7 MB (29740502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79c5851a446b3b5b175c8d0ac3f08bbee9078a0b4863c6e57fefddd86b32c0`  
		Last Modified: Sat, 16 Aug 2025 00:49:30 GMT  
		Size: 18.9 MB (18862801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837b1c4b03ec273ca0621a1a2eee5af08d62b0e1a1b7d7d4784d47d5b54b769b`  
		Last Modified: Sat, 16 Aug 2025 01:08:49 GMT  
		Size: 47.6 MB (47585971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0dfe6f864b237ed0728d18eeb09c0e03f57fee45f74052be2abb85ff64039710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f307eefbb7827788b871c36a5a22992fbc09e07eef2edab3e1988e91aec9f0d`

```dockerfile
```

-	Layers:
	-	`sha256:9f0c2aff8e55002b5a23ac0b4855dfea1490e4aa62e2dfcaa1bc0fa81ae11b6c`  
		Last Modified: Sat, 16 Aug 2025 04:20:10 GMT  
		Size: 5.4 MB (5434497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5cd706b25c395cf8d96fb20e605cd56f07c491dc4e710c97dc33b69647c46d`  
		Last Modified: Sat, 16 Aug 2025 04:20:11 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d7dbcac0bce5645f4332b14c5cc5f8dcde008cc057d3376e5e91e1ff6ebbe2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95383381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092401eaad31e87381659e78f62fbb2ecbea41f5eb007d601a48e711de523df3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:6cceeaa1e4c04b40ea2fa59915877179d13dfe75963b2bf5af2d179b7651fcab in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5fdf70baf2d69a62d712c5290da1eadd264d65ac840f33b44cab7084448ac925`  
		Last Modified: Sat, 16 Aug 2025 01:48:56 GMT  
		Size: 27.8 MB (27766578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f5f8859e7c63a9c160d8e856742d21c1c5cd88e9979620c98d02e7400a78d1`  
		Last Modified: Sat, 16 Aug 2025 02:09:43 GMT  
		Size: 17.3 MB (17259103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b0ed35808f1a066354a407ef01e08a829b491ab11dc1374245f9a9fe35239f`  
		Last Modified: Sat, 16 Aug 2025 03:09:34 GMT  
		Size: 50.4 MB (50357700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d99208e3c1e5b45aa66bab165191e3abf1144bd54981cf77f85b89b24ad0c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4cbf9526d0cf2a2d31e85dcb171180a5e0e49b50ca105523322dad48f2c897`

```dockerfile
```

-	Layers:
	-	`sha256:b8763f9bd098dcd4a461da832621d5382ab6cf12dc0c84397f6cfd233e35fef6`  
		Last Modified: Sat, 16 Aug 2025 04:20:16 GMT  
		Size: 5.4 MB (5434993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e5627166b2422513e58d5e640373f058cc8180dff748dba4bd1ab4b58c277a`  
		Last Modified: Sat, 16 Aug 2025 04:20:17 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4cee150f8e6d60955b009f6ef44bfd4db91f2f329f690d83fb5c6112261a1061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95014659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50730012c5386ed4d35afe6014915a6f20ebcb15c4f6aa55e39cbd8715ccff03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:b572189ec957414802fcdd31718df41b6aa37b1788b72c0b4276113a05ca3847 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1303c7d3dea2855daef53d0a8f3ec020cf348b429dc95ae8653a86d0d8b8ed`  
		Last Modified: Sat, 16 Aug 2025 01:38:38 GMT  
		Size: 29.3 MB (29310925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97eb8f278e435c853098d1ffa029d384d7ea69f796411aa8cddffc825cdaae`  
		Last Modified: Sat, 16 Aug 2025 02:09:42 GMT  
		Size: 18.4 MB (18384161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd834fb11e0a39629f2517d7a2504b48ab7ea76e3adbed4e69a2970486f0d7c`  
		Last Modified: Sat, 16 Aug 2025 03:09:59 GMT  
		Size: 47.3 MB (47319573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b65cbd760fc5e19492af933d18a14f3f32e68ae8d67faea074143e0a53462ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6029ecb653b56fd34ea7e4043710d85d2664d8671e8d300bab6211cf98bf94f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a65886f126fb8a63e359ea9fe569a9cd6a79f3c2057f6b65b685be07a268dca`  
		Last Modified: Sat, 16 Aug 2025 04:20:22 GMT  
		Size: 5.4 MB (5440884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fbbebcdf79e5b163fa0e965f4a0331309dffbf213603f062efcf183d73f0d0b`  
		Last Modified: Sat, 16 Aug 2025 04:20:22 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:acb5173bde33b5aa95ba8ae32862f52ebeeb38d3803f38bfbabb8470f36bece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107867248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c05f8109585df3a15887657cca96c2d7fe53f566fe3902d7c833f63d99bc1b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:9ee944b262d08273ebeed7c7e10331931448ce12dbbf68a399e8c06bef0d9b1b in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c17919b40786dbdd1b0e57e5e0f6254429096c2a4edd2c2d1abb619a9860b100`  
		Last Modified: Sat, 16 Aug 2025 01:52:43 GMT  
		Size: 34.2 MB (34171496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cee2a7f9203ea1c35edf02b23466082a11ceb072dbbb218de698867c4cd518`  
		Last Modified: Sat, 16 Aug 2025 02:14:52 GMT  
		Size: 20.7 MB (20745793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e6e139026a2451641d9dd89313b21889f2928a9873bae1650f841fb688f4f`  
		Last Modified: Sat, 16 Aug 2025 03:10:37 GMT  
		Size: 52.9 MB (52949959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:56b9d1240b127ea2ee0d0930a052591e791bfaebff77c150e0304d12acd5beac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5801ee8375608c326ff849c13ee82890dcac898dc2f98cdde4589b01111d32`

```dockerfile
```

-	Layers:
	-	`sha256:c63c8a5707a8a85400bdaff735010989ae46d01938156f27a891d10a0358f273`  
		Last Modified: Sat, 16 Aug 2025 04:20:27 GMT  
		Size: 5.4 MB (5441555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154e772195955555c7adff519ca8203248bbb6f8c5162981c4494499dafd8193`  
		Last Modified: Sat, 16 Aug 2025 04:20:28 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8d88b6b499c665705483537e918b09f0cff9124e194c3d6b38f92dd82e5a2791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99503961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a626de9da9246855d6287a12fd00c62cbf1ebecef3ab020fbc21e0e22f0ba06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:5d7fc1c7ab0341c0edd5218b95f2477fe713c704c0bfd784afe2ecc5f63cbe37 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d323ed134b3da3f8123622d5cd2d3cec4a1c728577e76ebc6912f3735a9864b`  
		Last Modified: Sat, 16 Aug 2025 04:58:48 GMT  
		Size: 29.7 MB (29651850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c69c954dcf306c929945b1d30400512da9d95a60defbb5ae061ed32651efa`  
		Last Modified: Sat, 16 Aug 2025 05:12:35 GMT  
		Size: 20.9 MB (20949164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ece2a3cf86e85414183f79d9f7d1e6a9dbaebe0b93e05f6abedcc3de4b81557`  
		Last Modified: Sat, 16 Aug 2025 06:09:35 GMT  
		Size: 48.9 MB (48902947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f0c4b1be06e04d19f69edc73ab7d4ea81fbd526be6b7ce7f00449870cc8c976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4789dc653d7aaa481b8977e11ebefe56b0c25c9637b0324dda0f68ec3bf6f81`

```dockerfile
```

-	Layers:
	-	`sha256:09bf200fe402b7e99a5b6725cffc1eaa5f21958d1c01a07f8c2b4c6dcaf30321`  
		Last Modified: Sat, 16 Aug 2025 07:20:16 GMT  
		Size: 5.4 MB (5436035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23c4459d03c974c4cd519ec13ad4a182b5fbb4633d30144b6942a56824afceb`  
		Last Modified: Sat, 16 Aug 2025 07:20:16 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
