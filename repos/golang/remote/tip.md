## `golang:tip`

```console
$ docker pull golang@sha256:fe67281a7210065dedaa25e96f9cf90b34cd432d8c4ec84409549aea5b133442
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:47cdb594bc235c76630b6241f590f524d4a3ccac0d9db3b41a9e85a33b9712c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342481451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b103c5aa243182fa1a0bbf898f957dd29ec3dadba3c66baf5f437ebca431e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:18:15 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:18:15 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:15 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:18:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:18:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ea4c649f3309364982563a9d872a4eb0e0ede2653c1c9450d1295d9d3e9a90`  
		Last Modified: Fri, 08 May 2026 22:18:47 GMT  
		Size: 102.2 MB (102227854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d96c16acc57376a8754a417b68e92c70474d0352b2593c49f87c63da03c328`  
		Last Modified: Fri, 08 May 2026 22:18:43 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d4385ce90f5844812271a3a71f6bb3278acfcff7dcfbd02189ec16ebf8a5c046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef69710cff6b61276ce6733ae514395839055f2d492cdeab6bf92c5d1f2489e9`

```dockerfile
```

-	Layers:
	-	`sha256:e0f512ac909597cee8b28982b8e2887e7a0e488a4098768a3ad66f6d30cd5255`  
		Last Modified: Fri, 08 May 2026 22:18:44 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af793c13e3c37409ea5d4f41d9f60217b839c3afa8469a7079e431bf9223bab`  
		Last Modified: Fri, 08 May 2026 22:18:43 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:6a05de06eafb3cb289d5f3e9a414e9cf5075a89676d1f5740cf29aa0acfc33e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298349077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9f7ee4c0db761320bf86313c8a9e742b0f8083f82e7a4193c0138827b0cf09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:01:00 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 23:01:00 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 23:01:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 23:01:00 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 23:01:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 23:01:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94e406ee28014389b6280983ee1bfe112e4cdcc9e6374f9ccb84bbc17749af7`  
		Last Modified: Fri, 08 May 2026 22:14:14 GMT  
		Size: 72.9 MB (72867024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba2326a71c6e75a9069eadf789196742e3d656e68c9263828f65590b07627a4`  
		Last Modified: Fri, 08 May 2026 23:01:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:13d0495180f6f25d189f542981dfe4e739650fc94b9cfd9ed47a485b94db3b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4e2c32bb74659c2736c16a2221e602ffb88f0304b1bcd43a5c2763947b4b68`

```dockerfile
```

-	Layers:
	-	`sha256:637109bbcfb94ba8f8d1afa9966794ddb480d2893c4d666220de9af210dc96e7`  
		Last Modified: Fri, 08 May 2026 23:01:30 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45514d7211444ad3f5dac8f929f4cd2186ea35a47b5abcb9540933279e5d6215`  
		Last Modified: Fri, 08 May 2026 23:01:30 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d47a8f8a58804eda1ddb0108555a06c2928a130a7caa1c9aeb01f277b97b985e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332900099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b120201d017077a988e20655b7db42a3e3389c1e5f6f6230916053de28b03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:15:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:17:29 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:17:29 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:17:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:17:29 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:17:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:17:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a66c0c3d1f3d600e2c1f2ce7b46cb6312a5f0db9083ec333e75ad9404e92086`  
		Last Modified: Fri, 08 May 2026 22:17:59 GMT  
		Size: 98.4 MB (98372601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeb6fc490f9cf969d9cfeaaa291fd77d81ff18ce9243e4fd4b690454add7c0f`  
		Last Modified: Fri, 08 May 2026 22:17:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:5841f914f63d39f8688e43005f36907dc656be6826a287edba58c88b380c8f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b064d92d1993a7aabffe2ac8255e756844a63f34fa302c398cae924b21f2c8`

```dockerfile
```

-	Layers:
	-	`sha256:5ac16a0634b0d270d84fdc7d053d543b9d9c88820075d58102d454c8db8b29c0`  
		Last Modified: Fri, 08 May 2026 22:17:57 GMT  
		Size: 10.9 MB (10906168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d94470108072b2e24f73abbf701db41423acccf38a560f1bd4f21d66afa26c8`  
		Last Modified: Fri, 08 May 2026 22:17:57 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:db9d6e104b8d9e6508ed1531811daf5965c41d347975a3e10e3fc229697cb9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343364854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fea33e77cc9272b4c782964c12e2e5d0768d978069da12ea8e1f5dbeeb7fb26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 17:44:18 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:44:18 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:44:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:44:18 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:44:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:44:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cdc00799a2a5d425863c783516cdc5139f867d081df458a78cfa749e9d7c3`  
		Last Modified: Wed, 22 Apr 2026 05:03:55 GMT  
		Size: 69.8 MB (69809793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da63c9b623cf1e53b55a9ec8360a0ccb64a313a3537a93850f861bb10f36bb`  
		Last Modified: Thu, 07 May 2026 17:44:48 GMT  
		Size: 100.7 MB (100664883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aba472b97870b51ecee9c3d0b7075b214398ea9db6bf6fc6c45cf3c1d74cdfb`  
		Last Modified: Thu, 07 May 2026 17:44:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f9784b771cf9c77017ddf176e358a7e52a06c1d05d8993c0ebcc0402b93a12f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d32dbc3d2c25447a5256a9c19dc62d18504716d0eb9e48447ac878f55608cf`

```dockerfile
```

-	Layers:
	-	`sha256:fa99fb161f9644442ba6ecc7e4b1c7fa69437e40345a7c2224e619e2c6762d25`  
		Last Modified: Thu, 07 May 2026 17:44:46 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfda900b5210f525febcc5d126c4ccc8e0c93091a1a4bcdfb4bbf16e32b060e`  
		Last Modified: Thu, 07 May 2026 17:44:45 GMT  
		Size: 28.9 KB (28924 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:c494e6008d8900fb62107ee8b0d9961745a6496468a8aac75a4a4ad9b0d15aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340234309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8956906fb79fba8a0088bf6316066b95aa24c2038432b0fd860793b0ac65e6c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:40:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:40:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32542f6ae8fa91e3c4f7aa2ae71b01665f1f0f2721fad64b8c6c798ae91cefd5`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 92.9 MB (92928186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ffe1ddcbfaa8c6da8237e96a5f8cbc5bb2fe068d9e535108c816dcf5a040e`  
		Last Modified: Tue, 05 May 2026 23:41:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b3448fca0715266f1dfb277df8eb1529f0a1091e7aac03d8a6c7787e1d1c4aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7eef87bd957a87c31cc58ca2afadeab16187296a106ed836194d0186277d6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6e2aa576b07a0ef58d7b8c1137ba3e6a9bef63e272a7181e10456cdb1f6269`  
		Last Modified: Thu, 07 May 2026 21:33:50 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b5044706c14aea35645d4e43c2db6c5492a1d66cbc84e16b8cdaeea078bc6d`  
		Last Modified: Thu, 07 May 2026 21:33:49 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:b101b3530a834f6f2637934631929654e436fc35c9dda8381ce82629581e3343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97a02948ed67849ed219091967d854bf2ed613ab8c6e1c2acba313f89ca49b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 06:45:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 06:45:06 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 06:45:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 06:45:06 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 06:45:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 06:45:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954c4b6ce8f364903d1d8a7ac953d1cbfe6ecf95f3d8c267e0b27a58b6e61bc`  
		Last Modified: Sun, 26 Apr 2026 20:39:36 GMT  
		Size: 131.6 MB (131649887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d77dd072bbe9d4ad01204d701c796e83867bd2e370f7f50879f12652b55ef`  
		Last Modified: Wed, 06 May 2026 06:52:06 GMT  
		Size: 94.6 MB (94621433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b99fb2cf5b5e5ae00b5a307aede37e49ad6185be029faa9a7d2d16cbe5087`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1bf3c5cd79effde86c569d59a4efa2efaf655c0e8fc50a49c512abda4bb94a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c76be1fc8380fc35898c9aee1718f73783c88470c254c67dcd5d3aa1bb1a2c`

```dockerfile
```

-	Layers:
	-	`sha256:84108ed3b601c6d36e56b947c104b072e29bbcffee990f2657bc0188c4b980de`  
		Last Modified: Wed, 06 May 2026 06:51:53 GMT  
		Size: 10.9 MB (10855334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c42688186c1da119f2be2e426528f8f693876aea10fa6700f25559591e02c4`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:ea8017af8fad1064c371d4168d74d3c83016b31d66ded0f0ee4b48315d256a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316950570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afbfd573201352248aa9d8085ddbd36ee55aaf7dac785c7437b77c9659d1610`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 18:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:58:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:52 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:52 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 20:09:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 20:09:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7889200e1892d95c7def52ca1b80eaca9e5ac49a2da4379dd9c77471fbbd5bb`  
		Last Modified: Thu, 07 May 2026 18:39:08 GMT  
		Size: 76.0 MB (76033391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa5d861c6edcd2ca743b24a3f0d4e8b86c925f3afbc2c87bcb946bdc254073`  
		Last Modified: Thu, 07 May 2026 20:09:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:38b1bd3fd98efb1f4d52647fb4d2554030b3cd9cc264ea07f7a298c225bff712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2210045576a31e81f6b1afd6906fce9ff4ce9c314a00d513029115a77a809db`

```dockerfile
```

-	Layers:
	-	`sha256:573eb24c8891028114699883657a5bdf301f5cb11841bec9816d1b71264a0fb0`  
		Last Modified: Thu, 07 May 2026 20:09:48 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70911d4dd4ed26daf03226f128ab17c8da3056d910f0a55f51de5cce36b53a08`  
		Last Modified: Thu, 07 May 2026 20:09:47 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
