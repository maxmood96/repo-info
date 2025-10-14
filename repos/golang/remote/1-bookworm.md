## `golang:1-bookworm`

```console
$ docker pull golang@sha256:51b6b12427dc03451c24f7fc996c43a20e8a8e56f0849dd0db6ff6e9225cc892
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:30a047583beb38aab377dfd9090b64e9c174ff0ca73b8d234b86f7f262ddaab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289456235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5553127626a0558e322d1023cef7741e7cc13952c7932d1fa927fe02adb6e74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f84ed72eeb7d32d0368c4d46f7daca76234cea1502859d7c2c69118f364763`  
		Last Modified: Mon, 13 Oct 2025 22:32:28 GMT  
		Size: 92.4 MB (92401881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631faa732ae651543f888b70295cbfe29a433d3c8da02b9966f67f238d3603`  
		Last Modified: Mon, 13 Oct 2025 22:32:32 GMT  
		Size: 60.2 MB (60150352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301bbeb38950c5fbda435f2370f4c542763d716f7d891b031a419134ac9cd0f3`  
		Last Modified: Mon, 13 Oct 2025 22:32:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1174cb5d528db630c2c55b10757d097f0abb4e022a550f4a707e283fb20fd4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce634e696167b368c611601840cb34a471ba6f70d36a59b6f27b2a71e4de3c0`

```dockerfile
```

-	Layers:
	-	`sha256:0ba4628065fe7c5857f5ea9c7f6597c5b165b0c1324b1787f7ff1fa12795c99e`  
		Last Modified: Mon, 13 Oct 2025 23:23:54 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b23cf92c4bd7c3c216f4d5a5133ffc79476285c4c946265c4bb34fb155211e7`  
		Last Modified: Mon, 13 Oct 2025 23:23:55 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2e9aeee66338237a33ec869f3c2df9653f27ea8a461b677f0dd72c5d2cb29fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251107282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafc41e3a76fe81d1b6f630bf1be50a5f1e818c9e0e3cb9fa011cb132a4392ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e432c46d591d11b21fb54aee2c21c8e370175cf28e68aa8795c071b4cf1ea2`  
		Last Modified: Mon, 13 Oct 2025 22:33:15 GMT  
		Size: 66.3 MB (66255009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af0985c887920d8ad25f36932e706271ae84032a3ae370b1f5325188b8578bd`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 59.1 MB (59072951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cdf2439301e2b0c917fc027624a209e63db14e88f420966bac9ccdf7bdd34f`  
		Last Modified: Mon, 13 Oct 2025 22:33:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:eaf7db0b93e5dd178af4cc6732d1fd73cca280ed91888dc88ecca22015a4715b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d795da50e427160f2113a7fa4d859e1d9020685f6d9d1a7f271ca27b022720e5`

```dockerfile
```

-	Layers:
	-	`sha256:00d7c6849c75ba0bb42010860973870dc462bb1a90f9a477936e7f704a81553b`  
		Last Modified: Mon, 13 Oct 2025 23:24:03 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7c6a7d5c76eff3d66d1bc3c160b2f947229b34743901458dc479679b740979`  
		Last Modified: Mon, 13 Oct 2025 23:24:04 GMT  
		Size: 27.9 KB (27946 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:888af1320c036966e26da7612aeb1e71b49385043d37e7583b4ce6abbf9491e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280447161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f6aba71f2b9a292f958b79cc33646a24137808f8ba66745150feddb7f3966`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7982ed0ea6de7e0ea7686569e2bf264cedee341af6812b72a18f2108ce6d03`  
		Last Modified: Mon, 13 Oct 2025 22:33:18 GMT  
		Size: 86.5 MB (86471984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dab1238d3d9c3bd1753609badeac4c19b7239aef9927c6dc13db4335a66b568`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 57.7 MB (57650163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063e2a783293572ba78cddbaef12dcd6399448586c5fdfbadb552868e53c852e`  
		Last Modified: Mon, 13 Oct 2025 22:33:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:20c94e37a91b2d4f8bf7e457f417b04e677bcb6efd3f7f536f99f2d33a10cde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e695dd74b5cd23f9f9513f4f242d3535e28ddaa60069db721734b556ca647e3`

```dockerfile
```

-	Layers:
	-	`sha256:6f8ef95317d060bf0bbce767ad215bd7b71e5a69acb06bfdff8d7e49d464fd56`  
		Last Modified: Mon, 13 Oct 2025 23:24:12 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ddac28621b5d043d2c19e95171a939a26a19707e60d5b537d4504e66583cb3`  
		Last Modified: Mon, 13 Oct 2025 23:24:12 GMT  
		Size: 28.0 KB (27974 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:d07b1fa9eecdf3809273738327c11487bea17e382961de456a90c6ab281ed518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289255303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95930503391e7e5d0405f5a43b35eda758defc5ec3574592a97dc51420019d7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3ddc9b41e66e4e771621da9eafe798d94abee7b9f01549fbbb1d26be007773`  
		Last Modified: Mon, 13 Oct 2025 22:32:59 GMT  
		Size: 89.8 MB (89823523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95a97777f39c24f1a92cb9717c8fb60aaa699bf624bf9ea8e2cf61d0d8d4abe`  
		Last Modified: Mon, 13 Oct 2025 22:32:51 GMT  
		Size: 58.9 MB (58870901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c026c8bd4e8597a0a907eab0e8bd17d7ef2c0f51cf73a99bd2d3a296a493d7`  
		Last Modified: Mon, 13 Oct 2025 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d02c06074a63f8e43f9701c26a52e01f14a183650d6f9bebcca021c14f3a24a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5e1c314221270bffc6e963e9bb9e353ddfc2cc41efba91ce40a7547bc253b`

```dockerfile
```

-	Layers:
	-	`sha256:951f8766466b36f73daa5d844dd65335b88bf9e52955b9c32dfd720e583dd6e5`  
		Last Modified: Mon, 13 Oct 2025 23:24:23 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04f5df7d3cdd217ee30ee2c6ec4f98690e2214fb6b50e9431efde34bf77d3ae`  
		Last Modified: Mon, 13 Oct 2025 23:24:25 GMT  
		Size: 27.8 KB (27804 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:7f299bf8cdaab7f7309e1c105a09debb88462f09300e4640741664ce785b789c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262252457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d05f468731cfb94d552562b6808ac6f0e99882ca2b125adf164de8bbfdf9838`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39be94b43c7b8fee0fdcf795208f91323ad52fb7cc0e21f16aaaac555d61b8`  
		Last Modified: Tue, 30 Sep 2025 22:53:31 GMT  
		Size: 70.0 MB (69997146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dd8206818bd27a5e75e0dc8f188f71d95a622e6e1f691d7856fde2440fc249`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 56.6 MB (56573738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb133f90519862cbc0ffc092146ef2f07c56ef838b689b7a86a15587a2e5eb3`  
		Last Modified: Mon, 13 Oct 2025 22:33:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fb8aae65325ac874f2d0325661f121b89d102b1ddd27e94b5883527341263bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f9e2224e926dfd3e4022a9debe3c683d61f02b972679aec5eb42e0a8caedf4`

```dockerfile
```

-	Layers:
	-	`sha256:d2afef7639c776afebd13fe0c7ec85d5ec63d3b99d4974c636e0d0b745e6daf9`  
		Last Modified: Mon, 13 Oct 2025 23:24:31 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:77812a15cf7f2bc6885d2bf5d1de4002747ed00ad7bd0e897e3b4ce0dab371a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296393407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bcacdd6b5407a9a70428d1065f391cb6bc738bbcc00d960aaa3cd008323209`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc7393f12c50be43563a663d899f76ad97c089e8eff687160119c7058ff4c9b`  
		Last Modified: Mon, 13 Oct 2025 18:29:15 GMT  
		Size: 90.4 MB (90417562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd79e032fd555b767c904ba3576a69bc211a15c564010ebf1a3788cd00df21d`  
		Last Modified: Mon, 13 Oct 2025 22:32:24 GMT  
		Size: 58.1 MB (58134461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2485d32131fcc8fadac2957281863f52a57dc5b903b063ce1ae394aeda4e8f2e`  
		Last Modified: Mon, 13 Oct 2025 22:33:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4a4f12e2165771de55ef91ae4dfa67f8eb8dd5e0fd8d5590c0612dac2f3a8c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8daa3fe77679cb4d329fad923165dc910ca41b245996869f5e6483c0420dbe`

```dockerfile
```

-	Layers:
	-	`sha256:0120fd507898c8ecd370fb8378a909e0dac6ddd34f3e5b33213d5e936009de5a`  
		Last Modified: Mon, 13 Oct 2025 23:24:36 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37192afd0a0a8f76781134041f7fe3e8dfc812adc44fba94f4a9a12ab7d30f1a`  
		Last Modified: Mon, 13 Oct 2025 23:24:37 GMT  
		Size: 27.9 KB (27887 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:014de132477960a21fadf087f0d6799d74ff1f10f7bd6c972cbc8f1f534f507e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e85c61169a7a6fdf89331b04e2559dcf14edbf025fd1447da4bc0f6cd352d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4dbf2eab022c30a4f1ad0d69bb0be8e9a7b59d1d848c5eb4bcf43acac22ef`  
		Last Modified: Tue, 30 Sep 2025 23:54:17 GMT  
		Size: 69.0 MB (69006320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cce485d826b4034b25b00ba2ffd0ae02402af07840c83aa561b76bede0f4bb`  
		Last Modified: Mon, 13 Oct 2025 23:28:51 GMT  
		Size: 59.5 MB (59483110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc137ab2cede9eaf3a9e7ca715270be7ec86d929b2fe5af2005aa00999e58652`  
		Last Modified: Mon, 13 Oct 2025 22:32:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1de256552008f766ee84aadbf6c11aab9d2d1537ba0260a9e1ff5aeb785bb9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d044f59d84ead802ebe417a433ce6e1b62966d9f2f6cb1cf211fea32ca16c49c`

```dockerfile
```

-	Layers:
	-	`sha256:091f064e199862a042cdbad8cacffc1c192d84323b23531513a3af8b912b5543`  
		Last Modified: Mon, 13 Oct 2025 23:24:45 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bfd66506eb050d43c8f3f339dcf78eac88bf0c71164fabd1737718ca437476`  
		Last Modified: Mon, 13 Oct 2025 23:24:46 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json
