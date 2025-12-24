## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:56d8968a0976bcc5d099f6bdab587a8b7f8e4f8ddf3f9a67c4575989b4eae02e
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
$ docker pull golang@sha256:a9d3186b38f1eb7897ed1738412dd6947104c58d5dceefee0f794b6ecef18d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324354924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43f9f095dea25a8d6af4a9e4bc81f987103bdb181f9a9d0e22df7ee93c3fb63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:19:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:09 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:09 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:09 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3940342d31ff658653f03ce34e36d9dc9c2a16219b602445f4d585a75e09ec65`  
		Last Modified: Wed, 24 Dec 2025 05:21:48 GMT  
		Size: 92.4 MB (92410513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8ab74e427643c28187f0d3b567e6fea07c0d44d52df85de53b9ccdd7a063e`  
		Last Modified: Wed, 24 Dec 2025 05:21:26 GMT  
		Size: 95.0 MB (95037660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a66b6bee18388e3fa044b2bd0b6e7450ce0fe960925e4f929052b17dab7ec7`  
		Last Modified: Wed, 24 Dec 2025 05:21:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c60d0d34418f73b1ac94c8e701fafafcba98677a047c21a4e9bcec0a4d5cc707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f859ef09facdc7fc94bdd2790d41d5eaa7159fbaf66d08ede334a1bb5b1cdb`

```dockerfile
```

-	Layers:
	-	`sha256:7212e95ba12f5b64dffda0f4b6596576387bc8ebd8ff0c77ed15f8ea6f09aa75`  
		Last Modified: Wed, 24 Dec 2025 06:25:02 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9b32c680522deaaaadc286dacbccb0bd72312a50136ade86c0c44dbf4f0ffb`  
		Last Modified: Wed, 24 Dec 2025 06:25:03 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:622200765cb6c469487a5e470fdede155f5ee4707fc92d30024222f0ab8de7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283166152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e2c2d2a14134a4bfe4d769ad61c145bb1cb0e5719d25516d142635cbf9c510`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:17:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:17:24 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:17:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:17:24 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66aa6761aa99c557c882b6cb71cf839a06b4634c5e4d98e4a93d946b4554c6f`  
		Last Modified: Tue, 09 Dec 2025 01:33:23 GMT  
		Size: 59.7 MB (59652900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c464975149333ecd22c2b1585c6c1899694e68137e6c95424c1e8efe2e822b2`  
		Last Modified: Wed, 24 Dec 2025 05:18:01 GMT  
		Size: 66.3 MB (66276566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916e480570823a95137488489c184e78cf3bafa0a643be0c57f52f82930a006`  
		Last Modified: Wed, 24 Dec 2025 05:18:05 GMT  
		Size: 91.1 MB (91105827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1364e49f487327810042bca28f745c4be447b7f30a59d9a92db207b9e18b9`  
		Last Modified: Wed, 24 Dec 2025 05:17:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:904fef61c7f167d5fe76709cf3d466b2437fd3b5c76628c696ed0d7cdc19af0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196b5515f0f8438a80050c7196ccf50a7212e9b30c49f95c6a97fd24c43937cb`

```dockerfile
```

-	Layers:
	-	`sha256:d18134e362574c326e9ba2b1f26c7c2df5ffc642fb53c2b63083fe0ba4da7293`  
		Last Modified: Wed, 24 Dec 2025 06:25:12 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1eceb674162a051dcf14bb5381b88e6359a1f95fd329800a9d4660a7ee1e0d`  
		Last Modified: Wed, 24 Dec 2025 06:25:13 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f3a56887b8d7d3005f55ac9e89660ddcf3f28fe0811de78923c7c2ccb1844bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312933396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee4a6fe024f100ea77bd2d68658f995f6458ee7a29306a61e6badb7d87580d8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:45 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:45 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:45 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca68d1674fdc5944e0c1b040df88f41d8815ea204c1fa9ea719e94530c2ced7a`  
		Last Modified: Wed, 24 Dec 2025 05:22:27 GMT  
		Size: 86.5 MB (86490944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1a52724d12595cbdd937d1a6f8220032f161596f409cbf2928a4904bc545b`  
		Last Modified: Wed, 24 Dec 2025 05:22:14 GMT  
		Size: 90.1 MB (90113486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06aaa92b9ad22378c7d21b087b6288a64cf9acc2036000d08bc9a182e987ace`  
		Last Modified: Wed, 24 Dec 2025 05:22:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ae235b4838184d8e88a2cde7227a7fa408b69a0fd6313913c15c58cf5eecf1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403ee559a02550360cb23506943c09f535b3af77d7248674dda628538d6f1913`

```dockerfile
```

-	Layers:
	-	`sha256:d447948b28bacc962ed49dfeef33ff96179a01209e789b55450a3a009666c512`  
		Last Modified: Wed, 24 Dec 2025 06:25:22 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ade071fadf1b60d25f72f496086da029f0887f86c1bdde37418069f4e42eb`  
		Last Modified: Wed, 24 Dec 2025 06:25:23 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:6f04b9298f6e4a20747f76962bac7de06a0909e790c60c0bb419f6404565cb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323329065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cfc940c665d267f7e1773bfd701e3092bf4985f931cb90184fa974a36280d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:24 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:24 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149c3e3fb9d733e97bcc3a03363a84093198317227943faafcd54ee1bdfb160e`  
		Last Modified: Wed, 24 Dec 2025 05:17:05 GMT  
		Size: 89.8 MB (89840388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fa6b6fe890c82489ba635114b540868912dc247cb535fd5b44aa5a94fb494`  
		Last Modified: Wed, 24 Dec 2025 05:17:06 GMT  
		Size: 92.9 MB (92923502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6be93320a5a1d93ed8311b12b4bae6c7b69eaa298073e0b82b14686c0058434`  
		Last Modified: Wed, 24 Dec 2025 05:17:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:43e93efc8e3c721de052d5f0549cfa83014ae56223a1959326b984c980d33032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f5a4ede28cb80325f681aa0778b03de279abe97aa82b02b97f05d95fa176fe`

```dockerfile
```

-	Layers:
	-	`sha256:7513ebb3687916e9d55b66f102555c8a5d34eabbcbee75309be88ebd2181ce9d`  
		Last Modified: Wed, 24 Dec 2025 06:25:31 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1424eecaa63b5d620634cc0f19762b483ddd9441e52e27ce2a3a190e87e28fd9`  
		Last Modified: Wed, 24 Dec 2025 06:25:32 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:1254a244581f6024ba88a54ed40e8abb23b621c8528a3f7df0ded8a602fae82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294482305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1428e52d7333c0d7a3ec32b856b7969dca0de03cf446e357ed2033049f3b66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 21:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:33:43 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:33:43 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:33:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:33:43 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:33:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1571bb35c4ff72a581f317370ae35a4e1c5896fc868d9d6a6a545382b80d1b1`  
		Last Modified: Tue, 09 Dec 2025 15:10:23 GMT  
		Size: 23.6 MB (23613949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e7f53e0184cfbc8481d8bf6e3898908651f4106389843dddb844d4e45ba75`  
		Last Modified: Tue, 09 Dec 2025 20:10:46 GMT  
		Size: 63.3 MB (63309593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c4012ce2cba975e6e5e0c4498492dadfcd953fd94bfbda58e546a544114552`  
		Last Modified: Tue, 09 Dec 2025 22:01:04 GMT  
		Size: 70.0 MB (70017142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86ad292263f0dfa306f559c3ad322dd640eb39c35eea018d60400c403af1b26`  
		Last Modified: Wed, 24 Dec 2025 05:36:07 GMT  
		Size: 88.8 MB (88780566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a478bf6ae33c4a25f8b9d98e914c32dea75bef68209a9775898c416289423`  
		Last Modified: Wed, 24 Dec 2025 05:36:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c89ed7ee55a027281dbde75d0d7a45e4d10ab8a4d497fd516e4d8ef956f81d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2a0b1e09c0266b83fb6a3f49ef173938806ed5c5e115701b84471870f74c89`

```dockerfile
```

-	Layers:
	-	`sha256:5bcd8146657380333ad45e9136dd8ae55a8b2eb0765b1718ce793d9e70ffa93c`  
		Last Modified: Wed, 24 Dec 2025 06:25:40 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:574c5757c5a3166189f86ed26165e51225d94028eabc2e46a2b43f53293aa285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bdbd5a44ac2c130ae47b6536ac867b06878560fce1361260a263c8bb195fbd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:34:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:34:00 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:38:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:38:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcf0300c06237c12ec60c09556f95a6b8c833ba82bfc5828beb977742de538`  
		Last Modified: Tue, 09 Dec 2025 02:13:29 GMT  
		Size: 90.4 MB (90419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de3a0302474d051f06a0dba49ec72e6a84fba75a10ec5c8dcfe3ca9da396d`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 91.7 MB (91655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d464ec50c73f860af7c2680be60379908f83f71576b09e3b4f497d25e7b917e`  
		Last Modified: Wed, 24 Dec 2025 05:39:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1c542cb1531ff92b9b20877092763ff43b1f2f1bab52e35f325b1b5ff8587e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97dd8c3da9cb325454819fe77fde2d62afde10dcb53842564bd8b816028fdd2`

```dockerfile
```

-	Layers:
	-	`sha256:601377588229a457ebef35b7fcd261114e3aa406d5a19f3ef19f49a870731dc9`  
		Last Modified: Wed, 24 Dec 2025 06:25:43 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba22cb44bc92ae76dba04b858cf6c567ed21f418e9aa5b2879ea2db8558049d`  
		Last Modified: Wed, 24 Dec 2025 06:25:46 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:4e1dd257a5782056018874366240559a70dfda47419d6b8183bd9b3b18bd8d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297875033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d763b7e31c468c0fa4718347844eb250be60fc44d9cc3e00a927742fbe69003d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:36 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:36 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c78d8ef4c672ad3a1b17951daa282f21316a1dab32f99d9430a850ba86084`  
		Last Modified: Tue, 09 Dec 2025 03:00:20 GMT  
		Size: 69.0 MB (69009858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eae26383a5ec3ad19d41ec233e74f5aea1ebfab7013779b5b7f518483b785a`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 94.2 MB (94198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbe8d902201377f19c9a9288c7247ace24f89ad72ae429f340f859fcc58bfe1`  
		Last Modified: Wed, 24 Dec 2025 05:17:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:04bcd0b264bce4e6346fe7c1fe08cdf3a106985072e7fcde29af9a27b406e69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ea109948f990096f7010cffa8001b32c682474d3d4b815cfabf8099decd343`

```dockerfile
```

-	Layers:
	-	`sha256:2ced991d0c4f2c8d138551e124f6f6eaf5aed41deef7528cbd7a1969c21e897b`  
		Last Modified: Wed, 24 Dec 2025 06:25:53 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9f7b019572297f4938681c6cf403ed0f0ed55563690c3f980e9947d32f4c1f`  
		Last Modified: Wed, 24 Dec 2025 06:25:54 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
