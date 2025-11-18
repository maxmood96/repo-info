## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:bc264ec7639a24aadb8b11b4c36ffc7f5da130633e6970232154893de6ac639b
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
$ docker pull golang@sha256:89c73db5127b7f7dc835b3c2db5f5700a78dc464ee40f35bf761f1f886afe1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320985718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9adca349564e2927cb280419bbe8d70902991afc3d3e75f6d52b2d3079baea2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:25:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:27:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Nov 2025 21:27:10 GMT
ENV GOPATH=/go
# Mon, 10 Nov 2025 21:27:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:27:10 GMT
COPY /target/ / # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Nov 2025 21:27:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da27cee6b4f0fdf751dd58d18bc54b5b33b316079756547a6443f03b9b5de2`  
		Last Modified: Mon, 10 Nov 2025 21:28:06 GMT  
		Size: 92.4 MB (92402013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaf52c0c17111119e1092b7027d6d86d20ff4880cb34ac8f9ccc8cf394dc978`  
		Last Modified: Mon, 10 Nov 2025 21:26:54 GMT  
		Size: 91.7 MB (91677046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5f06624625e0072879f3dd1938ce5ea342e0748c5a698f05fc9616dbceba4c`  
		Last Modified: Mon, 10 Nov 2025 21:27:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8c0d33d5c1e38cc454748b3372009795888de28c58852c992af132befbd000fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8593c2351a6acf8f48784399a156fcdbae73e58446800ad1837c723d9832c4`

```dockerfile
```

-	Layers:
	-	`sha256:e79a87480e31d708aceda9bfb414a765ee7dbb50144eaf9912f25541a0706008`  
		Last Modified: Tue, 11 Nov 2025 00:24:44 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e63122af1b0f9d669381c61e22e277ed11c565f40073f375c9108a6428233a1`  
		Last Modified: Tue, 11 Nov 2025 00:24:45 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:64f8adb172cd54bfe27c352a331353eb49a46820ecb73718f8b97e957728f05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280172346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bdc6b4d38ca71af83ba2f08818d57619887e7cd3c1471ee7c826167c72c476`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:45:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 07:45:16 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 07:45:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:45:16 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:45:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:45:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da52e1f5863f83171406f12efbdb64d4d6aba9cc3a64ff1d9bf3fe27ae39703`  
		Last Modified: Tue, 18 Nov 2025 07:45:53 GMT  
		Size: 66.3 MB (66276525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2c69f85dc047cff5b8e0c725d241fb21eed7123e04e156a844669a6e5e5d3`  
		Last Modified: Mon, 17 Nov 2025 23:23:14 GMT  
		Size: 88.1 MB (88112716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39f130c63f1c12a02657231fb331c824bc231de1b35c64dfc6d60287d6078a`  
		Last Modified: Tue, 18 Nov 2025 07:45:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:47b440aab20c26dec02cca2dd142a7b6080b76e0146871fecb41dc1761d15d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb795efa55c91431d09929ef5097ad1e6e53a363039a88130dd0f9b6af4f0ee9`

```dockerfile
```

-	Layers:
	-	`sha256:d490c368fada729b80f3c9a76dbbdcfc9a5043698e0ab642796f4ddf75471535`  
		Last Modified: Tue, 18 Nov 2025 09:25:42 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd00d9eebe2578d11d58e20f63081e06c8f4fd512ff0ae7343b2471fd878be6`  
		Last Modified: Tue, 18 Nov 2025 09:25:43 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5e3bca53ef7d9e5be2e33f82aaaeb12b7e1aaef8c526ea8d7f32478897469ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309997833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd800fbe0ac11acf2d1d8477a8df88c692cf2a87507fa7e82ad74f470e02af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:23:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:24:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 07:24:44 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 07:24:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:24:44 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 07:24:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 07:24:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8fe1c920c7eabb05d9d3d458d76a9993f7e062e9f050435627e4b875de4af`  
		Last Modified: Tue, 18 Nov 2025 07:25:22 GMT  
		Size: 86.5 MB (86491065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72859aa41c7126c75b0eaa6f62530c6ab6d97e63fe3d290a8c1d237f80407685`  
		Last Modified: Mon, 17 Nov 2025 23:30:36 GMT  
		Size: 87.2 MB (87177738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776d05e87a677b6bbc9e589a3a23740f7f06ae30209871f2ea7d6af0e7b3572f`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ea9787758684033f65a698ef51c04ec4cebab7b743896ec1786ac85304c9d0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd03a9bedf2d38105f3bfd6fe9268ac8e9629a202126d69c6ac8aeca2b68d08d`

```dockerfile
```

-	Layers:
	-	`sha256:1ca4fa12fb5e4cc04c678d0589c850638fca4b3c0e050a93a023e72702363ff7`  
		Last Modified: Tue, 18 Nov 2025 09:25:50 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcc2a769ab2ee9ed6dbf34673970ab75268e507e34d7b6db891130464f00f99`  
		Last Modified: Tue, 18 Nov 2025 09:25:51 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:00e90eb145add6fc0ba23ad4c3f2f529bb291e03662e5d6b0ec5b5857dd889fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320310769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba22dc34a284fc393d960ab68983c4ec81218e362bd8bb0b8281050da65b06e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:23:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 06:23:50 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 06:23:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:23:50 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 06:23:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 06:23:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784af9b30403c66a1af5c61ad5b3f286310ffc85ae6d220ded549f6a5ed105c`  
		Last Modified: Tue, 18 Nov 2025 06:24:35 GMT  
		Size: 89.8 MB (89840564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb363788838918ac7e550b93200cd675ca2501f3ca5b79cee14723fcfb2dfe5`  
		Last Modified: Mon, 17 Nov 2025 23:22:28 GMT  
		Size: 89.9 MB (89904896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b366cc3d19df094062076a8c6f0e24c5d605ed95eaeb94e242c63014162555b`  
		Last Modified: Tue, 18 Nov 2025 06:24:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:49dd67600652be214834a30ef12fd4479c86399ffcb106d45a46fc725f3de576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46591b785ab89e3964697542affdfcc8975d25124d065b4105d3b7a6e4febf`

```dockerfile
```

-	Layers:
	-	`sha256:584ef8f5835c0ca0e427491947f0e23e5adebcfbca69a3982ce0a965e1484627`  
		Last Modified: Tue, 18 Nov 2025 09:25:59 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5b2f4f60ff61b8590d501733e3db492c3eed6281b859d166fe28c719c64af3`  
		Last Modified: Tue, 18 Nov 2025 09:26:00 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:fdf50c194151575d453e9141b2aced602ebc04079a80659f4b3a40fcd928049f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291564939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0654fa297467ec28b7d80a99a8ec8b1c49a8679a3517d37ac2b11400361b1aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 14:04:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 20:51:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:39:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:39:05 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:39:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:39:05 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:39:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:39:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6492253d4f5d673ee74abc9e254c218714a0737c4c244dcc729821fb543170`  
		Last Modified: Tue, 04 Nov 2025 14:04:51 GMT  
		Size: 23.6 MB (23614047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305f9457e9c1a9cba16fc581959f009772a1561916f3cc0ea635018606420380`  
		Last Modified: Tue, 04 Nov 2025 19:50:51 GMT  
		Size: 63.3 MB (63309635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96817f9c963b6341e1b5f5447538613cbea1464e6f61848ae7af7c6e1ea82e01`  
		Last Modified: Tue, 04 Nov 2025 20:53:40 GMT  
		Size: 70.0 MB (69997094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa61b21a4c87c35f7ca28f985e9cffd80c7f86dce5df846a5d6c167dbfaa97a`  
		Last Modified: Mon, 17 Nov 2025 23:41:43 GMT  
		Size: 85.9 MB (85882723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93529de83b2882ec2a3cb0a05038fc85048700983f89639d94d46dcf589c3750`  
		Last Modified: Mon, 17 Nov 2025 23:41:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dd18e33a96044bf50f781623598c921dfc857d014a0c4260d4e513ed8237b117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0a587fdc77988b5e0637b7be035949e97ccdfaa023641c3f5891b643b2d03c`

```dockerfile
```

-	Layers:
	-	`sha256:bd8ae1bf32085384b4127d6933ed1e115eaf92b281198d0f2c2142935cba38c8`  
		Last Modified: Tue, 18 Nov 2025 00:24:50 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:72c14d57427c0eaee8d98b002a0ae8c17dc2c8d29e10f9b73047cab86277eb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326903476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35568de879fc6df396dcd38f2ed62e8d851261dc009f22f7f7e702dcae691bc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:24:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:47:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:47:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f89c76b3026966e039b432e1b66b1655c47c97f236438dc626e5acdead5cd`  
		Last Modified: Tue, 04 Nov 2025 06:25:48 GMT  
		Size: 69.8 MB (69845633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6996afb16c311d5e15c9ff129db6522d4d830e76ed83f36edf67e6b305a936`  
		Last Modified: Mon, 17 Nov 2025 23:49:25 GMT  
		Size: 90.4 MB (90420245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4298f1c2ffb8d9a5bac1e4f839a570317beb22ade4f530e25058d22c157a1ca`  
		Last Modified: Mon, 17 Nov 2025 23:49:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3b7b79a0a2f3fd532fae92bc8e1391ec30da34d86648328e949872294ae56dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f7677391b88c28fa67392c83ec6d12735e92b9053934b9a26875cea40d0862`

```dockerfile
```

-	Layers:
	-	`sha256:126b3c90641a14846fb08c09749964243c0b4256f75e174796e7e30e4aa55535`  
		Last Modified: Tue, 18 Nov 2025 00:24:57 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db21f907f0bed2497477f9c0da4cb909822fe946a51a01efaec56532c18292e1`  
		Last Modified: Tue, 18 Nov 2025 00:24:58 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:a745a26ddcb22a3e75769dd8ded9914591bdf1e9af9401ae5e848205b0c4dae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae94089b2681fe3fb198bb43f740ab7f47305074223e9fd97fe413f16c84749`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:26:35 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:26:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:35 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba91dbdb50f511980482385b36987be0332dae93638fc6697a70724b1e1e5c`  
		Last Modified: Tue, 04 Nov 2025 10:00:10 GMT  
		Size: 63.5 MB (63501365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb6e3d04d15f50e03e99299cadab5c2fc5e8301742c4ae35f188b0f56a2f2e1`  
		Last Modified: Mon, 17 Nov 2025 23:27:27 GMT  
		Size: 69.0 MB (69010923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4515f8b1d9cf2143fbca8f466beb9046119009ff0c9973ec41a536bfa5dddca`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 90.2 MB (90177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbedda227caf79d9e898a8f056b86f881a0d5a741e456e3ef93eb633396abfff`  
		Last Modified: Mon, 17 Nov 2025 23:27:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:17bdfd49c98cfa496355029071aa8e8914e7ce0d83bee5ab9da0685383c52407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d32f328e19b4708680b389b51cebebf1389a4814fdca58adf582348ca8df96b`

```dockerfile
```

-	Layers:
	-	`sha256:3dcd6a2c7c0c3758974599c336a7cff13afa93802b02855d3062a985fd1bd1b2`  
		Last Modified: Tue, 18 Nov 2025 00:25:09 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7cb356085d57387f968e91b2c7fd56eb4d287c32a5fef14f39d09b412eab31`  
		Last Modified: Tue, 18 Nov 2025 00:25:09 GMT  
		Size: 28.2 KB (28213 bytes)  
		MIME: application/vnd.in-toto+json
