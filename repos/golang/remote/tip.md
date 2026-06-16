## `golang:tip`

```console
$ docker pull golang@sha256:3cf8e24ac6f59ef6e4359da18951c2c30a1ac4a67e2a5b91659153ccf77c8ed8
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
$ docker pull golang@sha256:8db93f4c2c0a6c5a52f3c9c140ce2a880f4543be96d970e4e8e71cfe764d6edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347077886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691eeb68e0952985a5155127439170d0ee8ebdebed50003909c2f186fee25db5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 23:27:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:28:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:28:49 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:28:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:28:49 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:28:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:28:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df638407e1b06820fb29332d5e1ea8fac3d097d9a6c2208b910c4f7836115c0`  
		Last Modified: Mon, 15 Jun 2026 23:29:20 GMT  
		Size: 102.2 MB (102236082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f299e0e3bd5e6acb73b7c4b5cab40f1e2dfe3ddb2a4bbbe05ceba99d84f0fdf`  
		Last Modified: Mon, 15 Jun 2026 23:29:20 GMT  
		Size: 102.1 MB (102104608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76272dff0f2529c1d761f55cf0cba8cad06d3c70e147dab00e741ae6befeb5d6`  
		Last Modified: Mon, 15 Jun 2026 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f4e15092cf95c6ada50710b4c16988f43766d6433450539ea7571dc56a0bb65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb7f0e3929066a47605018d6dadf645e2d618da2c7c118c39fa3c62a3a6b2af`

```dockerfile
```

-	Layers:
	-	`sha256:ececffd88dbedcd32c2fe3f4a2579c44c998c4cd3023054024db41812a671ff1`  
		Last Modified: Mon, 15 Jun 2026 23:29:16 GMT  
		Size: 10.8 MB (10785971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8ec0b75f4edbde1b67a1c1ac9673e5255da5303e192112f9eabbb07e187672`  
		Last Modified: Mon, 15 Jun 2026 23:29:16 GMT  
		Size: 29.0 KB (28972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:1b27d924950bff26f9d35225cb4d8b836c444e63678e07eec27b36c42c99e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.8 MB (302844416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72f1ec106a791a4ff772c62cf2e67771b78e8bdfb9f7ec7249d1c3d6842de13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 23:24:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:27:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:27:08 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:27:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:27:08 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:27:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:27:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04879054973f6f0ae366a776f1ee6e23a5ae9b6072a5861ec514fdf29f7dbd68`  
		Last Modified: Thu, 11 Jun 2026 01:27:20 GMT  
		Size: 23.6 MB (23635995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e960af1a374080feee4d695210e1cc29cde28cd70c56fad7cb555534519a7e`  
		Last Modified: Thu, 11 Jun 2026 02:45:25 GMT  
		Size: 62.7 MB (62746530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dd477b7b7f86450f66ecdb51d9860ac56118afb6bd65939756afdee40f1dd8`  
		Last Modified: Mon, 15 Jun 2026 23:27:36 GMT  
		Size: 72.9 MB (72876912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3afb2b46cd31bb80c259a8638a98ac035a8bd800ea0d4d4395dd90003ea00`  
		Last Modified: Mon, 15 Jun 2026 23:27:30 GMT  
		Size: 97.8 MB (97836180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88ba65b7dd52a86571db72d433c3a8a9a72a098dab0833ff151000ac405830a`  
		Last Modified: Mon, 15 Jun 2026 23:27:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:971ac18a5a059b13ae32d20168549ab97ad6be444e6ae59bafdbdffdb01416ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a674dd971c17186a1148941ec95791bfca79b7f3248f4593cf96c257c4e4c`

```dockerfile
```

-	Layers:
	-	`sha256:80be196726563e1b9baa085e2b3b9a3fb4ea4e3b5b26c3a81dc0d805f3e84634`  
		Last Modified: Mon, 15 Jun 2026 23:27:34 GMT  
		Size: 10.6 MB (10581858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:374981f654c1f3870446f183961cd940ff496ad8661846f61fd5646f483c9205`  
		Last Modified: Mon, 15 Jun 2026 23:27:34 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f002909106ad55990ded187d5ed314ebdbbfdf74eb8355ac000d2ce3d8c1d72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337231585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c62b3d48a7703debe8c2305aabb06f9f27cdb23bd14e0055245f2735135c3b4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 23:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:26:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:26:19 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:26:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:26:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:26:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:26:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899debec46c079098eef0762e218ec1fecae7ff51174cf300f8a761631414e2c`  
		Last Modified: Mon, 15 Jun 2026 23:26:48 GMT  
		Size: 98.4 MB (98380388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc6f594300f89ac123e28e6396b82aeb7db11414dbbf3d120d335b23be9022`  
		Last Modified: Mon, 15 Jun 2026 23:26:34 GMT  
		Size: 96.5 MB (96546025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfe4e1dcd2fc969695112e25b82cca258faefb08446a8f9850712cdfa0e40ba`  
		Last Modified: Mon, 15 Jun 2026 23:26:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0d73b90a81e0aa36506acc7bce919b44d7f4c94769caded1ac402656e22e8d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7278bfcb53d4829beadd6bd6851a477f44225e8b8e7c34463e24a11aea092f2f`

```dockerfile
```

-	Layers:
	-	`sha256:4d7b37799c2480b4551037655cdd6a58fb1d3bd08c0cc73288811f4bc7f5057a`  
		Last Modified: Mon, 15 Jun 2026 23:26:46 GMT  
		Size: 10.9 MB (10905789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838d67d57416b44be21207cd8d102e73ee67eecb5cbc2ca990a8edd8a8d2d317`  
		Last Modified: Mon, 15 Jun 2026 23:26:46 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:1f9e79c51d4ef256be5279eebacfc4ddd44c824868642b721c815c844db70f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348007391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8f1611a4530e77145cc06d316e549758989c96cb85a7f8670c50bc082ac86e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 23:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:24:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:06 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:24:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:24:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ac1ec51d3293c1ade0065529ca23d5fc365d00997ff4e5a290cef3692dc04`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 26.8 MB (26797651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0028665ad759d9a734f0342c043d69fa3d024141c3329c900f163c639953f`  
		Last Modified: Thu, 11 Jun 2026 02:25:16 GMT  
		Size: 69.8 MB (69823550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952cd25eb5d3e073f81748a2b75e6a5f6b3fb754fcd65c8128bf0f6ed18fac4f`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 100.7 MB (100675328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1792fe3654cd71494db1238d388e796cd8a11c55f4bdc3626b4c71f43b9583c8`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 99.9 MB (99875141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668f8afdab34f7764ba986e39c7b965402e110826aca0f319d17ff64aed69126`  
		Last Modified: Mon, 15 Jun 2026 23:24:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d17699a7943b9d45cb19a6d8d2eac282b373f1826c384340a91f81274a3099ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c700fcdbba5e4583d4dafe4ff634b0651caf970d20fb6b199450520b50c9d1e6`

```dockerfile
```

-	Layers:
	-	`sha256:e8192080b0e6ec165cfd8f419ece051caa904bad0a264a00885bfb437943eeb3`  
		Last Modified: Mon, 15 Jun 2026 23:24:32 GMT  
		Size: 10.8 MB (10757234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:114f4a16e5783b4f76fb82efa4fb04630dceab9d8c7cf9c04cd0fee229f6c664`  
		Last Modified: Mon, 15 Jun 2026 23:24:31 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:f4ceb7e4e66e502b21f1d373cca9db45993a806824fae426fc88de9cdb0d2473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.7 MB (344652998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c6b0b91173ef26348a6e47b2a1c971bd887b3bdd4e5df7fb04fbee1f874c35`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:35:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:35:08 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:35:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:35:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ae5d968e23911f86d428bf6a67c0599a9449efc6170bd77e591b9eaf7c90d`  
		Last Modified: Thu, 11 Jun 2026 04:45:58 GMT  
		Size: 27.0 MB (27021977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a68ee36453f6ba3cb200c7dbe5182e1d61ba54c525dacec15d40f163304257`  
		Last Modified: Thu, 11 Jun 2026 10:28:58 GMT  
		Size: 73.1 MB (73050891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057fd15b7ca117f12314b7318acb10a98d15767505a892e8ccdf2f4fa1e2028`  
		Last Modified: Thu, 11 Jun 2026 12:51:34 GMT  
		Size: 92.9 MB (92942557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89039b34d27b51562a15e0375b32ce61f3263152969c65f76567c3ed39aa8a9`  
		Last Modified: Mon, 15 Jun 2026 23:36:20 GMT  
		Size: 98.5 MB (98499477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca878ec77c20f872fba47e8c73d0470f18e7982b29fc2e6e6e075f2c5b2586`  
		Last Modified: Mon, 15 Jun 2026 23:36:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:474a4b7ccd5db9957e9b6e757119e5e2ba96a38f79c1718c07979ba366a1389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed51b691389a799b8ff6468e31cab01e091d7a7df241847bd8ef03086f1fcee`

```dockerfile
```

-	Layers:
	-	`sha256:c98772be3ed8ce647fdfaff6accca0216acb78883c95a0baa365b86a24afa88e`  
		Last Modified: Mon, 15 Jun 2026 23:36:18 GMT  
		Size: 10.8 MB (10781759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c419543661c8aa5c8dceb3f3fe7610757565abf31b8df2e4998d516e2d520bc`  
		Last Modified: Mon, 15 Jun 2026 23:36:17 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:9fce34e58952038cfa3296e478e81f54f5e11fe418e259452e6caa3919a5cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370589400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa2b7d24df5793f5fa6967ed2b93faff746e296dd6fc7e3fe7bc7168a947f31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 04:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 17:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 17:11:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 06:42:10 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 06:42:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 06:42:10 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 06:42:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 06:42:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d828555072267505fd8c01bd511aa2e85b57db4591d7af1c1c5df9ca568aac0`  
		Last Modified: Thu, 11 Jun 2026 02:59:31 GMT  
		Size: 47.8 MB (47802538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d2b568729c379fb90b9e1cebbb6d837dbce6619d04c8fefdbc963a4896afbc`  
		Last Modified: Sat, 13 Jun 2026 04:46:38 GMT  
		Size: 25.0 MB (24968420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa945f549d69516e9a84b82f6960a728d5cfcff0ade0170a3411238a96eb3a92`  
		Last Modified: Sun, 14 Jun 2026 17:09:04 GMT  
		Size: 66.7 MB (66673413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e605738ec26caec03266e5fc0b8ff626025c1880c9f5890af814476789666`  
		Last Modified: Mon, 15 Jun 2026 17:21:49 GMT  
		Size: 131.7 MB (131720183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dbe4000f17519e4596fa5552054546772fb32ed45b8efd349e760fdf7b0b1f`  
		Last Modified: Tue, 16 Jun 2026 06:49:17 GMT  
		Size: 99.4 MB (99424689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca9f87ee35443e866dc4581fc76f95d1339b7fbe471b7d99a5bc0d7e03fe958`  
		Last Modified: Tue, 16 Jun 2026 06:48:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:22ccca09fd084f24ca066486114acf62549c744741261f5f2ca2f0d8fee68855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e93e63027c3bbe0baecce99a7a49a6ae3499db3b85f0df4e7284ef867a3f09`

```dockerfile
```

-	Layers:
	-	`sha256:bed1c2851b51c2bad829ede8cf5890327427159c2df5e2c7c64c5b558f53e7a7`  
		Last Modified: Tue, 16 Jun 2026 06:49:02 GMT  
		Size: 10.9 MB (10855592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b68621c213b6e875eb8f152b247c7422b7357820c51c32c272b0122c3ff365`  
		Last Modified: Tue, 16 Jun 2026 06:48:58 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:f039ac38711f450cfcb01454586e779af44c53c38ed6bbcb2f6b466ce099de38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321445716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc1ee3f7f6340c5a4ec38be44c7edbf1b1394273d60d6ac91b23e36409ad3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 23:24:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:23:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:23:59 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:23:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:23:59 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:24:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:24:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67e4e83aa860c5b719a4e0cc01db908ae525049821b3c459f866ed434f070e`  
		Last Modified: Thu, 11 Jun 2026 03:27:03 GMT  
		Size: 68.7 MB (68653348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9cbeb4b8e2d3dd07bb4469b5bf4804fea440dd71f3ec714bd00282ca528e4f`  
		Last Modified: Mon, 15 Jun 2026 23:24:48 GMT  
		Size: 76.0 MB (76048638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ac3a6fe312cf44641985605a72c55cfb44387624bfcf4ae9738ab565d3ad9`  
		Last Modified: Mon, 15 Jun 2026 23:24:39 GMT  
		Size: 100.6 MB (100553757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb2ff2f51f0ecaa382a90a5a5676e1320d14fe18c970d6e512bec34972c0649`  
		Last Modified: Mon, 15 Jun 2026 23:24:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:44e8ab49f23c7a8b22fe40f04c9ff0cd93c7ad6030b21c625a1f6238b16732c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8227d720ae2ef5f78754c5782a83d88f5bb1da80f4c7eeb7c32f7c12145cad7`

```dockerfile
```

-	Layers:
	-	`sha256:b763990be51ab2df6ccd91021115fcb43af97d21b0bfad0bf711be22b6f670e4`  
		Last Modified: Mon, 15 Jun 2026 23:24:46 GMT  
		Size: 10.6 MB (10597119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da806bb3b52c9e737b88ef6337c5f6ad8a0199bc0bc3b662d657f1e82c8df79`  
		Last Modified: Mon, 15 Jun 2026 23:24:46 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
