## `golang:tip-20260103-bookworm`

```console
$ docker pull golang@sha256:6d0e6dc7e568f2e25a94305aaaef146e3ba27c22997735f7cd349e79b973cfdf
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

### `golang:tip-20260103-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:c4ed14eaa2d2ee572701f62553cf41ebeeaa4f35ed961c3538954ba13f5317cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324365633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a81647113abe92426ceaf740f993e423af5b6677bc204c2881b84ab6b6fead0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:12:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:50 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:50 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0f1fcd0ffcdd8a107c92a0e63f4cf34060119d4cfec78fac522a6a437457c`  
		Last Modified: Mon, 05 Jan 2026 20:14:44 GMT  
		Size: 92.4 MB (92410539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8d0c9ecfcf551b6bfe3152ed041603d59cea546df67e4bc43073bc9a2f5e7`  
		Last Modified: Mon, 05 Jan 2026 20:14:07 GMT  
		Size: 95.0 MB (95048707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd14aa30c389871abadcad008aa3283025268c931dc9b3d6e4072a6abf2d51a5`  
		Last Modified: Mon, 05 Jan 2026 20:14:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c7df0b8112a2225f46cf5c598026367c581316b2f16bd48d6081396e9a1a93ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ac34b22d9fa9e82cbf251ea991614d861f8258e3b0ac02430a815ff29b617b`

```dockerfile
```

-	Layers:
	-	`sha256:a391cb0e962814ca4ca95857e8ab48be0b4350d5fcf5008e1da1a255ac5d43e9`  
		Last Modified: Mon, 05 Jan 2026 21:25:06 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2256852dead760f6c8a1f448966201175d40d17ba8f6a39ba537547192b1e9`  
		Last Modified: Mon, 05 Jan 2026 21:25:07 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:ee5dbbbf4321340ac87b3ceb7b4e484347a0d843c0a2eaf22660989542028774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283186222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a0a1e770a6d1e6e6bc7958c641491c292c417a6835d65bc409a5662d794853`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:16:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:16:47 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:16:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:16:47 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:16:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:16:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcf81dac4189b5947ba08040cf89b3ba0705aaf8d62020c9fc0bf6f26aefd4f`  
		Last Modified: Mon, 05 Jan 2026 20:17:27 GMT  
		Size: 66.3 MB (66276495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e6b96a7f28bc62643bd07c2486d1581cdd92ecf9bab96beac98ff164054e9b`  
		Last Modified: Tue, 06 Jan 2026 02:36:10 GMT  
		Size: 91.1 MB (91126293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e47e270320939a6c75577f628a4c964ee3ea75fb056f8d7debb21cc380340a`  
		Last Modified: Mon, 05 Jan 2026 20:17:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ee5aae226ab0a2900ae3370f7487c825a0622051aaae71534d36e8e6dd482c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7815055f702269daf41567905b801d83bab282f9df89604d2f6f0f4522e04c`

```dockerfile
```

-	Layers:
	-	`sha256:3bf6547f911af1af72a8dac21845efb1396878c0fd066cbadac5d1289659c24c`  
		Last Modified: Mon, 05 Jan 2026 21:25:17 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d09c558b2267d63bbde4e00592e9d405ae6c67df7a9a681905ec84741ce8c2`  
		Last Modified: Mon, 05 Jan 2026 21:25:18 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:351b1c096e2ee30e2467b6cd89fa79cd8f46f73b459175db70ebb5a910ba9c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312954302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94a6cd1e9d60103a3b3197b44cf537dcbdcbc2199d806fe0b852e33ea4f87e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:12:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:41 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:41 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fac5c0e82f6d28aee3cbb551bde90df81aaec3476638fd30e3e1978e40c8694`  
		Last Modified: Mon, 05 Jan 2026 20:14:30 GMT  
		Size: 86.5 MB (86490981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea799c03d09b63583e3ebd313f2aacd577c4821e87f618e936a7b9c3c7ca14`  
		Last Modified: Mon, 05 Jan 2026 20:13:38 GMT  
		Size: 90.1 MB (90134470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6dba97d28e139d3cd9632e7e1e09386e291ba7e8b089202be614583fd649a`  
		Last Modified: Mon, 05 Jan 2026 20:14:19 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3593b3792c8884494a018f131c5af063edb7c97e6afef0efd1bd9193795e0069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fd59ccd6b430403c71cff26fd0a68bdb23e00bc8707f39605b43eed300c46b`

```dockerfile
```

-	Layers:
	-	`sha256:016542c62dbb5efc405dd9fa02045109bbcb53feebb5c091044546ba5ddd86ba`  
		Last Modified: Mon, 05 Jan 2026 21:25:28 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8634703947cb5f220a40f88a74f3bf08c0be21a9f748309bb61b96eb744e9e15`  
		Last Modified: Mon, 05 Jan 2026 21:25:29 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; 386

```console
$ docker pull golang@sha256:51e348af021e664e64fc2a5dea9bdb2eeebdcd17a8aafdb6edd5cbd43733ba5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323349521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc2db54f75f2652fc09bf72e76d0133b4d6b82eb2270b4dfd61d298ec0d4502`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:15:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:15:48 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:15:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:15:48 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:15:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:15:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63bb42155eb2fe3cb6496304c20382db95885b672da0e34a3fffa188861a6ec`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 24.9 MB (24864466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10eedb7d741cb151d52259302acf62c6c98590a9a4168d4370619e890f15715`  
		Last Modified: Tue, 30 Dec 2025 00:32:36 GMT  
		Size: 66.2 MB (66233282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6520ac6aac07cdb97ed098828f2c246eefa980726bafc96aa93430b75d4fed`  
		Last Modified: Mon, 05 Jan 2026 20:16:32 GMT  
		Size: 89.8 MB (89839925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7adeeca0c05b570f562d36e2ca80fe92bff9d338efdfb31d2c7a616347bb0c`  
		Last Modified: Mon, 05 Jan 2026 20:15:35 GMT  
		Size: 92.9 MB (92944811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6a1220234953fefc6670dcba86859c38beb65c2d5338dbaaea4c86eba3378e`  
		Last Modified: Mon, 05 Jan 2026 20:16:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5540a7046a1d5d7017798c9c7941630541471a7a46b493fb3367482169122501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4df8dd5b12ededb301cb5689133ae145307ecfbe364e12e24fd0b2f3e0a7c`

```dockerfile
```

-	Layers:
	-	`sha256:4236c970a4d7960eec8c52998045666f17e64eab117d6db69af301db5a5389f3`  
		Last Modified: Mon, 05 Jan 2026 21:25:46 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb51c1152a785a0adfd6a7fae970ba8ff3153ce5b0c7d377dd51ca47c5730f`  
		Last Modified: Mon, 05 Jan 2026 21:26:04 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:8ce9e0dc7f49b945d72085d36189f6ce81699c0cffd0931cdabf934705dad4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294512730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489e6970ea51eb1f0c082f3c166e6ee1d6a4f4e826a57c592eb2d4b3f7366472`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 11:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 18:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:31:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:31:50 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:31:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:31:50 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:32:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:32:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a43d59f754c088126249c7de1413be451574eda24274414bef9aea85a3ac886`  
		Last Modified: Mon, 29 Dec 2025 22:38:14 GMT  
		Size: 48.8 MB (48760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec26c7ec0c76b4716fe076707c8489ced71c06858c4f9f03f18c306cb4344cd`  
		Last Modified: Tue, 30 Dec 2025 11:50:06 GMT  
		Size: 23.6 MB (23613812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2269474ce0b0fca7a225e6021a034ce6b526a7a59bdba22d740e8cee0614ec`  
		Last Modified: Tue, 30 Dec 2025 17:14:42 GMT  
		Size: 63.3 MB (63309491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89852c6abaaf7d3796bc5819d2aedcaf5c64f4004295c9c5b5f990b11c07ba`  
		Last Modified: Tue, 30 Dec 2025 18:23:03 GMT  
		Size: 70.0 MB (70016959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546ecb7ce7ed01bc15e9b825bf83bab14e8ded6a008d4f22ada02317b21e5f54`  
		Last Modified: Mon, 05 Jan 2026 20:34:21 GMT  
		Size: 88.8 MB (88811385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1d8270e45661251cade0912fe0729e2ae19414a102d878582c5544508fbff3`  
		Last Modified: Mon, 05 Jan 2026 20:34:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:500845f0cb6f41f066afa89e718c9bca42829d08bf7a26e98695a0807db2b64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f151155c03e6a53f7f0d9fc0f1c1debd643fb86c2211576d5c08a014457c881a`

```dockerfile
```

-	Layers:
	-	`sha256:1800d90829f3d89a51e6bf0f4c13274d93169feb16cff8e383aa705d5574f168`  
		Last Modified: Mon, 05 Jan 2026 21:26:12 GMT  
		Size: 27.1 KB (27123 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:7d516e62f6da06db9d05d466d6cefb77700e13e4df7e0c5abeee5d22e3bb4bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329945323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f86809568c5d710e3596e7aecde0adbce225fef5b6bfbd261a48c754d602276`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 08:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:13:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7517c515ac5fd6799cec288b72512b8ea3fc54d2d37de5af54d06ba0ea2f21bf`  
		Last Modified: Tue, 30 Dec 2025 01:31:20 GMT  
		Size: 25.7 MB (25672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff2cfb691fedcba1692cb13fd0632001d1a876833f4cd2aa52eba87257a8f`  
		Last Modified: Tue, 30 Dec 2025 03:17:48 GMT  
		Size: 69.8 MB (69845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3fd09a1e6774e533a42b26351be92003f5bdea475b8caa70173ad58b79d9f`  
		Last Modified: Tue, 30 Dec 2025 08:43:16 GMT  
		Size: 90.4 MB (90419830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0091ff10375737167c3b5f9f5d9decb460a2e2aef6a9ae134067abb7cbf2b`  
		Last Modified: Mon, 05 Jan 2026 20:15:39 GMT  
		Size: 91.7 MB (91680642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ceb1c604e886374029d4147565c0001f8016321f5cfd6f82c9d05220c0db72`  
		Last Modified: Mon, 05 Jan 2026 20:15:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a02abc7bdb5b64b1a579f914d092169d4429649c30e96b1ddcc606177972cb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58feb3a696386d5b71da27c09b8ccc9dd1c1df022e5666edec10c3efd10b58b`

```dockerfile
```

-	Layers:
	-	`sha256:e6ec2a29de2413a107877630a68a348d4d6db9761d26dbdb8f2c869ebdaa2a87`  
		Last Modified: Mon, 05 Jan 2026 21:26:17 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03cf2ab0b5e2de6a0c2b10c82cc38ff8aa1d20f32e57de4b46b08c018b5c829`  
		Last Modified: Mon, 05 Jan 2026 21:26:18 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260103-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:778a3e08122540259d083b66c1e3bae119ac6aca77b9384a961e1e7fc0a6e2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297901620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc390e45fa16714bd9b2d1465989c88c6b3e9ea960359642005729e116f6a61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Jan 2026 20:14:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:14:09 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:14:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:14:09 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc4c1479120c6249296b3550670caa7738ba389b23a7ca3973f7732c12c0ab`  
		Last Modified: Tue, 30 Dec 2025 00:42:34 GMT  
		Size: 24.0 MB (24027124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d337299523414af9c112b1b1a1d201a2c6eaec2baa26798cdadeeaf575ed2`  
		Last Modified: Tue, 30 Dec 2025 02:20:20 GMT  
		Size: 63.5 MB (63501425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cade7c11e2a384e856bb2917369c47ddecd37868c2ef72ed6042a2765c4308dc`  
		Last Modified: Mon, 05 Jan 2026 20:14:59 GMT  
		Size: 69.0 MB (69010692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c1a057ff0ba348d0b96ad5fd481980beed6ee225e3440d5e3c814a12014a9d`  
		Last Modified: Mon, 05 Jan 2026 20:14:55 GMT  
		Size: 94.2 MB (94224494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37826ac07e3f30f5969f8ec9fb46f37ed130df84cfcbcd4cab7a5339058b9edb`  
		Last Modified: Mon, 05 Jan 2026 20:14:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260103-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a36754aa42d053fd48f04f1332a5e5418c76c6026042f1058ac91151d0c2baee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275c051a1c3288623a6ef631d0762c79b7203bbf617375c4d33f00c122bef54b`

```dockerfile
```

-	Layers:
	-	`sha256:b2ac69de44f236c863273b9e5bfe839bc8ddba677ac2699bafcb2b03a4b0dbdd`  
		Last Modified: Mon, 05 Jan 2026 21:26:27 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea837acd1cd2547e4199faeba7b81b85672c647b3c66a9c52688d5de1bb3f722`  
		Last Modified: Mon, 05 Jan 2026 21:26:30 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json
