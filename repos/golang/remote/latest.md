## `golang:latest`

```console
$ docker pull golang@sha256:f7159064a17ccc65d0e10e342ae8783026182704bf4af8f6df8d5ba9af2be2fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:7095ad02810845fa35d1fb090b8e57dd20dce4ca36b29b42951802350d2ec90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312105435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8255f11f47e6d46eddd971909ce2a6db51db9ac94b93bc100955161f68e717d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:13:36 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 22 Apr 2026 05:13:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 05:13:36 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 05:13:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:13:36 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 05:13:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 05:13:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac375eb07889c3cf24bc555cbb9cf76df6493da08a081d27c0faafb820ec42b`  
		Last Modified: Wed, 22 Apr 2026 05:14:08 GMT  
		Size: 102.2 MB (102170142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a65ea81e6956199ccab1a9545fab11b52e88464415e0c831db8b8a62d226bdd`  
		Last Modified: Wed, 22 Apr 2026 05:14:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:f9eb5ab4627fa027dc076843b2b0f1b815f07cd3d6b0e4fcbe635f17e6f32dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a139924b878fa157a293ac9fe4f67ddc7046e2ed8a0315e8bafc1143623308`

```dockerfile
```

-	Layers:
	-	`sha256:41aa7d426a0559141fceef9aa2aa2c9895b7ecd52ba41e62ac4a992af1e68f1f`  
		Last Modified: Wed, 22 Apr 2026 05:14:05 GMT  
		Size: 10.8 MB (10787103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061dd788996066af6fccef2d5dc01b261163b18431bb93aa5aca19b639e28fb6`  
		Last Modified: Wed, 22 Apr 2026 05:14:05 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:4c51c8e7d02ba8627a70486cc5ab3830ec2b2b37e6873ba81fc77e8c33d927ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270652405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b8bf02892ef66e0c032d31d243b4415107c8dc964896bfe8c8aa5855c68f14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 04:15:18 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 04:15:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:15:18 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 04:15:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 04:15:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624b0aa4927ac16af36086312095e6ed3b14f62fdd3e3051375e01f62b46df2`  
		Last Modified: Wed, 22 Apr 2026 04:15:51 GMT  
		Size: 72.8 MB (72805007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c9db2c2e213532638f94b4cfaad98960ad1d0f0e36b1f944691e81cc1ad52e`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:a8f20c21c5ed109d8e740a3948b286596d42e2b909452139384665bcdbb1081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ed4e59cfee33d3936c185f05adc9a73a447f39b62b3bdece425754d0aace7c`

```dockerfile
```

-	Layers:
	-	`sha256:a0bd4a4da5655cd0b06c64e0f3a7047a5a7e1859c28c3be2f4b68128c4f4aa9d`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 10.6 MB (10583022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d343bc3a02dcdb385b8d899e318b5cba75f08c3c5cec3795b0e0999a5ba7b8f`  
		Last Modified: Wed, 22 Apr 2026 04:15:49 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9cad238cf0e07195a64c4e7c26f0fe9ac82db343a5d15441fe01538fdf432210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304696197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5882e9c78e5e1665fbf20a591d6ed6fda053fbb0cc6d41a523556d12aaa21b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:17:11 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 22 Apr 2026 03:17:11 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 03:17:11 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 03:17:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:17:11 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 03:17:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 03:17:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ede21c35a32eca30a8278ef8a73d89de914c5295ad0ac72f1c01a916b1e8d3c`  
		Last Modified: Wed, 22 Apr 2026 03:17:46 GMT  
		Size: 98.3 MB (98309893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa38556daf93d83c3188869b15d523afe3ea7db8de8af556ef56a0d67a62f38`  
		Last Modified: Wed, 22 Apr 2026 03:17:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:a61a46d8ba2ecfa77f6d6797e4deb8bbb817a0fb9b73397d3058d51b3daa5b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4225a98329dd902623053d99f4222a2a58ccc3aa68f1f8e1a46a9242554a87b9`

```dockerfile
```

-	Layers:
	-	`sha256:d9113a642003cab34c497ed5950fc7bc6265869ac21dec4a81b876b3abb8f0c9`  
		Last Modified: Wed, 22 Apr 2026 03:17:44 GMT  
		Size: 10.9 MB (10907606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e60829158657d78a76222e643bc43d52528f7630cb03821537efcebf9cf85c5`  
		Last Modified: Wed, 22 Apr 2026 03:17:43 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:c7ca455a028087b0bea90e7b6cebd43af0f88ddb2dc92a325781051eb460fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313569742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa560bb5bc6f131d6bb07ac85817cb500bcc50e46f359e5bd2573451a9046092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 08:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:28 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 22 Apr 2026 08:19:28 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 Apr 2026 08:19:28 GMT
ENV GOPATH=/go
# Wed, 22 Apr 2026 08:19:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:19:28 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 08:19:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 08:19:35 GMT
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
	-	`sha256:2d9be4adce76cbcd2a2b354c31cee973f88db604038ec0ef4e8b0f2ca1460508`  
		Last Modified: Wed, 22 Apr 2026 08:20:00 GMT  
		Size: 100.6 MB (100607834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6328bca7b52b9cd1348686498d17eec558a30af5cb0192825d7e98692217a238`  
		Last Modified: Wed, 22 Apr 2026 08:19:57 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:ebd7f0596cad964cdbfb37446388e674f7a8fa41ad67218c7485be716902cbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253a5fb54bb0f3651e10b5704204163db44441c5ed3925d9850655ad71b70d9`

```dockerfile
```

-	Layers:
	-	`sha256:aac1402151de02709b654d86a31987236149edb88d8df27e783e90662bfabd7a`  
		Last Modified: Wed, 22 Apr 2026 08:19:58 GMT  
		Size: 10.8 MB (10758346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38137d6f10b788e28742a521d7b8ea4c2e224da4de5110aa473c4fc76e240a61`  
		Last Modified: Wed, 22 Apr 2026 08:19:57 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:e53d1eacf57e0bcc47d8207c28d23ea808c74317050e60ff45c86b8fc184a837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310795438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26330b13d814c7724bc958fa31ebd5fe695a61168e43165339e5172c9ce946`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:21:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:27:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:27:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169353b9ab6307e2b065964fc878588895f32907dd884c905868bc86f58edd0`  
		Last Modified: Tue, 07 Apr 2026 09:55:34 GMT  
		Size: 73.0 MB (73033989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb540501f7eb5e096f520ca2cb5637ef4c3bca5b6d3ccbe7a39cc10f271f5f7`  
		Last Modified: Tue, 07 Apr 2026 18:22:27 GMT  
		Size: 92.9 MB (92871008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea234f486ce457907609835f97ea0b384bcf0c9bbf12fe2904da472e3b5f6dfd`  
		Last Modified: Tue, 07 Apr 2026 21:28:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:93761aaa3fb8b0d61c195ed12a9c5e73c28cc5946db262c3e3f41f0369bed398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0185f22755fcd56ae8c8ac9f0ceffb699a56379c82774a65f4856a41b5a3b4`

```dockerfile
```

-	Layers:
	-	`sha256:9c6fd9d1d117c1c00889b806b0f6a895920c3e98b064b4fcaf417133ae16dca9`  
		Last Modified: Tue, 07 Apr 2026 21:28:14 GMT  
		Size: 10.8 MB (10782861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7dd30365115fd720ea8914b89f26da29097b9958a260f1e5c4820d74f7fcdb`  
		Last Modified: Tue, 07 Apr 2026 21:28:12 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; riscv64

```console
$ docker pull golang@sha256:774afba3c5a32e4cea8924ff2cba83a6780d8a5dbc649f8f10a42a3d0911a31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339317847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5bb0e4a988a091b0c3e680e30fad970131a5604d699d5b219fa4f107fc1316`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 09:59:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOLANG_VERSION=1.26.2
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOTOOLCHAIN=local
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOPATH=/go
# Sun, 12 Apr 2026 09:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 09:58:49 GMT
COPY /target/ / # buildkit
# Sun, 12 Apr 2026 09:59:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 12 Apr 2026 09:59:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacec47fc648b6d60a98d7ff6fd4e23039ac63553f44613cd15e968e674616e6`  
		Last Modified: Sat, 11 Apr 2026 03:02:36 GMT  
		Size: 66.7 MB (66662977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ae371f482aac04d17f4b10d6a0cb36e2673a9d5a8d69e7d7b268296cad8a`  
		Last Modified: Sun, 12 Apr 2026 10:07:19 GMT  
		Size: 131.6 MB (131649469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1608ad74eb78794c13df4d01468bfdfb9c55c3ade34cb0be90e33ceed80b90`  
		Last Modified: Sun, 12 Apr 2026 10:06:58 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:ecef0b104f82796c534c6e1c0500ac346c2666f62ad3bc5851e60d343d507d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fa8f5df23ac2c3b43f84c55b946d4f27417d9c84bd0d2b7de16b4c18f08e0`

```dockerfile
```

-	Layers:
	-	`sha256:7bdd9a2981b1ee1e8a1b0f34ee7fcec960cd650ad1878893159cb02dbbfd2551`  
		Last Modified: Sun, 12 Apr 2026 10:07:01 GMT  
		Size: 10.9 MB (10856694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03c6366a09f3dff3fd24a4c1693ae52f8ef52e5298da0495880daa183078966`  
		Last Modified: Sun, 12 Apr 2026 10:06:57 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:3f44033286f04c0b1488b9e19b60d550bcd54e9d201b61657f2fdc1fff21500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287225591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81e63f22061f2218ac5097d7438454e0a66d0f6306b9aa2fbaa9dbf3ef241d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:12 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:12 GMT
COPY /target/ / # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
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
	-	`sha256:a8027314e609c53cba98fd110647ae82f15ca5a14a5ca8b1f7f0efac414d3719`  
		Last Modified: Wed, 22 Apr 2026 05:15:27 GMT  
		Size: 76.0 MB (75981818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c2e1ff04fe5ced2f859f0fa7e592143f21967e1554851814be99c86671e778`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:b422e292d58e2a28a79f7b55a76b24213c54834bf7e9c10c7bb71f1cae2812d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711efc5c86a93c7b6c58bffc80dbce2e52a6d217d8856aaad21abc3b352d3fe8`

```dockerfile
```

-	Layers:
	-	`sha256:aad6b17d8f7c5af42fa77014326d90d7a180e8647686cbef532def29e14c5981`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 10.6 MB (10597503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5987e2da20ea0e6e6cb950fbe2978bb4d1e5974725a28803227f48e5c38591ac`  
		Last Modified: Wed, 22 Apr 2026 05:15:25 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.32690; amd64

```console
$ docker pull golang@sha256:94f1961ff53812ac6f554fc5fd6d1f9c6986a3b6edf6512d910acce9729b2964
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251428455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec38fab49af31bece8746eda2b2b9fcffb0556197a0c57e3fb9ae9c96be18b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:11:49 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Apr 2026 21:11:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Apr 2026 21:11:51 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Apr 2026 21:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:12:04 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 21:12:09 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:12:09 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 21:13:25 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:13:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00876c5c306a40bdb91b29e1bfe5c5e3a30957345f5b4217492950932921f085`  
		Last Modified: Tue, 14 Apr 2026 21:03:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab6f7f8c04a918d6984281136988db80e26d2e49e506c24235a6aa24d3ddf8`  
		Last Modified: Tue, 14 Apr 2026 21:13:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9a4de2d156c81a0b97862c3aab31aed462414093a7a3548c0e075dbff4df45`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905977893c27c80019254fc21606d27924fc7e8f15995ca1e93d995d0f9da1e1`  
		Last Modified: Tue, 14 Apr 2026 21:13:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11d045724382783805a4ed4a39e0438de91e10ce9ca26c4c1386c8c1a42022`  
		Last Modified: Tue, 14 Apr 2026 21:13:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517fa67870dec0ffc5542cea5ab7d6f5965077f9b323899b2c9e3c769823b2e`  
		Last Modified: Tue, 14 Apr 2026 21:13:38 GMT  
		Size: 51.2 MB (51227687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0c782a756fd5efe99734cebd326bfa111492e8514da6ba7ff44f2f23b0781d`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897c264ceb6ee8f252b0fdd9730a6339aa994740a00c6ecc3702353781a65dd2`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 359.4 KB (359353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afaf9528a576024002874bdb07610060adbb25dcf8cee62e667f97304a75e6a`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd318c5f8d24379da8ea97d3b862c1a1c3fe17f62a8c3168da4a9fdccbcfa1a`  
		Last Modified: Tue, 14 Apr 2026 21:13:41 GMT  
		Size: 69.8 MB (69844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccfb531c02a788d97bfa192c0263ddafe73165dbf8bb40ea3cc1195581d6fe`  
		Last Modified: Tue, 14 Apr 2026 21:13:30 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.5020; amd64

```console
$ docker pull golang@sha256:f54874bfed40b5e99b1a62be4eaf99569ce113b53ddb1f65dd62217a90a44d9f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2191742480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8be753e6c9be6988e147453928affa05f55a5f5501ce4d51243c65cda15415`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:27 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Apr 2026 21:16:27 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Apr 2026 21:16:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Apr 2026 21:16:30 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Apr 2026 21:16:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:16:54 GMT
ENV GOPATH=C:\go
# Tue, 14 Apr 2026 21:17:00 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:17:00 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 14 Apr 2026 21:18:42 GMT
RUN $url = 'https://dl.google.com/go/go1.26.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '98eb3570bade15cb826b0909338df6cc6d2cf590bc39c471142002db3832b708'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:18:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebcfde08590ee1d8e1fc13f10328237120c5059d4cb5fb9cca78ef9475f3a62`  
		Last Modified: Tue, 14 Apr 2026 21:07:22 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d090b769fc5e142d320bef003f0bdb353b56d05203a83f1583a9d263e6a20303`  
		Last Modified: Tue, 14 Apr 2026 21:18:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579af4f3a0b4882445e7c4e593e5cc4b68b5cc575937bf85d22ed7c0a469115e`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726be3d7369a0206806f3dbb666744d68c9a77a4d48528dee84fbf4af0e002cb`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a477df0158ff310f6e299e9b273e3f64da64606f523131ab2f45f07d27d90`  
		Last Modified: Tue, 14 Apr 2026 21:18:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f0c7a95636b85106b0c191c8d9ec0d8b5a492e0b44b05329b8411b8b68e8f`  
		Last Modified: Tue, 14 Apr 2026 21:18:56 GMT  
		Size: 51.3 MB (51347005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2299b8256c980a964ef2eb57ce33daafbd269dd7b9c23c12c9ec51c1cb1fc1ef`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e5548fbd84ada2f921610c3795968099a10dd5656ad21960a6dfdc6c8df095`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 335.8 KB (335788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf3b50d1724544802ab699d194893340124dddf14863ecee5182cd9c144293c`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50c3513b2c439439a0494bb8443f20c22b1bbdf00fc0f378332c5e2deb545b2`  
		Last Modified: Tue, 14 Apr 2026 21:19:00 GMT  
		Size: 69.8 MB (69837725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04d5273101b31beed5f88bf60da131b30ac28731b927c7e024e8942a216854a`  
		Last Modified: Tue, 14 Apr 2026 21:18:48 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
