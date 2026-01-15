## `golang:trixie`

```console
$ docker pull golang@sha256:1763926ff08117bdf4c76182c02fecbcfc3086771169b2a03574273dde17fcee
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
$ docker pull golang@sha256:22bd1c41c958c762e9633f07a5fee8266300e5f25e18e269a6d87a4b870368aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304975795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08bd36a50979e7b09561e4b804b1f112c9d6509c0a12b15bd7b1b410e8a34a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:50 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:51:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:51:50 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:51:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:51:50 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:51:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:51:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde6dc0eb067ea9bd99026818d5648d0638a3aeab1d74d3d62841af46bb2e630`  
		Last Modified: Tue, 13 Jan 2026 04:52:34 GMT  
		Size: 102.1 MB (102138516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42e087ffaedfb9fbf6b1453d723debe79af9030924d5e7bf3cb73f58068917f`  
		Last Modified: Tue, 13 Jan 2026 04:52:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c91556ea10e613c21ca41f119c0f97d9ca197ed7108771826192462a537ecf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd16e5746c17c7297abfe0398e64d37b68bd984af85eb308a8c474ed77e3464a`

```dockerfile
```

-	Layers:
	-	`sha256:63e38d6ffeb66a7b7ddaa792e467c20522bc7a8f4cd350879bdbe8a5482770c5`  
		Last Modified: Tue, 13 Jan 2026 06:23:54 GMT  
		Size: 10.8 MB (10785503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cebecd000f9e7c7f31abfc027372f021db210d81aa6fd8a4af6c8d62944940`  
		Last Modified: Tue, 13 Jan 2026 06:23:55 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:77306500d0a94ee795789cccd68f535bf61492028ac632c43c3dd37506a56628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263913535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4303522f4e6aff946896ff0a7abe878eebb96c306d22109a410078115aa65f45`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:20:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:20:46 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 05:20:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:20:46 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:20:46 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:20:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cc2db46e5c9715a538195126ca8725046d7ecf42782f1eea29def41aaaa934`  
		Last Modified: Tue, 13 Jan 2026 05:21:21 GMT  
		Size: 72.8 MB (72783446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc3110388cfc83bcdbd7ec2e6800b0612bf9ed9652012958a19f483b36ad36`  
		Last Modified: Tue, 13 Jan 2026 05:21:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d6dee7c5bd9caa8a565b5171fd530cc8c1c6e222128e5587dc0cee0e65ecc92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bf53f5f90c3a8a7369ac7b5ca552a432cb8f47ca2a3a04623b67f466f73265`

```dockerfile
```

-	Layers:
	-	`sha256:9be9a786e26f245620b13a1bb419125ef48bd632a8045566737372dfdf27b065`  
		Last Modified: Tue, 13 Jan 2026 06:24:20 GMT  
		Size: 10.6 MB (10581424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8213432c8b21a77d85e54fb59b653e19142fbaf93f55c6690cdb6e0a5d045e`  
		Last Modified: Tue, 13 Jan 2026 06:24:21 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:23100830be089e331f4673f8ecfa9a0015c33589b8aca55fa6586e709250fd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298196748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457064282507991b22420344f88e9229a917630a3492834ba51ca9b466f507b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:53:25 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:53:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:53:25 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:53:25 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:53:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:53:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
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
	-	`sha256:86db67b47ae7a00d38cff04c02830175515fad118b73f3b669d5af77e2639c30`  
		Last Modified: Tue, 13 Jan 2026 04:54:19 GMT  
		Size: 98.3 MB (98283441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1582426bbf77354c33a073709ea629a31743b6b52f75195bff71ef1fc06ba4`  
		Last Modified: Tue, 13 Jan 2026 04:54:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:15babe8edb6f430d350c7febc76734ee8e65acd859356b2fb44d1e6b2579030a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcde0e0d6588240b69cd69d49eecf938ed4da2ac49ba6efad67df165b8745813`

```dockerfile
```

-	Layers:
	-	`sha256:1057e6bcce5615317375880c45dcac27fc95fc9f8577937e3a2d58b70338b023`  
		Last Modified: Tue, 13 Jan 2026 06:24:32 GMT  
		Size: 10.9 MB (10906006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e55ec02f50276aa9f92677c1da4859b7bbffa27b941182573dfe94d528c9a1`  
		Last Modified: Tue, 13 Jan 2026 06:24:33 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:fef2fb55ebc8bbaf57c25561d76661ae404672e53941082a15b99c5a91808cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306834867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270378c2af3cc9edf83b9b975dad48d2b231d6ce527d6ce890f36cef1992d038`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:58:35 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 03:58:35 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 03:58:35 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 03:58:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:58:35 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 03:58:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 03:58:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
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
	-	`sha256:04cbb27b41cb1fa4bca0524d176a1649310dac5a9075cb9d9297170dbe10ef22`  
		Last Modified: Tue, 13 Jan 2026 03:59:18 GMT  
		Size: 100.6 MB (100582412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a72bb9a794b806c649b0879f2f11f91d460838730d1c84174fe89161de870e2`  
		Last Modified: Tue, 13 Jan 2026 03:59:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d21867a05023bd36c9e1e8a674e93fefbdbf03a87a8e668f8518dc2649837ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b5fe273d6a981235c7381d621587c813714e7940aa64891cac4f058c5aa036`

```dockerfile
```

-	Layers:
	-	`sha256:a008e57ff6e442a588ee1351ef1eeded7855d53994aff97fd7b2600381c3d083`  
		Last Modified: Tue, 13 Jan 2026 06:24:44 GMT  
		Size: 10.8 MB (10756748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482a4038e7fa46e57912fa3094d4d9234839c74fd414109f0942c674dbfc62a2`  
		Last Modified: Tue, 13 Jan 2026 06:24:44 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:69eedd18842fb89c854554b24e8389e9b97b6afc1f30daf5aef707334f2862cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304122327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a469f1a153ab06775a56cb6014ec69cb9cd2cce05cd60ee8d8a19a61f116b173`
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
# Tue, 13 Jan 2026 08:54:04 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 08:54:04 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 08:54:04 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 08:54:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 08:54:04 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 16:13:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 16:13:11 GMT
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
		Last Modified: Tue, 13 Jan 2026 16:14:59 GMT  
		Size: 92.8 MB (92844600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c6268e2ecd1668e4d1b3ea389324c9b9097a5cc52597aa2991b4af390c49bb`  
		Last Modified: Tue, 13 Jan 2026 16:14:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8123c0e28abf5fb6ba3c1a1f6a52244fcda834693f7e68e2a1006da340b70871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13160cdba708a2b3263fce5f77ac946f2572d3c7611dc3298afd39edaabd5deb`

```dockerfile
```

-	Layers:
	-	`sha256:18a34975c86f6b8ade4e688f9f5bd47435cdfd99c7316184e1a73e1062a87ae8`  
		Last Modified: Tue, 13 Jan 2026 18:23:00 GMT  
		Size: 10.8 MB (10781313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6ddddb20ef3754db1fd8e91f3ee32150c8eab1092983013e5de42e8ac18379`  
		Last Modified: Tue, 13 Jan 2026 18:23:01 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

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

### `golang:trixie` - unknown; unknown

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

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:346354ff31d5dc1a15b62b1ea70326c1a8843cd8867d7eccd9e2adfac8636ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280211279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb01280229bbae858529cb6035e85838e9472517718491ce9221c29b35e556e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:19:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:20:14 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:20:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:20:14 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:20:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:20:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90abf8b3c99e1ce4c207d1c4afcda6c0da8e954a6a2cb51f7277f6a22f50e40`  
		Last Modified: Tue, 13 Jan 2026 04:20:02 GMT  
		Size: 75.9 MB (75949629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a384f72f273466ce6542484f79bea6b5b3fc44a9c272f14257187692bf3b014b`  
		Last Modified: Tue, 13 Jan 2026 04:20:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4413f2e427f3f12397a60a1c9392d23c1cb41d1b9fff0cfd10ff4eb54bf09fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5983f83bfc5be9db60db733d1378f183dd1f7dc5049602523b61d28179c1c908`

```dockerfile
```

-	Layers:
	-	`sha256:60225a5940b04ee19b6cf7f9ea645d4b1dd18db86e4022a611182eacff4c815b`  
		Last Modified: Tue, 13 Jan 2026 06:25:11 GMT  
		Size: 10.6 MB (10595903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe71d31545b1d357283ddfb50dc3f748dba7e01dc72adc5c4778915d436a9d3f`  
		Last Modified: Tue, 13 Jan 2026 06:25:12 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
