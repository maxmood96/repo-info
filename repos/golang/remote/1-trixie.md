## `golang:1-trixie`

```console
$ docker pull golang@sha256:503c84fd135f0d9bb9fb3be1c9ad0524fdba1d06ff81c79ab1d013cf474abe68
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

### `golang:1-trixie` - linux; amd64

```console
$ docker pull golang@sha256:b53c282df83967299380adbd6a2dc67e750a58217f39285d6240f6f80b19eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312090118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827331d697aaa7923ff6b6c107edf772875f40b58cfca6c3ddfa155668ce0edd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c21dfbee0a20016b8b6053efb4c9a5743bb9373bbba6d9f2ee60ad9e53914a`  
		Last Modified: Tue, 07 Apr 2026 21:13:55 GMT  
		Size: 102.2 MB (102169242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e102291f75c96b251bde878d5163a895f883816bbf6de39810b683e3770bcd`  
		Last Modified: Tue, 07 Apr 2026 21:13:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3340745fb7a4003d8caca3f42cbade10278d1f7d1044c0ed9df13d449bd228b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd76e654f6c56d681bf39f1a7eb65701baeec469239351457bfc55ee13ec770`

```dockerfile
```

-	Layers:
	-	`sha256:c95af664400165b8bc6d32fc7367416269ca11bb08427a035c947067e041db46`  
		Last Modified: Tue, 07 Apr 2026 21:13:51 GMT  
		Size: 10.8 MB (10787049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f76e3f8de8a3a68bb4b55990380a51d4a5ddb13c7d5c6a084e97e04821d4495`  
		Last Modified: Tue, 07 Apr 2026 21:13:51 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:196c026b69a111385dfb76ff582e88ea82c3f485a3420a61cf48ba3efe53629d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270648911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb28ee3495e98f9caba5942ea0f5bac219d4c51d1e5b966cff79748de1218299`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868f799858ac0f14507e60a2ff0757894394681e874e60066914254664b5431`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 62.7 MB (62722704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f430503337b9d8f480cd5d9711a173d70c7ca8704a38c2fb9eeae92400af99f2`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 72.8 MB (72805104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e102291f75c96b251bde878d5163a895f883816bbf6de39810b683e3770bcd`  
		Last Modified: Tue, 07 Apr 2026 21:13:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e49f732faf5cc4ae2f4dbf1ef8a469b252ca3f74767db3a2dd2eee172f7e49b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17741310ac282094016c983c7c3ff417f2492fd04acd72a737d263c7b584541`

```dockerfile
```

-	Layers:
	-	`sha256:1ebfed8aaeb6cdb3a117e95576db45287d43ef23c658fdd015926d004c45808c`  
		Last Modified: Tue, 07 Apr 2026 21:13:52 GMT  
		Size: 10.6 MB (10582968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2103c0b2958fe39e214bbacafb571248200e17a8f37e486573179735ffe472`  
		Last Modified: Tue, 07 Apr 2026 21:13:51 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e920f0b89b2305c72a5e2b5d52b0e18cb37c060a28f48c7b986ac3bcbb33cf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304699627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1daca594364dbb9c70b9037c94da617ab3b4f829d3af8a43664a8521c854d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:13:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:09 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:09 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:09 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214ffd6c2ef841a75e5b236324897e6dd38519ab1dfd0e465f0b9d2bfb617a1a`  
		Last Modified: Tue, 07 Apr 2026 21:13:45 GMT  
		Size: 98.3 MB (98309886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec6fabf96ca3ec3e3e3edebc30113ace8b8adb683c1c0aa265eb0bab599f79e`  
		Last Modified: Tue, 07 Apr 2026 21:13:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:94c64d601576d84f3c7e10f2282052248110c7aeba65237b20d71bbeada30049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962b4d3f506280f949b9a25f351c597bca223a7448eff02cd5e9e9b91f304a8f`

```dockerfile
```

-	Layers:
	-	`sha256:8e142eeecf94be00b76411c7a2b6b0a3300d5f105db026f46bb31a730e575b0c`  
		Last Modified: Tue, 07 Apr 2026 21:13:42 GMT  
		Size: 10.9 MB (10907552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d18d6f15d213c9b79c48dcaa43b6fe5ce990c6322a8c1f5bea89f73e8ef87e`  
		Last Modified: Tue, 07 Apr 2026 21:13:41 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:5e650bb55e1f0ddcc07aed98b0c4178f80438d84d214ded1469cbf0c424fdf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313547577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020acefad9c95209a2c8d2e5278e5815a4b033c2f002d0822ce89df6fa0dc95f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:26 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:26 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:26 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422a0ecc8495d593aaa5a4fde885dda355d5068b9a580f7b63db08c09cef995a`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 100.6 MB (100607883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b26e2b59e2659356bd5578e828909bb73ed81331ef7ca1d52f14c03bc6426`  
		Last Modified: Tue, 07 Apr 2026 21:13:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e7e0b24693d9dbd576b3bf45cb9b4b87773581404a0757ea3bb0a4dea64f478b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f774d575a898f5c1e8b2321293af612effefbf2d8b7f4fd91a26c88311e69a43`

```dockerfile
```

-	Layers:
	-	`sha256:d74312c80937410369bbe4de56cd8ae0657bc058fedd00772953671916b31b2b`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 10.8 MB (10758292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756dc91c194b1d368e4a299c22fa24733d97204d814ae9c7b0792566aedae482`  
		Last Modified: Tue, 07 Apr 2026 21:13:56 GMT  
		Size: 28.9 KB (28896 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

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

### `golang:1-trixie` - unknown; unknown

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

### `golang:1-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:cd849a9e37dd46e231aa571cb623028fb7d039e2c8efc8994cbfed5bcd7cc8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336137796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3c9b7e9b9e39705c8662927b7724683a4669dcd1a46eea0f14cad87493634f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 04:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:00 GMT
COPY /target/ / # buildkit
# Sat, 21 Mar 2026 04:55:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 21 Mar 2026 04:55:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9a450c15c86147b6c308f2cb25a618ec75f2ab5a64203aa728b5e309ab137`  
		Last Modified: Thu, 19 Mar 2026 05:35:26 GMT  
		Size: 66.7 MB (66662504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c3d8cb0eb3839f60f443c07c78a4e233d415f3d669a49057b1e5f1b8cb424`  
		Last Modified: Sat, 21 Mar 2026 05:03:52 GMT  
		Size: 131.7 MB (131650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7741c0adede1d2e9597a871420fa82f196151039c468eac7755d531cfe50922`  
		Last Modified: Fri, 06 Mar 2026 01:18:47 GMT  
		Size: 65.1 MB (65077505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dff05e9819213f71b22f7567f2c8916e2376c427d497f569ee32f29aabf3664`  
		Last Modified: Sat, 21 Mar 2026 05:03:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2ca6fbc82401dff6b5b081d4881d5fefcc3a0b9bdb2a62efc73bb4d43d2198a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743b9a83cae947c4be7d249f6eabbd59c3002896e8a6019870a3c321ddfec87c`

```dockerfile
```

-	Layers:
	-	`sha256:ca357689676e204f5d5da2a78aa60752372e8088702996e65fc2310ed1de4470`  
		Last Modified: Sat, 21 Mar 2026 05:03:33 GMT  
		Size: 10.9 MB (10856694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde22c1c7f07ee804fd0e9640554445e890a987413a1e4437eb622c167fe5583`  
		Last Modified: Sat, 21 Mar 2026 05:03:30 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:ff94c77ba0f042d7199ca2dea6ca43320f291895bbd31f59fc18cf7504317558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287210304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7805980d38c1786072e16f599d28404c90ac0b053c122c00904d55f164d41b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 21:15:54 GMT
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
# Tue, 07 Apr 2026 21:16:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:16:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b42c01b5de7637ae2e011d2f9775f913b01f72b9797773d410bb0d8b437e3`  
		Last Modified: Tue, 07 Apr 2026 04:55:14 GMT  
		Size: 68.6 MB (68627207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d238309bad3a5eccfd4206504a4b2b322fc3d481e6d5359ad31c9f8e286eac`  
		Last Modified: Tue, 07 Apr 2026 21:18:30 GMT  
		Size: 76.0 MB (75982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b09e017f650e851e83fd70dd5ad9f39437719c345bfbf8b3b97929b4f7edda`  
		Last Modified: Tue, 07 Apr 2026 21:18:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1c06d6c4e88ac9f3637e5de6db2ab81fa8c06def619a3c97f36a68193641e427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cdda0eb5da0b47b4ce3ce4bc7884bd65b58c2b6cc3d8abba3cf2e789eb0027`

```dockerfile
```

-	Layers:
	-	`sha256:2af3c7cbc79dadb4493e8a8c5ae2f8b0a4736f4bc9cea1480b98fd206d0c4e1c`  
		Last Modified: Tue, 07 Apr 2026 21:18:24 GMT  
		Size: 10.6 MB (10597449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb27f3bf71852edd9d711f2a9b7fbaaa07a34a659ac62c04b6d29d68d7c8cd6`  
		Last Modified: Tue, 07 Apr 2026 21:18:15 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
