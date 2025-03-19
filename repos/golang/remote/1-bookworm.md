## `golang:1-bookworm`

```console
$ docker pull golang@sha256:fa1a01d362a7b9df68b021d59a124d28cae6d99ebd1a876e3557c4dd092f1b1d
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
$ docker pull golang@sha256:a9b272427592056660a10f0a1bb7ebbbd43678dabe96995fb37fa9b29486f4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308135495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5669eb73fcacac2733d7797376d746e4953ae582afb131ed00b275ac663ae3e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:7c2eade47c1465391d64f09556a8b517a11cad229871f9367786ae78f3dc49a1`  
		Last Modified: Tue, 18 Mar 2025 01:13:19 GMT  
		Size: 92.3 MB (92332810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cc98ff0842a2601bbc4e7db3db70a323469849a03684d1b9b21e7f825b7e4`  
		Last Modified: Tue, 04 Mar 2025 21:17:18 GMT  
		Size: 78.9 MB (78927068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ace7bb406660c77b54f118f07e013a9d199fe452726063f9f1cda6bf9e88a`  
		Last Modified: Tue, 18 Mar 2025 01:13:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:de6c945b27d14d2c87cf0e2129cfc4cb5fee28df8d53a072dd240c39be3054bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ed011a02b449a36d51c752bed27ee64478a58ac0b22cf65e3cea24afeec711`

```dockerfile
```

-	Layers:
	-	`sha256:cf14ffd999a193d4d69b5ab3ccf3066654f9664730e617c20a40db6d3a2dd040`  
		Last Modified: Tue, 18 Mar 2025 01:13:17 GMT  
		Size: 10.3 MB (10275638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023c3d3b140412b992ce3c33d72a90d53ce06b2a4cc8d2868a91b3a41df7df7d`  
		Last Modified: Tue, 18 Mar 2025 01:13:17 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:898576ab9f45f17bbe5fe0c5bf5eb81f7655de0b113797c2a61b303715c41a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269019597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b69408c8e6ef58c2d7a18631fced421a3105575aa112478957aa14041efea2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:942c762e5659795d4f6aaa827e039a42ab97a6e3ec651d1ff497332bb958710f`  
		Last Modified: Tue, 04 Mar 2025 21:56:10 GMT  
		Size: 77.1 MB (77086405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77feeb3a1a155fcc5f0be2f0bafc6ce34695987840995c7b74d0431453544be`  
		Last Modified: Tue, 18 Mar 2025 16:42:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4fb36bc585713b48ad483b6820ed717a044db86b96d0954ab87bd5aaa89a491f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10111776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f797f4264576dd72a1c78982cf93c3ded9bf2f48ac231994df9b2721f9ce7c`

```dockerfile
```

-	Layers:
	-	`sha256:317f3ad4e4a691f2ca5b2729ffd2aa8a320043cda78735fa8ac51f3e6afe4aa1`  
		Last Modified: Tue, 18 Mar 2025 16:42:47 GMT  
		Size: 10.1 MB (10083996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75518b1619503b75f80ccff19520b557cfd2f785683966fd75ebbb4f315b91e3`  
		Last Modified: Tue, 18 Mar 2025 16:42:46 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f32028b6b5937c12b2491f2855060ce352ee3aea835bee0d6c0c4b2c67b72f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297786570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927babd7991763e9ffdb16851f4af5426d395f5785b04557b58bd27fb3062e6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:57f2b93ee17017a4673f1a381ec312f22e8e9c0cee491adc746b10d3d5f200b7`  
		Last Modified: Tue, 04 Mar 2025 21:57:12 GMT  
		Size: 75.2 MB (75184010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ee742c567fb4da9e28f9583bb92bb9017d377317f4a5c4c94d5e7de062561d`  
		Last Modified: Tue, 18 Mar 2025 14:43:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:23c043a341767ccca8869a43cfd43d4bebd196c0904c1647703059955710c023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c35387959854e378c5d3da88c1609282fb8dc9a90263847374582257fd5b19d`

```dockerfile
```

-	Layers:
	-	`sha256:78ce4356efa45ceb97c61b36d1995ad055ca513024bad88d2f10f52c23561f54`  
		Last Modified: Tue, 18 Mar 2025 14:43:50 GMT  
		Size: 10.3 MB (10303533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61df39f7e775e4a9e1e4882755e3bc87bf2ee8f197ce3c5f20b1240d5ef0209b`  
		Last Modified: Tue, 18 Mar 2025 14:43:50 GMT  
		Size: 27.8 KB (27827 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:7fffa50b6e734de104d6e98545d45fec5a487089b6e25c86cf6614ccbcf6e40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307151782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ab36bce7f1fa57df519fd66c1515f330e4886b26e1c85988c795e6b43e1dc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:f8e98ff60ae8324abf709d5b8bf7a9a98f856ccfa025dbac652f9b962876a9f8`  
		Last Modified: Tue, 18 Mar 2025 01:13:14 GMT  
		Size: 89.8 MB (89752756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d9251e0d8de5337c7947faa7a74d8a5743e95d63c085ef6f4a9939b793d5e3`  
		Last Modified: Tue, 04 Mar 2025 21:25:23 GMT  
		Size: 76.9 MB (76860148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327fb7c8856fc15f74859e6a44c605c8e0f59ac85de7dad98621aeb2a58ca888`  
		Last Modified: Tue, 18 Mar 2025 01:13:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2025f6a5685b34734b2ccbd01bfcfc5d91ee6d3aa4d1037f80763054cdd355ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dab38aa0af819734f871f05d390306c8ccf8631ac5049c9d5a0d1200769c9c`

```dockerfile
```

-	Layers:
	-	`sha256:a52c9a369675db3e5be299719da0d1856181cbe345ac5bd07abb6f34da9c82d8`  
		Last Modified: Tue, 18 Mar 2025 01:13:12 GMT  
		Size: 10.3 MB (10255696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e94268e64ded514237518d772e9fd7b90458f99101579eda63d4b930270a0a2`  
		Last Modified: Tue, 18 Mar 2025 01:13:11 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:e699cc2b9a075aec5018321d28f56f582ba9cc05d9023cca139a36c53246e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278470321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f114795670f2c3b106a7216497a074e7d9d00a3c80ff23cc70a756c1f0c30ecf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:61534752f9c3abcae097f6c0ed37b190cd20dc837badc14c61d13d828c41d11a`  
		Last Modified: Tue, 04 Mar 2025 21:20:10 GMT  
		Size: 72.9 MB (72893823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2738f9f7dd8f58732e6b21d631f682c3c1a81c3e8f9462c12a577446d5ae812`  
		Last Modified: Wed, 19 Mar 2025 09:48:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4e00d5a819a6e8914870b79dfa6500ad4e05b9653d63a7a6a656aa5039878810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12350019b5ab0d2be8b38ad40d8cfe7b6084b00bce7ff777202d6c775126486`

```dockerfile
```

-	Layers:
	-	`sha256:3e865e3ce5c7e9e65565c39528a98b904385049204fb7e37607d20f50d573176`  
		Last Modified: Wed, 19 Mar 2025 09:48:49 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:80af4c5f010a4c5af18ec08e0e1c32ea04fc36fe9d506f7bbe4a4b79c2ebd1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313625819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9738bf07ce219b573552595226e73374f03566d3cdfac00a7d8c93ad58ce1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:a5911afb128e3f71046cf878de8eec44c93ec9b167d4e1c0d275b0bb6705ba8e`  
		Last Modified: Tue, 04 Mar 2025 21:17:56 GMT  
		Size: 75.5 MB (75490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4822cb369634be6eb6abab4c031a6e47ce63a8b3b5f97787a40f49494917b1`  
		Last Modified: Tue, 18 Mar 2025 14:01:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7e02703b51b249d0594625df1d0ee96e81b3a0fbbddad92090e7a60d2ad99fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10276069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2394323b9812e794ce5c314459a196c837f94161f73ff89178cf51c9745ccbf9`

```dockerfile
```

-	Layers:
	-	`sha256:e5452732d4298764eb4d5ce2bf368305f13ad6fcb34bad36e409f4c70e95af03`  
		Last Modified: Tue, 18 Mar 2025 14:01:51 GMT  
		Size: 10.2 MB (10248351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ba6cec7de3adb68e56caeaf99b82ef837b3b7f20298f3d09bb2c3bf8149150`  
		Last Modified: Tue, 18 Mar 2025 14:01:50 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9c13d517042a5df084d9b77be4bc9ad02c5782256d45e1be30935f6e6dc41f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281290423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2903a8bc3ca7d73e46907320c1339ca307e870bcf6452de971d712b6621bc1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:f8de37e33097ae1468a19882a2526d339560c4de2ed0728e2c2fccb5003120c7`  
		Last Modified: Tue, 04 Mar 2025 21:21:51 GMT  
		Size: 77.7 MB (77732848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357cc85d3a71386c101f9ce6651b54134a5d8886cb961eb957a9c947d1acd29a`  
		Last Modified: Tue, 18 Mar 2025 09:32:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0636904d2a6b0d413125017cb24177924cc4d792e7815a62d9fae3b3e8acd158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29be01bbce51c4120d2c9a4f357bd5451d8e80d56acd0e6c2cf88732514edc7`

```dockerfile
```

-	Layers:
	-	`sha256:b082f9d6f6da46d7a030758710a936c892bdd8dcd56d156203666901b400e44c`  
		Last Modified: Tue, 18 Mar 2025 09:32:55 GMT  
		Size: 10.1 MB (10111618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3c6b77904329e8964542149e09d0b54fa2c2f3658828de25ff10a6e833bd56`  
		Last Modified: Tue, 18 Mar 2025 09:32:54 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
