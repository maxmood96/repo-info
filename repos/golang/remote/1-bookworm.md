## `golang:1-bookworm`

```console
$ docker pull golang@sha256:96a23e75187cec3661fc96454cf7adbc5de5f1a2cfea4d5374bed9a464a32287
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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - linux; arm64 variant v8

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

### `golang:1-bookworm` - unknown; unknown

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

### `golang:1-bookworm` - unknown; unknown

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
