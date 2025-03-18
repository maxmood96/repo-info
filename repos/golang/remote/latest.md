## `golang:latest`

```console
$ docker pull golang@sha256:762bb9cb6d35eb03537551112a3519cf0e6bfc66891530ce7dc7d6169ea1eeb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `golang:latest` - linux; amd64

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:1a9bc401e9504d096795eefa9a00d22fd57ea665dbc7694c4aea8c551a241d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269054194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f831c4b6bc45fb1999822628b11dd3f32750a48e1c78ba7317e20b109b7ea848`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:942c762e5659795d4f6aaa827e039a42ab97a6e3ec651d1ff497332bb958710f`  
		Last Modified: Tue, 04 Mar 2025 21:56:10 GMT  
		Size: 77.1 MB (77086405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f30de0685b77991e952ab3de96d4a37ea5e2923c37fdce81d4bb331f3fce9b`  
		Last Modified: Tue, 04 Mar 2025 21:56:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:c8ad85a4814f7ee8687b0baab0eb476741c44f54428ad4d6708174899947d7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c024768f82a6c511192feeecd7075871f132b7489316dbc9e764fb6401410f23`

```dockerfile
```

-	Layers:
	-	`sha256:dedc5e7eb493dd0a9951957a26af0f8657e58095b64c4d2cd4ca81988f11bc7b`  
		Last Modified: Tue, 04 Mar 2025 21:56:08 GMT  
		Size: 10.1 MB (10087682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53df401eab12f893e7e2c9de76905f929bf2f0c48949b2ed992fc62dfa89f387`  
		Last Modified: Tue, 04 Mar 2025 21:56:07 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fcac9ac2c01ddb5ea125d3d57e536bc890bd8d74a773b73cc9bf858630dfbd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297828017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88de62925c535c1a9006f31ea2adccc609e7c6ce90f84f4fb326376d287f67ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:57f2b93ee17017a4673f1a381ec312f22e8e9c0cee491adc746b10d3d5f200b7`  
		Last Modified: Tue, 04 Mar 2025 21:57:12 GMT  
		Size: 75.2 MB (75184010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307ec346c8f5c8f1cd4b4e7eb7909cfdd1526254d752a6aad28ce8c34d04335`  
		Last Modified: Tue, 04 Mar 2025 21:57:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:164e6495ea668c3c80ec7ca28495633d1b963d852d7658baf945553773b3d78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10335047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07093f29d79fc00252de577e2c8d4e35299ce2c35c25bb361ff9e91ff4515a79`

```dockerfile
```

-	Layers:
	-	`sha256:fa1f1889053e2d98a27e6de47292cc656dea6dea65739c35e70ac3346328aec0`  
		Last Modified: Tue, 04 Mar 2025 21:57:10 GMT  
		Size: 10.3 MB (10307219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5dcc94c560eef45f1c5e0fed96148842a57b75dd728f44143e1ac93d59ecc4b`  
		Last Modified: Tue, 04 Mar 2025 21:57:09 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:bd5046c0750ec0b80059427efbbc56bec3a6fee8a557d8d0ea7d58a053dfc03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278516798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cde330b44496cdd6e913f4de7b015b39ca6bd94dacebf6d63851a5713ebe8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:61534752f9c3abcae097f6c0ed37b190cd20dc837badc14c61d13d828c41d11a`  
		Last Modified: Tue, 04 Mar 2025 21:20:10 GMT  
		Size: 72.9 MB (72893823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba914a0b66277a6de8d59cdb28ad2ed27d28909dcc09109b7c76533f79124671`  
		Last Modified: Tue, 04 Mar 2025 21:20:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e3f8fb901ffb073be4c9d24a8d888348b8497063bd5bbd041c17d33619ff3565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e016b240a5bc4f605706cafac0a338645d3c045d5e3635a201c0e8631c0ae813`

```dockerfile
```

-	Layers:
	-	`sha256:86154ee45f9d4caafc2bc25365a69204c98feedba799ae1baaf1f94d11e3fd29`  
		Last Modified: Tue, 04 Mar 2025 21:20:02 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:42afedf6faf3696f8d492dcb2fcbda4196e49c56a206b66c2f969b28b25e1849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313676352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa245e9549266ce31932aa6d61d799aa1820b7829722a571d3b66a35913bb8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a5911afb128e3f71046cf878de8eec44c93ec9b167d4e1c0d275b0bb6705ba8e`  
		Last Modified: Tue, 04 Mar 2025 21:17:56 GMT  
		Size: 75.5 MB (75490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de81eaf1072017263dd398316ee422eadd9c7d03ae344ff75347f125bb5ee9`  
		Last Modified: Tue, 04 Mar 2025 21:17:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:9f18766593c6ffa70a0bbca1f9bcc0ebdc800b05c9d58857c85d8c69106adbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4121b500be7191fc7d088df4bff9eba910c85880b5a5041ad2c0f894aac55`

```dockerfile
```

-	Layers:
	-	`sha256:5e53d541c2f266664b9c48a4944cca59d733789b0c1a3eaaf6f1b7a0c208dd81`  
		Last Modified: Tue, 04 Mar 2025 21:17:53 GMT  
		Size: 10.3 MB (10252043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c6abca72b11633c66b276ebb0e70ab985b51715e2f0256fa94d582c3f70ddc`  
		Last Modified: Tue, 04 Mar 2025 21:17:53 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:93663e2a3f82cddc281b508f0845081d35d6e0541aac65389246289ccb566d15
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3042716400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4521fea3b4ab32b6c4894786d417d38077e4bac0149393e066c1765526b11ff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Thu, 13 Mar 2025 17:56:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:56:27 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:56:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:56:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:56:30 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:56:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:44 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:56:51 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:56:52 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 17:58:06 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:58:07 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cabafad37383a76746edfcb2071953269124a2265ba09441ee0f5d7f71198d`  
		Last Modified: Thu, 13 Mar 2025 17:58:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50de0436cf9ecfa74fc5d95587b22832b984ea8227ca754847427f312104c6d`  
		Last Modified: Thu, 13 Mar 2025 17:58:12 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75aed525537a85f0e03308401bcdc47750a3300892abc8ea627041e4b835f29`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467bb08e0639dedd01fcce8a6154413b2afb3dbb2ebb7299bb398784b35bb790`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcf78f047f3484aaece02ecd4a59d5984810bdf2d5627eae59f7a6a64bdc99f`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc180882dccbcbfa8ed2c24aeed59fe82f22d7c2703782b9671137e04efb6df`  
		Last Modified: Thu, 13 Mar 2025 17:58:18 GMT  
		Size: 51.2 MB (51243951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a136d0465fb143e0d7d496e097d70e9811be3247a61030b9295bba520699a`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba33351ae4b9fc70289ba768d1144182d84527ca94055f51de19e8002557af1`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 368.5 KB (368501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f818c7fc05eb20c78075dd4cac280ba03d2788ebe1ec8a4f8ebe72aeacec52d`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877f11928db80d3e7990cbe1a38b96b6f336c9c4e8dae51dc5af77a13999e1e`  
		Last Modified: Thu, 13 Mar 2025 17:58:26 GMT  
		Size: 82.4 MB (82445659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7b36712399b98e09d95ac09a8711d211d7817039520c1b2bdf76e202e9b32c`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:800cffaa1fb68ea86108aa0e47799657cefb5eb2dafec292736d26a250d5090d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2403740620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cebe5eef200c42e308ad630eb5e0ff1ca5a8648c191a55290b9e515a29d77c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Thu, 13 Mar 2025 18:03:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 18:03:52 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 18:03:53 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 18:03:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 18:03:54 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 18:04:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 18:04:17 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 18:04:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 18:04:24 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 18:05:39 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 18:05:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f99de87a30a6a17cfcb672b7f4ee158a3b5e425660bab42f52d6a7e2f669`  
		Last Modified: Thu, 13 Mar 2025 18:05:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abedd7c76e3f893429d285cf368820ab93c85364936bb1b75c3b477a3d05fc7`  
		Last Modified: Thu, 13 Mar 2025 18:05:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070850bc0ca89244d2c69c30e03d37ea28b65fe02554aeaf19492b5f6a8df521`  
		Last Modified: Thu, 13 Mar 2025 18:05:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b85d83886b6143c40018855a4ba72fb650d98a4f16e07e4183f42ae42c5410`  
		Last Modified: Thu, 13 Mar 2025 18:05:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf89c75fd7760c0c1b1b2cc82356717272f0ceb467fc8ce8a85d07fdc903fa29`  
		Last Modified: Thu, 13 Mar 2025 18:05:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33517bbae483baac54ac53322dc846f325d40014b2a10dff5fe6132bc948ac99`  
		Last Modified: Thu, 13 Mar 2025 18:05:51 GMT  
		Size: 51.2 MB (51208026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c00643481be58c834803b2f8f601e7d1fd01e6e6f762bc6140b32109c95bd5`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b771b9dd29327d0054d0805bd84833beb52b8cce661da3dfbcd86894fb098`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 347.5 KB (347465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d47ceb326f6b5b5f9fd92c4bac848bd184921f3996ec43442666bd196f7163`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4805646d0f77baad2a61712dce4bea52d805818c042a864bed39b4470a400e4`  
		Last Modified: Thu, 13 Mar 2025 18:05:57 GMT  
		Size: 82.2 MB (82233485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205471dd2aad8662d29c018eb66cee449a0b7f964499a8010340edcef468801e`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:2940aedd805dfb2c60a71de5cfd7494ee9f27ed2b9bfba6a0ffece0a30129ea9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2285425680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8284e2aa9c65a7dd983155736b366f64fabe6ce46da64e85904641e9534dbf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 13 Mar 2025 17:54:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:54:58 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:54:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:55:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:55:28 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:55:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:55:35 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 17:56:48 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be870f634812fa1f6d6ef69c59c30cc849eb7596a61e1f3f6373a0a383d4ac`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8b22dbc93c5dd5761e377d70a307b01859c72506a434bc7980ec33dd3aa2e`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b726286f3b4261c8b41eab22833c2eab62b8539b5d35de8da22ccc3be40d2d`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c64d4aaf2deb795cad856869013cbc6ea6c0ba2e8e476e4334e0acc8853062`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a721b86de1025ca9822807d4bd52272090272764f25dfb8ac69d0eb36d6bba`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ff4d29b2cfc97e0bd2e86cd87cd9db4f784be84bba2afad44d47e1d586839`  
		Last Modified: Thu, 13 Mar 2025 17:57:02 GMT  
		Size: 51.2 MB (51205680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7600c08bff7cb8b879392f339bf34ba620f20b441e46dfa3ab55239124304`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d55a8591bfdbf361f4d5d6e9b6d827ba7fd30637673aefa88663f8833d6c1d`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 345.5 KB (345509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e482464a247f4b87adba57ccbb331fc183aa2204a3cff45093cdc076ba360`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729385db686e034d720cf2a1617ed95ae204a798aa1d74e015319a4426eaaf3`  
		Last Modified: Thu, 13 Mar 2025 17:57:07 GMT  
		Size: 82.2 MB (82229348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350fe0982ad03eb420de2fdf529fceca297915292bd006b4cb4e29d6d84b487`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
