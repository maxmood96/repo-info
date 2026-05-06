## `golang:tip-20260503-trixie`

```console
$ docker pull golang@sha256:ec19cf9b16bb16e5710273a7baaa7380d18655717e238acfe076f41a6330aa9a
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

### `golang:tip-20260503-trixie` - linux; amd64

```console
$ docker pull golang@sha256:a459972676a5fdeb2f2fc4e942c5d962d3f5508d09ce0677d62cbc3db1aa33f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342476056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec18ea038d29610ecc6b6bd1264b41c8c39d3f8a7f2b064f73ef7815438c312`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:47 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:47 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:50 GMT
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
	-	`sha256:e2c18bfa5bf4e25fab50b3153ed6700b696cd0173c9347e2c6491587f0008a27`  
		Last Modified: Tue, 05 May 2026 23:05:17 GMT  
		Size: 102.2 MB (102222455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693b02c0881b20c78c1ee19fca1d834c53888794d0ecc6201daad07c58d9288a`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8786f7e18901f9eb89d68d70b6dd7c34b612fb2dc7a69bd5ffc1e58f063672a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a70ce1786d50e666fe6e1c26811910e1fb504816c7562d43234ff3076f9df0d`

```dockerfile
```

-	Layers:
	-	`sha256:21e58bb1bf366681ad5ab422873b465cfe727d636bb440e701686a8b618f4608`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd80e38221ecf44803daf866d5485e45756a13f9d4313bc3458744ebe82e2b31`  
		Last Modified: Tue, 05 May 2026 23:05:14 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:7e9e7a33fa9e73afae4d469088aaf7ea4cb29a593e91c4ab1ce14d1a8968ae8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298341338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755dd8883ee9a6badc4c04cd5a590c7f53662a9c55c9e994a29d60cc85a7ebe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:05:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:08:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:08:33 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:08:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:33 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:08:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:08:37 GMT
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
	-	`sha256:7f1c6327a1718176ef21a0e46efc4e5cb9dd66800f1da69928bdf4f543a0b56b`  
		Last Modified: Tue, 05 May 2026 23:09:03 GMT  
		Size: 72.9 MB (72865886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0781561680e77db0cc011222384eb13abb0e2cffbb12993971595942a8a1752`  
		Last Modified: Tue, 05 May 2026 23:09:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:43a1275d6d2f3bc5eebcb7c160c83297292cdf9b5514a5499fa6edf5ebac8288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1a21d9caf450c2db95565a89fa40c65b16bae323bfb66754a599c872554c95`

```dockerfile
```

-	Layers:
	-	`sha256:b84f517254f57aa90f10c2c51a402fa6fa9b60f7f85056bc9f93cde840171040`  
		Last Modified: Tue, 05 May 2026 23:09:00 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f6079099704ccc06996a5d64f9907589c78a111f05ec3ec39608d21192ceb8`  
		Last Modified: Tue, 05 May 2026 23:09:00 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:02426a2e16784700e78603260df5e864ed5b7c1483d3d456b22ddadfcd18900e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332887087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3305d20b79b253e9e42114d89557230e6780a009bc8f7b90db694d7ba1dfba04`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:02:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:27 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:27 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:30 GMT
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
	-	`sha256:1b19eb497ed9eb70fe2817684b166bcc9a51346a198e206dab83cf6a08c69533`  
		Last Modified: Tue, 05 May 2026 23:04:57 GMT  
		Size: 98.4 MB (98367177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8522060ce33eac8345d4400d0d71f120aec5961fbd7fcc11c1fd697b5cb42`  
		Last Modified: Tue, 05 May 2026 23:04:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a5ed24b47622a5d1eb146604ad21af6000b5c35965e3c795e4de15cdcac1e440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16122173b44cf2ed0852d269b6b0cf6914d9a2d30a517f0b0b1c823152698585`

```dockerfile
```

-	Layers:
	-	`sha256:82561316c417da2f14e82ddfd6fea1ec963296277e0953eebaf52878889ab545`  
		Last Modified: Tue, 05 May 2026 23:04:55 GMT  
		Size: 10.9 MB (10906168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc2936ae71a1eb994899bdad8413870fdaf2ad77d79ab254f1bcbab085b368a`  
		Last Modified: Tue, 05 May 2026 23:04:54 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-trixie` - linux; 386

```console
$ docker pull golang@sha256:a7c560ad0638d5a7b99008a78ff4b0afd3af3f1d035be9ed6a1edecf1fb26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343364957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903849def7e9b0e4a5fc9b2db47d71804a5deb28f1e2faf83bdbc673d1f5c47d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 22:58:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:01:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:01:00 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:01:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:01:00 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:01:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:01:02 GMT
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
	-	`sha256:fb2507b794620dbc689ac5d48214d3b52c8a3be99152364a585ba286189a744c`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 100.7 MB (100664983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8072a9ab27c7b55d716ef673a7b1be906c88938c45c325f05652e194ccef79e4`  
		Last Modified: Tue, 05 May 2026 23:01:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6d772bf7046e6b17dc92ea0345019b59ca9f169680aa803072c4506b0486b405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6eb097de3ce4c8b837c5625ff435bd5f956d1dac99e3961221f48509d1506b`

```dockerfile
```

-	Layers:
	-	`sha256:696e4c53e56e3f6500115c785aba012c3d786948e94d3f7f7365374e038fcc3d`  
		Last Modified: Tue, 05 May 2026 23:01:26 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f368c9239f0d53aa29bae0f720ae865cc5953cb24bd5b7e2555b36a7f037675d`  
		Last Modified: Tue, 05 May 2026 23:01:26 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:20412a007790159dc1c1fb7eb7967b00cc1c1b4f8834c8ee782d9f4944717898
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

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:96bd501de05e6db326fc0381c4973e095921540f65238bf67dc66b39e89373d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbefa6d36e90c5a7b10b93f281c723a5a3fd3648ec761f6369dd7dbaff600881`

```dockerfile
```

-	Layers:
	-	`sha256:cc77ca15d570c330bb6ab0c53d69b2c83f7fbfada3be8e43265bba9c8051a26f`  
		Last Modified: Tue, 05 May 2026 23:41:38 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53001cad588d92ff3c7b69f4b77dd35c602ed58dd407d4b4a033e50f28944de`  
		Last Modified: Tue, 05 May 2026 23:41:37 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260503-trixie` - linux; s390x

```console
$ docker pull golang@sha256:e8049597941504c1cd06ffb521b72fea76fc5a98255429b957cfe4ea0b53a5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316950863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf7d1e7e80faaa8a451709d31c047d9019bfd6feaa57e79c9c2b8ec59799ea1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 05 May 2026 23:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:58:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:46 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:46 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:58:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:58:58 GMT
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
	-	`sha256:dfc6a2d536e288af87ccee171508f7485452c85c478a1a2916967410856a3ebb`  
		Last Modified: Wed, 06 May 2026 00:00:33 GMT  
		Size: 76.0 MB (76033684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1947e08859b0c3f97c35038351830813035cc3c013360a7fb7297c7bfc0beb8f`  
		Last Modified: Wed, 06 May 2026 00:00:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260503-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ddb37034dbf21c1010ff73a880096111081a7d079900026be507dc1012c5b95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f42d34884be43eb3c19dac3f0f6f4c7654d730a60f7aec70d86595b9a4ff2e1`

```dockerfile
```

-	Layers:
	-	`sha256:d24440f7425ba276a10259afb3a1d8e7c5eb2f0b77b5c63d88ee1ca382415862`  
		Last Modified: Wed, 06 May 2026 00:00:30 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fa92673422ef544cc11c19bb95fa0d48223b8852b6c2567c66ca1a57889c5b`  
		Last Modified: Wed, 06 May 2026 00:00:29 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
