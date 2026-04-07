## `golang:1-trixie`

```console
$ docker pull golang@sha256:e3474b933b6d2ba307819482c2d7faef57bbdc3beda1f5caf3e8ed51b3177844
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
$ docker pull golang@sha256:03b6aaab8e80cfb1d42bc33e5190c7e78e1e6ea5a431942843f26f50ad7920a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfe2aefca8479f26a6c42873868a13303e4b0dc433da29c1754e5d844aea0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:23:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:23:09 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 07 Apr 2026 03:23:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 03:23:09 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 03:23:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:09 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 03:23:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 03:23:17 GMT
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
	-	`sha256:036a2b928f21a97a75b68d236d38dadf5d9ffcdcd9030c059ae87eeba18278cc`  
		Last Modified: Tue, 07 Apr 2026 03:23:46 GMT  
		Size: 102.2 MB (102169673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7a4d41921817b4fb2d8d61c937c1ced84b398fdffbc28d8f9309313f93c1d5`  
		Last Modified: Tue, 07 Apr 2026 03:23:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bb2d8a9a066649b8186f8e037ee96020f77b49311441d28c0995fa85b4af15b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d942b6f576ed12de4507d8b2070ee03454a65721b206a7574b806886a32e4611`

```dockerfile
```

-	Layers:
	-	`sha256:cbf9e519dd16386124daa9f6afea2af1a33baddd1be666992488749042c8222a`  
		Last Modified: Tue, 07 Apr 2026 03:23:43 GMT  
		Size: 10.8 MB (10787049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075de63283e646ad47ff00e6266a467100e7b23681ec60e312cb6d611bf7d610`  
		Last Modified: Tue, 07 Apr 2026 03:23:42 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:42917e77b10a47262a6c7d125c7ce75e431231c0af3327e582fb89cbe9991071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270654963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da10fb8cf6a8de08ea4d6a50c1c60a98aa459cd641d987795b5ff86df28f3b98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:29:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:29:26 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 07 Apr 2026 04:29:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 04:29:26 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 04:29:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:29:26 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 04:29:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 04:29:32 GMT
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
	-	`sha256:7185411919610e2ffc1d37ab0906a8ab856c3ab70ba46e06c3b73115b00a555e`  
		Last Modified: Tue, 07 Apr 2026 04:30:00 GMT  
		Size: 72.8 MB (72805027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3209e32f7bf51319c7b685880abe9a9fd966afde3d994a5f49d5fdff618d3`  
		Last Modified: Tue, 07 Apr 2026 04:29:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f1f0ceb18838f32ba001046dc88bd8b485c2713f6c68b6144c4f8dabecf23b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0376dfb3bfb3bd820e42befca440f66379e4ef8a9643e1a8a50024041053ae22`

```dockerfile
```

-	Layers:
	-	`sha256:37952ddce587331d0307025ecb4aaa2dfe9c0af27f8454112bfa5bdc17b88232`  
		Last Modified: Tue, 07 Apr 2026 04:29:59 GMT  
		Size: 10.6 MB (10582968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6ae85eff61fea28c4f4c22287f3ab786efd3f8c23844dd0d06efbad3896a80`  
		Last Modified: Tue, 07 Apr 2026 04:29:58 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b028b4be00d2860de59cf5f5db2b6a897a16f4c20b09c7f0a014da6cf59df55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304697696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abfa7348a8006cb2d2374824e6e7de7ae12862edd87560ebb55ca2cbae777a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:34:59 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 07 Apr 2026 03:34:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 03:34:59 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 03:34:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:34:59 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 03:35:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 03:35:09 GMT
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
	-	`sha256:9c1a9fcb3763bc4560a8692acb14d225ec4a4c802c552303f745805afea55864`  
		Last Modified: Tue, 07 Apr 2026 03:35:36 GMT  
		Size: 98.3 MB (98310584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610e9dc7808b9ba9d67c958891b84c6993f5403d3c5390a9c47f7a5038efe397`  
		Last Modified: Tue, 07 Apr 2026 03:35:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7f8d8a0338ae25f9629b43ca18c71b9cfbbbf7c66d8d1dbb85204b3c7580004e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c293ad525e1d1b31e4e4eec79b548f2a072ff464fcfeb5e90682d223a7414eda`

```dockerfile
```

-	Layers:
	-	`sha256:75ec673a4c19b99ba0cf23324b6f87eeb43a930a58b07114a5445132b07699f0`  
		Last Modified: Tue, 07 Apr 2026 03:35:34 GMT  
		Size: 10.9 MB (10907552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc6b5bfdeae97671e04602084f1388adb3ff274e3325ae517b46da8c056a0a1`  
		Last Modified: Tue, 07 Apr 2026 03:35:34 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:044c1ad3679f0ec926a171bb56638b538e925b403aa32f2fd5ba7033ea4d1611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313547606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7a5b871d670102f7dc6fcc5f5464e3af524d780564a4299b8216d4cb083e30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:19:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:34 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 07 Apr 2026 03:19:34 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 03:19:34 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 03:19:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:34 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 03:19:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 03:19:42 GMT
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
	-	`sha256:81ea9146b5924b4ad6495e34d5e3261119b962a743d7d7a1a9b16ebd836b1a16`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 100.6 MB (100607885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb07caf9c739767295e4b0d3b36abebfa29f9d22222644122dcb4a2deeeddd8`  
		Last Modified: Fri, 06 Mar 2026 01:12:15 GMT  
		Size: 65.5 MB (65541795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ed7155f01542993d5b3b6026d857f41b0139716ecede4c00bb4dede3a7f842`  
		Last Modified: Tue, 07 Apr 2026 03:20:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ace6bc572941e8db1757520c3ed90cc780efbb654d0e57a337c1e5505834c12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f939f0ac84ed6e41a0d78404206b67ed9b5c33157cefbd85b566f8641bc5ae`

```dockerfile
```

-	Layers:
	-	`sha256:2bd9628f01706d59443c882a375c626f81db4de3c4dd447e468ebdaf13b23d60`  
		Last Modified: Tue, 07 Apr 2026 03:20:04 GMT  
		Size: 10.8 MB (10758292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9acc1bcc54659cd0378095ec4dab421f27a3d15559adb909a3fe22b790376886`  
		Last Modified: Tue, 07 Apr 2026 03:20:03 GMT  
		Size: 28.9 KB (28895 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:9d4285400ddbb1a385c69fe5c83099b88c10e8332ce9e4869e5d42381b17697f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310801014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49092f7f7b10f1e795fbf0370d736a176a9907f2ed3a0911afd2e5717c3aef4d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 08:42:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:37 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 08:42:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 08:42:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1ef0247ed38f7a4b7b7776f4f220241d718538977da0d861b980db4a8bf1f1`  
		Last Modified: Tue, 17 Mar 2026 08:43:26 GMT  
		Size: 92.9 MB (92869851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace710cfb3bb4da72d185d83d05e86cb22a686c0abd5be3e83cdf74e34b68d02`  
		Last Modified: Fri, 06 Mar 2026 01:12:05 GMT  
		Size: 64.8 MB (64765980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67dfe706ac5dcf941588fa9bf37ca305dbefede92ab97b32dcfa601b0f5cd08`  
		Last Modified: Tue, 17 Mar 2026 08:43:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:27f965c2ed0931ef5f59a89e3796a51f75a2d301f6846bdbc0c60185a62d1d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37941244ea84f0bd5c0f8ee3d2ab87a59abab9f26fcd71c15970fd3bd21a1538`

```dockerfile
```

-	Layers:
	-	`sha256:53c4a4bfefa374129199c8038efbd33d3ccdf89e5aff8431a564370a9b36ebde`  
		Last Modified: Tue, 17 Mar 2026 08:43:24 GMT  
		Size: 10.8 MB (10782861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629191f1936a344faa3ab76e2f08a8097b8dc60f6fed4806b647911659aed179`  
		Last Modified: Tue, 17 Mar 2026 08:43:23 GMT  
		Size: 29.0 KB (29020 bytes)  
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
$ docker pull golang@sha256:1fff05efd62314e4617224bbd229e3857f180b2b02173640a0fb8faf972ad8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287210169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2e889b465d4f22d87f6b612d2a4d586bb7edbf168e36bb7178e1cf4246fae2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 06:01:47 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 07 Apr 2026 06:01:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 06:01:47 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 06:01:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 06:01:47 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 06:01:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 06:01:51 GMT
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
	-	`sha256:de09fb86ca93d03c7033a68934d3836b7d73a92db92a91d8e192cade1e2b3477`  
		Last Modified: Tue, 07 Apr 2026 06:02:25 GMT  
		Size: 76.0 MB (75981910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106d4aab6b73d7cceb22ee0e78a7d7693d21df87cd6ffbc4fe552dfc356b28cf`  
		Last Modified: Tue, 07 Apr 2026 06:02:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f1580f2c1a77305bb53255fec0102ef34b436d9db81e762039e8fe40b6b8deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9159e68eb71f3cdd730c5eb4c4402fea33e90cb4007bc757018821ca911d41c`

```dockerfile
```

-	Layers:
	-	`sha256:e8771292e339b77db0a13240fa838a067063b1acfd8333a8ceda7b1a66e49351`  
		Last Modified: Tue, 07 Apr 2026 06:02:24 GMT  
		Size: 10.6 MB (10597449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c43903e9f542b50955c1307ee9f688d5618c0e4e2f59a30a1bae9436fb765`  
		Last Modified: Tue, 07 Apr 2026 06:02:24 GMT  
		Size: 28.8 KB (28776 bytes)  
		MIME: application/vnd.in-toto+json
