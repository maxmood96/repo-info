## `golang:tip`

```console
$ docker pull golang@sha256:28703400f852b3bfd2b152dd870c3e6d3c099253acc7a9014a64bc41c1455a76
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
$ docker pull golang@sha256:319b219d4df413ef30123a7f69bdf00032d9841af58d7b0ef6971542b29875d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355174318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab838f59d5e063d964d85f295a3aabaf825a31753d32813ca8d8fc2adfb5183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
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
	-	`sha256:7fa3c8aa4070fb481af519cff70ccf37561f95a8716e639e081c1a35761ca2f3`  
		Last Modified: Tue, 18 Mar 2025 03:20:09 GMT  
		Size: 92.3 MB (92332909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a83b25ec0e0c49ecd36fb9980281b7ce15ce7da6877f867a2e7766c298175`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 126.0 MB (125965793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50014ecf9e596dfc7ec8e3222b00920b8fa4d4e9c9bfb111c6641b51af3425c6`  
		Last Modified: Tue, 18 Mar 2025 03:20:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:2d0dc238c9e3492d9de05ff6ac4f5806cc4c741c46453003668426ef58d7e1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f61abec3206c2588016e8cf671b89010c3e50ad45fc6c31a94ac5963536265`

```dockerfile
```

-	Layers:
	-	`sha256:f71622386e88616e907e76a04e6175d1d86ed03f774e263728ef84f44df347cb`  
		Last Modified: Tue, 18 Mar 2025 03:20:07 GMT  
		Size: 10.3 MB (10270388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15ed36b47e4eb96093a9b241a7299e5f459e2672eab08d9f5a4d27d957ba265`  
		Last Modified: Tue, 18 Mar 2025 03:20:07 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:c46c8252521bea0fe8a4448b971fdc459f0aabf3549fff823bfc43878c60fafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315241687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f8220b9e9c3f65a6a7569fc432b98492f9f73208319f17c06f8f3122ec30fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 10 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
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
	-	`sha256:ca61e995b8c13d851dd3e3c6f227fdb4c36ab271e17ec8b18961597fba4895b4`  
		Last Modified: Mon, 10 Mar 2025 21:09:26 GMT  
		Size: 123.3 MB (123273897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae5c7c4d7e0987b9fb2648a63fbc9e04b4892618ee0dd821fa0ed6e2ab2f20`  
		Last Modified: Mon, 10 Mar 2025 21:09:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:62defcfd781bb3206398f7d15a76cdcf2b0b5a289a23c3bce1abb73cc7c3e291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10110183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf52f1797b7e403e77bd5097bb9ff51bb9f3c76296ac5c764167e6f52a72717`

```dockerfile
```

-	Layers:
	-	`sha256:2e6261371457be63ec193dfa35720397f6217a80989dbdbd7a5585f3e65ea359`  
		Last Modified: Mon, 10 Mar 2025 21:09:23 GMT  
		Size: 10.1 MB (10082396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4482a37d1a7c45d386aba106bbbf38a4d48327ae79a808d06ea48d071c32d3`  
		Last Modified: Mon, 10 Mar 2025 21:09:22 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4dc74b33b86cc01139d2e88785df527f0bd9d84976bad7fc3b3867f8f508573d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341106426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fecd0abf1f8f8efb24e047eb5921a61101e799f5966f8109be9ce4ffdd3cf6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
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
	-	`sha256:33fec41d8cea8d405aa42d9093a8aac6c3163d9643759441cd5e55b364f8ad55`  
		Last Modified: Mon, 17 Mar 2025 21:14:15 GMT  
		Size: 118.5 MB (118503866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a6709e126e1c6e9294efeb51ca1b8b25506b112faacd5294d26473a388de6`  
		Last Modified: Tue, 18 Mar 2025 18:52:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:db7f4c6b288aaaf167be99e49c0df2f7c5ae5d04db4fddbdb51b1b6762f21299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de204d4e51878144261721b9471b671c9a9cc9f8030b6df63f9875300a946b40`

```dockerfile
```

-	Layers:
	-	`sha256:155abdc9c5c2aca6d8505df90cd0b78d5c8d0ac9681db02abd1f2c981164941b`  
		Last Modified: Tue, 18 Mar 2025 18:52:23 GMT  
		Size: 10.3 MB (10298235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b803c934914af9017188e03f7ccd950e9a5a2b7a96dca91dfe76ba27a6463612`  
		Last Modified: Tue, 18 Mar 2025 18:52:23 GMT  
		Size: 27.8 KB (27822 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:fb8f2f17a254e26d8da5c493a50fb7cdc1ea7a4863a9a517fce189711eab6c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354359913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd0a23fda06c2efd9c790d710ce2e053c121301ec6501d7b0a8f2c6c0e4db96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
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
	-	`sha256:f1edc4f718f62e041d676de446cb4888c5ff5f42f915a298f242bb7b74beb275`  
		Last Modified: Tue, 18 Mar 2025 03:20:40 GMT  
		Size: 89.8 MB (89752454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a94495553b1c250ac72571d6400e4136caa9f00d345a28d3faea166cf26f298`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 124.1 MB (124068582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8153625e804204a538d4eed13a510f89a5b70c2fe3ad7ed4bca473fdc736504`  
		Last Modified: Tue, 18 Mar 2025 03:20:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:658035dfe68909a6428c4a28a3e420366ba418b34fc89c234c3caaedf680f6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10278082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d0392623dc467056237f3c7bc0b89ea262c48e0774f0483835117691d4caff`

```dockerfile
```

-	Layers:
	-	`sha256:e0637bdc9c6cdff98d75cfd8ad6a1dac23bedb6b750cd9d3ea8981dee72dd2a1`  
		Last Modified: Tue, 18 Mar 2025 03:20:38 GMT  
		Size: 10.3 MB (10250462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d526b4d058ea320bb86a3ab778e391ef5e708b2c8843c2bd4e31f3c4b14a21`  
		Last Modified: Tue, 18 Mar 2025 03:20:38 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:9f9507d1aca1df8ac6665840cc3d068bcd917352b0be88554ab2045316ba15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325572046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2607b962e3c7a4ed556e81edc3a785eaf9e63ce175c6aa995aca2d081da963`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 10 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
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
	-	`sha256:681aae030c647e6116514faebe9fc795b381fd8c5db6a6fd70eb54da72b73dcf`  
		Last Modified: Mon, 10 Mar 2025 21:27:49 GMT  
		Size: 119.9 MB (119949071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193535263cfbd887fd9e175cbf523e2140b8afed77b5d04c769c99438bb54be5`  
		Last Modified: Mon, 10 Mar 2025 21:27:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:86377daae872022c37d7c691bb95db9735682e7241d8075d20cbb9c9e4882eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d711977ca7e7552c8c3ced2df8b8a7db4156b4b942a755ab436ae89a8b43b12`

```dockerfile
```

-	Layers:
	-	`sha256:8a104b5089ebd8f37b34d09fc10a7f0844b717f39af735c74476bd727760bf5c`  
		Last Modified: Mon, 10 Mar 2025 21:27:38 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:8be384769c5ea89778e876f605700d39ae30431845dd5a4b05ecbd7563d82d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358928840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726c0741f428f3a42c9f0aea307359d6fd77a777ef99c83f9e571fd684b15b20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
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
	-	`sha256:a7e4c876f35d00d63f2c866ec3855df7279e987d349b282a213db1668751ac44`  
		Last Modified: Tue, 18 Mar 2025 14:01:55 GMT  
		Size: 90.3 MB (90334911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c78cf9a0739a8dae1dc72464edfce0456a58eb76be29f8acb49a502b699b46`  
		Last Modified: Mon, 17 Mar 2025 21:15:53 GMT  
		Size: 120.8 MB (120793562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636435a7c60e29a29ea2f26cb4816976d67ed954bd7ac8011097b39dd0e83f6c`  
		Last Modified: Tue, 18 Mar 2025 17:17:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0a8a9f47a2cafcc03223e330920610f0417fe3ecadaf6340c6c8d16e5c1fa3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10270800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3287f1a3aa58e2b089ba6f08ee44784178f0ef9fb32094bd0bd81a1ef05660`

```dockerfile
```

-	Layers:
	-	`sha256:eb0d617f17efa5dd0564b098112602418080be0a2da40259247dcd1e14e92fa1`  
		Last Modified: Tue, 18 Mar 2025 17:17:45 GMT  
		Size: 10.2 MB (10243081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cbfa6da707888868f851c67f358d5768ee6717ffe4124ca9e33e6e22e21a592`  
		Last Modified: Tue, 18 Mar 2025 17:17:44 GMT  
		Size: 27.7 KB (27719 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:a1bf7fdb3a33d042990f51bb2299f2902ea0414155c77b28c5ed6c71260cfb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326692211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf33d34d5e66ce1a26b8dfe6e2d664798cada99ab1a7d3fdf55cb76afd1c19d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
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
	-	`sha256:8a13e6f9abf2d06fc1ee4c87de50c8b3c8fdde00639d695bed23ca66a5a31ed0`  
		Last Modified: Tue, 18 Mar 2025 09:32:56 GMT  
		Size: 68.9 MB (68923120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d46e335600bdcfe68156442397e360bf7b9f4f575af2fecc2a06de9129e542f`  
		Last Modified: Mon, 17 Mar 2025 21:54:19 GMT  
		Size: 123.1 MB (123134636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15fc2c01ac55aa5d6d10e9ea73cf17bb03774b70a3fe8935a91e7499982523`  
		Last Modified: Tue, 18 Mar 2025 16:48:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:532968f97d60e739491ac2a33f211aff9f616e8b5f5da4592966208b4088b2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871a81acf1dd7b3016681c72940043436c402db7d2bc2683d89b916f46fd520e`

```dockerfile
```

-	Layers:
	-	`sha256:42e78977ffbf68a38bb8ec578be3a540e299e0079c66c99a3a09a2dde78a2a92`  
		Last Modified: Tue, 18 Mar 2025 16:48:29 GMT  
		Size: 10.1 MB (10106368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594544fd8f72fb3de6304007d93b4f596ee073d66d432aa024e383ac0689763d`  
		Last Modified: Tue, 18 Mar 2025 16:48:28 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
