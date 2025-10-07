## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:c5be75f7c374ebbb88b8b41187f9872f2981793392499ceefb9434b37803c7bb
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:b256687fca8a17fb61df836d758dbeed72e20e8646e9b140adfad8927b46ec67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313905973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb08fcce01cb618ff31e05998d596721a67246de1c7b55c1cea34c2bd4db442`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b823c52a941268e726ae0c19a80f372dd76311128b8c2dd831096b90889246`  
		Last Modified: Mon, 06 Oct 2025 23:58:48 GMT  
		Size: 92.4 MB (92401956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87c5516348c20492dff99d659dee03862a1ce9c75c123ece7fe36f9d97cd726`  
		Last Modified: Mon, 06 Oct 2025 21:04:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:669564eefc9525d73139a7daa1ed9f3aa242da2a60bdf3158c6fc1e5befe1866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8cbc5c46b61a674f0bbc876e8f15e9c93418cbf0a7ae0db8bfdda931d4c621`

```dockerfile
```

-	Layers:
	-	`sha256:fbc0143aa1c39d7caf85b3a6b683f00023497b0109b37c8b14e210da26d85c1d`  
		Last Modified: Mon, 06 Oct 2025 23:24:41 GMT  
		Size: 10.5 MB (10494916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026d55ace311917afce97c3dceb65c0996da1f1c2ba81c91c0240ed2cbcc0ccd`  
		Last Modified: Mon, 06 Oct 2025 23:24:42 GMT  
		Size: 28.4 KB (28428 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:a76fe242a1f292fc0f7c1fc0e26fd3070c155e195d6732a39264b7edc5c0845d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273584007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5356d216d2ed9e4d8f1079c82e6d95a7c6b502a723d6919aa96b1240b4d9c7c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb4963ee2dd9332bc4e54accae4ca2aaddc29f4bca8e860acb044054d2c59a0`  
		Last Modified: Tue, 07 Oct 2025 20:12:14 GMT  
		Size: 66.3 MB (66254794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec7037df85907dab4d5892a572d7b0e4504c4f2a53085073d6e436da25df91c`  
		Last Modified: Tue, 07 Oct 2025 20:12:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4e00602ec90979fe224c653b1e5a27500f63a268e2dfe97ea8c61effa1db630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2b20e50276e10cd25ff55a1fae228d19ce971800fe988d3e3ae331f1962bcb`

```dockerfile
```

-	Layers:
	-	`sha256:07d3ff2ca8317e64279d109ce367660e2f542b415bd6c9c465589fe1bb12c499`  
		Last Modified: Tue, 07 Oct 2025 20:29:14 GMT  
		Size: 10.3 MB (10301614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f9d187f8800614918d8b703a5d51bb92104342fe6906fbcd6b4f3c0974260f`  
		Last Modified: Tue, 07 Oct 2025 20:29:15 GMT  
		Size: 28.5 KB (28541 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:75584c0d444db88836811014fdff71f70d54a02547d1c9139bd6512af20a5235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303329194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac69a7183e2849ca6095f8946661cf039ec0cc1bfc10d9837133dab08469271f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ffd9c3660e16209cf215821bf6beea946474bb2bc902df6732f5a1f74f168d`  
		Last Modified: Tue, 07 Oct 2025 20:12:31 GMT  
		Size: 86.5 MB (86472328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca03e8af4ef42f2f7626cbb0aa7577654d74a2cc35b2d681e9042e37f0acc40`  
		Last Modified: Tue, 07 Oct 2025 20:12:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8e9f8928742965f14bd61a5b3145d3c907fc4a0acdc261ffa153e1266bfed260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773ae6ac44de22bceb28c8930469b1b81ce1524f8523811ac6ab8f2555e85633`

```dockerfile
```

-	Layers:
	-	`sha256:faeab7046ad54030e9146f78595c9c9950b00b3cab795b82977c088edee607e9`  
		Last Modified: Tue, 07 Oct 2025 20:29:26 GMT  
		Size: 10.5 MB (10522740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e0480a1e254f8ca3ca4d5ab69e022ce91d4ecee6061dd21d46790bc1dcffef`  
		Last Modified: Tue, 07 Oct 2025 20:29:27 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:dfa4c1506f504baa077d9a6cdf421739317de5e5c7e4be983b9a84d0504c66ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313529744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f43529fc5359c34b879bc81b95a44c30d431892ee8d9f042354bece2ce3f8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11964e5368c9868983a0c55fb321bb64b45388c42fc90c90e24ca9641f7b2055`  
		Last Modified: Tue, 07 Oct 2025 20:14:16 GMT  
		Size: 89.8 MB (89823399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e6515faa0e56f1a5f6b120076cdfa09988205075540c75574ca5eb43a1a656`  
		Last Modified: Tue, 07 Oct 2025 20:14:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ecb98db060d5fab4cb7abbf9ac428f373449b66a2dbc1531ee4ec1b814a24b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e534b38c22bc642ec41d679943c534ac3bdcef980ae0b73681c2bea4adc74cc`

```dockerfile
```

-	Layers:
	-	`sha256:3bc5b1fe2fc019d2ce57fabcc2e48fc192f1d622064eda0ff0ff0b0b8b78dfc4`  
		Last Modified: Tue, 07 Oct 2025 20:29:36 GMT  
		Size: 10.5 MB (10474499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c75fc2df146289cc8a13627bb2e8edf81eb85809c12e5e72d8bf6d5dad3fdc`  
		Last Modified: Tue, 07 Oct 2025 20:29:38 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:30a2713a717585e8757cb00d9038f312694f6cf768a3c097be591e3b7d5acd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285051957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437ace28b58e3d8dc9308b48a4c51df2579b879292a01ed8d3436b0868fc9298`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39be94b43c7b8fee0fdcf795208f91323ad52fb7cc0e21f16aaaac555d61b8`  
		Last Modified: Tue, 30 Sep 2025 22:53:31 GMT  
		Size: 70.0 MB (69997146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1ed2a50f0596556a219d15d43da29c3ddc34d7e3f3de6d4f6537bc7f99a8fd`  
		Last Modified: Mon, 06 Oct 2025 21:21:28 GMT  
		Size: 79.4 MB (79373238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4524d0c56b872a869b054aaaf6444d3f733a6f5de3eddf7f01cc032e537506c6`  
		Last Modified: Mon, 06 Oct 2025 21:21:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:246b9e59b4996efa379a150dbf5ebde776b25e524916e76f8bf6c19b6bf214f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20111425d951183dc53ae8e781d98d7980cc5fc2eb07979a3fa0142148be7ee`

```dockerfile
```

-	Layers:
	-	`sha256:bea6905cc0baa4e4b1afed6bc2035fd548326ce6997fd046d9a9c969d50d0cb8`  
		Last Modified: Mon, 06 Oct 2025 23:25:19 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:8c12f181b439873de5cac320c5cf4339f05e654e3cfbf66ab5e2318086f60c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1cc75e4aba6b1b1b814109a35572ba34a9227d262dca7dcdbcbcd46cd61577`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b052a32cc9593256d5096437790565c79483c5e1e301697d510145037fed`  
		Last Modified: Tue, 30 Sep 2025 19:48:33 GMT  
		Size: 90.4 MB (90417716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7c70e9f5f453d1342236044bb3e57429e9a5f73c7eb63233fe3328a5c8361`  
		Last Modified: Mon, 06 Oct 2025 21:10:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2f6d7e7c3fe7548a1b5885f1703169bd54cdb377daeb2dc83874c0f599c3a042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5723fae9c08c35f09e10d2a885f87a5c21697eff7bed9179c0d354b257b7f58b`

```dockerfile
```

-	Layers:
	-	`sha256:d96631279f83d172e32cdc9c6060bb64cf6d2e4b8e6e0bdc9582ab003fa3ee51`  
		Last Modified: Mon, 06 Oct 2025 23:25:23 GMT  
		Size: 10.5 MB (10467397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e649e9265bff9fa739334f816982483420810d76581724056c1160e7863b1035`  
		Last Modified: Mon, 06 Oct 2025 23:25:24 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:80bc941d5f594e05e644158b6a4a09eaf84e52d18af25389c5e07acfc77704e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286722991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7c981714e6e94f34cd74239ee43d13029c135cda2ed402d66c7fb5e6386b9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4dbf2eab022c30a4f1ad0d69bb0be8e9a7b59d1d848c5eb4bcf43acac22ef`  
		Last Modified: Tue, 30 Sep 2025 23:54:17 GMT  
		Size: 69.0 MB (69006320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057af9e0ce051959c59f02dfdd2f6c2deef6d89bde3f6b94c88303a8e08f318`  
		Last Modified: Mon, 06 Oct 2025 21:09:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:eeb7d4f831ad88524e20f0e7a929ca94e3269b26a29b7b205a668d02d7e1f79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d93dbbc8a0bf6c3540f40089a354cb5d0b6c994bb03d5b2dcb0a6f68ba39424`

```dockerfile
```

-	Layers:
	-	`sha256:82fd9de59682b1afd7444e424245c90fb0b8bf20a1be3a747030f2a7743d3d18`  
		Last Modified: Mon, 06 Oct 2025 23:25:32 GMT  
		Size: 10.3 MB (10326674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25a80be6852d16e9f785a7863a8a1b88bb31433b9e59eea49b2553ca572ccf1`  
		Last Modified: Mon, 06 Oct 2025 23:25:32 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json
