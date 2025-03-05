## `golang:bookworm`

```console
$ docker pull golang@sha256:d7d795d0a9f51b00d9c9bfd17388c2c626004a50c6ed7c581e095122507fe1ab
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

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:7ebae3e990ad9a8406da7ec4cd127decc408c98f8a88d0f2bef629bcaff691cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308188515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29616a01ff27428aaf681f7abd8439b6aca78cadb73fac0475196cb261a34b91`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:ec6bde4714ee6491f090f4367e5c540e43ac6f9b238b25b0838f2a9d1d10f577`  
		Last Modified: Tue, 04 Mar 2025 21:17:32 GMT  
		Size: 92.3 MB (92332444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cc98ff0842a2601bbc4e7db3db70a323469849a03684d1b9b21e7f825b7e4`  
		Last Modified: Tue, 04 Mar 2025 21:17:18 GMT  
		Size: 78.9 MB (78927068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10ccacbd8ad4103e29b0a10e17fcfdbc768b1361d50b2c9222d457544de4cb1`  
		Last Modified: Tue, 04 Mar 2025 21:17:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5cf2bc9031df9cf885d1df93b3f8a892d408864f5b62cce50ce095bb3b42b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10306969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4348ec71d2e80493c7791e1fa74e1cdcdc3ba24a0a53ec949385a37396e4d6`

```dockerfile
```

-	Layers:
	-	`sha256:b28eeaf4ffc854429faaf6f13c55a8df17dd3ca9f914019a89b8f6ac8640ef22`  
		Last Modified: Tue, 04 Mar 2025 21:17:31 GMT  
		Size: 10.3 MB (10279324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8928caf63e04ab63261d69f3893dce8ad9b9e677cc754e3e413f637c6a958153`  
		Last Modified: Tue, 04 Mar 2025 21:17:31 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; arm64 variant v8

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:afbaa9ed2766af436d3a71b162a3efbe7c364b39b6ba8a02b85e60f4a879fe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307200316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff61230b9f968ac2be36b595336d27c6920c8db38f9b062584901adbf5480bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:8529ae9c6214f5023dcccaec364da9c9cd11daaba3429c78406482cd1b30395e`  
		Last Modified: Tue, 04 Mar 2025 21:25:34 GMT  
		Size: 89.7 MB (89744391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d9251e0d8de5337c7947faa7a74d8a5743e95d63c085ef6f4a9939b793d5e3`  
		Last Modified: Tue, 04 Mar 2025 21:25:23 GMT  
		Size: 76.9 MB (76860148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b3aa8f5b79229ab9b2db1375099ac45128e1990da09d7a154084c039d2f7d9`  
		Last Modified: Tue, 04 Mar 2025 21:25:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dc818059ba9279d577e3544ef5ed1429eed766d8018ae0f5b990b4971a401209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10286967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd8ffb68a32a5ee87742a6c6e7a1224af8d71f68089bdcd5e5ca0a5d72c8586`

```dockerfile
```

-	Layers:
	-	`sha256:9264590d0b5cbf2dd2f9b0edf041a56c4a79ae42058af859cd2423a07466934e`  
		Last Modified: Tue, 04 Mar 2025 21:25:32 GMT  
		Size: 10.3 MB (10259379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e892e8f1fd2a0cc3370af83ca01341b8b273612d010083106852cff1fe176c55`  
		Last Modified: Tue, 04 Mar 2025 21:25:32 GMT  
		Size: 27.6 KB (27588 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; ppc64le

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

### `golang:bookworm` - unknown; unknown

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

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:2049d27fccac73684ec5d57a04f7b506d961eadf9ee8d3a937bf675c9fa6eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281322736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756dce1bc27014083f29e3b1e49c4a3227fcfd0d7420e467c6143a382f1b26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:f8de37e33097ae1468a19882a2526d339560c4de2ed0728e2c2fccb5003120c7`  
		Last Modified: Tue, 04 Mar 2025 21:21:51 GMT  
		Size: 77.7 MB (77732848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8969a4fafb83040eacf848e13d5022d90b003d834d8202da1714b8ece5fab17`  
		Last Modified: Tue, 04 Mar 2025 21:21:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:391a7a76ea30a887f0e19fb6179d4af760ac88c8bb50794b5e907be6800e9a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10142950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b819bbc46f63f97fb950c1e7dce33f25097e245b5d726dfe49d5cb86ff038ce`

```dockerfile
```

-	Layers:
	-	`sha256:a197094cf8ce0b70c49fa289ecd8c90207a87b3fcbffbd9f2e045022ab2828da`  
		Last Modified: Tue, 04 Mar 2025 21:21:49 GMT  
		Size: 10.1 MB (10115304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5986139e52a7968ecc25480806351330794eb3446a849555f3332401f33921f3`  
		Last Modified: Tue, 04 Mar 2025 21:21:48 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
