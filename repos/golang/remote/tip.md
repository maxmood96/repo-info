## `golang:tip`

```console
$ docker pull golang@sha256:86a242d957534b13fa88530edfae6faf02479ca9a0e15e914eec8d462830d05d
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
$ docker pull golang@sha256:1766e6b7732fe17ba09e0c3d509918e3e76f8f5242b5375f66b4a8bd65f47ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345442028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251484140ff28bba26839219abfae4a326bc6d38d777f829ad90814ce0875bee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:5401acdbd47da62354605cdc39280e128c1fda32c0830d209bca96e7352c65f9`  
		Last Modified: Tue, 04 Mar 2025 00:39:28 GMT  
		Size: 86.4 MB (86383185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e9a129027ad3875ac19234bac00390ebdd61f752809a25128556ac5b500a6c`  
		Last Modified: Mon, 10 Mar 2025 21:42:38 GMT  
		Size: 122.8 MB (122798022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c3921de02e975e97ed07a2daa03d3bcff05547ec218b570f40b9ae4428dfd0`  
		Last Modified: Mon, 10 Mar 2025 21:42:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:03a032e883b84ee13cb0f10bb49cad700d1646fdad15319bbf713c4577f49721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5554735f988abf81747e562a33610eb44bf762445e4c9e18d50a490f586e732`

```dockerfile
```

-	Layers:
	-	`sha256:19ebef96a144e9cb68cc5de730c276462fae5adbd776bab3b0be248719eebcb0`  
		Last Modified: Mon, 10 Mar 2025 21:42:35 GMT  
		Size: 10.3 MB (10301921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162ea8bd3e39b27c95047df94355fc69db39e35cd67ec3be1567f4d2b704784a`  
		Last Modified: Mon, 10 Mar 2025 21:42:34 GMT  
		Size: 27.8 KB (27823 bytes)  
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
$ docker pull golang@sha256:db01e16eabf08b18032a8eca630654624ca701af61b2a294137181a0faef9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363384808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d5e612931ae2da2b12fa67a0f70dc19b142a9bd3223b8c192d3c4497fff115`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:34eb0a545ff499f8c9f925571d19e4ecfc63b1db1f51e83434ef213b02ed36ca`  
		Last Modified: Mon, 10 Mar 2025 21:27:32 GMT  
		Size: 125.2 MB (125198997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20623fa1687eb847193fbc0dbd4f3ddbbe06f8855f2dc0344ed9c431b771556`  
		Last Modified: Mon, 10 Mar 2025 21:34:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3a9af1879706b5660103d46b2bb955e11719a4230414c328c3caf81219b3614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10274494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75feb8b6d156f26f6735bffa0dd76279b68f65aaded78f11559724cb809bc96f`

```dockerfile
```

-	Layers:
	-	`sha256:12d871128b6f4533cc13f206f22a41e1d7228db89897549bfd9e0b3112ba8ac2`  
		Last Modified: Mon, 10 Mar 2025 21:34:59 GMT  
		Size: 10.2 MB (10246773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20daa55a8b7b293af75b4fa0209edbcf653a057b7291a9d52718adff008e9a81`  
		Last Modified: Mon, 10 Mar 2025 21:34:58 GMT  
		Size: 27.7 KB (27721 bytes)  
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
