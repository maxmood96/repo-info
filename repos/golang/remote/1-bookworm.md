## `golang:1-bookworm`

```console
$ docker pull golang@sha256:10f549dc8489597aa7ed2b62008199bb96717f52a8e8434ea035d5b44368f8a6
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:57c2a5d8fa190d48c3ab19374eee0df78766263072c99c8d569c909335212f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 MB (308251846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca47f4a3f6a6dae115984e55d027898e8cf644fed7504413a57237b66d7af95`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25547fc71e9f6774808379879cd076212b14a7beb2a2c3e74cc90362bc6e3fe`  
		Last Modified: Tue, 01 Jul 2025 04:13:14 GMT  
		Size: 92.4 MB (92355023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca80243f8c0be71064de84e6e95775bfaf315e1885a99ee49f422a3b92c222`  
		Last Modified: Tue, 01 Jul 2025 04:13:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bee38e4687cfbd74a8fe601fd18245877e4a06ffe9966048f38e5b78dc908e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10534067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9782eddb761bd61fa47e55c1e46a6df16a38cdcc16f3d183506ea7ec549058d`

```dockerfile
```

-	Layers:
	-	`sha256:9aef17a8ddebe15f5d6c27b84235e900f3e0787a99d6ceb420f3e0c7551e5c7e`  
		Last Modified: Tue, 01 Jul 2025 05:22:24 GMT  
		Size: 10.5 MB (10506421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe089fb5e931249d4ba78c31a7ebd17c6f8239dc7dbed4a2c120ba485a75d2bb`  
		Last Modified: Tue, 01 Jul 2025 05:22:24 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:89b9c01c9798d02d15cc19413db1b0ccc48b4e6deb0ce39337bbc206d543a774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269145910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7631526962b3c550889f6e47cf11ab85d211d1ad58bd58bb3110f926742f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db66a5672ae3586307aae98741965819f3d140302c02b7d781087e66393285`  
		Last Modified: Tue, 01 Jul 2025 21:45:51 GMT  
		Size: 66.2 MB (66208443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85bfbdf71cf85fdaf7b2ee6dbc14e4e8d98555632cbddcdb88970f38d7c36b`  
		Last Modified: Tue, 01 Jul 2025 21:47:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8d9c4fc97dc29d7cd3ecbc7cc7ba9a25bb2545305225aad7fdf99a08f6efefe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fad1b73ab00d6486382508098b2bf7465be081eb31d49e2b43cf4bda3b29c9`

```dockerfile
```

-	Layers:
	-	`sha256:9b0fe828df5eda10222cc8d57ab15975c55711dba2cd3647f1a94a5e0860f072`  
		Last Modified: Tue, 01 Jul 2025 23:22:28 GMT  
		Size: 10.3 MB (10313145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d871f0216cdc4ce54e7a0c095003e1c2372d04cb472ef710e298e2427c8215`  
		Last Modified: Tue, 01 Jul 2025 23:22:28 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e7a673a41cb5cb8c083ea3d9b7a79f611aa23303f44d0dd47d4e217c7f34a72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297917489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17fca0b78aed7c905ca57c4ba0b1f30444485dfa8a47132e467775d61f57e86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5af7432e9cb22948c121a098c8ad7dd537312ccb8756deafc1f7970fda5bc7`  
		Last Modified: Tue, 01 Jul 2025 17:18:12 GMT  
		Size: 86.4 MB (86425700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9106da882bb6c4352bd75a3b17f5a07386fd4986331b7e2de27bc3950abb21`  
		Last Modified: Tue, 01 Jul 2025 17:19:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0b338dd1665bf8add93be8e41b1bc843553e7d4fad3213a66ff368b2dfd3276c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10562145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e179205a2953ac179fbc8850f46a6adc18b3ff4cf2976d640f6a6d2f13acec00`

```dockerfile
```

-	Layers:
	-	`sha256:20b198d9a4a99fa7aea7ecc475741b273c4670bd5e6554f307c03813d84f41bb`  
		Last Modified: Tue, 01 Jul 2025 20:22:33 GMT  
		Size: 10.5 MB (10534317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d971fd3e1756346995236611ac1f376a8f6238c9f742b4dc26c5b3e2b7f3a041`  
		Last Modified: Tue, 01 Jul 2025 20:22:34 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:f981a85e7f0c5ec2b0ecef4a9746db2fe697f0d2fb90844824c7b7f8aa06c428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307234854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9766fc9ffa7a4df02128363754dcc5cc231e5f37406746ca539b5086a873f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34bb265d7f6a754cb336f97d1d43f0e1886057d4208fbbd1ff08364f76f6d4b`  
		Last Modified: Tue, 01 Jul 2025 04:13:08 GMT  
		Size: 89.8 MB (89774446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8c216dfc7d21900a97bb4a53779d234444f879ac32bf359d08ad7a1d1eb6f3`  
		Last Modified: Tue, 01 Jul 2025 04:13:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f5ff28a8a5b8f9aa3fc20425a82dc10bb4c6842135f00ae42215a830a9add990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10513546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda66c3ccb936f0e48b1f23c6eec6302d1511c0aee359b59e3d783aec7d6a879`

```dockerfile
```

-	Layers:
	-	`sha256:76f78602b22bc79df27461feb6bbd74751bf5e297f655330223dfb98aaefbe2b`  
		Last Modified: Tue, 01 Jul 2025 05:22:42 GMT  
		Size: 10.5 MB (10485957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4778976200f400d2bd6aee2f459a4ca9ce869b7403d8a2516c412f8e4a2f8a9c`  
		Last Modified: Tue, 01 Jul 2025 05:22:43 GMT  
		Size: 27.6 KB (27589 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:4c107fd6a76a4698daa1ab1beec34ce6eacc27bb676baf28cc5d2a34b661a1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278562317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b34f33fd1212593ac80c74eb24b5b313ada97b3b38cdbd59edddf22397941b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99debc858569995ebc7f6d9290cbc19f540a471b716e06514603892b92705c6c`  
		Last Modified: Tue, 01 Jul 2025 01:14:35 GMT  
		Size: 48.8 MB (48775546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158647b6db84897a383ed457f276b7c4d602a99d74b1c159bd2c138fd994fd1`  
		Last Modified: Tue, 01 Jul 2025 18:49:08 GMT  
		Size: 23.6 MB (23598851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ea11d1e2f3faf8589ad741098f10976c65ebbdefe26521e25ec1f6abde856`  
		Last Modified: Wed, 02 Jul 2025 03:03:00 GMT  
		Size: 63.3 MB (63308526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101e074dfdd957bfcc26997ac19a46968730be97837b2a8da82e402cd8790465`  
		Last Modified: Wed, 02 Jul 2025 11:23:33 GMT  
		Size: 69.9 MB (69945665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e8449b0f1eec02691482cf8a405aeed88398feceed91dd2882173d43b2ff08`  
		Last Modified: Thu, 05 Jun 2025 19:30:59 GMT  
		Size: 72.9 MB (72933571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c3916f36fc098c7fea7c0b5d570e820ecff60eafa474fbe79fd1a92b3134cd`  
		Last Modified: Wed, 02 Jul 2025 09:44:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:19c846d4d45f24189e7fd0b890648dfac4a05b28d9d722543c28cc737753c910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94880407ec4f39d72dfa4b8e1e13801dff793ac9ae9c62cd0bf06bff8394879c`

```dockerfile
```

-	Layers:
	-	`sha256:83eb454b2aaeed54ac98d6aae3375d552380168011491db42fbfdf7749acd7c3`  
		Last Modified: Wed, 02 Jul 2025 11:22:46 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:40de09e51095d03b9c947c1b7eb04d720ed923f59d34c7e5d0fba5f27c8bba30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313758765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25a67abe3b1a02e574aa8967010a670f9277b68c21d3e281024f20f26b0a99c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7a19c2e3e967726562c175307372b4ea465a8ab27cdf3b24df05b8ed8bffd0`  
		Last Modified: Tue, 01 Jul 2025 15:10:38 GMT  
		Size: 90.4 MB (90370094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857e797654b7f586891362befa86842c081cc043ee887ea9708f0fb0ac7c27f`  
		Last Modified: Thu, 05 Jun 2025 19:28:59 GMT  
		Size: 75.5 MB (75547589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3894d9392c88e392ee47cde0e8ae6cf186522be82ae0806d6e60840b26376a`  
		Last Modified: Tue, 01 Jul 2025 15:12:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e565abe3f232a408310f2eed199cffa3b7333cf1a997bb4688daac8d2e946171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10506668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c543e70df8cd4fd0ac9e57fb8cb48758ef575ebbdd4c233c88b6cc2bfb1c5b13`

```dockerfile
```

-	Layers:
	-	`sha256:be7b7410b3d8393f59d77a2658714bf4d37f90df5586ea3b7baacd499f853b68`  
		Last Modified: Tue, 01 Jul 2025 17:22:49 GMT  
		Size: 10.5 MB (10478950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5386a24925da96424719d2300a92aba2584e1c39d87896e333ad4915ef2feead`  
		Last Modified: Tue, 01 Jul 2025 17:22:50 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7695097f56b6be4b36740009955e33801352ca1b85c004d5a0468472cad042ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281414039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d300a750ba83f4f3ebbc30ecf5b1a62e801f9557bf99a2dcdf04d0a7e722d4db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae47c11c46102ab7ff9335e654c0977270faf61319eed0a1a51e7f85f25cd0`  
		Last Modified: Tue, 01 Jul 2025 11:37:27 GMT  
		Size: 69.0 MB (68958019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14182d78ce72a37aa9fbd4fe4a033502956e576c76e8aecb7ce69961caf57f90`  
		Last Modified: Thu, 05 Jun 2025 19:28:45 GMT  
		Size: 77.8 MB (77788070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5129e1a0a908a20ece7bd65d67f3fe4511e6735683b527cfe78a2e510188a6fe`  
		Last Modified: Tue, 01 Jul 2025 11:38:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0695f3613b300adaf92c77a618b79eceba4db399902a95a8a37435b47730d23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10365824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a35c10f23076b008c46358af92a04e04b675ce684bd712ea712ed3be1a1e6a`

```dockerfile
```

-	Layers:
	-	`sha256:df0c034da4499799973b33e01ac2a897daf4f3e065cd79eb91f900cd95cd5761`  
		Last Modified: Tue, 01 Jul 2025 14:22:56 GMT  
		Size: 10.3 MB (10338179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6713aa7dec9fc190a446267b3573743955a49eb52b90b2ce198048e8798bcf9a`  
		Last Modified: Tue, 01 Jul 2025 14:22:57 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json
