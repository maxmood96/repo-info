## `golang:tip`

```console
$ docker pull golang@sha256:0772f306e811e4677614a9a73d1090c070ab85c07dc65579a4411a5fbd71ebb4
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:f4740c1fd0494a5213d10a12836665ead19d60a1e46b2208ceca43f568369fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359005086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4236a65762e9448deb2f927e740c954a388667be48929dc9714823f4c2c78f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16446613f4cd20ecb55b79282327235bf0043ab1fc26a7a7a92868a93db5c379`  
		Last Modified: Tue, 25 Feb 2025 23:30:46 GMT  
		Size: 92.3 MB (92332231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a93651a1e507b5bd3cfde19fbfc91acf223de81d90d9e07fc812851aad09e7`  
		Last Modified: Tue, 25 Feb 2025 23:30:29 GMT  
		Size: 129.7 MB (129743852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0914a7411be28f43ffd1aa2ee2d6d5e57fa4df3d3a5267084b7ea794a9cb322b`  
		Last Modified: Tue, 25 Feb 2025 23:30:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:048ad480fadcf24e6e48d34425d8c4c94e3b4f176e7ee1dae7a303f2fcfe6a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94721e56130748410207bc1897f085e3a82c96062aa6d712a9ae005a653e0de7`

```dockerfile
```

-	Layers:
	-	`sha256:ab68e7163072f4ee7e4703d4a71417477aa18bcae84745f691cb32252f7792f7`  
		Last Modified: Tue, 25 Feb 2025 23:30:45 GMT  
		Size: 10.3 MB (10274074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d395431c4b8ebe0c40ab48c140f3a12c1443e38fb4dbb12fb3e530cde196ba`  
		Last Modified: Tue, 25 Feb 2025 23:30:45 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:a78ce900e35e34b7bc139b2fb6de4620563a8d7c0f316b7f1371c1087ca022b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (315002761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d98d1dfbf8b8d71e34f7644e31cc32591c9cc623eb90d9d3bc02826071e1684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654867856e71cf6e49b9c0cd4aa53b8135e92c7f0694dd70469ea7e9aef8a87`  
		Last Modified: Tue, 25 Feb 2025 17:00:54 GMT  
		Size: 66.2 MB (66187481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe77fa27af7b36c34f8f11e6bd2bd4b9ddf9e28c094fdee1cc3b2735243e847`  
		Last Modified: Wed, 26 Feb 2025 02:56:52 GMT  
		Size: 123.0 MB (123034972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225f55dbe57d5ef6d4bbe291890143ab78f37c5c6fc3e2e10a9e6fe789c7bf0`  
		Last Modified: Wed, 26 Feb 2025 02:56:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:38bbaeec36e02df74df79c9db1b450b433ed908d62f356a20d17902c33b4f186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10110183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5b90d93a254441b4930f10c70a4254b79322130f4e797444c949475df7ab4f`

```dockerfile
```

-	Layers:
	-	`sha256:0492151fba4323c2b5c1bd20f009b954288f11070a890641a57d92334583d943`  
		Last Modified: Wed, 26 Feb 2025 02:56:49 GMT  
		Size: 10.1 MB (10082396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfa1298840da960313dbe1e538696395be659bc7f89f391eda1d2c60611c611`  
		Last Modified: Wed, 26 Feb 2025 02:56:48 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2d1f6c66bdc3080eeb3088bb6f30a5cbb7955bbac58a5f22d61fd87e69728282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345209118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4eb62e14bdd6bca854e8ae6152bde8ae7e4db2006a465b62919da62206c796`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b8f871d0f3123ba15451c10996dab2d9e3570418f2ca8959fe0f2505e3356`  
		Last Modified: Tue, 25 Feb 2025 15:28:23 GMT  
		Size: 86.4 MB (86383529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e46df0fcf6e0e573af560112ea65411de1e4c09446bfe2aa5c396181b055ef`  
		Last Modified: Tue, 25 Feb 2025 23:43:25 GMT  
		Size: 122.6 MB (122564769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daee1eb23f0fe76d565365114c8b61eab059af866f349d4a7e669514c721eb5`  
		Last Modified: Tue, 25 Feb 2025 23:43:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:57fd7fe900c1f8d0dfff1cd91ed772b89f7bbf5f8e2d25aa1b6d1300caafb5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2196019bfd1d9c3eaa3841fca786d851166953ea2b8d99736855a4df130a9d9`

```dockerfile
```

-	Layers:
	-	`sha256:e0ce0776578279b043586175c0c76ac8ac151532c287a05372f3484f69aac682`  
		Last Modified: Tue, 25 Feb 2025 23:43:22 GMT  
		Size: 10.3 MB (10301921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285ae49b861599693440bd7486455c23b97aefedb7ecf3f9411bae90e914d223`  
		Last Modified: Tue, 25 Feb 2025 23:43:21 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:cec7a63777152ec95f04f00ef8483c0623530cebca854b6c245094bb33c62146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356743045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564bd5b6ac4f6c8523fb2db3607abb4c0ea94103e096172a10ebb10405261c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1934d5022953b1de34555c9c5b1c2736c06553e4f5594085144a3b8d62db526`  
		Last Modified: Tue, 25 Feb 2025 23:31:19 GMT  
		Size: 89.7 MB (89744477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ea1fd7113951d2f0ff9a9824c4749a117ae67be28d96b0ab33e27305a83954`  
		Last Modified: Tue, 25 Feb 2025 23:31:02 GMT  
		Size: 126.4 MB (126402793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e6e95642a9454eb977a72e2a045ce9c45594809ee7879e43548cce1f4075f5`  
		Last Modified: Tue, 25 Feb 2025 23:31:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0b4630e6a254c8daefa67ef1ff87cc553f68f3ada1509b0f664a1f02b491cc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03da10383e86a9cf1d2d5fe03c9e7566eea32e7a545864f8fc269b01b987400a`

```dockerfile
```

-	Layers:
	-	`sha256:25a8852040a45637895ff641da6150eac9268b483a9ef960147159dfd08a0351`  
		Last Modified: Tue, 25 Feb 2025 23:31:17 GMT  
		Size: 10.3 MB (10254145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2155adaf38cbcee4d2211e397ece33fb6fcfa90e9b7136a95940d80427366ff2`  
		Last Modified: Tue, 25 Feb 2025 23:31:17 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:ba37216c4e1cabc802c0c8a41ab61f50312365b545ae23bd7d2fb2f95abf3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325321003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56f3d59d75e216c9cebd2da2483598b310fe2bcdc4167e5a025b0686b58f9d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e93c581655a2c5138779556e6b049332bee85d015285d3106e767693cb64d`  
		Last Modified: Tue, 25 Feb 2025 22:26:26 GMT  
		Size: 63.3 MB (63306786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301664e1162c99caec998294841f4102a356459d19e18d2615cfe952fdad457`  
		Last Modified: Wed, 26 Feb 2025 02:31:50 GMT  
		Size: 69.9 MB (69904803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185800a9f713d98ac9d2aac09f99b2f4a4f4731b834516451f9516af5a43e77f`  
		Last Modified: Wed, 26 Feb 2025 06:30:32 GMT  
		Size: 119.7 MB (119698029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d584934ab730526320b3e0ea2fbc13183039e038accf72c31ba9f6414477f36`  
		Last Modified: Wed, 26 Feb 2025 06:30:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:312edecae2d61aabc50c16eb9727ff793d0c6f4eeba6c8e64afaa5789f3482dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bef068da422b908e527f90d262f5152f7af3db62af7f9ee146ebff9a6a20651`

```dockerfile
```

-	Layers:
	-	`sha256:344dd9f933a2bbe82b7becaa62b8a48558cf3f474c27ef219bcf5d74b8e5f122`  
		Last Modified: Wed, 26 Feb 2025 06:30:21 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:da257d4f862f57ec1829ec816b3058b1a2aaaaadf7eebdd44d2d1e4243813de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363137677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149cd0175b5bc67bf2b5e63c668fee183a6fe1db1cdc75576122a5e34d60fe5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eddab3d8a04dda752c64b51fbaa29916204149752323327524cec69525c60b`  
		Last Modified: Tue, 25 Feb 2025 11:58:59 GMT  
		Size: 90.3 MB (90316651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d28a5af7632832dbf0a9896248be932971aba4af06c89b659315ee4a42081`  
		Last Modified: Tue, 25 Feb 2025 23:32:05 GMT  
		Size: 125.0 MB (124951869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c18513e83bf3035940a74a4429b51ddb6fcbb26dc6a3fce217760ad0d02724`  
		Last Modified: Tue, 25 Feb 2025 23:32:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:814c9532ce8d867d6de229a5948bab56e4595192c7f3cbcc28943f9bd8c1f181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6ecfe5cfc9738e9aa401be5a32e3634ceab5f93d548d1434579f3bde9f4a97`

```dockerfile
```

-	Layers:
	-	`sha256:61466539a5c931d89598fa340200fb1b1678796e28dd17d04ceaac752baff791`  
		Last Modified: Tue, 25 Feb 2025 23:32:02 GMT  
		Size: 10.2 MB (10246773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73d9f9873be5b66b913c1b9c1704102a871f94585e1df849f79945b86775aff`  
		Last Modified: Tue, 25 Feb 2025 23:32:01 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:3fe099ca3d6d62c58e845bc8ef5ca0707837cc14b03e60c32fc572cf05b82450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330924631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fecae51193c61c4675ccb71ce70d69baa5804edbc8786573f1381f2210ca1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16676c94eed4de3ccdb41bd857bcf5d665d34b49ee6681f62964150c8db326cc`  
		Last Modified: Tue, 25 Feb 2025 09:28:53 GMT  
		Size: 68.9 MB (68903037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0708d6fc70d6c17d917a582922c9c9c869293636d289db2a690696469b90d8`  
		Last Modified: Tue, 25 Feb 2025 23:31:35 GMT  
		Size: 127.3 MB (127334743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d00f295328f8c0dcd270293059170a76623daa783a40039a1af476afd85837`  
		Last Modified: Tue, 25 Feb 2025 23:31:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:534c8ceb4762e9182ef452e52d9382fd901f23445cbedf29b0387a7d01a4d7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10137717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bd95aee83f97b107381c83fd8553d76f87321287db5c54dd0bb2649a0104e0`

```dockerfile
```

-	Layers:
	-	`sha256:070fff8a8eb6dc302ee936d685651f5a05a361b0c9b61a45eaf7aec3f7eaa262`  
		Last Modified: Tue, 25 Feb 2025 23:31:33 GMT  
		Size: 10.1 MB (10110054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de463b76869743182e58c528077479deb959cf461914752c6bf0d05b3cde5679`  
		Last Modified: Tue, 25 Feb 2025 23:31:32 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
