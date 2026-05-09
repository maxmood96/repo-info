## `golang:trixie`

```console
$ docker pull golang@sha256:d08bf3ed2bd263088ca8e23fefaf10f1b71769f6932f0a4017ba28d2a5baf001
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

### `golang:trixie` - linux; amd64

```console
$ docker pull golang@sha256:6b3de2e6b4ccfc5fae404042cb1a025b1de13c73458e50455e3143bf12e98eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312227659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73204d15b474cccdcf60645cfc88bf3d8d68cbc1687334c70f66bd03832e8259`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:44 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 21:17:44 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 21:17:44 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 21:17:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:44 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 21:17:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 21:17:47 GMT
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
	-	`sha256:ffbb3703a2aa697a933b170b2ab225d727b803f4eff1bd3423ce38ae9713f49e`  
		Last Modified: Fri, 08 May 2026 21:18:12 GMT  
		Size: 102.2 MB (102227786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4544555c883ce51283cb378e30bfb396dd381db672b9d53338268d712c4e0f`  
		Last Modified: Fri, 08 May 2026 21:18:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9ce2a003994ffc31651060d62c5901217f9db0b22b149ee6b50b4697da54aaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90151fc90a04a76c31563321cf4572cc432334f0e6cf81e4c702d6b2ea314d66`

```dockerfile
```

-	Layers:
	-	`sha256:0c85f27c1c9909bdee505c7dbc21a633a91c6966677ff9635fa0b6d913441293`  
		Last Modified: Fri, 08 May 2026 21:18:10 GMT  
		Size: 10.8 MB (10787103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e79d4ed2df45e0811ce0274e3e560a534ad00fb1b8200971cf336c9ae048400`  
		Last Modified: Fri, 08 May 2026 21:18:09 GMT  
		Size: 29.0 KB (28952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:5644c90f5601600190b2b169dc1820cefaaa0fe3c195d90c5e0bd713454c2a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270756890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3204e8643dcdeae1013165c81f24e079b75cd2235763e109185913fd5e51cd8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:12:54 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 22:12:54 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 22:12:54 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 22:12:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:54 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 22:13:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 22:13:00 GMT
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
	-	`sha256:a45ffc67e0a58f78ed4d434853f5ab3d6c3b1e498ef96a04e9a5c965fcda069e`  
		Last Modified: Fri, 08 May 2026 22:13:24 GMT  
		Size: 72.9 MB (72867391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e7137c96fc07d2fc9e87f7cec43a327dd6c1385057f6c469907ef731cca2c`  
		Last Modified: Thu, 07 May 2026 18:01:49 GMT  
		Size: 65.8 MB (65786476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2b80efa7fa2b093e7c8b934f0ef9c24cdc3c01b302bf0d7e99a6fdd2e29e7`  
		Last Modified: Fri, 08 May 2026 22:13:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e8f08af2302b4fe4697a3ff27e14264f021b397990caf8b228149766de4202cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85b04d49511ac3fbfb8345867ecc9819476776adc7209a33539c0105126dde`

```dockerfile
```

-	Layers:
	-	`sha256:e213330c9a74eb9859cc6b01234980ab5ea87b9ee31c6500fa73729fdeaf72e0`  
		Last Modified: Fri, 08 May 2026 22:13:22 GMT  
		Size: 10.6 MB (10583022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c34dd901618675f21464246ac1745ae95a2d3b3593fb150002acd68ce7aa8f`  
		Last Modified: Fri, 08 May 2026 22:13:22 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:34ee7df46fb1743876b072acc9f876cd63d0e67021f30ed46bf62b3cb001b1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304825366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee5480078c6fad9ee74104759667f527e2051d2c461c6428157417fb4b3fd58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:25 GMT
ENV GOLANG_VERSION=1.26.3
# Fri, 08 May 2026 21:17:25 GMT
ENV GOTOOLCHAIN=local
# Fri, 08 May 2026 21:17:25 GMT
ENV GOPATH=/go
# Fri, 08 May 2026 21:17:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:25 GMT
COPY /target/ / # buildkit
# Fri, 08 May 2026 21:17:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 08 May 2026 21:17:34 GMT
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
	-	`sha256:105e5a1c75581c5ff16b35adb3d9b77532451534f72e2a73e8564235c7bfa6e1`  
		Last Modified: Fri, 08 May 2026 21:18:01 GMT  
		Size: 98.4 MB (98372447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e8de87f0b174c8517e3ee006efad91e8ead1353dc5e0172b06b9a659f985b`  
		Last Modified: Fri, 08 May 2026 21:17:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9c7ee59f1799481ced65fbeaa6472dd7c28183936355cf24553a3a331e7f3883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f67807aa8db18f0d3cde35a99a2bf2ce219362c8d9a69908b0df0ea084f578`

```dockerfile
```

-	Layers:
	-	`sha256:e7ea7aaff795803bbc5dcb17a4036cb51a6ea8e866a924fbaa98c6043c9b7355`  
		Last Modified: Fri, 08 May 2026 21:17:58 GMT  
		Size: 10.9 MB (10907606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bb313c4317bbb17a398979173f2c60a3d093c2d98f9d9858ea69764d482690`  
		Last Modified: Fri, 08 May 2026 21:17:57 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:6e2019adcc0a26cfde417375eb90cb8b9ac53319fd6cc8774512e4b7d0162950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313695256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f275e586f06317908b04200d15a21d348857a188cdc3542cd221d638d389b9ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:25:57 GMT
ENV GOLANG_VERSION=1.26.3
# Sat, 09 May 2026 02:25:57 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 May 2026 02:25:57 GMT
ENV GOPATH=/go
# Sat, 09 May 2026 02:25:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:57 GMT
COPY /target/ / # buildkit
# Sat, 09 May 2026 02:26:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 09 May 2026 02:26:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e62fae88a4902a343661be96a706a183dcca41008f70ddd0aa28b2845ba3155`  
		Last Modified: Sat, 09 May 2026 02:26:29 GMT  
		Size: 100.7 MB (100669846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7096593cb9b70a849e2f81430ebf3017a03f26d02c1fe84d2f709874dae7d0`  
		Last Modified: Sat, 09 May 2026 02:26:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:40df1fb8e368b4aa730d4ce811214ee09f6581b770e8338c25c99c945f4d6f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e65a638759e96d07659f4834510e7bb7bd52813a443ebc50a05e9c850fea4`

```dockerfile
```

-	Layers:
	-	`sha256:472858713ed112e34f3c5250f14daaa3c920da352c554da6fc0db6d8b81d2dd9`  
		Last Modified: Sat, 09 May 2026 02:26:27 GMT  
		Size: 10.8 MB (10758346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da57e134b3a0ce792069b6ae2fe386f82f717019fdd3d4ad85e667351b58795`  
		Last Modified: Sat, 09 May 2026 02:26:26 GMT  
		Size: 28.9 KB (28896 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a8682b6335c5a3a93c01bcb672a03ae0887d36a6ed02509da6a6fe1b627de958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310951178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea368c7f5054b9f49fe955d8700e946954ac37dd87d7aa2f3c6bf8a2b19e2b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:11:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 06:11:41 GMT
ENV GOLANG_VERSION=1.26.3
# Sat, 09 May 2026 06:11:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 May 2026 06:11:41 GMT
ENV GOPATH=/go
# Sat, 09 May 2026 06:11:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 06:11:41 GMT
COPY /target/ / # buildkit
# Sat, 09 May 2026 06:12:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 09 May 2026 06:12:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cb66ccae0a2cb78baa3de6dddca3dd89318583070660e3aff2c76c7edecac8`  
		Last Modified: Sat, 09 May 2026 06:12:50 GMT  
		Size: 92.9 MB (92930782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677743e4af652dd79f8723ff89a284363d59474b87d72b559faf60d691a51c58`  
		Last Modified: Thu, 07 May 2026 18:20:28 GMT  
		Size: 64.8 MB (64842692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c00d2028b31c941a29a131501edd6ee177d759b991ebbae84dc3d4516e07c`  
		Last Modified: Sat, 09 May 2026 06:12:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d40d320c237072839613e5be322a5a01c6aec5b793870d56c1a4945931a3a988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc8e5821b4a9c2e61409b6153658c52fce3f38ea9c6647c7e6e7e5a848493e6`

```dockerfile
```

-	Layers:
	-	`sha256:f1cdb7915965dd7833c2c97e6334626885403d5307cd2e7126154703c2b67b39`  
		Last Modified: Sat, 09 May 2026 06:12:48 GMT  
		Size: 10.8 MB (10782915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:609cb001de1ebc315e622cb732c066662b29d2555eb94180c4da817410414fcf`  
		Last Modified: Sat, 09 May 2026 06:12:47 GMT  
		Size: 29.0 KB (29020 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4d2ec16155942cce22f20d103d94ed752e28655190c9b6797da8192499d9e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336201615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc611042058cd7fad20f02d36a85ba94b979e65e29447ad7a72131bcbe4558`
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
# Thu, 07 May 2026 18:25:59 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:25:59 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:25:59 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:25:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:25:59 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:26:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:26:18 GMT
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
	-	`sha256:4576730cc1188381475a15201ad7de7153b28247376e0d104bbac61494efc78b`  
		Last Modified: Thu, 07 May 2026 18:32:41 GMT  
		Size: 65.1 MB (65149474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84476f2048e06b28493634930519d5862c15a4c4b7a9c0b23c618440fb1f40b`  
		Last Modified: Thu, 07 May 2026 18:32:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ee1b14c36a1814e0b9a111e2d1428167791fb97015c4c769a5981ad3b0e222ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b50b62704cb714afb67204a6a876d6dd28dca0ada8d3f4ec7a9387c8767c9b`

```dockerfile
```

-	Layers:
	-	`sha256:165ed59fd6d9a940e1eb55ce1bfd8793d51b2081f9db250e1cd2061b32b83878`  
		Last Modified: Thu, 07 May 2026 18:32:32 GMT  
		Size: 10.9 MB (10856748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92841542c8b06f6ac5e0f8699574611b11de4af7919af51c4035fa7f7daeb8a6`  
		Last Modified: Thu, 07 May 2026 18:32:30 GMT  
		Size: 29.0 KB (29024 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:5682b70b8dd3adbbcba312dfbc5cc35f198c83296dd275ed2ea9920ae2d28c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287359353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df80cd2c26878979c24dc754ac052a04b1a09ca836a99e2f0bb59c505d101944`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 18:34:39 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:34:39 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:34:39 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:34:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:34:39 GMT
COPY /target/ / # buildkit
# Sat, 09 May 2026 00:16:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 09 May 2026 00:16:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3bbdd2fc257950c611fd6795ac67747b411ad1789b54a283e0cb1bb22d4b2`  
		Last Modified: Fri, 08 May 2026 22:34:34 GMT  
		Size: 68.6 MB (68627825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c775d8e658bec93d151c4a165505e929181b99ac8cccbcfc3139166ff0a26ccd`  
		Last Modified: Sat, 09 May 2026 00:16:39 GMT  
		Size: 76.0 MB (76040301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585ea404f5b1266beca471637498b2c7b5b5d49eff5d438b1d1e375a59498340`  
		Last Modified: Thu, 07 May 2026 18:35:38 GMT  
		Size: 66.5 MB (66516126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4604d1af55159c277fd88bd65cc498764b3018ad8ba61c74ddc2867c0f4394c`  
		Last Modified: Sat, 09 May 2026 00:16:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bb81daca6ec11309cee379208a9151b357bc0a3844bd3798cdf790ebcec72ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33004b6ee40b9fe58fba15b688ab2c495d027c90c8b92c02ee0a1c3d947ddb1`

```dockerfile
```

-	Layers:
	-	`sha256:885c5427325c9012991e84a767695c0100d6ce50bd5ddab27155a7d5e093dea8`  
		Last Modified: Sat, 09 May 2026 00:16:38 GMT  
		Size: 10.6 MB (10597503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01984f9548e85b25617e0d14197fd701af9f31183d0d95ab93d865f64109b5d4`  
		Last Modified: Sat, 09 May 2026 00:16:37 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
