## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:d67325ed369d61827257e8cfe7cf4c8502061977c3745036dcf74e545588fa17
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
$ docker pull golang@sha256:b092f6063a25c00bc6d9e5c57b49bfd7c013059f1fb4085d3811e70459fa1d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320935300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e52dfea3eea128f78436d4965d6a8b9f87199717362834c80c995cbd678d15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 11:01:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 11:03:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 11:03:01 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 11:03:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 11:03:01 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 11:03:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 11:03:03 GMT
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
	-	`sha256:b963b30056449a490244e531dec5d01b93bbd5b130c1fa4891edea04f895868f`  
		Last Modified: Tue, 04 Nov 2025 11:03:42 GMT  
		Size: 92.4 MB (92401972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a365fabe6b823601cbb44d18708b9677073ecf1d933162e2fedd76cb5c8dd038`  
		Last Modified: Tue, 04 Nov 2025 11:03:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:db367b7a0a2efd31cb735a3588a9a81473cac3116df35143c61497125e9aa983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff59a11fa387eb7959ecaf3114b544e95d232ace2ddf0e8280dbe1b08b97a2d3`

```dockerfile
```

-	Layers:
	-	`sha256:88097d686ce2ac110e71b60ee82db7241d5aeadb94cb87b6d2cec8f79599fb27`  
		Last Modified: Tue, 04 Nov 2025 12:24:41 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e4b835c3dd8c5b21921dea864ca40b2aa7c4be50fcae2ca5f432c0f24b4a94`  
		Last Modified: Tue, 04 Nov 2025 12:24:42 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:18d7b9c9f63747b1ef790b7c2390e58e05abd6bb5dc03f941b342c9b17c2a537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279845706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d69d8270aca7c3030aa77476febe77ed04a7de5ddb9b1ac25612308222895`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:38:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 04:38:24 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 04:38:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:38:24 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 04:38:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 04:38:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c6c96cff86026dfac835fc2d229a348ec06ff2d2c520014ac2aeb4555bd9e`  
		Last Modified: Tue, 04 Nov 2025 02:18:15 GMT  
		Size: 59.7 MB (59652141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547cb6d02339d91f3e8b1e24206216095a1a9df38903775836ab5a656c589444`  
		Last Modified: Tue, 04 Nov 2025 04:39:00 GMT  
		Size: 66.3 MB (66255412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e31ae3cf3231dbebcc29f855465beb4dd182f07c1f7e379abe62dd3f7304530`  
		Last Modified: Tue, 04 Nov 2025 04:38:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b2299296645a55ff0a64f164f586c8538c4e791c370fe11ce8cbe9c235bcada8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df86eba074d4f0eed4dd73515658cd78a074e9ff66e3f4b8a406dca2691b9a`

```dockerfile
```

-	Layers:
	-	`sha256:01e129940d25ad81a08e035cda02e89b909a8f509d3e0adae977ebf124081d5a`  
		Last Modified: Tue, 04 Nov 2025 12:24:52 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0068008b5b090e96504df9f10c5a4e2b21817865d9435d24d4a25fd32b805eed`  
		Last Modified: Tue, 04 Nov 2025 12:24:53 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:24cd4ba385a71a2441b765f6150c6336ab20be41cde708371a75bccb42eed210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309680411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c601bcdbd5cc6e4f507415d754da45744d86eb0dfe00e7ef4b26a5e261e8c3ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 03:18:57 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 03:18:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:18:57 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 03:19:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 03:19:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0723c59e9ea36ac04a714cf7e510efb1dc2f5c8558d0c626739b6e5a9331b1`  
		Last Modified: Tue, 04 Nov 2025 03:19:42 GMT  
		Size: 86.5 MB (86472356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e9fa456ab208c2b2de5a7798d2122a64a56ec86ec82ec8fd859e97354c0fa`  
		Last Modified: Tue, 04 Nov 2025 03:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:608b11b051bb6db1f88fffdbaaca80c48b1066c13fd92c2340952bae62720395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74afb6723e4807266b93e706a598f0b2450718240d3247e689ffc138fc84c16`

```dockerfile
```

-	Layers:
	-	`sha256:710ad7138146e317610037cdcb0a28b4d5e2c042f0aba16a72a1af95836332d9`  
		Last Modified: Tue, 04 Nov 2025 12:25:01 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2e499d95287449c662a03bb8f6a3156a3e3cde141b4b303336c932642a1edf`  
		Last Modified: Tue, 04 Nov 2025 12:25:02 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:99b4f4c215f7e3a10cee60136f04f242c3312823dd1895488a89f9d7dc4fe63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320001856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f179f79bd4ca2dd1476ec31374ede8a1723f2bab9d90afc0d6e3ff80ea88bc89`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:17:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 03:17:38 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 03:17:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:17:38 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 03:17:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 03:17:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b596182a9b4836dc17a3bc5eadc1e2798b0aa5aa0c8f50fec56b60d802ddb375`  
		Last Modified: Tue, 04 Nov 2025 01:32:07 GMT  
		Size: 66.2 MB (66233815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035d668f3d0cee78b1e6e409d066db558c08d74e955f89ae8e0c7e0caba876d1`  
		Last Modified: Tue, 04 Nov 2025 03:18:38 GMT  
		Size: 89.8 MB (89823373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa89e75c0c953319d9bff7e39d68ebb6f7b9628befd4d9afcd44ce4625752bcb`  
		Last Modified: Tue, 04 Nov 2025 03:18:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ea5b86cf6d5906bf8f5c0bb07dd52552104213a98d394b16a129da39d374d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e25fc0e0004bc68551441b305d62b481152a4546f8f09e3c8638544e983f97`

```dockerfile
```

-	Layers:
	-	`sha256:d0a111a2f545045fcc0b1581612e8c45646fa56d793e0337f66400369b3facc8`  
		Last Modified: Tue, 04 Nov 2025 12:25:11 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91ed3908d18781d09d81c6f408f1f6344a04d063bb6c1c5a292b62e44c535a3`  
		Last Modified: Tue, 04 Nov 2025 12:25:12 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d011a6b01b93bd831802cce3e8f8889729936097c798ab9fc910a64d29f4ac87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291258703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d236c5c6c78645d50928faf5d1cbece1e5adf476696444cde910e68681a534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Oct 2025 01:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:30:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:30:42 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:30:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:30:42 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:30:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b8b987535d1ca746e1df1d7a5e1bbbe17811a45d2a394c4b90bfa962bb4cb`  
		Last Modified: Wed, 22 Oct 2025 01:07:48 GMT  
		Size: 70.0 MB (69997127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1ab417de53c45975d074e15d8a2784ffc35415dd457eb8b64a5003a76fa88`  
		Last Modified: Mon, 03 Nov 2025 18:33:12 GMT  
		Size: 85.6 MB (85577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528cd1f90bdbc4cb79582836a13ed72ac50ab9030537170cf285dd020075779c`  
		Last Modified: Mon, 03 Nov 2025 18:33:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c110eb1696594ed6fa1c723b971a08eaea556027ea898d3d57d64783a48fb26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d1594e699507dadd5a747042315c06641bafed7b3b93d56e57a269dbb9bad7`

```dockerfile
```

-	Layers:
	-	`sha256:4b677abee1335d54c4a7a19dbb3d7b329bb7a7cf970e7fb9f3929b511036c4ba`  
		Last Modified: Mon, 03 Nov 2025 21:25:24 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:9bec222a8c7dc39a0cecf71fb7e3a91914786654099a6959bc53c7692a270f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326554393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e237afc2805334976c53fc85dfaccc3b5bcf722015dc8ed0b1e629421afa29c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:13:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:13:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04d953bc0afef745a3953fa8df1889906decb886f69b2e0f1dddd428304c77`  
		Last Modified: Mon, 03 Nov 2025 18:15:09 GMT  
		Size: 90.4 MB (90417832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d9f54e97ecf205f2ef4a1c61973f3cb75b9f1d82bc6e244f9ae64a40d14f5e`  
		Last Modified: Mon, 03 Nov 2025 18:14:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:65df137c0154b83adde8b9cdfb423b248e3cc36cf5f44cc3bef57ef46453300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb502156cecefbb0db1e29901af19cc5fd8f1e29914b3228fbc98c5def51c7f`

```dockerfile
```

-	Layers:
	-	`sha256:7e5feffbfe6156f20fba19c6bc92f4f2d2536bac47a16bfff900d36f1dab8e22`  
		Last Modified: Mon, 03 Nov 2025 21:25:28 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e35dddd45b93327122f98395e548e5416c5bb80b5236eabecdc288ae1dbb298`  
		Last Modified: Mon, 03 Nov 2025 21:25:29 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7e2ab9486e1a9ecb75d079ff8f7754f1d7c204c78a3ddfcb24010eae2b33cc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293509250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6838646d980ffa422db3d7fad7e0ade5a429b192c40d33112145146918018eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:11:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:11:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:11:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf804e47683c20db733d9e6818bc93d28616af2adbc4f703221ee8c9dfe09c`  
		Last Modified: Mon, 03 Nov 2025 18:12:00 GMT  
		Size: 69.0 MB (69006468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27665b1ca1f4878aea3b0aaf64c4342038dfeac7ba27def228ea78d9ee8384b1`  
		Last Modified: Mon, 03 Nov 2025 18:11:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:01144710c64cdccc6582829db56153769d12513e2355b30b6922e82125c8ea2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd75720fa4e794829e00cf1019d45cff8560950779af66a52808db0bb1744f2c`

```dockerfile
```

-	Layers:
	-	`sha256:fb15c6d5ee49747949c0812a8c3364d5a3312b3bd9f79b2f1aa5882d6131c72a`  
		Last Modified: Mon, 03 Nov 2025 21:25:37 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99e91bf2876ea15ca2f677c2637eb36c905507943234ed5fa796c91e1cdb521`  
		Last Modified: Mon, 03 Nov 2025 21:25:38 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
