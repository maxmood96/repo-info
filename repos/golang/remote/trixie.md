## `golang:trixie`

```console
$ docker pull golang@sha256:100774df3fd947fbd1f2b674e71215af6bf087b3676d9fcfdf1a9d0ec9e5cb9c
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
$ docker pull golang@sha256:324a6d89573c3e72f69aa7b5b1a8b9bd6870ce9dbaa254548b0d7516d3720598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312029979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ab73b54863fcdf3d0c657635ef04e7214cb12963b3e7732a868423e73867b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:39:16 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 20:39:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:39:16 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:39:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:39:16 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:39:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:39:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a069ea1e4db555aaa432873bc33f67ff652f145b73a6832b11cbe7e05b718d1c`  
		Last Modified: Tue, 24 Feb 2026 20:39:48 GMT  
		Size: 102.2 MB (102166493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec41210057e053bb052a2039a683dbb9e18b55a8f2e434938fa1ed62804063e`  
		Last Modified: Tue, 24 Feb 2026 20:39:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ef36cb11611f3c944990eecdd4bc04e1c17727b1c5950e2a410d0470aa354bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10815928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d3b7a0f16a6740dcb849175085fdc29c5b82cdacfbff8bceabebc50292dd78`

```dockerfile
```

-	Layers:
	-	`sha256:a40f721e8c96c781f93d1738d0ae977de844ebdbfdeb61eceba9ea12e2bd86b5`  
		Last Modified: Tue, 24 Feb 2026 20:39:45 GMT  
		Size: 10.8 MB (10786975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c95be9ef1c7c8d42f9006444fb504429ef9f2d73cb7ce3a16eb5103bb24f853`  
		Last Modified: Tue, 24 Feb 2026 20:39:45 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:ca5cb1ddfd00720ab00d50bdd44f9fa587a9cb0ac81e64908398246f866b0531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270608967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f96b6ad477eabf8bba285be633b9ab71879e5b7e9e0ad44bb8c4b0d3cc1739e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:16:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:09 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 22:16:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 22:16:09 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 22:16:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:16:09 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 22:16:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 22:16:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8a73a64ab827189cb274459a9f6939a773a8981c5ef1ec488f5e6260dbf577`  
		Last Modified: Tue, 24 Feb 2026 22:16:40 GMT  
		Size: 72.8 MB (72803593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f553fd49f263c8a7c2ad9bf49fa7c964df2d75012f984cbc27f8f7bffeeb0e`  
		Last Modified: Tue, 24 Feb 2026 22:16:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b0a773a6bc4d970d431fe2bffea5c914445ade6f3a37e3cc17dd2bab4380b21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10611981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ca1b1460b4c54d15ca654d346c14444843d2e2595d92160af82f30513df94f`

```dockerfile
```

-	Layers:
	-	`sha256:c583a2c750d361569f28a7d2ac0b11a3d739ca3e3da0f298c58a0dd5e9cc6f69`  
		Last Modified: Tue, 24 Feb 2026 22:16:38 GMT  
		Size: 10.6 MB (10582894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9533281710160ed3b0d6b4d2e1cf784973020ac1b27f0e532a932ad11b12aff7`  
		Last Modified: Tue, 24 Feb 2026 22:16:37 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:af7a70ed876e197ac19dc85ee864bd94c45c98631724ad89feebeb78e013fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304655738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f38f049761550e2d6926dd3c1ddd3be68322457316ef4269904d288618cf53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:30:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:30:07 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 21:30:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:30:07 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:30:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:30:07 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:30:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:30:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33369bbd18310cb8c67024b362a9bd95e521f969610f0fbff998753ca53290f`  
		Last Modified: Tue, 24 Feb 2026 21:30:38 GMT  
		Size: 98.3 MB (98310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f1fc5e824fd42268fe5447077b303c658ec4053d4d7e75d4807e95d4655328`  
		Last Modified: Tue, 24 Feb 2026 21:30:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:39b445d0c619657a67734b69d457240f0ed5d89a6e715d07824dea79ce3c6a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e2b6d2be9efe31761266ea3dd99d56bfc9d849e622af19347e9fe03104fddc`

```dockerfile
```

-	Layers:
	-	`sha256:b984fa49d844ac5de1c0bb121b48b39bdad818a6307972fbcd8799cdbf0249e6`  
		Last Modified: Tue, 24 Feb 2026 21:30:36 GMT  
		Size: 10.9 MB (10907478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6244d2a89305200a19b4e40f3742ece6cfe9d7289f74891f38f0ddb43ebcd3d9`  
		Last Modified: Tue, 24 Feb 2026 21:30:35 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:f200f27a113fd26789f07ff95ec1f7e337e295ddb711c693cf5b18a6dc7e88f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ab1b99f9ffc4865801c7e3d9df78883718e74a24df4d2566219fe1214681fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:33 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 20:18:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:18:33 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:18:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:18:33 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:18:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:18:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ea86e04361f5b4e05c4674cd1bb26a648ade2ed4e0873109ca1f362d4c097`  
		Last Modified: Tue, 24 Feb 2026 20:19:01 GMT  
		Size: 100.6 MB (100607857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbfad3c600a3a9c8302db25d37648349b37e769601e5490f9bfb9f615fe5677`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 65.5 MB (65521738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b084ed595188c3e4175891ca6b88122995ce8ed43e9fabb4bb432d27a4d7698a`  
		Last Modified: Tue, 24 Feb 2026 20:18:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7554d437017bd597f091816a75c935309e9e46b0bf43c7cccbb4f62e23b07b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466562af22723a5597e9a2b543ae7a33e15e44a26a043cce32802a5a480bcfbc`

```dockerfile
```

-	Layers:
	-	`sha256:7be948e710dce1a180417123d41be75947eb56ba1b4fd99f800c05f11cb9ca6e`  
		Last Modified: Tue, 24 Feb 2026 20:18:59 GMT  
		Size: 10.8 MB (10758218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31330bef2b039c46ca4494d8ae4b824e36bcb1f60f1a51cd968efe31322d35f`  
		Last Modified: Tue, 24 Feb 2026 20:18:59 GMT  
		Size: 28.9 KB (28896 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a893929c79733e71980d255ac922c75834b0216d12fb8bf69f70cfd97cc47e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310737390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71122276bed6d31acb8d2a12432cb35528c3b2cc9a5046edab55d799052e46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 06:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Wed, 25 Feb 2026 06:24:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 25 Feb 2026 06:24:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a32c319fb2bd4f3da9db7adac112a6d72d6ee18f984754c089281bc484a90ed`  
		Last Modified: Wed, 25 Feb 2026 06:25:17 GMT  
		Size: 92.9 MB (92867869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126790c7f277d9549d33c9fa0007db9cea40f63e4211cc5e6a66ae768cd987f1`  
		Last Modified: Wed, 25 Feb 2026 06:25:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:77fc122f333ba577468433a86fd34cccfe6658868b70ceba67016f30a7b9cff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f82d1c380ce5e5a4b51fa7a6b700a496c29e0dc8f17d40fdc70b5b9d5de959`

```dockerfile
```

-	Layers:
	-	`sha256:168b8450840e1b4bcb6494d7d6ab514564037ff33d323c0910e65e7e16a14098`  
		Last Modified: Wed, 25 Feb 2026 06:25:14 GMT  
		Size: 10.8 MB (10782787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670f3a7301ce3857a0cef9eb94a2d45613fb402aba33580d844aca62101c8f4`  
		Last Modified: Wed, 25 Feb 2026 06:25:13 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

```console
$ docker pull golang@sha256:6273d0002e0dd473a4f372597aae20c530fba172144f45372094df38133b7e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336073217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c97355d7647f19a8da80a4dad4d41880803085c7f2116f58eb57337d52a0876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 08 Feb 2026 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:13 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518328709aef2ec161ee90f4be9eea82346936a41f7fadae6c748b8ca89b81be`  
		Last Modified: Fri, 06 Feb 2026 08:00:06 GMT  
		Size: 66.7 MB (66660429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30992833d130e4aed39434931ae478a9ff84677bfa5deef60f6f4f9de9312e34`  
		Last Modified: Sun, 08 Feb 2026 00:50:26 GMT  
		Size: 131.6 MB (131627094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e59666da981e3405c1b7fd86ade4932c92816496358034a16d9db56a3633b7`  
		Last Modified: Tue, 10 Feb 2026 21:32:56 GMT  
		Size: 65.1 MB (65055611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74afc761e2a6a2434adf94d57ef14b4b8dbd95715c17a65d6b2fbff8a076d852`  
		Last Modified: Tue, 10 Feb 2026 21:32:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d00626367dc16a3fc6e4ec71240cbd2cce9205cca99cf7e2019687f5af7ca3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d833f524fa0697ff6e6f79e00c78c79ed58c6bd7e4f7f80a490ad159fd16d4`

```dockerfile
```

-	Layers:
	-	`sha256:59f057ecefd5d7c90c89bdf34e5e019712b3caf66f0bbcc8ac445c6e681416a3`  
		Last Modified: Tue, 10 Feb 2026 21:32:47 GMT  
		Size: 10.9 MB (10856620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e1569a8156f3f91196a9f60bd66360960ff76f54ec9d53b344a37e2d3e1b1d`  
		Last Modified: Tue, 10 Feb 2026 21:32:43 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:868a82678998958e2cc5ace67965e0d7cf9048c9cc6bd442793aa6fe994637d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287163340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c73f9b3e363e8ba0c6df5d246354c02d3584e20fdfeb6ea774d6928b7736f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:16:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:16:25 GMT
ENV GOLANG_VERSION=1.26.0
# Wed, 25 Feb 2026 02:16:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 25 Feb 2026 02:16:25 GMT
ENV GOPATH=/go
# Wed, 25 Feb 2026 02:16:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:16:25 GMT
COPY /target/ / # buildkit
# Wed, 25 Feb 2026 02:16:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 25 Feb 2026 02:16:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed19e0b88f5617f04af5565e09ec0a3c3a53e6d0ae5d29fc321338a765f8378`  
		Last Modified: Wed, 25 Feb 2026 02:17:58 GMT  
		Size: 76.0 MB (75980295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60ccb3435f025a8a9ff8ec7737cece81b24341d4a50136f896bcdee8ca1583e`  
		Last Modified: Wed, 25 Feb 2026 02:17:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:14b29de725a415623122ab64c700532ae432411aa66b4bcfd2585a4bb42e5c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffbbec7360078678bba7436effb5d49fa77943d279233a9e15310b167c85383`

```dockerfile
```

-	Layers:
	-	`sha256:18469307019fff3bfee46bdae976aa59d36f55d59ace73caf6b47d5e858cab6b`  
		Last Modified: Wed, 25 Feb 2026 02:17:57 GMT  
		Size: 10.6 MB (10597375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b5ca99aa6e2b7acd4002f0f6f4b29768a9d720a7ebc25f77845839cc15a75a`  
		Last Modified: Wed, 25 Feb 2026 02:17:55 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
