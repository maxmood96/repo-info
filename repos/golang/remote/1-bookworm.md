## `golang:1-bookworm`

```console
$ docker pull golang@sha256:74908ad827a5849c557eeca81d46263acf788ead606102d83466f499f83e35b1
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
$ docker pull golang@sha256:6b1c4ee47e59ac4bff30e232762b0cf6894ddc05b46d2606bbfd42e3ed2d505b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289340236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b17b6c17310e140ca037d8973c2bebd685442be66736c0e92f0d4012eb406ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:9f18b3dcb2714f20cd117f241f74a35a8469e65b3d0eeb4d44a3b8bfcc1ba5b6`  
		Last Modified: Wed, 13 Aug 2025 20:24:55 GMT  
		Size: 92.4 MB (92378828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d6258904bfeab4c51e0be8616dc30e07915eec6cfc8504fec4e3e304a5bca`  
		Last Modified: Wed, 13 Aug 2025 18:04:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:27fbad688d934fbea0a78b85349580109c63d177541e207d2ce28fb1d0e275de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aec989000839526daa2e37c2be7e8334302a913b33d8f72c102633602c03bb5`

```dockerfile
```

-	Layers:
	-	`sha256:eda58c8364f7a9dac60eb62a2a2436669e8a825e203cdc7444386be484316d95`  
		Last Modified: Wed, 13 Aug 2025 20:23:09 GMT  
		Size: 10.5 MB (10488967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365e843ec7958e3810df22573d70cb37299457f697def8035ce7854de3d5c415`  
		Last Modified: Wed, 13 Aug 2025 20:23:10 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:4a7fcfa5f0dc2b22c53a6a54780290da8d800617081a42c50ceebf7d0c6376ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251016152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad06cacd49458872ce50b60f9d6b12c706749ac798e36689deb4d8cdc72b68e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31a3965f59121d0e041b2030968e46d20ec5f8012ca4597e6ceb971de1b16af`  
		Last Modified: Thu, 14 Aug 2025 04:30:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:96f58cd3a6c9ee5b8fbbe90187b7f4d7326e905bff68dee031ce2b849e1be694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10322251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a527e867747aba7ae75bb13c20668ebfc64138b38afba09beeeb87f0d7d08184`

```dockerfile
```

-	Layers:
	-	`sha256:f0afbf8f7580e3504d4db357325aceb01a83df7f0fe80f7d67a9a162430830d3`  
		Last Modified: Thu, 14 Aug 2025 05:22:55 GMT  
		Size: 10.3 MB (10295681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f559b5816985c932be5e6996a1af21fdf9004ecf875440e732a254ac43ebd45`  
		Last Modified: Thu, 14 Aug 2025 05:22:56 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:019c4aeeb97a4b1c7566d9aba6a0864dcf9e78a8371c2ba9a9aca53736035efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280276722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9904b37713afef1464153552003f5e174248167a407d6667ae511d091f2826a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a468ab485ecde99bfb464dd221e0c141abde3d45c2104ba58293437525130f2`  
		Last Modified: Wed, 13 Aug 2025 20:54:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5be99de591fedc7d10526f7a3266194645c2095fad10c527c177d00f5dce3675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbff03a6fb35c9659b824cffacce1f8dbd976467f31a3bbd1095f55737986b03`

```dockerfile
```

-	Layers:
	-	`sha256:03ce46a397e15dcf96cb74580e59f017c605efe4d853aa5c6c65b1e37cf9b97f`  
		Last Modified: Wed, 13 Aug 2025 23:23:15 GMT  
		Size: 10.5 MB (10516815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13895f88dc3bd140aebf7722ea1636886844e8fa567261f2400abe6ba7e9f93`  
		Last Modified: Wed, 13 Aug 2025 23:23:16 GMT  
		Size: 26.6 KB (26601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:89bd1d243f3a5a48c9acc03e5fb01e97e0ba4874c249a54e693dee430f9ef74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289137143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebcdcdd761be87ea5d4451cf0ebfee878ae686a79263e7699cfe57792f3ac19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:a46844bc7408906019f64eada5dacf1a4525dfe6325236573a49840d37f5a280`  
		Last Modified: Wed, 13 Aug 2025 18:04:52 GMT  
		Size: 89.8 MB (89808541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c63a4b9dc1f72141c9a2ae757dabf818be084da59430ae2f1f1200a26ac66c`  
		Last Modified: Wed, 13 Aug 2025 18:08:47 GMT  
		Size: 58.8 MB (58763097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c66a28816b71d73b58ee0345b002ad4b10cc5f146a17c27d867aaf483bfa74`  
		Last Modified: Wed, 13 Aug 2025 18:04:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f481919b706d9231605074fe6d8db662582d9b6b15dff3eb8fb8b0c8f4ce5560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dad9057feb40cb7ca72db71a3606a7e92ed4292031908933cb89941bd7dd924`

```dockerfile
```

-	Layers:
	-	`sha256:4ec83d0f51c09cb70d5979d678977d573417c2ff734226fef26f72df7014ea35`  
		Last Modified: Wed, 13 Aug 2025 20:23:26 GMT  
		Size: 10.5 MB (10468545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca84abaef6f0b029ae8b34baa195e217d252ed1d27560555cd584e61d3714263`  
		Last Modified: Wed, 13 Aug 2025 20:23:27 GMT  
		Size: 26.4 KB (26431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:4339c6271365672d053811e599ae9a6f55de4533d949afa053340040db114491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262145216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c553a596e1533c2ad5ead37dc4254a4aa8c8bb8fa53b80a1c854153a83be753`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:a64d7d31a426d383e806555d9302503965894656b9b89f245b6304166ee9e2bf`  
		Last Modified: Wed, 13 Aug 2025 20:42:16 GMT  
		Size: 56.5 MB (56472763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f09f531247d2aaa114e55e9ff43f3b365c7e0bf0df98dfe2f24c68c832a241`  
		Last Modified: Wed, 13 Aug 2025 20:42:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:096f11a48801c871a76111cd0a746342af065832ccc8897baf12ad0ddce88d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca68e77101606b769c800f8317f277303b2039412ebbd46b5df0f367dc9108bf`

```dockerfile
```

-	Layers:
	-	`sha256:01ce5fe4966e50442ee69a8fcc7300b18069b9983395493edd79c456d4ed074d`  
		Last Modified: Wed, 13 Aug 2025 23:23:30 GMT  
		Size: 26.3 KB (26324 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:49599233f8791f6181794a0a7e744b88b83821a8be9978186d220159635ce3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296265777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9329b0b01c1d178dc148959181f869192fb3ed75990ec05f879d3deb589d5ebd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7b64cb593d2a583e3a239efedd898492253e063312d25cdfc68031f2e5ca1a`  
		Last Modified: Thu, 14 Aug 2025 05:45:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c40f6019f707dd8a53d15bc7d2652de413164f42fafb177e6dc1d66290c544f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5124836e5e9adb52e7ee316b01faf749910aaa2ee2b12db7c3d3a3a1320c7a`

```dockerfile
```

-	Layers:
	-	`sha256:bbd8d3e1334ced62c1b517d7bd9aa684a821023cc7928a7547003f0640cbaf52`  
		Last Modified: Thu, 14 Aug 2025 08:22:46 GMT  
		Size: 10.5 MB (10461450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96815a8ad4d1ea65843155f4c84b72a1850b7b9eba94837bf543e75bdce8488`  
		Last Modified: Thu, 14 Aug 2025 08:22:47 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:c9324864f70d9a6f78b8a4484af55b56186aee007f0dc3c951e9769428dce023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263018383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1590f142bf572a6b4e987dd61e32a40dfe57a16a322822c4e92d57cb6e7c79ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
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
	-	`sha256:1b1e506bc177a1f42c07307ec64698eeb413400d5476072130fb93a50c047b98`  
		Last Modified: Wed, 13 Aug 2025 17:19:51 GMT  
		Size: 69.0 MB (68974617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cef7f4a807b94ebdc6320479ffcaa66f9578cf51b68557c32399938bd0545aa`  
		Last Modified: Wed, 13 Aug 2025 22:24:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ece51811da6b8e44b2391e9c2f388c71115a484564f28a7edaf71b809e0b86fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acda94b03357a33e7be6e9002e3020c37c0026046d163a25078ec201b654b64`

```dockerfile
```

-	Layers:
	-	`sha256:9da2a4e00069e33ee12dfa492b18e905425d4b2c28054f185c3d24721ba42970`  
		Last Modified: Wed, 13 Aug 2025 23:23:41 GMT  
		Size: 10.3 MB (10320725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45d84aa29cd1731bdc6a2770b30f298e6d195220daccc6a6da9da44b598de40`  
		Last Modified: Wed, 13 Aug 2025 23:23:42 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json
