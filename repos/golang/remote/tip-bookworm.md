## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:5ddec45472a6ef800be0b073e12f96912d31174eaf2eb3709128321346527c69
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
$ docker pull golang@sha256:3f7fcd77a8f1ad16f4413304c82626aa1ed15012f1ce0c6ae89ce3797d192be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312428385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895f9b3827cc8948c486a79977289150585a5e2bd2b588bb096f82e0ea83b990`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854872e47db054bd9fc02d53e2bd77eab3e680c5e0037c740d64b4bf52c796ac`  
		Last Modified: Mon, 18 Aug 2025 18:21:04 GMT  
		Size: 92.4 MB (92378597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7e0855ca36f610906757c6b7d60a0cc7695b1050f79b46c01f422018bae66`  
		Last Modified: Mon, 18 Aug 2025 18:20:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9a8329783e3d0a0b52d6c010198455e0415ea6c408cd1193d5740c0ffc0aa356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa7e0d905fa7db33525515b50e861d12e4f39ab36ee61a3b70ed2bcba54d91`

```dockerfile
```

-	Layers:
	-	`sha256:c205bedbf252265bf0f067ec6e4cc206328b069fbd3aea29dfc58de4a6589a72`  
		Last Modified: Mon, 18 Aug 2025 20:24:10 GMT  
		Size: 10.5 MB (10488143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e660e9926902a7fda631c699bab2dfceb56026419f3bc4f6a0d218248ea6e93`  
		Last Modified: Mon, 18 Aug 2025 20:24:12 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:bf31e81ed316d2dd02f802f885350bab61025df0d620d805872457618f37d0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272119683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1399833a289440f3ca0f00ce07cd6cf33a7a757656a78319cf2d73571518c4fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348703b73efb0f6211572f7fa5d5ad5d8b51d1edbda217c252e893ce4db3e055`  
		Last Modified: Wed, 13 Aug 2025 13:41:38 GMT  
		Size: 66.2 MB (66243932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d10df13da6c65403fe5e3b6a9cc280dde2bb564435b287f2b85119c986cc8`  
		Last Modified: Tue, 12 Aug 2025 19:00:44 GMT  
		Size: 80.1 MB (80080443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ab9955e69b607669f320d2a78c63201e4728c72905ec1582736a6b032a6ab1`  
		Last Modified: Thu, 14 Aug 2025 06:04:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:55dffa09e34e9651738d938d7de05a7abedeaca9aecd90453dc556b087a7410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10322006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4953ca9c3f7a353a5b4ba6e3243f26782b903ee053ebc55036141a104478a`

```dockerfile
```

-	Layers:
	-	`sha256:76103760e13d4413da9e9353f21338794c6ec230f720530d2fb462143e75878d`  
		Last Modified: Thu, 14 Aug 2025 08:23:59 GMT  
		Size: 10.3 MB (10294841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39041528656201e313568c31b0002065b23d45fa01456ffc5efaa040ba31461`  
		Last Modified: Thu, 14 Aug 2025 08:24:00 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b414998831233adb111ccd469f1f53617e635ff5ec2b84acec773fbed97654b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301726558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5afc73106a488959d1359bf7fb7f23db81b5b7fc3cc2d26ba0a0fc0a6cc7e05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74428ac8e178a1971d9dbb1d3fd3dbca228cc3be24099b1bbb9f5ce6c61503df`  
		Last Modified: Wed, 13 Aug 2025 20:55:24 GMT  
		Size: 86.4 MB (86441689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b7cf68665eac7cfd64f5bb944a8b17de913d4de7e1d26ec5a73f422afb207`  
		Last Modified: Tue, 12 Aug 2025 22:36:24 GMT  
		Size: 79.0 MB (79005413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb32cf199116769a1a1050c83a4611e365dfe734580d6ce91bd596d43982dc5`  
		Last Modified: Thu, 14 Aug 2025 03:43:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6d697bbed19836a6847997361d0b1e6681210e4aebf62cdf4e2e666fed979da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349f0a5349bb6ad2a177236c89f734e0a1cbd845c286fcf2ccbe75294b78bfe5`

```dockerfile
```

-	Layers:
	-	`sha256:7dd55f997db59dab248f9dc51f974fc990eb943495e3168d906e68a2ecff1e58`  
		Last Modified: Thu, 14 Aug 2025 05:24:37 GMT  
		Size: 10.5 MB (10515967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eabb3e450b3ff079bbd3843e5b0ec68f7b70a07f73c9488bb6a4020be31991`  
		Last Modified: Thu, 14 Aug 2025 05:24:38 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:6288c0a21843205ea4236c4e090ff58a27a4dd3481cbbd185462eaa03f4c9937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312132902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da4c48ac88f6abf8b5ec9d871f0aceb1999f609788c59c8e26a4998ae2a753f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874646e2459984b117c58d731a64ebcb9d23f76cf755c68e1ddb30317e57abc0`  
		Last Modified: Tue, 12 Aug 2025 22:13:36 GMT  
		Size: 24.9 MB (24861125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c25d261fc893dbf63d447e191cad0237f37f95f01960ee9b9026b75ab3a74`  
		Last Modified: Tue, 12 Aug 2025 22:14:47 GMT  
		Size: 66.2 MB (66226107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7da6bd442fc01337a65d4e2e72190bcac60085df6599eafca2c93963e3d8c1`  
		Last Modified: Mon, 18 Aug 2025 18:21:52 GMT  
		Size: 89.8 MB (89808302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e8e68078f30759bf20f28e6048f172006be5ecc54bcd4119ae6177151f1f2a`  
		Last Modified: Mon, 18 Aug 2025 18:21:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9717ed775e04c1f24430264f1159e939a8ab9cc1bfcca859057614debbdb6025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4baefad78ea1fbd8f0790485fccb13f47b5031437c61f18f4d9403bcd0e1`

```dockerfile
```

-	Layers:
	-	`sha256:1d14ae53482ccd2a92b4b282eaa9a5912e79d3e77a4da9f68788aa1fc3574ae9`  
		Last Modified: Mon, 18 Aug 2025 20:24:20 GMT  
		Size: 10.5 MB (10467731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fb93a440f0652a4affadcce1346738b06099c22bc3c348633157da9a03d5a1`  
		Last Modified: Mon, 18 Aug 2025 20:24:21 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:2e1d4d6092dab78981c32f874d20a2ee2a98035d253c816fd58d3e99d8c385c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283441332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c190ec9719221b2463832177742ee28bb21890465980975ec21ccf17a6a98d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a6c9e42f300b90af431e64763dff49b7a85c93e85756330e2e61065c60996`  
		Last Modified: Wed, 13 Aug 2025 20:42:15 GMT  
		Size: 70.0 MB (69983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4d8a0af12b6081d7443c050710e5a1992fda8864981fcf1223d12ff162a8b5`  
		Last Modified: Tue, 12 Aug 2025 18:12:25 GMT  
		Size: 77.8 MB (77768878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005195e07c4af420a8aed447d327387918a74841f5e31c5dcfff25046ef214f9`  
		Last Modified: Wed, 13 Aug 2025 23:54:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a58cc2ffd22be5b3b3f76ed194ac34ada1e76a40ffbceb00861b7cb67e905863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efa28a699f12c34f72547be65b48300899948d3df1e393e1782aec2203b0834`

```dockerfile
```

-	Layers:
	-	`sha256:0aa3b10127e9c47966b305fadb268619f38488222759fdbf763e9b02ad2e439b`  
		Last Modified: Thu, 14 Aug 2025 02:23:48 GMT  
		Size: 26.9 KB (26911 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:fa13f27a82fce120ee2e7bbca3492421f1754dc7b733913a7148220ee6679f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318633712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc64f7a4bd1b1a5bd4da69754a721e59d487ebd55360c696c85a1647115f45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39109abe29c871d1d44890534b7e51d78b7fe59e173aa5e7d80b7e5cc0036fce`  
		Last Modified: Thu, 14 Aug 2025 08:24:00 GMT  
		Size: 90.4 MB (90386437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d949d12b56c803641dc1ee823fe0b4254f92598b51ea3dd4b12bbfc422e9b7`  
		Last Modified: Tue, 12 Aug 2025 23:22:22 GMT  
		Size: 80.4 MB (80403035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a99eeabe577e8dd91a6d47d857c3edc5ca76254fb164dd857eea0e288512c`  
		Last Modified: Thu, 14 Aug 2025 12:04:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fd77100030a97c219a192609a7deb53d22ef70f4b1ccd585d564313243630774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f1652267298200d7b7de7bb42cf1b499b753563b685757a27e7fc76dcbecad`

```dockerfile
```

-	Layers:
	-	`sha256:c7a86488595df5b40329c3c504a83aa5bf43809b383f551764113e8a9e356467`  
		Last Modified: Thu, 14 Aug 2025 14:24:37 GMT  
		Size: 10.5 MB (10460614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01575325d97663471046a93a91d75e04e661fd4c37f4fb77b00176732d3b0eb0`  
		Last Modified: Thu, 14 Aug 2025 14:24:38 GMT  
		Size: 27.1 KB (27103 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7a3959c3ea628cebf4248826559616b5e272d16211533d8a8575ecc49b467e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285340912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76e40bcd88cf7d3457b0047e84e9b31aee57d679b4a5076e2638825583cb865`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d677f893a7543d9139e8727a2143b6c7402f5276d6e82ee3190a647e7dffd02`  
		Last Modified: Mon, 18 Aug 2025 18:47:09 GMT  
		Size: 69.0 MB (68975545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ccec7fe320ee8c37e0889e53e69af11d798227d6db8eb04340ee1bfd893535`  
		Last Modified: Mon, 18 Aug 2025 18:46:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b4373899c9221bdaed3be7752f89e5cf83b21abd79d2290706a8e3770f92d236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10346958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f45868906435a423f2b48a079579302696f236fb76945518535352eddccc16`

```dockerfile
```

-	Layers:
	-	`sha256:302f50ae268776a7df6545183e14bd0e9e3e3cf4b7ed0b13e5e749fd05f735aa`  
		Last Modified: Mon, 18 Aug 2025 20:24:31 GMT  
		Size: 10.3 MB (10319901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31b0554009bbd468694b2a8ca247c5de62fd1644e42e9b287c08c79cd4ed52`  
		Last Modified: Mon, 18 Aug 2025 20:24:32 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json
