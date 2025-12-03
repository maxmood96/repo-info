## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:16009714ec126619019671239456aa29435d7005c96c9411e527db313922a2a4
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

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53829124c3354615baa0ce31bef4f58b8a0da8cf764183a0d78fbd238a3d7e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b109c7bc3868b0a339173890733dea15caa0bc1621b0606ebbcf0ec5aaf4eb7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:28:38 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:28:41 GMT
ADD file:55d8d7c2a599eebdadf029d609185a93b70e5c572fbf864d8e1dea8ca32c7e8a in / 
# Sun, 30 Nov 2025 03:28:41 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1cebba4171ff5f2efb3092f20bb54ba4f8853e67ae7ba36b66c426fd17d4b4`  
		Last Modified: Tue, 02 Dec 2025 21:29:21 GMT  
		Size: 33.8 MB (33763754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db10505684265b8f15b7389af79a333e81deff06c492e0c86a76684ac37bc564`  
		Last Modified: Tue, 02 Dec 2025 22:11:39 GMT  
		Size: 19.4 MB (19408148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:58a4e052539da57adbcb7627968c875f5553b9e4ab2caec2500ad174d0416a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2955677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5528abe792c2e15d30bfa779391654edefc021599a4fdec91ea464bab39912`

```dockerfile
```

-	Layers:
	-	`sha256:fed97198a65fd3842f368d0b7f89a514fbdc7633cab15b01acc7b0086077d546`  
		Last Modified: Tue, 02 Dec 2025 23:19:49 GMT  
		Size: 2.9 MB (2948742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1474deb2aaab422fad136de1d6a4d889aee4bba26c29e5b050cedfbf6edb1f25`  
		Last Modified: Tue, 02 Dec 2025 23:19:50 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:189bf05ea6e44849526f0404d0b3338b8ffde256fe6ef434210da5e03332c2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbf92840b267a82b9b1fc6dc55fd69dce31b870f9fe9cacb05c5866aeddfdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:31:00 GMT
ADD file:9003dc9541ce76045dd67f0ad2d95c2697e3b7155bc6abaa06ebbf38b78aa407 in / 
# Sun, 30 Nov 2025 03:31:00 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd71ce16db91fba8d9cd0435979699051c3f118fd7c402d7cbdc6eb32d240426`  
		Last Modified: Tue, 02 Dec 2025 21:30:00 GMT  
		Size: 31.1 MB (31147436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d15adde59bf29b7e8735e2ca69fe70d44a2559de9882a34bf8c8ed08114a7`  
		Last Modified: Tue, 02 Dec 2025 22:11:34 GMT  
		Size: 17.8 MB (17756410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:142fd8d56c79c2b659f9c6ac1fdf838a483a70e1779c35709196ecca0c597efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91bf3c61c61c7351468c2ed5eaeb868be507aefc3777ef7accb539ea4b9162`

```dockerfile
```

-	Layers:
	-	`sha256:3258da16d998962aefadae6f03ea6dacc814e1a33a9d59647137cb4a695cad60`  
		Last Modified: Tue, 02 Dec 2025 23:19:54 GMT  
		Size: 3.0 MB (2950244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d54ff88251bd4b781bacd1fc8ae840ecba24a4a26cb89f1f5a065f8f37c969e`  
		Last Modified: Tue, 02 Dec 2025 23:19:55 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d3d4a97849a75036dade9b603fa7fea12d66aa84fa0a46f4bc1b05513f345838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52265401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d30f3b6081310bd4fd22085fc3c6b6ac2f2b89603d32a75ddf9da6cdc538bb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:15 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:16 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:30:19 GMT
ADD file:980aeef211cdc1dc441eea6aa6e600765d2ad909294a70a9dfc54b86b8acb82c in / 
# Sun, 30 Nov 2025 03:30:19 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a3b546ef13e5307a10c1657c5a408cce9d7fd8da967afbb8383018e2b2c2a8ed`  
		Last Modified: Tue, 02 Dec 2025 21:29:59 GMT  
		Size: 33.3 MB (33301426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67396e94407424cf9bf12089c47b3de0191e9811df778f7c7d577a0ce4e2d3fa`  
		Last Modified: Tue, 02 Dec 2025 22:11:49 GMT  
		Size: 19.0 MB (18963975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d8894336f433232d4d379d1763cc13e66b7d3b5c6db534992f61967a314f26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abf6c34bf9021703befdb4db9967727558e7d3ab34518fc123ef6e849746477`

```dockerfile
```

-	Layers:
	-	`sha256:24c72b56e7eaf118df644e989365768d2b0d311e95fcf65aea5e620025431836`  
		Last Modified: Tue, 02 Dec 2025 23:19:59 GMT  
		Size: 2.9 MB (2949000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801314cd8c8db83bfecda32eb4ca99908758d2f845a89a9c39440042b60e3f36`  
		Last Modified: Tue, 02 Dec 2025 23:20:00 GMT  
		Size: 7.0 KB (7015 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:50f9727935641881b40265e5f4e7352a83dea7241f4ed47bde435c74b4eb2813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60636514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4a974c2c4156b98ce0c8ebff49d16d47a6cf209ba73cc934815bf44f91257b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:41 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:41 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:30:45 GMT
ADD file:872eae4a5b1a2d784c6000bfa0340820ef8d8fc0223e8fca3b6b238401dce6d9 in / 
# Sun, 30 Nov 2025 03:30:46 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 05:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:85a46f829ef72b57840ae44da74a41c2e782285d586199aa2f8db34731cd5cfc`  
		Last Modified: Wed, 03 Dec 2025 04:19:29 GMT  
		Size: 38.8 MB (38792345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cf61dac70d00a6d6ab793db795e5dd163b9463a26f9c9b742e77e254c3543`  
		Last Modified: Wed, 03 Dec 2025 05:11:14 GMT  
		Size: 21.8 MB (21844169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d6a47609a74a7bf672336f96a660a1dc8382de8c0296dfefb27b1808a59550f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f426ef356fa2ded7a4de65a6083ecdd43ff5b83aceb52fa46eda04cb1865ab`

```dockerfile
```

-	Layers:
	-	`sha256:665838c344bcb7cd5049f103d0d017d14fc13be7959685759a095f9ba7c1036c`  
		Last Modified: Wed, 03 Dec 2025 08:19:49 GMT  
		Size: 3.0 MB (2952565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84f54ba1ff7fe73d0539ffc36f40539ac383321f47b31a262e6f243cd6faa63`  
		Last Modified: Wed, 03 Dec 2025 08:19:50 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a94ba1ed0460d5205223748674ff971f019765f6f9cd2d2f00e53eaba3940231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53262897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4941d714eaa214bae6a5b23f48254f99d4f8b48bdec5ea33c23fed3510d78d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:41:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:41:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:41:57 GMT
ADD file:f463f77192f170ee64673f5278f91bdada45dc922d8fd7d4131d154fe01a4fec in / 
# Sun, 30 Nov 2025 03:41:57 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf3c1d5ff4ce09e68a22f9e6e4bbc83188de5c366e0945d8cc5e8dc699355c91`  
		Last Modified: Tue, 02 Dec 2025 21:28:26 GMT  
		Size: 33.4 MB (33395368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df4f0b4855de3fe403ca5d6b658f6b8866dffa556bc1fe856875a56977e649`  
		Last Modified: Tue, 02 Dec 2025 22:12:00 GMT  
		Size: 19.9 MB (19867529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3414d20d60b871b743cf3a453ee10129be4614f92a883edcda2960d2c50acc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f29708ffa69ddcb1cb9ea73f61ab1d7792572b60c23b0dcb44a374e711b837`

```dockerfile
```

-	Layers:
	-	`sha256:4b55e8f475946eabff9e0f2b171e248351169912a585d0a25ce1cbd84d1ad7a3`  
		Last Modified: Tue, 02 Dec 2025 23:20:08 GMT  
		Size: 3.0 MB (2950773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc064d07e2341ff9882952b7a89e764fedfecc0aef895a95a2ca6fff36274011`  
		Last Modified: Tue, 02 Dec 2025 23:20:11 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
