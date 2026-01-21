## `golang:tip-trixie`

```console
$ docker pull golang@sha256:5b27144673c4dd11c7cb6958359600677c3fd49fe1d2c34b56995de7dd2a94d5
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:2f1fb97a38dc0353ae47f59b1254728326c90d7edad2fde007e5b61858d78b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339880902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa8737fae26612ba23d33679e8f0f6e88900bc9bc69ef040abb8818f07c7d8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:51:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:53 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:53 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8151c7cfc345cc51449c0dd6a8ccaa18993e1951c412f678cb306fa4645d5`  
		Last Modified: Tue, 20 Jan 2026 18:52:24 GMT  
		Size: 102.1 MB (102138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6a5b8343289eb0c3c52bf550e1fe8d1945ce754f136a34955c716ac7e17d7`  
		Last Modified: Tue, 20 Jan 2026 18:52:04 GMT  
		Size: 95.1 MB (95056396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff79a52a3e6af098975415b98fc3cd77f86d91fcf8cf62c054110a6fbda66eb`  
		Last Modified: Tue, 20 Jan 2026 18:52:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3929d66d11e4098811cbe58fd40add2f6fff1ba235a8d34f0b824b95677f7a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0ba2a8f860a7389f40e7211a82a1948dc840267ca4a84dbc16e58991cdb971`

```dockerfile
```

-	Layers:
	-	`sha256:a492ad9317179f1e263fde1393c870b1e14ad230cabf0ce61ffa666ed2709876`  
		Last Modified: Tue, 20 Jan 2026 21:23:54 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce956bb3d4493d4d78719088de1ebdf35614e8a5a0d9b7275a9b29218506ee84`  
		Last Modified: Tue, 20 Jan 2026 18:52:21 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:85cdea13f383dd3d8c25d78c30b5547363b752a72c7cc0a2718ab8627d11d761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295969268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf15eb779fde6cad094ed0aa172ff33fffd3136aa8b3596485b4492f802904d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:52:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:49 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:49 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:52:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:52:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:01 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9492438db3c959bc13b01197d48adae88a361ac0b6f74fab79e159bcd7c18c2b`  
		Last Modified: Tue, 20 Jan 2026 18:53:17 GMT  
		Size: 72.8 MB (72783454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbc1ebe88b1983952e0d3b08c79038602b5105dcae7c600fd0a26d7e35cad0`  
		Last Modified: Tue, 20 Jan 2026 18:53:36 GMT  
		Size: 91.1 MB (91127787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153725f2c75936e40ffd4a5fb837cdee5b6c7541adf5c825b6c31c43bf298c1`  
		Last Modified: Tue, 20 Jan 2026 18:53:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ae3de0a4b2b578a13a238a1001ef464d75ec612e17bde24422d16bfcdbdbb607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfec1a6a0d1c52114320f538b3da124de5c0ecdf20f60c5abb65fbe2d972efe3`

```dockerfile
```

-	Layers:
	-	`sha256:95452f70c74043a60d110e3bc1343245f8cdc277621300d09077ebed3771fd6f`  
		Last Modified: Tue, 20 Jan 2026 21:23:59 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c7860e9ce20c2def589cd7e3850c43c7c742a9bd87b3f9ff1a05fbab6048d8`  
		Last Modified: Tue, 20 Jan 2026 18:53:14 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:de936eed83238af25913055c7ca78b4227e0a84c4b75591527a55eae4aac3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330677613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83f61752d6caa4bc61d451f368b799234c31004672e393ae7a16ea0c84c3a8e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:50:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:51:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:43 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:43 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76a4e6f647d5353d735d4610905934ff4c7c173cf2ddb32a8d6cf01950209e`  
		Last Modified: Tue, 20 Jan 2026 18:52:12 GMT  
		Size: 98.3 MB (98283267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8704a9b461e9f9c3cf81dacaf53a5375b1bb82e9194e9ce88802dc458b5979`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 90.1 MB (90131959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0879db78529b13232ed9a9d224ed17480d2a1065eb4ee06bba1f0820975cba`  
		Last Modified: Tue, 20 Jan 2026 18:52:10 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:32167ff7ede87fcface4b8eeb3e5d01933f37bbfae5f3c008b8425757339c84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631e3c4e0f68c0608e8a3c7b79940ddd64eeaf2347dbc1a569ceaa30ca548e7d`

```dockerfile
```

-	Layers:
	-	`sha256:dc370af24b8438d0ddd631a2da1b3ce0e23d17ac2de2e05019e668fe8a0d128c`  
		Last Modified: Tue, 20 Jan 2026 18:52:10 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28488d374a0eeec4d947a9a388b893861f223b9b8aab0cbef3179fb66a780c6b`  
		Last Modified: Tue, 20 Jan 2026 18:52:10 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:2a4b4e4b947a0d9b36b1c46cea92604a70d6b33b15dc773cf3bf3a2e6cf3054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340911266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70bedfbab79403c81e5d76c273d1bedba8ceb4508b31c1175c4a6d52665cf6b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:52:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:10 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:10 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:52:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:52:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:36 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:46 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef5027b958752e28c867e0224ceedace391a04c31cbec134b624d41cc78ec14`  
		Last Modified: Wed, 21 Jan 2026 01:07:38 GMT  
		Size: 100.6 MB (100582709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2898920cb13c505259be6cf40bfc2b763657f2a33b173994b269e661d72ebfad`  
		Last Modified: Tue, 20 Jan 2026 18:52:52 GMT  
		Size: 92.9 MB (92948041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce94e6ea14af13855597c22f2a583a651f9360817c7dd9be974304412607e55`  
		Last Modified: Tue, 20 Jan 2026 18:52:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c8035b0c9a641a043eeccaa6d33c8c8cf2fa7de2a6f1cbb08ad68dc6cdb25504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab58a4c6333e1643561674043e465f276bf09e130e710032ff2df57a343e9d73`

```dockerfile
```

-	Layers:
	-	`sha256:87277977dcac2415b21d9554e9a612153a111230ca204dddce9f95016bc80e08`  
		Last Modified: Tue, 20 Jan 2026 21:24:22 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06b5bdd956f85b4d84e51e4225b4db25488e0ba1e0b1ec55a7b26012e477160`  
		Last Modified: Tue, 20 Jan 2026 21:24:23 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:3d119dd629d31268438eec01f173a74ca972cbece972aae6e68f39617c48ae62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337669237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18302d805f31f0bef398d019c51fff12fd5c73bff96c0a25bd261de3ee7b283e`
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
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:54:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:54:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:55:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:55:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:09 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:20:19 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6963c45fc75dae1c69a32ad6c3270c86fd5157751391796c0d838607e88acc0`  
		Last Modified: Tue, 13 Jan 2026 16:14:26 GMT  
		Size: 92.8 MB (92844600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daa35feb63e7ef5c9399e73cf4420af92b3279e1deb9e79d9f88735b792386c`  
		Last Modified: Tue, 20 Jan 2026 18:57:07 GMT  
		Size: 91.7 MB (91681857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd646111c5ad28f7fbd4c0cdba986d1d7447f81858765d25e24d7ffd7c69d6b`  
		Last Modified: Tue, 20 Jan 2026 21:58:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2c77535ab8ba2ce6d1bb2c546c08ed7cf6ed81ba59ba159ff5e02aee244f10e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e696884dead18616a3896165e1b410e34ab91b36edef83fcf6120da7a155c40`

```dockerfile
```

-	Layers:
	-	`sha256:b4e1b38f4363cccc01697a7622de889101a276a6afa58eb8a9578af47bf15c7e`  
		Last Modified: Tue, 20 Jan 2026 18:57:04 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf57a9d739fc97a55e39de75aa2e979dc7e39280b68fa47bb267b9f748b27c13`  
		Last Modified: Tue, 20 Jan 2026 21:24:35 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:e1603419aeae51040c83697af76da88655bf1231105481a3db60e31cc7dfef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363327223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e26427ceb139268698756f7265627c5924577889801cf3ae4f1702d08f9e7a7`
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
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOPATH=/go
# Mon, 19 Jan 2026 21:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 21:38:33 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 15:32:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 15:32:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:23 GMT  
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
		Last Modified: Mon, 19 Jan 2026 20:50:20 GMT  
		Size: 131.6 MB (131626895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a3cc83856871e3a177f0a6b27128217f73d5993c49818bd1374bd92a6bcb48`  
		Last Modified: Wed, 14 Jan 2026 03:11:49 GMT  
		Size: 92.3 MB (92315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d78e76785749d0ac401245d8942ca726f77c355bd8cdf257ac34d6dab98fbb`  
		Last Modified: Tue, 20 Jan 2026 15:36:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1b47b0201e1b60c52ce92e02cbf87bd885d55b30a111e27998f83e82cdad9bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94683b11ffeb8e63723328d37ddca685e98c2f69e5e54815a6348419b7fa80cb`

```dockerfile
```

-	Layers:
	-	`sha256:2b4e49d5275f47d4a479a7fef7586e9af3030fa040737ab74c2f17f9091200e9`  
		Last Modified: Tue, 20 Jan 2026 15:36:55 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef2e55a93efd6a7a119fbd80284c21623805c76f9bad1844036c7243e7cdba3`  
		Last Modified: Tue, 20 Jan 2026 18:24:25 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:1980625c138f43e6f22060dc5b93a12b612911f1235980fbb3ac9efb36bda09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314956646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061c0b877e4930a413bf6a5d31451ab97d25afe4942da2686ab28a9c81ae68f5`
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
# Tue, 20 Jan 2026 18:53:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:23 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:23 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9c35bb3053dba6b62f75a6cd643bf82fdafb8d0b167812e0490b0fea155955`  
		Last Modified: Thu, 15 Jan 2026 19:30:38 GMT  
		Size: 75.9 MB (75949527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee8ceecb5a37e7411922ba0485d5dd3cc40ab1953ffe651cbe56f40f79a249b`  
		Last Modified: Tue, 20 Jan 2026 18:54:10 GMT  
		Size: 94.2 MB (94232686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d559b6dacd263516b1d4bb8cdc3fbca487dfd9f3c1ef044d35e22d568b5aa6`  
		Last Modified: Tue, 20 Jan 2026 18:53:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ae0ed4660b88d49b71fd521b70dfec79f61fef6039722776e5512809d8476b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455e4f3266de4c700405c6a6b5e63c0df1e47c7a06b69149b23b5bac53878ccb`

```dockerfile
```

-	Layers:
	-	`sha256:ee8cbfadf0858a63655f3e15a7c2bf0860900b52a149747c136839300903c88f`  
		Last Modified: Tue, 20 Jan 2026 21:24:49 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75bcfd3bb8c5ed5796a635d91a63150afc6e73649bf38ae00b0e8445f3f49b10`  
		Last Modified: Tue, 20 Jan 2026 18:53:53 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
