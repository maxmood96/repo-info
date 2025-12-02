## `golang:tip`

```console
$ docker pull golang@sha256:112aae4ffb6f30482c0d5fcddaf7f74388814a1056deb90889965f8eb0d7d81a
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:b087cd101298d716b002495eead58dc074951cfabad0590b82a5dc35cde16b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338904504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8684e14c5afdcc6b0e0c3fcadc702dc603e6cff451dc5a0d65416360d6b6d762`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 18:09:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:10:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 18:10:46 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 18:10:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:10:46 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 18:10:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 18:10:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5becd1c95ca291ce7cedde78455ae18a4face9efcec058160f938b2dbf7c3c`  
		Last Modified: Tue, 02 Dec 2025 18:11:34 GMT  
		Size: 102.1 MB (102108655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad64e80e49a41074f81bc07cfccad93afb6fe3ad38cb7d1f60c0de26e52fa9`  
		Last Modified: Tue, 02 Dec 2025 18:11:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7c8713f189a47a9e373d9ded1859ab46f300422a5c8a5155da949ea83e56c27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171d964c3a25cf3d430b8c124675e7f1d4761bbbcdea96a11b6181bfd9fdb733`

```dockerfile
```

-	Layers:
	-	`sha256:d4a93c93fb91fa3b69aa209a61c31a7f8433d293b7ca186d1355d651961f1cf0`  
		Last Modified: Tue, 02 Dec 2025 18:24:17 GMT  
		Size: 10.8 MB (10784510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd74859a37f871b3e337f2d9c6e03370e325465b6a941dd093f5d36856a2754`  
		Last Modified: Tue, 02 Dec 2025 18:24:18 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:a0c5f9b912ddb7eb6470f3b7a800d44553c8dd9393fdc75c57837db45bf84fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295004126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c224dc4d2fc90e5a8134304d265009fa4ac9b62c99b2d2e446ca60050c6c099`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 17:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:56:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:11 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbc9638d242d7c50bbaa4dc5c73dfc88355ceb4f9314921c7e52953097058c`  
		Last Modified: Tue, 02 Dec 2025 17:49:42 GMT  
		Size: 72.8 MB (72753906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d6c373d165edd57ccf29f212c9106bcc6dbcb4f0038a410dec7b4e94fc272`  
		Last Modified: Tue, 02 Dec 2025 17:56:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b17ec7425dedd663f26348e2e3f59c8ac47f32610c442b91c82d280161fc3380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772474de4810c82091aff576e7ae05004f7c3c37d9d0d46680a69d34a518cd1e`

```dockerfile
```

-	Layers:
	-	`sha256:87ec2599576e19c7a07fab13ab77cf9dff214d8d38fcf1348ac447f5bf36f761`  
		Last Modified: Tue, 02 Dec 2025 18:14:10 GMT  
		Size: 10.6 MB (10580397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275d7b835c24ed2394d82171a2e8f95b5a9bd80aec8b72c5048b108d853ca601`  
		Last Modified: Tue, 02 Dec 2025 18:14:11 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:30caf4a5008beb2e0565bd42078e2d795811b9dbc80c138216032f04253f292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329721905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078c9140b9ab50d53a830d45455ef3218c4559b6be48a2b96c89406709a7d3e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 17:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:55:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:55:56 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:55:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:55:56 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7737ea2176ef14c32fcfd2e62f5ba913d20a7bb220e6ef5d6988e26d82c7d`  
		Last Modified: Tue, 02 Dec 2025 17:56:50 GMT  
		Size: 98.3 MB (98254335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc435efeffe938383deaa9e8953d2840885b4c2bf78fc755e5f676d0f2d675`  
		Last Modified: Tue, 02 Dec 2025 17:56:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4de73567d67775021bfba3844fcebb8ab3b905a6e933d94d02371d09c6a848e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517757cc5a04201e575840cb5ed300736cd027d45c678e196b1d5a6d3106d8c`

```dockerfile
```

-	Layers:
	-	`sha256:1196284bffafa0a0668948661fd321d05cc45afbeb9c4fdd6ef7c779b44240a6`  
		Last Modified: Tue, 02 Dec 2025 18:14:21 GMT  
		Size: 10.9 MB (10904965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715a519fca51296fe9b0a69b6701d5fedb0e372891cacafd3f7501eb02b40bd`  
		Last Modified: Tue, 02 Dec 2025 18:14:21 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:e3bb7f797f0e3931d8ba5d210b54c21a9e33738dc665291df002b4236c2d738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339965063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bc7f91676df84d228d8eff7c3f198b1b5cb67b8cf6522743b89b90f3f1d8c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 17:54:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:56:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:26 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:26 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc600ab9b8f3341b540cda9da2c6bc66b96299282d51e1f9ba51ceac278aaf4`  
		Last Modified: Tue, 02 Dec 2025 17:57:31 GMT  
		Size: 100.6 MB (100555199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8fbe72dece1d5dad9d203aa297893a3a905f5d8c3f8c60ffe70b3551969c4b`  
		Last Modified: Tue, 02 Dec 2025 17:57:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f34f43125b7c81043486035538c90cf8b4044190991ad72c1dda710ac738b80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2ad8b014b052a0a4636a13f5cb58ad718324c7190c4c4d18833fa3f5788c7`

```dockerfile
```

-	Layers:
	-	`sha256:5c80f4482239d40dff5166a1d68e61f2a01d8133940222ec5ac0d991a1504b40`  
		Last Modified: Tue, 02 Dec 2025 18:14:30 GMT  
		Size: 10.8 MB (10755774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb481efbec70529e767357a57b1f3de19f00abf9d2a3874eb24df4552cf8fab4`  
		Last Modified: Tue, 02 Dec 2025 18:14:31 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:535835975343908067c4c541fce670a57c0712feefea783dbc757ecd80c489b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336684119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f606fab4265ae9826d6506a37e0a93618fc192aabacb1081df0b2be8bdafaf21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 02:50:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:50:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 02:50:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 02:50:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f27d1d6766589192c9783cd48677f240bda846fcb9b1b3cc7956e55f813b1d`  
		Last Modified: Mon, 24 Nov 2025 22:47:08 GMT  
		Size: 92.8 MB (92815523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ee4242807d5eec61fa095a5c2f00f155044d9c099f2f96b9280a66eec7ef6`  
		Last Modified: Tue, 02 Dec 2025 02:52:27 GMT  
		Size: 90.7 MB (90741131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48deb93f3cbb45b7edc6ca2db63735814f002cd7dbbf1968321d2fa3ce51e7`  
		Last Modified: Tue, 02 Dec 2025 02:52:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:999325edb8e5f9aa6b13f669ad25b5fd61a04e4bb6970ab720dffeaaae1c2375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9763edd59d3440f126fb6b465fb78476a5c55b49ee698f92d3db672a205031`

```dockerfile
```

-	Layers:
	-	`sha256:987f0765e96f9ec7abe4f8b0cb55f1045f5bd8f26434be4744a3d729880058c5`  
		Last Modified: Tue, 02 Dec 2025 18:14:39 GMT  
		Size: 10.8 MB (10780296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea05819265039652298944b95f533891c98abe6f687b7b0a5808bafe046b1a1`  
		Last Modified: Tue, 02 Dec 2025 18:14:40 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:e1fd1b07ffade77905b8ba97a01b10c9fbac72359dad506fa51795ea937132e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362359534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f79d5084f776552197747423f5573ff23a484cee56035664b07e476eb2c5dca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 14:37:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 14:37:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 14:37:11 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 14:37:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 14:37:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3dee934585ab74409616bca59b39f30d113b18941a71d91f5e16fd83b3d954`  
		Last Modified: Tue, 02 Dec 2025 14:44:57 GMT  
		Size: 91.4 MB (91379080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eabb86a339e4698577a792043a92fbc45fe6d4333876beb90e1e48d96ddd56`  
		Last Modified: Tue, 02 Dec 2025 14:44:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0733df859159f4ad5951fe5c56bef52fbe65b0a42cfd5629920b9c18786a7612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc5673918c10be78f6e38b13fc0ba65c9a415c7f7fc90c76c09ff50392e699`

```dockerfile
```

-	Layers:
	-	`sha256:d21b0150e0d49132324c2805270df86ae8f667794fd73b94ef617b87cabfdd6f`  
		Last Modified: Tue, 02 Dec 2025 21:23:59 GMT  
		Size: 10.9 MB (10854129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2438de5e81d1fc9d07f840bcb55a70c0090d8edfbc460c9a161b431a9c33466f`  
		Last Modified: Tue, 02 Dec 2025 21:24:00 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:bea5cf1a9fa6d7d50b073e6d9cc85026e9c21877e7ee29d3820ab2ce6bafd5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313962149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f4a20bc6408728548972fec2719a685d62d4c191fe3fc6887044d6bb471154`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 22:37:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:24:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:24:38 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:24:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:24:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5391d091a5bc1ee814ac074a3bb08930ad54989e68737b6f3ab762b3833788`  
		Last Modified: Mon, 24 Nov 2025 22:38:37 GMT  
		Size: 75.9 MB (75919106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d587a6ce9332cd64ade4d6449590e6112812b54bfc350eb8b57100babd31c208`  
		Last Modified: Tue, 02 Dec 2025 00:25:52 GMT  
		Size: 93.3 MB (93286276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08440b358baed72456badec2929b9cfc484572f9545f484bfe295627a36acbb3`  
		Last Modified: Tue, 02 Dec 2025 00:25:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:18195eb3a197ae381a2b5a6726fdaa292a972df514850c9412d39b39fafde550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c426c6b79bdb6bb17b460660228be119c9f4d5c785da1d91493b339d1d6549`

```dockerfile
```

-	Layers:
	-	`sha256:d15431144cc764d37858072d6bace88eb6800887ea1fac49adddcd3e821c662b`  
		Last Modified: Tue, 02 Dec 2025 18:14:58 GMT  
		Size: 10.6 MB (10594910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b407e9bc9349fc6d873918ab50fb9064220fa7a094bae16767c0bce21485ea0`  
		Last Modified: Tue, 02 Dec 2025 18:14:59 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
