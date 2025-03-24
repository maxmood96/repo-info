## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:79f45ec8d879dc2aedfcd1c5ac59a5cd13c4f826de98c3316077ff25428e7677
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
$ docker pull golang@sha256:abcd87118304daf2a092c420ad00a6c238998be2112d3250796ded27a9cb2f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355230817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cee17dd318d50324666fcbf30e741ad8a9eec0abb5ddc305f24ffe2e9e2d1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6bf2a7c47b1658a34e0aadaa36370a5a2643fcd931361b70a93c80b06a1219`  
		Last Modified: Mon, 24 Mar 2025 21:23:39 GMT  
		Size: 92.3 MB (92333171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cbe769fc954b1a5756fdf48e31713555a112012d07425d7d4a076ea9376a7`  
		Last Modified: Mon, 24 Mar 2025 21:23:19 GMT  
		Size: 126.0 MB (126022030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9524a11f044feb20827479a3452a1402915ead2ef6a38e03c39a1cd36c6183e9`  
		Last Modified: Mon, 24 Mar 2025 21:23:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d135d595e8d32314413004c164ac4f4ff3c10a344542d8176464e04bde44423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5d5312453b91f1aa3c56a65d55d00ddc2f6b96a4b4f3776a96e75ef8400dc0`

```dockerfile
```

-	Layers:
	-	`sha256:4afaad2734c1c303a5f17fb98c0ac4c50bd912cc0892c817ca20e4c4f974bf9c`  
		Last Modified: Mon, 24 Mar 2025 21:23:38 GMT  
		Size: 10.3 MB (10270388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e97dfabc0f4567789c352a4ab1e0d45867100ada73982c6b236326a306a3d2`  
		Last Modified: Mon, 24 Mar 2025 21:23:37 GMT  
		Size: 27.7 KB (27662 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:cbfa0e4a931d4d2eb58a3bbe3e29b31ed931023c2979ab78f0ed6147dc7efa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312878524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf98c6ce013073c0417935631b22d39d6e864ac8d878afc7018a92040e1bc04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00519b34344176105ca045ed023ebae6a0a5c6298dc42892bd398946022f439c`  
		Last Modified: Tue, 18 Mar 2025 16:42:48 GMT  
		Size: 66.2 MB (66197750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353e9c70d02c05f5d0756f45338b0d2910b536c139fce40d68a3d97077441d9`  
		Last Modified: Mon, 24 Mar 2025 21:24:23 GMT  
		Size: 120.9 MB (120945332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb33741f9f9931e86ecb03dcdbd7d75210e621bfe68829ccef7a260cb9c60b1`  
		Last Modified: Mon, 24 Mar 2025 21:24:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b4f99c4fc919a16b46286719c9410318228c23d4520606a28aceb6ec5f749a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10106497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6821b3340db1a8b18ae23e95682183e5c4e8c0d5ff42989153c96f8e4ac542bd`

```dockerfile
```

-	Layers:
	-	`sha256:28803f4c226bef3cf9c80402222956dab7cdb45e9ac61e6fb8062efb7c4650e0`  
		Last Modified: Mon, 24 Mar 2025 21:24:20 GMT  
		Size: 10.1 MB (10078710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5923a6d46b7c11dee3e11729d0232333fd138d6c7ab3b20343d659ef5c1d7ca`  
		Last Modified: Mon, 24 Mar 2025 21:24:20 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4c29538c0caf3334fd939bf3137f7d74cbf0588fc480293c5e0564efe8224813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341161799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a266f7abe33263d02e049de65b7cb071a4afd9c7d70499e55fe81968664a9036`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7d0b299d26ce0f065a1fac5d6ad12aaa605ef18f04114a5b9e048f7d59782`  
		Last Modified: Tue, 18 Mar 2025 14:43:52 GMT  
		Size: 86.4 MB (86397409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa27b15393e951766b04748acddefa2554a614c3407abc8145f05a37f7e1559`  
		Last Modified: Mon, 24 Mar 2025 21:24:41 GMT  
		Size: 118.6 MB (118559237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb131713b9c36148e3911a96ecc93ced3c80d0af2a0aa1c6fc76446341030b2`  
		Last Modified: Mon, 24 Mar 2025 21:24:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4ce573d040dbe8cf4adfe1afc866b3e8ebb50f90727f12a3303ec4cf90cecc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22b65c07b1d3314f2c44772d74ad0c04b6df77d402b103363ed853cf8abe00f`

```dockerfile
```

-	Layers:
	-	`sha256:d6711502dcf632c191f6bdb73a2bec8c7f11d0d4915f96ea52959bd5fb64b09c`  
		Last Modified: Mon, 24 Mar 2025 21:24:39 GMT  
		Size: 10.3 MB (10298235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cd217d0d5eea4018b8df425fec59dad519823655dcb95ed5d655d97d2f241d`  
		Last Modified: Mon, 24 Mar 2025 21:24:38 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:e5a392f29ab1969503a674be9a6f889f834b5ef53d165197f2ceb205b18fd100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354404106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6985a648e53c47fe57ceaccf43aa1726e6b71de2bf385479cc9490c33928de59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c625a6cfd88ba2c1630532b97ccf2a882ccd5db19766865e5a7ba76a1230193e`  
		Last Modified: Mon, 24 Mar 2025 21:23:59 GMT  
		Size: 89.8 MB (89752909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76390dce495fb7dc13ff79afd09a2f809cad266d649bc9c2cf3aae32aea2ff71`  
		Last Modified: Mon, 24 Mar 2025 21:23:39 GMT  
		Size: 124.1 MB (124112320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78bea31ba2b26454da68837cae072247ad576a3e98fcf88c3e0eb25246dc69`  
		Last Modified: Mon, 24 Mar 2025 21:23:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fab611fdf8f7e59aa657dc46d90dcf620ae8de7bfdad9127df398b98a97d0ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10278079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051f588f61d00ce9a5e436c59fbef60c84f44345c7d7ea1c132661d7844e2e2a`

```dockerfile
```

-	Layers:
	-	`sha256:44df89b4297c032d0998bcf0abd757624541a5d1dab7d6a62dd786c8e306ed4d`  
		Last Modified: Mon, 24 Mar 2025 21:23:55 GMT  
		Size: 10.3 MB (10250462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c23d38ccecbb3062895ec14d9c332d08403cbe3440cd9254319ec1f0d53d641`  
		Last Modified: Mon, 24 Mar 2025 21:23:54 GMT  
		Size: 27.6 KB (27617 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6e0762249c216eb3105125cc58e90f28a21154d53b32acc6bb4fa9dc8f1a34eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321919544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd27d59a43b93a8bed3dce511975c02230ef94670bcb41714194fd19057b8a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4688093ff24a7c0a47c52d04ce08c1411187824a95dc1fb509b4ab01c8c4`  
		Last Modified: Wed, 19 Mar 2025 05:02:22 GMT  
		Size: 63.3 MB (63308534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231f6ba5c37aa271ccac7a0771657978751e91d524c076449ab434853b6fbd6`  
		Last Modified: Wed, 19 Mar 2025 09:15:32 GMT  
		Size: 69.9 MB (69916047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c099fdef0621bd5b9f240c4da0e4f837aebd577fab07cf707e8d4a975659e`  
		Last Modified: Mon, 24 Mar 2025 21:42:07 GMT  
		Size: 116.3 MB (116343046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06632e762407f5a749c78b0d4e4faee4a95cd46e71024df3365729cc02d20206`  
		Last Modified: Mon, 24 Mar 2025 21:41:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6d4a8457ce1b3f520a9458fa2785c4403f55ed5d3b8310f107cf4540090c0f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513bdf2c732247f8d54701923d04996c0aa61a47c4fb951c8b25998cf481c93`

```dockerfile
```

-	Layers:
	-	`sha256:19d1b43fe5d2daf15858587b2786cdaccfc64e6f6a22e514a85cc92010e73480`  
		Last Modified: Mon, 24 Mar 2025 21:41:56 GMT  
		Size: 27.5 KB (27534 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:62941e70f2a74c48bc1ff2ec8f15fb73e4685dc4bfbbc75d780ef803e34164ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358973274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ef98b89da222ee313275cd0fb6825a641e0f9092166e93279a650030a0fdca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d300aacbc73f5f66a38fd8a02deb1a013bd64c099f17f3efe76c226cb8443355`  
		Last Modified: Mon, 24 Mar 2025 21:44:57 GMT  
		Size: 90.3 MB (90334664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1867a2d294df0d3b21b808b4672bced3956fb4c495003b07361f0a8e9cb5d1`  
		Last Modified: Mon, 24 Mar 2025 21:44:58 GMT  
		Size: 120.8 MB (120838244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36040fc5dc5bd1142ec34b2e197017e0ffa697ef102a06094adf42d822bad41`  
		Last Modified: Mon, 24 Mar 2025 21:44:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ab072f97e0f304114b313c960269012e5243750a40bdb2e7c91e8b794afd5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10270802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c2023b7371b4ea452afa1869800ecc4cb1f649afad8c79a8ecc4051e908f4e`

```dockerfile
```

-	Layers:
	-	`sha256:67a2f9a599ec3988a210deae04945ec43f4a1e3b015a26a56b8432b25e66a071`  
		Last Modified: Mon, 24 Mar 2025 21:44:55 GMT  
		Size: 10.2 MB (10243081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42da73630cd8d858cef54dd6b75c18ea693e11a12e1801b5179a3edfb5995ef3`  
		Last Modified: Mon, 24 Mar 2025 21:44:54 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:ca40b4ffbf7421dbd5d3026315c1510649e0cc768e35b5f059a6c53d9f5f53eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326840259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d53e962f45c5149adce006ac4df2b2984399eb1d7cbd69125b2ba573a3ff2e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b90f4963e2742395335d2bc5e908f7c9081649b808703a7348aa8213d7b75`  
		Last Modified: Mon, 24 Mar 2025 21:23:36 GMT  
		Size: 68.9 MB (68922898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f92bbf60c027242fd3e59fa4d4252eab4d7c2b21b8d05ba9b89f6a7dbd625f3`  
		Last Modified: Mon, 24 Mar 2025 21:23:38 GMT  
		Size: 123.3 MB (123282906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33a76f0a8acd749a6645f179d3fa32b0a4761cf3b63f1dbe2b441d8356d6c2d`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ecf09e29b8fa71695f8c48c76d38ead2f3e02d9ae6f2c0ba7c6a9e802838835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e565dc3937a48b881b8218bb05c395940a15298d3d2f8d483e6d7d2e93a08e`

```dockerfile
```

-	Layers:
	-	`sha256:edb80b4dda3017df7a502086fb05722dadc564237b3bf6d5005f289a5b2d99fd`  
		Last Modified: Mon, 24 Mar 2025 21:23:36 GMT  
		Size: 10.1 MB (10106368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfb9fcc82c0869516daad0b5155b8d121ea931deb8bf2403dcde56712c8b8c5`  
		Last Modified: Mon, 24 Mar 2025 21:23:35 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
