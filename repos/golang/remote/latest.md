## `golang:latest`

```console
$ docker pull golang@sha256:ce63a16e0f7063787ebb4eb28e72d477b00b4726f79874b3205a965ffd797ab2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:c1252002e1a0ba34875937d59d4f123d0a4673a50f69c38fca4175cae194c7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304978850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe09d2a291ba702f877ea295de7aa66425feac0910533c88199975c9890c52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:05 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:05 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:05 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c1cab6671eed9a89352ef15db3eca9ee1c8077c264b7dd4daed6695dbf4d25`  
		Last Modified: Thu, 15 Jan 2026 19:31:52 GMT  
		Size: 102.1 MB (102138596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:22 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d0d9c72cf24c1f23f89d498c74c4e556ad64db721b8e85e1feb68f85fea7c`  
		Last Modified: Thu, 15 Jan 2026 19:31:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:67480ae6eae1776950de4a4eea3842de12d6c577c6f684ce94558b6b615fb983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4142ad5615285587d03b565fdf985941e349bbe7e1a7ba72e75f6ebd9db881b7`

```dockerfile
```

-	Layers:
	-	`sha256:955d6afbde20fd380b907b376cb8e7fe7f934c4e499ff9056d311ae4d0bb8f20`  
		Last Modified: Thu, 15 Jan 2026 21:45:42 GMT  
		Size: 10.8 MB (10785503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90ea038ce26208360d921b0d9315f25fbd1da60cd9330fc68c6902286baf7e1`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:290be57b792f7ac6abceef24b4fce9634553181cc8bea461e94a4bcafd132ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263915378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d27475033a69e8add253031a6fc3245485635ca65bf7eb83a54a07c5fb2b954`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:21 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:21 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:21 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:21 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f261367c1ea195c3c24b87d9aae56a2e3efc7595d6cd662b5695492bc804d8`  
		Last Modified: Thu, 15 Jan 2026 19:32:04 GMT  
		Size: 72.8 MB (72783541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:05 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8190541343da7a6c6a568eda61436abc2c54b2b9ac0a2358a73bcc7be743e1`  
		Last Modified: Thu, 15 Jan 2026 19:31:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:248007f52ab49be03f2398674cca1e3db8c450ffd622e219d6d25fe8634cb51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb940d9da613d3342f15a512188b3ce3730d9405294849ca72980dcfd0e5861`

```dockerfile
```

-	Layers:
	-	`sha256:54d593b330f3d518d4cfb7061a6b1cd60069656b498bad0e3bb464e436c312c3`  
		Last Modified: Thu, 15 Jan 2026 21:45:53 GMT  
		Size: 10.6 MB (10581424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ddc4a6986a28d26ff6d772870b1c0dcf445e41e360ec4b18ef4758332efb3c9`  
		Last Modified: Thu, 15 Jan 2026 21:45:56 GMT  
		Size: 29.1 KB (29086 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:226d5b4e541aa23f860743cd1719879ac1c2be3929697137812cf22906568c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298204654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef45111ba5eab2d4f0c694f700c342b243ffa0674dc2054f622316bac0cf048`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:07 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf0b8a807c2eba959326591a264b2e464d70f28bdb151bfa8892097a09d6ab`  
		Last Modified: Thu, 15 Jan 2026 19:32:00 GMT  
		Size: 98.3 MB (98283068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:21 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802482bf6331395a479ff591f73ad14f7e0c13903db55166981241fb07ee77a6`  
		Last Modified: Thu, 15 Jan 2026 19:37:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:a0531d06645b080392bf589f8e05f43767fa012e04fcbaec370618d70aa1b136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1abff5b3ff5ed80eab47634048fe3acedbc8ca42dbcd707cb136c693af0d246`

```dockerfile
```

-	Layers:
	-	`sha256:4c1082f316ceffbf216ce72299fccd5310ae775091fc6a37286470fc8bce5269`  
		Last Modified: Thu, 15 Jan 2026 21:46:05 GMT  
		Size: 10.9 MB (10906006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0379b02025f9abb26fda43d7699dcbd72c74240df7d57c3942b55e775577ae0`  
		Last Modified: Thu, 15 Jan 2026 21:46:06 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:bf3379670697153f4a9d0dca7edec6bfb211acfb26f8ea0016fe230cf3606daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306834847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b963c52faefc03762e6e672b0e862528a55b7566456b554c813ad85aa02ace72`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:35 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:35 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:35 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b98c6d71136a5e0ede9df527a9585f22a3cf5c3b603df1de5764ff015be90c`  
		Last Modified: Thu, 15 Jan 2026 19:32:10 GMT  
		Size: 100.6 MB (100582576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd402dbe928e14f69063c85f23dc6c9bbceb27e04cff93cac6dc77cf1a8f6be`  
		Last Modified: Thu, 15 Jan 2026 19:32:08 GMT  
		Size: 58.9 MB (58871754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3015a2e67a414f81ac644eac544a316906ab0f92ebe53e14b096f969eac2c487`  
		Last Modified: Thu, 15 Jan 2026 19:31:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:d8bb8b781b6ded582fe98212e15fa9318fe92c9d70150d7a24e15309e645f8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ae229b6f0a62d55d563216f5c513ffa22b456dd2dfce8c9d23f34c7ab9578f`

```dockerfile
```

-	Layers:
	-	`sha256:06a045f3236ccd704d1121947e086436cb8dcfc3d8efcf437c6d9b16033282c1`  
		Last Modified: Thu, 15 Jan 2026 19:32:07 GMT  
		Size: 10.8 MB (10756748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c83a22b977989a4d93a7c8684d3b3a2915fc2b3bc8c775f53ac5d413ad464c7`  
		Last Modified: Thu, 15 Jan 2026 19:32:05 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:a495aa757a91b8031418f46c61f3d1ab2fe157ce4bd8db6a0ca896fb9ea27611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304122648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d69eeef418a6b98839011ea5fd74f67e27d7221d269dd4fd898202ea98b866`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 16:13:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:15 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:01 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:19:44 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6963c45fc75dae1c69a32ad6c3270c86fd5157751391796c0d838607e88acc0`  
		Last Modified: Tue, 13 Jan 2026 16:14:26 GMT  
		Size: 92.8 MB (92844600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:34 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1718e0e8b3469607a4f3444c04539e164bf8911fca14caf1a1103766bdf84f`  
		Last Modified: Thu, 15 Jan 2026 19:32:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:eaf423f08545df568f64c2f4036b7384b45c1c0641d8c277ebd6a1d92181d321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fd9ee042a475b3d674f7d7058bde5c6f2a400000bc8ea7b7a0744941d19a9b`

```dockerfile
```

-	Layers:
	-	`sha256:3cbe35f9becefd0da0bb5eb6c88e5b26fdc99807180611087cfb9fd1451865cd`  
		Last Modified: Thu, 15 Jan 2026 19:32:21 GMT  
		Size: 10.8 MB (10781313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fc4a9cdf8c275e31e9ef1c6653cc31120a87dc1b81d93316a50ae7a297ee8c`  
		Last Modified: Thu, 15 Jan 2026 19:32:20 GMT  
		Size: 29.0 KB (29020 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; riscv64

```console
$ docker pull golang@sha256:eaf774b17f5de007277ed8a891e838feec74d98c8d7a13389538e5897b581a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329682990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741a865cda10e5cd37d8f790109cfa17ca7babe3e076e3872bc2935a94c07aa3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 20:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOLANG_VERSION=1.25.6
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOTOOLCHAIN=local
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOPATH=/go
# Sun, 18 Jan 2026 23:11:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Jan 2026 23:11:45 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 20:49:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 20:49:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:13 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f745939b2d13a20bc5767dafb02ca8b86a288cc70e3062fa70de76ce5b598`  
		Last Modified: Sun, 18 Jan 2026 23:03:23 GMT  
		Size: 66.7 MB (66660714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6ae4171d4a5e53813caeec0fed4e819700c3a0b1ae7031301cbd179639a4c`  
		Last Modified: Mon, 19 Jan 2026 20:48:15 GMT  
		Size: 131.6 MB (131626895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76383bda51f6d2301c4d245b282d3ec6e006fd6e4d52961e3dd0dba3364c9182`  
		Last Modified: Sun, 18 Jan 2026 23:14:35 GMT  
		Size: 58.7 MB (58671645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce3a7064671db6af53faab519b9c5576be791225c917043b2a010d21fa4518`  
		Last Modified: Mon, 19 Jan 2026 20:54:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:eb2d9ff7c734ff3896f819192ffba026a820e03cbc305a81beb97ca520b212e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5803995ae5e5263208ad27d1d4e879cb76c8163b59aea068b2793e7a426ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd89e7c8db28bb4552d6bcdcb6e522395d8e0040044f95b3b33a203bc7459d6`  
		Last Modified: Mon, 19 Jan 2026 21:23:11 GMT  
		Size: 10.9 MB (10855146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f94aac16989691ca3cea76c38d1f7b81c1c42035c01f78d9bcdddf3d00dc6b1`  
		Last Modified: Mon, 19 Jan 2026 20:54:32 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:cf57a7791a68b3f1d36ff2cba5e40c332482400dc80dbc59db2f17c21d4e417e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280215132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15aee0decbb2a2bef25c8c7697db8378ae15c1c84126291d71c6c2e16797cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 19:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:07 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:07 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:06 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9c35bb3053dba6b62f75a6cd643bf82fdafb8d0b167812e0490b0fea155955`  
		Last Modified: Thu, 15 Jan 2026 19:30:38 GMT  
		Size: 75.9 MB (75949527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbb76a0abaea4244f95f500f5dc112f9bb60184d69f79da921b7700e619209f`  
		Last Modified: Thu, 15 Jan 2026 19:31:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e16bf932eb2312e47fcc78c666f6d09d46a7482ff5b787ac75a4a2fb090089fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05bafa1753636c71502ecb7fa70ee5314fd714c3d6b846c8549287187f0f62`

```dockerfile
```

-	Layers:
	-	`sha256:68e914194c561e81e281a407a7dbc148008a2d7f26371af7df8be5772dd92669`  
		Last Modified: Thu, 15 Jan 2026 19:31:35 GMT  
		Size: 10.6 MB (10595903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6d3e84380dd4a392c8516d96044f170abf00ce8da2ed5c5fc0990cc4eeb117`  
		Last Modified: Thu, 15 Jan 2026 21:46:46 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:5f6958ea91abc3143040e63d0cd2b46856c1d46ec0d07d7d5f0313bfe0e8df7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1609984458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ab35dddf263a786bc4738f2813cf63f3b1ccc1bf79f4001cddbf507970c49a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 15 Jan 2026 19:34:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 19:34:24 GMT
ENV GIT_VERSION=2.48.1
# Thu, 15 Jan 2026 19:34:25 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 15 Jan 2026 19:34:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 15 Jan 2026 19:34:27 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 15 Jan 2026 19:35:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:35:08 GMT
ENV GOPATH=C:\go
# Thu, 15 Jan 2026 19:35:14 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 15 Jan 2026 19:35:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:36:38 GMT
RUN $url = 'https://dl.google.com/go/go1.25.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '19b4733b727ba5c611b5656187f3ac367d278d64c3d4199a845e39c0fdac5335'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:36:39 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a519eaac22a8e810614a54d1ecd7e172debe7d71f6e27ca1ba91bdc6a0f9e`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484d141a3d44935a72760270d4f6787bbe4cb0a32e834e840563a8475284d24`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4d7e64245aaea9d2fb7e300b6b88fcfa0ab8772b159b7fa10c961614f009f`  
		Last Modified: Thu, 15 Jan 2026 19:36:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b180294a8ef453ef91144aefda6c2e229b04efcfbdb95eab84205d8a65efd9`  
		Last Modified: Thu, 15 Jan 2026 19:36:53 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf89600227a0242479da3c0ae3a845b2b51c2833a42c2472f7e2b259315f5ca`  
		Last Modified: Thu, 15 Jan 2026 19:36:53 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5964e8cbe72df39254ea3c852054cd26c479539b1e7559f92f1864adc4f0fe3`  
		Last Modified: Thu, 15 Jan 2026 19:37:00 GMT  
		Size: 51.2 MB (51244732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bc7300c1c68770859c4873c9728130f2acab3a6b69c81c88a3851fa61b7e70`  
		Last Modified: Thu, 15 Jan 2026 19:36:51 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783588cc72ed2dde28deae4066216333e60f144bed1e46a6a1371f44f8c9d7d`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 373.9 KB (373923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd53c6443492192c1e4fb1d656f1a9f1df39d5baa327d49554328c37470b032`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad2e2cac32485cbbf78ff68f8d974f3149d95c10d58c27c9f46fe3d5cdba801`  
		Last Modified: Thu, 15 Jan 2026 19:46:07 GMT  
		Size: 62.6 MB (62594900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebd4c763d8b6cd3b0be5903a8169fce4c2a3b16ed7198f56bccc2f2ce70802`  
		Last Modified: Thu, 15 Jan 2026 19:45:59 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:e1e18dacd7adf4add2a92b430d2621d557642ee5f7ee14d1d74c74d03018d9fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1949861460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c31a38ccbe1df3dfd43cb0ea6c5a478451e019fbff2ddaf95ff22979d6e1a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 15 Jan 2026 19:34:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 19:34:57 GMT
ENV GIT_VERSION=2.48.1
# Thu, 15 Jan 2026 19:34:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 15 Jan 2026 19:35:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 15 Jan 2026 19:35:02 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 15 Jan 2026 19:36:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:36:28 GMT
ENV GOPATH=C:\go
# Thu, 15 Jan 2026 19:36:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 15 Jan 2026 19:36:35 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:38:18 GMT
RUN $url = 'https://dl.google.com/go/go1.25.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '19b4733b727ba5c611b5656187f3ac367d278d64c3d4199a845e39c0fdac5335'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:38:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9355121c1c656746840ac1667840551ca50eb91ad0fdd5998abd9d407f7ec`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e650ad6dc6e066ce5e98eae46bc7fdc181bb94897c176a9fac4e5c33d06274`  
		Last Modified: Thu, 15 Jan 2026 19:38:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0059e169699b2133b64196e2053a699198a865461c46920627374ed91ae3e3b`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c3479ac13b4f0fad21eaa97d5868653c2de98db906e73faf9af41936565c85`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2f972e1fb7c232eee99601e54d6ba5a085c78284136a04bd1997110e6ed0e0`  
		Last Modified: Thu, 15 Jan 2026 19:38:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dded11f6514d2c10ac7774fdc2b1aed3edd4b6df953de96fe28c8747242f052`  
		Last Modified: Thu, 15 Jan 2026 19:47:15 GMT  
		Size: 51.4 MB (51350079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5035611c4ee80cdb6260d1bf9958289618852a8c763eaa2d57a2879e6190a300`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12f97a129fa2c30c4b78a7bbde3cc80c9b460cbadb80e26d8d224325a16b0b`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 306.4 KB (306414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c766b55e02ffebe111ee9e49a75c64daea8c2f1b370a37e3e6251fb947b14a3b`  
		Last Modified: Thu, 15 Jan 2026 19:47:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dac534bccb1f1636aff5bafa24595f20ebd2580f7bc281d5ae023b536612b9`  
		Last Modified: Thu, 15 Jan 2026 21:44:24 GMT  
		Size: 62.5 MB (62535180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0430c60056b7aed784a829b8b012a32c9aa85cae0a1930bc8aa2684258b53de4`  
		Last Modified: Thu, 15 Jan 2026 19:38:25 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
