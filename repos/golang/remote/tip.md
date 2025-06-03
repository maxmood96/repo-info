## `golang:tip`

```console
$ docker pull golang@sha256:10b8fd90094467f25bf5e3978e43ddf6b0b61b412028c509c9d482a95722725a
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
$ docker pull golang@sha256:5afd983dd1473c7b6b00cc61dde47bd88e59508cf09ac3750d23f4896f1f76e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355814605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac4ac8d7de5f2bb3904440c81e755fca4d6f8a4df011533c0e8ad834bb999ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc998b3188449ce406578b5343bd0dc7f796bc2b4d570f2c9adca3cc4d828420`  
		Last Modified: Tue, 03 Jun 2025 13:54:39 GMT  
		Size: 92.4 MB (92355135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c772e4d16fa9b2fa9b4ea3dee2c356c3597d08d324bfd3a1c2b9b5a987e5a2`  
		Last Modified: Tue, 03 Jun 2025 13:54:37 GMT  
		Size: 126.6 MB (126555573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e144d157a8577d05183fc6da43aa5ec513cb7552a6f9ac104f6088a4795d676`  
		Last Modified: Tue, 03 Jun 2025 13:54:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:eb0d3a187634d344fb4c9419165fc70bec290bdd4c343c277f69d9e0a45f2d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18c5dd0e19e1ac1880dab2d5e255ec28721ba19fd0615126b7393d224f864d2`

```dockerfile
```

-	Layers:
	-	`sha256:bab3398afa2dad7468f44de97c05567127330c4d160ea7adf921af7cbd6f0bc5`  
		Last Modified: Mon, 02 Jun 2025 18:24:00 GMT  
		Size: 10.3 MB (10313121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbf0b9a17291e50e5beec41cb4c2ac0bb71e673ff75b618cbafe8f1a5545b13`  
		Last Modified: Mon, 02 Jun 2025 18:24:00 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:4374d143691995ba7ef55a5e642a553ba104620b9ae7b26acc3f98d8b962d014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313401316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eae904d494b3599eaa1ac12e99e811c360344011624222668af785de903559e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6769ccbcbb302e58183ef7d1b1458e5ec9e4e0e712cf266d56ddefb34341bfd`  
		Last Modified: Tue, 03 Jun 2025 14:36:19 GMT  
		Size: 66.2 MB (66210504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaef207e52620490d9796ba5bb1c39803d44a66aaefee2acfd8d44ca0dc7d0b`  
		Last Modified: Tue, 03 Jun 2025 19:04:11 GMT  
		Size: 121.4 MB (121406962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e8a8ec3da59bcab968ef148dc88def0c7b0b10f2b8942430484a07efdfdee3`  
		Last Modified: Tue, 03 Jun 2025 14:18:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:796d44f506015613598c583ce06e77e287844982977927c6569919ebee45ebcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10147593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704a29cbec4a28ff7bd83df071168999d91109eec957ac2dbe69f2585b142e1e`

```dockerfile
```

-	Layers:
	-	`sha256:540bbbc5f3c1b1a4268a371533c44752616c0fb4fb6d77585204a26d5cb216a8`  
		Last Modified: Mon, 02 Jun 2025 18:24:50 GMT  
		Size: 10.1 MB (10119806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67adbc89cbd3f3e12a4270945b13ce20dd5b951afe71c1632d696a22af352e8`  
		Last Modified: Mon, 02 Jun 2025 18:24:49 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d3c050d5d3a81446463420a3dca2b2eef66132fc816fd868f4092f40d8b7680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (341970565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31618d6b8b9d167ebb8f3d51493bd1ccfdafcc8de7884111ad1789d4e5dbe4ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e45158653cee17fd0433bb95f654076603c1dace770784457d1f08ffc1f1bd`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 86.4 MB (86409121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c61459497fa2e2873d988523a87fbbab1017c75b44162e22c190b9fbc0f92`  
		Last Modified: Tue, 03 Jun 2025 13:56:11 GMT  
		Size: 119.3 MB (119320718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb2d81eddb19d513169b11e00f952943c051c71e4b406d3cc61860161313b4c`  
		Last Modified: Tue, 03 Jun 2025 13:55:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f27ebb822fab806c7290ea0ffd2670e80e44bea6401e940162dd40e0e6d0dd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10368791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6de273cda4f51f8a850a69ffbd1f7cd001e67feadb76a99741d18c632bca8e`

```dockerfile
```

-	Layers:
	-	`sha256:e27565c397ed4d7ef72b8fec916f5de780eea8999731a7365f7c71d935a6bd87`  
		Last Modified: Mon, 02 Jun 2025 19:41:49 GMT  
		Size: 10.3 MB (10340968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822b5c448bce2d6c6756fb4e1183061bbed2b88b0e79c9b03007e6da611a4cf7`  
		Last Modified: Mon, 02 Jun 2025 19:41:48 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:1483b4bf2a85df484549de2d332335efe65ffe8ef10ce7a29a8a272ed67c4440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.8 MB (354840215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deaa957cc58e2df2ee670b123f7cd186cd6c7bfe5edc7203588658e2a9792cb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Tue, 03 Jun 2025 14:02:05 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Tue, 03 Jun 2025 14:02:15 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e2153d1065f232a989d9596bad856a7c433c56ee3cdba73b8d3e675fcf7927`  
		Last Modified: Mon, 02 Jun 2025 18:24:25 GMT  
		Size: 89.8 MB (89774548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59517f64f93ef3235377e65403c21a43aa149e3627f878c0069b20d4472659dd`  
		Last Modified: Tue, 03 Jun 2025 19:06:17 GMT  
		Size: 124.5 MB (124514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe46560c0552452a4de1455688aa69c90519160261cd02705ddcb79eea0c28a`  
		Last Modified: Tue, 03 Jun 2025 14:08:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1c7c6ae1fb2e435f3fa2fe9f0423c10263fbc79ce69dc71338b6fe404c884809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10320295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e909e5e97d7c9b544b50c99eff13c8d64a09499680217b68a9cb857a70f824`

```dockerfile
```

-	Layers:
	-	`sha256:120770c38faae4dea83a108cf0c9e14d4fc2a059d037e3b44bca24ea31a91bec`  
		Last Modified: Mon, 02 Jun 2025 18:24:23 GMT  
		Size: 10.3 MB (10292675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f132c0cdcb2d326059c17b46a83cdc9fae14fe2baff05c50f1eaa5e9573835f1`  
		Last Modified: Mon, 02 Jun 2025 18:24:23 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:b0ca1d62392c8e989059ef208e7958cc63b3ffbb3fd3217bcb03b3181d707e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322529348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425933ab34824c5e81f26b20017bc757588e6d769cd5e280644e1bc0d9e1e1e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Tue, 03 Jun 2025 14:36:20 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4ece845a4d4a4ec28b24cc19384f49afd8d3bee80380c09f3a36d476d34fc`  
		Last Modified: Tue, 03 Jun 2025 14:36:21 GMT  
		Size: 70.0 MB (69950183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db5cd1010d814e523a09de2416f990c5bb4b3798c6c676710e4a42e96fb635a`  
		Last Modified: Mon, 02 Jun 2025 18:42:53 GMT  
		Size: 116.9 MB (116902169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60fba964c6b3ce2627903872f8dbfc973b062ed17579c2168b9f73ae7fa34e`  
		Last Modified: Mon, 02 Jun 2025 18:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ce27b8eb358de862da28788712f5664e17ce572107752017d588b92dfa01b390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013210bad9648c8fd31a129210ddbab02f18c7440c1cea1733c41387aa0dbc45`

```dockerfile
```

-	Layers:
	-	`sha256:4e41e4b23e36208a0c75bfaaa5357a51e7bcaeecfce987b8af1bea4320ca0277`  
		Last Modified: Mon, 02 Jun 2025 18:42:42 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:ae8eb3b2e6eefe6abd19a26e7a887bd0b3fe991133094840df44345c907caf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359630988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b528d117bab43081c0be2012e5dec93c4d7d0d6b01536f72eeaf767f72f1432e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3651009f91cf27e970ae7dc7349e20fba94b97f4d2143617e748afd3d930d`  
		Last Modified: Tue, 03 Jun 2025 13:43:23 GMT  
		Size: 90.4 MB (90354720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00aee01924c56be514b4d5b89dd62e8a80222c3c9c95a0f0907430fb88a09a9`  
		Last Modified: Tue, 03 Jun 2025 19:07:17 GMT  
		Size: 121.4 MB (121447518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59347442bc397755e1d629eb2492c87cebf077ecbdc6ecbbec8f696f59bfded8`  
		Last Modified: Mon, 02 Jun 2025 19:30:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:bcf43773d92a9803e566d75d17c0bca842b7c0dfb743bccbed18c65eebabc0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62a0924975ad3ee1f2974a45b541df87cfc0ec3ca2388bc0f0c86044b2bc95b`

```dockerfile
```

-	Layers:
	-	`sha256:d5aef1bacd8769997f2796f2331b28f0e09c2c9f79ca321dfd1e5c2888ca735c`  
		Last Modified: Mon, 02 Jun 2025 19:30:32 GMT  
		Size: 10.3 MB (10285625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4010804fb6f9b48c7b5e9705090180071bd1e0a135d6e4ee39417bd14d6cbe0d`  
		Last Modified: Mon, 02 Jun 2025 19:30:31 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:14b682fe2c881efe3841d19fe91cf204afb473f8f635e7d8eff7e4fa207e890c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327359564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914b7cc751714bc929584524183133c198814389c56c84102d0b6ac7207448`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd113c317127acbfc86d7af2a1be3cb7e330fa8c58847cef98b51c46d4e19c94`  
		Last Modified: Tue, 03 Jun 2025 13:43:29 GMT  
		Size: 68.9 MB (68943692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d9aca011216cb8ec22b40335fd2aee2bbbf158897a84613b9937eba268ae48`  
		Last Modified: Tue, 03 Jun 2025 19:09:17 GMT  
		Size: 123.8 MB (123758489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50832a7366f5466e0e1fa0ef823b574578b9435666b121a74d4a1346cd3006`  
		Last Modified: Mon, 02 Jun 2025 19:05:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:39744541a7d7c680fa06b4c0e73af7a41c3cf181a64bae13244fb815ea9afcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10175435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211eff2d5052a8ee3cb671f98c65bb2afea37bd26d97003514e92187cf75105b`

```dockerfile
```

-	Layers:
	-	`sha256:79792e11f9e9b71543829455cc95ef826fd83c92d2abea8eb6d19233dc0ee565`  
		Last Modified: Mon, 02 Jun 2025 19:05:59 GMT  
		Size: 10.1 MB (10147772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c692ec78f709f57ea2653458f83d996e4d690404dcb3c779896424b5f660015`  
		Last Modified: Mon, 02 Jun 2025 19:05:58 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
