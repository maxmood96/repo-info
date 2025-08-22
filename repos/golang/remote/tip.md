## `golang:tip`

```console
$ docker pull golang@sha256:05782945c6a04e496145ad051ffb0e1955f498595bdcf1c0182615032e0f4787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:261e93838abdd77db8b2709a20b60d6961863e3753fb16e2c71aceac9dc55dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327858411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8540a80f4cd88e436a653a60d54a447548dc8b212610fe4cb88e8856a61d96c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0723a22cc634a788af63e71fcb9154b8a816633143012d4f0d8705ccbd1322`  
		Last Modified: Fri, 22 Aug 2025 18:11:53 GMT  
		Size: 102.1 MB (102055489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b55eed673044438e470d03433baf0615240b3df9a475f663db630286a5501e`  
		Last Modified: Fri, 22 Aug 2025 18:11:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:012c6f5a47b76c3e57b237a861822423d9752a4c39d8e6bcf853c229e4e7ca94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10807322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530bf654b98ac20f76f4aff38380e08eb869fb8a09020b18d0dba884ad795c7`

```dockerfile
```

-	Layers:
	-	`sha256:f01eb9a4814502108beb5077b188033229acfb0a7023a8259dd2c6136220dfd6`  
		Last Modified: Fri, 22 Aug 2025 20:25:07 GMT  
		Size: 10.8 MB (10778310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c1156d84fcbfc7187a585cbe04680abc4d715f549ccd59ed89623a654dac47`  
		Last Modified: Fri, 22 Aug 2025 20:25:08 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:4721545abda2c035ef6f0ad594edf1b241986ad296611142dab5536437205318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284902193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82cf74372233cc0085bb67e40cf0d6c090a9e5512cb84c9448759440e12cb33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e43eed239a19cf297a7ce2beb2041dbb4789440168f810815da1dfa6cf3c8`  
		Last Modified: Fri, 22 Aug 2025 17:33:19 GMT  
		Size: 72.7 MB (72699083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65db35adfd1c26b9fd865e957c7ac16cfbd5d2925f26a2f01840bdbea9cb3b72`  
		Last Modified: Mon, 18 Aug 2025 23:18:49 GMT  
		Size: 80.2 MB (80158777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8270fffd0e77cc9c1529a420bebe6f6e16266372ecc9b8962b5b33dc1f2e28ce`  
		Last Modified: Fri, 22 Aug 2025 18:10:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:98314f3f910fc1ca019de0600815d63ca9e92c44c3f6bd6ad739b9ecca886525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73201528a953456f7e898455c3c8b95477ca7b550ecafde1283bb8e80f88c90e`

```dockerfile
```

-	Layers:
	-	`sha256:6d8279b3de8bbef3fe8f734a75acc48c756bcd1f6d05de835c6e129d1b7ac292`  
		Last Modified: Fri, 22 Aug 2025 20:25:17 GMT  
		Size: 10.6 MB (10574199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed048a4f8b511af66678f331f1769eca2b2a9dc7766f731a2c3b79579a41c2d5`  
		Last Modified: Fri, 22 Aug 2025 20:25:18 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3875a7e4e7c6bea6b2342b465bdb1dd5969b97cd8fe8d3d943b6105204cbee60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319582721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d349cf310bfb6a113666a4afc93b6cb6ac642b65a76fe517f9ed43285ff6150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a43198c724cca3e0c99edf0ca63f8860be859f60068bc37cb39969dae61873d`  
		Last Modified: Fri, 22 Aug 2025 17:33:12 GMT  
		Size: 98.2 MB (98200099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a962081772d9ddd06f0164791e2d37e59bd0091e1d2b79d410ab8b218794c`  
		Last Modified: Mon, 18 Aug 2025 22:12:08 GMT  
		Size: 79.1 MB (79132623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212a8df8ca65df74b1fbd0232bd746973535f34de2e3a0613e3f324713270206`  
		Last Modified: Fri, 22 Aug 2025 18:09:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0760721b231b273360589b4aea822a669eb38b88859d678d8f6b8c21a18ea0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10927931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e825fdd919220e0e6d20df1fcf73b78df08c63d101df7d1d3daaaa11c9088`

```dockerfile
```

-	Layers:
	-	`sha256:21f615256ce76b84459cef7ac8c1e735326ef3eb05182531e5d6810c47284c83`  
		Last Modified: Fri, 22 Aug 2025 20:25:25 GMT  
		Size: 10.9 MB (10898765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07cee5e2aa4196c21fb13f8b71f72b90e3de7c48f8d50af90d50e475a495683b`  
		Last Modified: Fri, 22 Aug 2025 20:25:26 GMT  
		Size: 29.2 KB (29166 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:538f4a73e0cbc007ab32c84eb1f02acd36aa13ba6d5e5db964fbfaffaf141e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329619346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb5051ecde3b5da9f83886359bf3c09eb29473e8b035e51c60612d9bfc76427`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5675dc6e647ecf63e7554d0615e5f3a0486dc80db9f98582ed9a6f24455ac94a`  
		Last Modified: Fri, 22 Aug 2025 18:12:14 GMT  
		Size: 100.5 MB (100498523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0ac6f94fae987f4196520776661c9600e6ed250d6139b71a195cbc397054bc`  
		Last Modified: Fri, 22 Aug 2025 18:12:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7fbf99aa33a9695918773e4627ffbfbab278f3534ade04393d16fea3a75d33e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10778545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ca52c0b8a6b485c795b3bcad434899ef81fc29e3eaf04b5611e0e8cf3b3ce9`

```dockerfile
```

-	Layers:
	-	`sha256:59fc73f992cdda1558a7104b9bcac50b6ceaa4c64d68e96ed9a4891c379f2149`  
		Last Modified: Fri, 22 Aug 2025 20:25:34 GMT  
		Size: 10.7 MB (10749576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2f3bf1f897c51918f76392d8d7d22d9d4adc45d8939b9b70d67e007ab50923`  
		Last Modified: Fri, 22 Aug 2025 20:25:35 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:0f8e15bd82e60f27213b3edff17aa1af7ccaa3171673b10f16ecf3acb4bf2a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326357758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4599673a3b3a4201ac4ad902b8b28c16fac060fb3eddf8f52cb7ac9ce26e47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b620c97eb27d08e617f0dcc9cf3059e339c2f927c5a909f74445e10a25d9c34`  
		Last Modified: Fri, 22 Aug 2025 17:34:58 GMT  
		Size: 92.8 MB (92761258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d39b86dffb1db621a8fcea400d6f61123247f5d28fb771a6f68ef42e85a595f`  
		Last Modified: Mon, 18 Aug 2025 21:57:49 GMT  
		Size: 80.5 MB (80481431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bca1314b57dd300dc2a3d5c88f1dcf0f0bb04686ca620539fc0b95912a42e`  
		Last Modified: Fri, 22 Aug 2025 18:11:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3933deb97b4c059ffd4f889f2010800287607b2eeac4b8e2958bed6bd06b2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10803159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5376b41aac4a195f699159ab8b48c9c5081d893dbe89aaf5d04ff167d125d88a`

```dockerfile
```

-	Layers:
	-	`sha256:36f54d2ff3daa59a8799a535d3c5f12907f53ad66f622987505b0df03b83288d`  
		Last Modified: Fri, 22 Aug 2025 20:25:43 GMT  
		Size: 10.8 MB (10774094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a308bd48705c75f236a761f66fbf0a89914f750cbe9c8a8582eebf80b24ccc0e`  
		Last Modified: Fri, 22 Aug 2025 20:25:44 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:89ac25198754fa03580e5c2159957b9cf502d489bf6bd7db489e6d8c02b96d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302310689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5156212f4bf3b365b544300ee824a6a2bedc65005e7c7e9e033329b7cd2e1eae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d954366204dd198f5f29a2ea512acfb1c64ff1a9eab53a5c7474b137bbaab1`  
		Last Modified: Fri, 22 Aug 2025 17:36:11 GMT  
		Size: 75.9 MB (75868390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0948a73e9355048caabcb1e85b3b6fc5e4c424f238e5de30533b3ce531186707`  
		Last Modified: Fri, 22 Aug 2025 18:10:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:43786663251c37693e89f5096c9eaf39da32b332a173c582e96526e322c8ba22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10617716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6090d3ca2af97b2d76c4a470d5b347a69e43863754d6052d8aa5c7f12bbe9776`

```dockerfile
```

-	Layers:
	-	`sha256:23504061ab1a5b7d1b9c6b0d6dc8547876c66bdf89c0ffb6bca1df43ace4001f`  
		Last Modified: Fri, 22 Aug 2025 20:25:52 GMT  
		Size: 10.6 MB (10588710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e42ed5d0084031f093ee3ec36d15cfdc140915456e5d082fd50306878a0c28f`  
		Last Modified: Fri, 22 Aug 2025 20:25:53 GMT  
		Size: 29.0 KB (29006 bytes)  
		MIME: application/vnd.in-toto+json
