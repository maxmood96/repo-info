## `golang:1-trixie`

```console
$ docker pull golang@sha256:ef151f0384896831258e71065176f1e63f5a90bcbe6a98ec679a1990011a2655
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
$ docker pull golang@sha256:b3dde9df96709c60c299573912ee80d5e91dc28a8021015e620276a017ec86e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304940968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6f042fec77daa2b947c638e97afba641901ed4593e583e8793a5c56c6b7691`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:41:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:41:25 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 02:41:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:41:25 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:41:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:41:25 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:41:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:41:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338a3f7700be9b1ed87d9817ebba132d75792ab6586853e72cbc9c98a890113b`  
		Last Modified: Tue, 30 Dec 2025 02:42:12 GMT  
		Size: 102.1 MB (102108688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67db9e13c641ae9b38b919318cd762164f7b5c94f006a18ee533027d8ff79e3`  
		Last Modified: Tue, 30 Dec 2025 02:42:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e05d33914a5c7bb6aa0cc0713fb214a56cf41c42ea360ea3fdb5fc3b7d37df16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33358244968d960a35cc0de4daba8b9eef4eae82df33f2be8dffeec6feb01e2d`

```dockerfile
```

-	Layers:
	-	`sha256:ae22920f622263e44e82fdb01fcc25145a80d23721804b44c2a32fb942b13e14`  
		Last Modified: Tue, 30 Dec 2025 06:22:27 GMT  
		Size: 10.8 MB (10784428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbed4a1299ca77a7de4f03d2812a35dd902f2475cdf56a7e6c3c4a6db9fb194`  
		Last Modified: Tue, 30 Dec 2025 06:22:28 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:c699d07c51fc36cdfa464baf954540e313d26b779a1bbf717fc58e80cebf2785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263878140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e8c5c48a1a357e0149cc414664bfdf6a1c20763edb8081972a71d1ed83e64f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:45 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 02:35:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:35:45 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:35:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:35:45 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:35:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:35:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d733d3ff50acb6e1f52358e91c875cbd0af69a0b49fe8fc9cc9b71b546516d3`  
		Last Modified: Tue, 30 Dec 2025 02:36:23 GMT  
		Size: 72.8 MB (72754030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3df7af3a88120deb14ee842bb67bae0de0a3283cab4e86f294890e5619b7ed0`  
		Last Modified: Tue, 30 Dec 2025 02:36:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2f8e94690d9806b7396404c68ca44266d4a64262841776c03bef76385ac3186d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02561ef33e5f6b030c2d8533e64448c58de398e46368ab746832d1eb1f92b94`

```dockerfile
```

-	Layers:
	-	`sha256:367397f016b4011c33ccf2b7bfad168a08006f61ae54b6a2d3da83e7e816c2cb`  
		Last Modified: Tue, 30 Dec 2025 03:24:24 GMT  
		Size: 10.6 MB (10580349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83da40ff6eaafa9b27ef2300f22c8a8f9540ced1bb7807c129c062b753589029`  
		Last Modified: Tue, 30 Dec 2025 03:24:24 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c799205726276c79c8d21867350d66dea1e67d0222b8ae0dbafc4c342b3451dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298160341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75418197502b2b015f59f391ad2a84b7028723d0cee1137c69fff79b78fa437a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:40:13 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 02:40:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:40:13 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:40:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:40:13 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:40:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:40:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83a926d1dbf860dd3ad3471e01cec2d3554c7f29e1e641ea446871365373a7`  
		Last Modified: Tue, 30 Dec 2025 02:41:06 GMT  
		Size: 98.3 MB (98254246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d59dc6f51aeb61204f096d7914d4c87610ec113b2df821a78a77a21358a91`  
		Last Modified: Tue, 30 Dec 2025 02:40:55 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:137be202a61971dceb0f2d39c2ae6148c3dbff5db7c2bbe82846dd9396592569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f1ad63a893b5958c898f75f24e294f51ea5a373829bb262444231dfd97519c`

```dockerfile
```

-	Layers:
	-	`sha256:8d575bc4d004f63ec3700b2c15b8d5bda3f6809b7241dc96af90c08d8a6e543f`  
		Last Modified: Tue, 30 Dec 2025 06:22:43 GMT  
		Size: 10.9 MB (10904931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30957698d2758c0d9da8b40759c6f99ea5d64ff3b76ae96fd40d085148f2a47`  
		Last Modified: Tue, 30 Dec 2025 06:22:44 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:32a2a92abb162f9a654db7752fdf7c541e6c298f87f7f69dedc64efd362b7c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306800070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c3d466d541d51219dc391db2672c71e22e2d37096b888092c50cf4684bd2ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:52:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:51:58 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 30 Dec 2025 01:51:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 01:51:58 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 01:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:51:58 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 01:52:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 01:52:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a746d3726a038f2bab15f68f428defbd14ecbd8b5036cf5ea2c9c946ee3e29`  
		Last Modified: Tue, 30 Dec 2025 01:52:42 GMT  
		Size: 100.6 MB (100555123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a251cb58f5ee307c56e9f5e5b17e0b5dc6fd7445ecc203c8f38c250b62890b`  
		Last Modified: Tue, 30 Dec 2025 01:52:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:312235b61145fb1b0c9456ad38521dd04291819de65be02297edee7e21b08237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bab1c7e86f7064a9a35772805e776b06e23f6c967e215e0fe9beb57804752f`

```dockerfile
```

-	Layers:
	-	`sha256:453228f6f164e6b34ecad72bbd6219e20c7798a892d431c30cab760f10549730`  
		Last Modified: Tue, 30 Dec 2025 03:23:30 GMT  
		Size: 10.8 MB (10755674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0b9744cadba47961167e08a3710a33b11c38f099779789734b5dc0ae52e9c9`  
		Last Modified: Tue, 30 Dec 2025 03:23:30 GMT  
		Size: 28.9 KB (28896 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:d6ad7fce8bdce5315f037cd9aff445d4cf7d7325333c8bb003403f0563ae7d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304086918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fd018bd874346d1dc0a6ebb6af7e779e7a2fcc45e6869943a48eca07e1a658`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 10:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:38:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:38:02 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 10:25:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 10:25:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c305b2563d5a320b2f5d542cb42b58b482a07941244656f1dd066b0fb90900`  
		Last Modified: Tue, 30 Dec 2025 10:25:02 GMT  
		Size: 92.8 MB (92815505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a29a39a173b26b9ebf23e656da3218659ccc1713088694c73d5b2ce8105de`  
		Last Modified: Tue, 30 Dec 2025 10:26:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:fa5fd6b8bb561a988859f3d4a9ad6bb55aab28d307b6e2bbc6f9119ef2fa803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018751f15089b3b14839c7faee6f2236566dd323b394b432e1e43044e663795`

```dockerfile
```

-	Layers:
	-	`sha256:358257bb853235928e85e14dc05b9e21dba422364df90d265560bafe83dfc589`  
		Last Modified: Tue, 30 Dec 2025 12:22:50 GMT  
		Size: 10.8 MB (10780236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a8ca6d0806afbdef720cef4b9a9010482a3c8b4e93d03d717aa0a5a6173cc9`  
		Last Modified: Tue, 30 Dec 2025 12:22:51 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:a240d11bed7def177e9e2b2cf35a186654245e7119424367ba72d5324f1673b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329653036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b227a68aee9e60dea9f05a48cf07faf9777e24b86cba46235174c1541e0268`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 20:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Fri, 02 Jan 2026 20:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 02 Jan 2026 20:34:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b560385f3861ed5a056fb65f6efa479b98fb4edb93cd21d11160f19961a6e0`  
		Last Modified: Fri, 02 Jan 2026 20:32:15 GMT  
		Size: 131.6 MB (131594843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48ce238a38db398d712661189f55a9796e55115f30e6cd49fae9125576130d6`  
		Last Modified: Fri, 02 Jan 2026 20:39:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bbb0ec38618ff4e2c500569f9904ce0675df650f9619014ebf1eadabf4f674ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e63cb173368e23adfab54e948072ee2a7a29d79ed1e4bfe9476486fb0f0b24`

```dockerfile
```

-	Layers:
	-	`sha256:87661848f0abfa1525b65d00b80f220144040bf0ff8f3e948093bbfa4a1aa05b`  
		Last Modified: Fri, 02 Jan 2026 21:23:06 GMT  
		Size: 10.9 MB (10854069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5924eede0d0beb45f7f60a626be561c1d50c3e74735e86e37700dc5b0f1e8c78`  
		Last Modified: Fri, 02 Jan 2026 21:23:07 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:dbacffbf856eb14cf139f2b7c4d30338357928cfa32bc85aeb8bffed531c5f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280169485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c2c9ffd786468fc343769bfb474611a124ec22468a0bf9af8bc61cbe74541`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:12:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:15:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:15:01 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 06:12:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 06:12:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5388570833e7ff5a3b6ddf9a424d471e073c109ee58e115df3ece488cbb89d91`  
		Last Modified: Tue, 30 Dec 2025 06:13:01 GMT  
		Size: 75.9 MB (75919348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f5064feef79db34c21a2dd41749a2916949d03779f5c73c692a7d8deaadd7`  
		Last Modified: Tue, 30 Dec 2025 06:12:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9b4e9000d302d567d94b5dcc7fe080e403bcf723deb3d8794d544c32c71bd8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20064c1161ab4c5f446c880bd89a41873fbcceb4b33db56e9f4395f80aa77a1e`

```dockerfile
```

-	Layers:
	-	`sha256:374539d44b6a4a49375d49799d09dc7cc8efbb7a1c873191aa5dc9b9f426be60`  
		Last Modified: Tue, 30 Dec 2025 09:23:07 GMT  
		Size: 10.6 MB (10594828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e955d7ff6063882dc3be109953449ae3ee88be05efa1ead5ac81a297692d54b6`  
		Last Modified: Tue, 30 Dec 2025 09:23:08 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
