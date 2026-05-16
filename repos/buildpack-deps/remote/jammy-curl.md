## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:db2dd7c665d240ada447bfa30c3bf3c39783a92189d39df02c0a4c4f688d5cab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7bc3d1a5c97bc74e93cc68bb8d7c1b812e3cf32abf355f3de2de6ea829f32339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36843417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb2e1d7910873af882bc500917212a845ba29c8c6966b3817219bfa2f5dec04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:342d87c72df94bf083d2c9dcb77b6059fae5ec46032fd5593dd48abb62cd52c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcbdf59ae830fc78b62d1d210092ec39c8253e309453ffda738da1ce897e3ee`

```dockerfile
```

-	Layers:
	-	`sha256:f1cd69aff7f3874908e5a7b3180c5d24fe90a7a1db2672d2225022710296258f`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 3.2 MB (3205219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f842958b55736e710a60122e447a453e7ed2972c7f4199568b78207db7476e95`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7a785880f4ffe59c79c6832fd217ceb9d327e1a7866cb45b893109acfe7bc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33852889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e2ef0b281f4e6f8328be50a7f4bdc34afd80954b5af1ba2a30f4c2a8ce8ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:37 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:37 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:41 GMT
ADD file:1699ef25ec41cfa214b8beff2f000963a775084d9ce11ff74fa817bb458c27c3 in / 
# Sat, 09 May 2026 04:51:41 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:422dc0f0ec960f769d890f368bdf0a0ba195325ef487f5b07a4d06efaa7b2c41`  
		Last Modified: Sat, 09 May 2026 05:25:04 GMT  
		Size: 26.8 MB (26841796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957e620b1e61061910c1027253dc62e684fcc45b084a25cee92e097c48ba1013`  
		Last Modified: Fri, 15 May 2026 21:11:02 GMT  
		Size: 7.0 MB (7011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a75ec30f60763e98fb75758a8530753de708b4093241636d69aecc84a3eaa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd14e1ed6900fa1bf0f3dafca0deaeeaf0d2ee1b1132b9789fb1ae8a550ab10`

```dockerfile
```

-	Layers:
	-	`sha256:63d0d0e02145d3e4deed0c22cfd29110a2877262d29e2eb7af95218d1563963f`  
		Last Modified: Fri, 15 May 2026 21:11:02 GMT  
		Size: 3.2 MB (3207526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb16472db5de724c66cc8a29a8d6ba314a5786b7f30e20c82c64725f45cd8dab`  
		Last Modified: Fri, 15 May 2026 21:11:02 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f83b19ab514ffa81dd24d94855e05c8c32bc38f4cd1c5d08aa0bc38a4974b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34668379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ab90dcbd51deb4e7ffdfe26f075c3f4cae341e25373f0187ff95c2a25591a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e527e2c82629e0e78660c24a3c982bd60e32a44a995766c42cdcf6498115f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51bc9341163da3b05b5a1ad2fd345ab4c7c33e7ff395502223c4d6ccc221964`

```dockerfile
```

-	Layers:
	-	`sha256:4e48e67357aa0a4d0fc9343825a29a9ab37de28d63ac21c14d8e3bde48f5d96f`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 3.2 MB (3205486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2429286c503836870d231b7cf9e5bc418d51915126d09fc76d14f8aa5c612fc`  
		Last Modified: Fri, 15 May 2026 21:11:06 GMT  
		Size: 7.0 KB (6961 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:46700a9f6ec620f191368ae6437edd3808fbe7dae023fe24ce72ebf79c5c0179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42834522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01c1630478a1afd3ca495bcf073a77dde3259a4fbc692e5943463d638291eb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df60d93ea7ba54145745adaeba4ff8f95b06acfd1fd21b54527b08b1549166`  
		Last Modified: Fri, 15 May 2026 21:10:26 GMT  
		Size: 8.2 MB (8187802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1569ab5a0cef9cc4fbd5b4ea3e2ae8a892e75d5fe52e6701443682f377e5bb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7d290fe87f93006d86536f86734dde1140eac45c5b3f0006a9e9e302e66408`

```dockerfile
```

-	Layers:
	-	`sha256:37200d5163fb118a45178736564678553b1b6e91878a95436aa56a760c415de8`  
		Last Modified: Fri, 15 May 2026 21:10:25 GMT  
		Size: 3.2 MB (3209855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e5096eeaf996ed5c55696db67041cae6972a0abf06733ef75933144309fd91`  
		Last Modified: Fri, 15 May 2026 21:10:25 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:90e78903570f0f5022ad5325e10d681438b01e927f307da8136bd91c4997bcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34358687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6105398a89eb786e16bd4baffdc346ef03df7671b440c1a9e3b464349f6491c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 10:46:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 10:46:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 10:46:31 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 10:47:09 GMT
ADD file:7ae2692e9ead2e53576d53cdb893209a70fe6f0a62ff35308c9fe5c855c10e94 in / 
# Fri, 10 Apr 2026 10:47:13 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:116177a8ef78c1de97a5262550388dc00d9881fcb4c367e06e4e52bbdb5a832b`  
		Last Modified: Fri, 10 Apr 2026 11:01:22 GMT  
		Size: 27.2 MB (27240349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ddabbfbd66006e6d36799950a3c7e93532654f0837cde6fe2521d8c52ee83`  
		Last Modified: Thu, 16 Apr 2026 16:41:28 GMT  
		Size: 7.1 MB (7118338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:836ab6a70af0f506d99fbc4dfb72ccd51ead4778e94ffd9824ac2e09c22b1fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71fd1b4c5ad5d4663be8f83f99983d1cf88e3638a0b56f0814470ac32cdff6a`

```dockerfile
```

-	Layers:
	-	`sha256:8e19fb94a996937db562e05519a70cd09975e47dfd67d77baa0d7dbb81c2d83f`  
		Last Modified: Thu, 16 Apr 2026 16:41:28 GMT  
		Size: 3.2 MB (3199103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9221f0915f26765af7215b424115a1350078ec074a080ae355d430045f864aa8`  
		Last Modified: Thu, 16 Apr 2026 16:41:27 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:10afa74aad9ba263ac6213f9ebf0e7920acc8701f71e829417b852d69540fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35222363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e47f35b113c4ae0af9e467ac1934668973572eaf5d8a57ea25eec3d4bee10ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78cbe544454213adb2a0a4ba71fd136f33191159e4da5a835e672c6cb14f90`  
		Last Modified: Fri, 15 May 2026 21:12:47 GMT  
		Size: 7.0 MB (7020058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe2ebe97778cd35f4f2cb86d19c18eadca865d5d8e166ac9a9a91f48d646a2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fbc368d87f0b0522ad164d5f674335ac9186f7a881d5cb2c7b276cf99441b0`

```dockerfile
```

-	Layers:
	-	`sha256:cf80db0e62c2b0c43712f24530803bd8cab50b8983288993a8ed9f9b8b59ef1b`  
		Last Modified: Fri, 15 May 2026 21:12:46 GMT  
		Size: 3.2 MB (3207436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bf254ff52da1105b1684da40b8d2f825e6c34352119d6e69dd0ffc36968348`  
		Last Modified: Fri, 15 May 2026 21:12:45 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json
