## `golang:1-trixie`

```console
$ docker pull golang@sha256:ce3f1c8d3718a306811d8d5e547073b466b15e85bfa7e1b4f0dc45516c95b72d
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
$ docker pull golang@sha256:7fd3360ef8b48094d824850c36831d84a6004103e280b9bc9203538519b0db88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312086872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04d1f731ff068b4fc71e19f0132941221961d4f4e105e7dfe8251dba9731359`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:40 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:40 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:40 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d14b9fe3cf04387fde1d9bf3c933855d2ff868fb1abf38be71ab202da6000`  
		Last Modified: Tue, 17 Mar 2026 00:20:15 GMT  
		Size: 102.2 MB (102169832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eacdd96638d1c23d2036ad1f887f1ddb5aa71b14524a49d41783f0d51c35238`  
		Last Modified: Tue, 17 Mar 2026 00:20:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:31cf43a0e80c706bc6a9f98659da9d8d6cfe6ddc522fe0ec0d524b05837dbc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10816002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b247110aed2d17193a58019a2690e0b0575ec26a4c6a81fea59214b1f1607ccf`

```dockerfile
```

-	Layers:
	-	`sha256:8803addc108c4d431fd12c41d43b520eec0d1a8b97130c6c55d9fd72d1e9832a`  
		Last Modified: Tue, 17 Mar 2026 00:20:12 GMT  
		Size: 10.8 MB (10787049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e06fb566122ef9e1d619846b4dfe6765e22b8a6326cabe944b9d1ba67dbe27ff`  
		Last Modified: Tue, 17 Mar 2026 00:20:12 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:5d3343de09a61f303ca7ac3572a8e952516ec01448de5e2c80033fe8882af4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270645999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80f70554a95e4a4f695037fa408d3ff37c7121b389d3e753a81ffa7c3c2a781`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:41 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 02:18:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 02:18:41 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 02:18:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:18:41 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 02:18:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 02:18:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadd3d87fed9ce0d3b69c332e87ae3c005fe2b7ae4b84347b69aa350d0cb394e`  
		Last Modified: Tue, 17 Mar 2026 02:19:13 GMT  
		Size: 72.8 MB (72805177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef054173131074299f532aaf3dd98fd1e22604af9ac81848e143f3d3ad5deeb`  
		Last Modified: Tue, 17 Mar 2026 02:19:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7d2d7087bf8632d00e4afafd72092b0db62717ddb2c7855691df08ea7ecee1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab950b7993afb3311dbfb8187a829973573371adb19dea25e43d61709dfd1cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d161394f87aa7ec4ffa65168a815565e3c3a900785ecff08fd4be65e1e08bdf`  
		Last Modified: Tue, 17 Mar 2026 02:19:11 GMT  
		Size: 10.6 MB (10582968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d89dbefeed56bef8b8e6a7e794dd11d7b2103c1dad1f793ed898aaa52f385e`  
		Last Modified: Tue, 17 Mar 2026 02:19:10 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7bf2aa59cf7d604790e9d14d78e0adb9fbea4050ca395bd739dc6a39eccf7d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304689572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b54881adaebb77a5a34526af6f469a712c8165e282c0f1eadd1e9451c35af56`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:43 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f232ecc1135e2f1dc2e032d5f442a0ea38c681c6a1e3fcbdaca30df6db9735`  
		Last Modified: Tue, 17 Mar 2026 00:20:20 GMT  
		Size: 98.3 MB (98310037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0375c8030e5733d2e772a9709227ee5017bac387b979d94d7db9081a8b44632c`  
		Last Modified: Tue, 17 Mar 2026 00:20:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:5bec9b593bdffb9b17ba24b2d671a0f881684956a5345bf3d67a2bc1976d0769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1777a24e8f1f96dc1b1da355658a23a1a6a0f243a7dd3f6b5873e13cf1e21654`

```dockerfile
```

-	Layers:
	-	`sha256:0265e94c30b759e32f94be463148859b1bb2bef068829ad6d105b9a6e2e98e56`  
		Last Modified: Tue, 17 Mar 2026 00:20:18 GMT  
		Size: 10.9 MB (10907552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da51ea871dd5c99610e5cd10bec9ff9e2f5995ea01502c9a3c1c86e568c9582`  
		Last Modified: Tue, 17 Mar 2026 00:20:17 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:07435f5b4fe868002d342e053485c0cc5b98ed4eb50e719e4494e6fe67b57b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313548848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc956915ce109bf9f2d9ade4030e25da292b559cdd60912d8f0702e57e5272b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 00:19:46 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 00:19:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:46 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 00:19:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 00:19:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f353f1e4a2f435640f288fe8fbc7e097c30d847501200ad100740bc0e0130983`  
		Last Modified: Tue, 17 Mar 2026 00:20:23 GMT  
		Size: 100.6 MB (100609249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb07caf9c739767295e4b0d3b36abebfa29f9d22222644122dcb4a2deeeddd8`  
		Last Modified: Fri, 06 Mar 2026 01:12:15 GMT  
		Size: 65.5 MB (65541795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882e68ce3988bef339472abefa19572fcd6ed4779ac42558ff7043e86c12e959`  
		Last Modified: Tue, 17 Mar 2026 00:20:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b47cec827e2620f5ef7f8f4f87d70a03a6f54cc9066ddb0537b14ba61cdf04b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d2aa6eb589719bc1de84973890704cf9a51e73ab8fd4ea3b7eb9b567d8911c`

```dockerfile
```

-	Layers:
	-	`sha256:766f8302939a2fee1ba4ab9077fbaad9f9f273f08aa97144c3abf7a11ce2911e`  
		Last Modified: Tue, 17 Mar 2026 00:20:19 GMT  
		Size: 10.8 MB (10758292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b54d2881d70d42a719082fe6b62e8b2c27532ca26ea42b99bfa82b4b2f9193`  
		Last Modified: Tue, 17 Mar 2026 00:20:19 GMT  
		Size: 28.9 KB (28897 bytes)  
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
$ docker pull golang@sha256:3a03f1c745c948f1873b6c142c167f9afbe2e0eb1e3cb396d63061c7073b6731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287211438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ff1c5be1e66474f647e7c60ef5867e9868c48b594646f8c032baa25261e788`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 01:10:43 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:43 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:43 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 02:24:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 02:24:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482efadc25a9b34b8c20c6c21be2b4702b2d6ebd6fad8110176296e602b9e6fc`  
		Last Modified: Tue, 17 Mar 2026 02:25:01 GMT  
		Size: 76.0 MB (75982125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743f19db539a4c379e26e3d72b0a852accf178a17b9880e8f2a12d6fd8095d38`  
		Last Modified: Tue, 17 Mar 2026 02:24:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7d71cfb178e68928f7e20842791746fe041047f84d3b2951e285cb161a57fa22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47171cc144f7437e65bedc09e19cb91a2c00500dc9b28bc14ead67e29e510203`

```dockerfile
```

-	Layers:
	-	`sha256:3583d30e885bdc1df1e785cb9b5de4a89cfcf5b56f77e827793f1122f605a5a0`  
		Last Modified: Tue, 17 Mar 2026 02:25:00 GMT  
		Size: 10.6 MB (10597449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf9fb39331c706a028c2a0765a7fd1b2cb66438373e1aa4df4e03311a2d794f`  
		Last Modified: Tue, 17 Mar 2026 02:24:59 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
