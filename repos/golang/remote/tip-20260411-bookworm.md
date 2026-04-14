## `golang:tip-20260411-bookworm`

```console
$ docker pull golang@sha256:c8db04841885c6e2767f1a4e981948da488a28848a53d31405355c2534050c45
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

### `golang:tip-20260411-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a3c36239fa26e3854e871380c2f558231f17c6eb203a6fa667e5c41ea5f458c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323953816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58613e14d7f970f2782583b83f2ca8840a68a2a8baecfe6db08acdd3595b60ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:00:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:01:55 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:01:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:55 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:01:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:01:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f0901e84e60f5f5f418994542e28156e5a631b6ab1987bd5c0d9bf06b8387a`  
		Last Modified: Tue, 14 Apr 2026 00:02:25 GMT  
		Size: 92.4 MB (92448608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab04cb4a8e454fc7559b5ebb652cf17e60070b889bacf79f9339f14ac23b48e`  
		Last Modified: Tue, 14 Apr 2026 00:01:54 GMT  
		Size: 94.6 MB (94581946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241fa746410dc702453c763ae0927845774847b8a2f8ca4585f4c418bf1e859b`  
		Last Modified: Tue, 14 Apr 2026 00:02:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2766aacfb2dd8ea5ecba076a426981f1d546db7cb3bdbe21ac763fda290d5373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4891b283d3fd9c1e2e85644326c3d5393d0b524f9a9bd54f550008bd12e2b58`

```dockerfile
```

-	Layers:
	-	`sha256:d6a95def8040c8d832f0717ea43e91781c49b73df148995a9f81d79d2c5020fa`  
		Last Modified: Tue, 14 Apr 2026 00:02:23 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322a23fec77fb53ea9dcc5efd1b5ef23b10a8c458beac52a0c662839a8b83b52`  
		Last Modified: Tue, 14 Apr 2026 00:02:23 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:1b3bf12623640ec1abcec6b4592ec48c5f75efd579f3b07297d3dbf19d77e3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282999700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49991be9718f0aeebaddc6a20113705d6c5629dbbec7af80f5c9c0a81d71461b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 23:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:30 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:02:30 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:02:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:30 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:02:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:02:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626437a99246a6d3dc330350016eb9ecbf357123cec9028fd988893fdf863224`  
		Last Modified: Tue, 07 Apr 2026 03:49:22 GMT  
		Size: 59.7 MB (59651814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a7d106fcf9fbe302c2d70ff92164fd909c416c0b518d0de206c01999002e5`  
		Last Modified: Tue, 14 Apr 2026 00:02:59 GMT  
		Size: 66.3 MB (66305358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5edd4ff2dbd145648193fafaa3d5f04805713affd95a7e7d9d0029f6ec1270`  
		Last Modified: Tue, 14 Apr 2026 00:02:12 GMT  
		Size: 90.9 MB (90892470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898901b5e50eb6737660753150b6e0d89a24e4e2f3fc75cdd519d4278d8d0abe`  
		Last Modified: Tue, 14 Apr 2026 00:02:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3d216190641f9cc165b0dd3b8843b1289ae8790a751c7b85fe26b107edf20602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c496a81cdbb3c096fa0fb2b667fb5d49e47661eb732260504d3fb39939839187`

```dockerfile
```

-	Layers:
	-	`sha256:4d6918dbc0e8f9222fe3abcd86bebaca1d84ffd3dae5132a4f3f960d77b63b9d`  
		Last Modified: Tue, 14 Apr 2026 00:02:58 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a1fdea723b0b5896f8867cb2827bfb9552b80cf16075bef7126cfb118fa99d`  
		Last Modified: Tue, 14 Apr 2026 00:02:58 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2442f3399557b797464e9b87fd177ec91e824b14e6d2eadc8eb06aae2a022953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312679922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8fd0d0a2c22ec00951caa6bcfb2a67c3a0924205c7a7ada722b7d556fc91ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:02:56 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:02:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:56 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:02:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:02:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755530342aec5f717a5081876f946443441baf62a2b27b4344511dae8ca54225`  
		Last Modified: Tue, 14 Apr 2026 00:03:25 GMT  
		Size: 86.5 MB (86521397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca293ee12e748379dfc7e49600a21d46479ed1f62dbf74c0006b5ec77222dadb`  
		Last Modified: Tue, 14 Apr 2026 00:03:08 GMT  
		Size: 89.7 MB (89700892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc6deb28e9b86ba5f2bb5ee4c1ef0732b0c8ec3b64dd3ce72f7d1b7d0d18b91`  
		Last Modified: Tue, 14 Apr 2026 00:03:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:09aa28ad96e3c6c05456a1463445aec1031d67593a22c9b30f0738fbea8fdf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5576aa4a2ce131a26a3ea27f0982756905263f2bbd4423139f318c241e989dce`

```dockerfile
```

-	Layers:
	-	`sha256:cb8139d00beacaf820d1a6839617e5bcdab46557515d9da4577af93a546c7888`  
		Last Modified: Tue, 14 Apr 2026 00:03:23 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ea0a15755096d64ce08d428fbc5b9871d8e307097fde339dcf13fcdf3904c5`  
		Last Modified: Tue, 14 Apr 2026 00:03:23 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; 386

```console
$ docker pull golang@sha256:cadadafb2cd8bf966079765a337752eb5e3615645ed4991e6699bdf94ec629b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323077181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1665021e520426328a739c9c3d49e53604d186810908ab7c5069673f765c58b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:29:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:29:19 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:29:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:29:19 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:29:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:29:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fefd2d4d18c0e4a1f706c31af7edb1bb87765de90f366b612fc4f713dbbfa`  
		Last Modified: Tue, 07 Apr 2026 02:40:53 GMT  
		Size: 66.2 MB (66234451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84410ba979cfcc9b020e0444b2750840f238eeb9f167050c47bc4c745af3f687`  
		Last Modified: Tue, 14 Apr 2026 00:29:46 GMT  
		Size: 89.9 MB (89871426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5425bebab36322e26303eb33424df1802209b7a6b3dc6b986570aca912bfd`  
		Last Modified: Tue, 14 Apr 2026 00:29:28 GMT  
		Size: 92.6 MB (92621258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f276195dd9c53a3793ce253229828d7966e5ad9d85b74bbce287bc3f648004`  
		Last Modified: Tue, 14 Apr 2026 00:29:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b7851406526b54509e6857ce1b30435ea788e554679ce3d41e4a875ebeed853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c484ac449da8124a48e4e92eaed6d63d3f45129bb2c3084666b47cb2010b9e`

```dockerfile
```

-	Layers:
	-	`sha256:360523c77a47955eeba861b980e21128d89946b3d3475dee71d74bdf1fee86b6`  
		Last Modified: Tue, 14 Apr 2026 00:29:44 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff7223d72b3d91585bf819ff18f5721ded2dac87b8d29dd757d21761d34a86c`  
		Last Modified: Tue, 14 Apr 2026 00:29:44 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:649f4a06634aea10f3424691417fa442633109bcdd16c4cacbab51a5949e1a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294239297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f5ae5e0d6b31676f8fbb9f862cf2e3bec1964255d28069ada4960a571ec66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:52:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:34:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:34:49 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:34:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:34:49 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:35:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:35:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf83c0e933a4e8a498aae736ebf10a823fd9ecc755d47233e566e941c9893a`  
		Last Modified: Tue, 07 Apr 2026 21:54:45 GMT  
		Size: 70.1 MB (70051233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028638a1bf8399bc8e48505c0bf67d893bfe367bad9e765872afb2b497a1ef32`  
		Last Modified: Tue, 14 Apr 2026 00:37:06 GMT  
		Size: 88.5 MB (88479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd9a7a4a5d96cb12c93edceb8ab9c61c972633c515113c0c1d812132e6f9abc`  
		Last Modified: Tue, 14 Apr 2026 00:36:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:afadc83a84406a9b385701508a3a556b18b20cd7224f6293118292ecbf4c55f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c460b83b1b84ccde721ece4766f83a366546deb6b2bfd6fe1e887f812454473`

```dockerfile
```

-	Layers:
	-	`sha256:00f7491909d9f25311e813317724ec61ce705ee73f786ecbb27b41ca2511edf9`  
		Last Modified: Tue, 14 Apr 2026 00:36:56 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:a5798963c1784c88f897aafa9826a5972935b369a126fe73e7e18155cc1ea4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329662433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe1d8287fe49457b0dfdbcb3ceb8888e43e086a528572819d730513e91d082`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:06:08 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:06:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:06:08 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:06:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:06:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f67f0a7bc2638109117ec62f84bf4d06b91348ec6d8486011aaadaa5f42f65`  
		Last Modified: Tue, 07 Apr 2026 18:22:57 GMT  
		Size: 90.5 MB (90462415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0175a2939aed372a8574a3f30ca86be23817fbc044f643da506137d0f0ef397`  
		Last Modified: Tue, 14 Apr 2026 00:07:09 GMT  
		Size: 91.3 MB (91345222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b06511df4fe82f52bbc4a52add1a56ebd068e6671c2f94c7d65c5f356a4644`  
		Last Modified: Tue, 14 Apr 2026 00:07:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8e03de87d40ac89623584c02e983f1b9f42662effec2111a007a945426b5eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ee191b8a797b579920671dbb8685d4862089f08343afa46b389e387d1f0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:2cd9c413495a1983f0f964729af6c2e337664a556fde85b63a4db1baabb7c644`  
		Last Modified: Tue, 14 Apr 2026 00:07:07 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9083aa9b52cd645cc50f727142a4a1aef76d2ca07f208a2f1f68303e2a83b5`  
		Last Modified: Tue, 14 Apr 2026 00:07:06 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260411-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:8bfa59db73e8e4b57c92ba3deaffafc1b3918d9029f889a13ff41bd094359de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297517299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452052d5eca59b2a994524e4a1d71b48b166051f6ec82f4573bde5d6353ef89c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:18:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:26:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 14 Apr 2026 00:26:08 GMT
ENV GOPATH=/go
# Tue, 14 Apr 2026 00:26:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:26:08 GMT
COPY /target/ / # buildkit
# Tue, 14 Apr 2026 00:26:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 14 Apr 2026 00:26:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47976b1872c5d8fc1ceda4d073087f195be5506b083608f5c0a6767f6b55978a`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 24.0 MB (24033635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3377e46a7f95ad649f4e145572c4253ed3ebf1b9fa463b58c96cf8b20d651ac`  
		Last Modified: Tue, 07 Apr 2026 04:55:04 GMT  
		Size: 63.5 MB (63501358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24453cb2bedf63c229f4b336860e90e96e0c46e040b8b2ea689630f1d4facda4`  
		Last Modified: Tue, 07 Apr 2026 21:21:30 GMT  
		Size: 69.1 MB (69055875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5aaa70187b5fa60b40f4f6aa959f778263834bd8f55472a34e3a940460eef6`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 93.8 MB (93778190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df041588aca5063710bf69bc675b66c9f35376e6c44aefa63986612aefa20062`  
		Last Modified: Tue, 14 Apr 2026 00:26:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260411-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c0b740bdafa96d20d2bfe8fcec38ca48de26dc7281f698266a4812d2fb81338a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76b7d108a3163f8f5331538a61696ed3620178206fd1b89fc81ac8f90344bff`

```dockerfile
```

-	Layers:
	-	`sha256:4e44cc37436b259444b3d64cb5e48ca75e1753fc69ea9a31fb4aa45abd535229`  
		Last Modified: Tue, 14 Apr 2026 00:26:57 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98802b848b14e7efa585675ac60f8c49a907fcd4d2dfd688220324f7234269a9`  
		Last Modified: Tue, 14 Apr 2026 00:26:57 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
