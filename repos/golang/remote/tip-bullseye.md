## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:a2d9b8eb03019c027e5bbe7381f5226069f2aa000f593ec9a0f2fb9a0bd4f547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:67d5387308c26673414f809b92a36ca3049b1c2f1664012b1882a99848ecc52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339891984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d44b32bdd6e331537cf1232a9853da418c0ca7d46776b0f1d859090f3d167c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079c6d14a20a26220335c21fa7c705f16064e3b24ba1dc159d48194615580d9`  
		Last Modified: Tue, 04 Mar 2025 00:32:38 GMT  
		Size: 86.0 MB (86001142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c2fe45d5701a9f8bd27731c298113978876c556feab51d76996561c120fb11`  
		Last Modified: Tue, 04 Mar 2025 00:32:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:3a8c076e80a0969275fa197ca903cf34c617774e29a56cb90532d9c4cdb60382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee56f410781256f7df163c7c7839a6dce57a5e3b435d848e9d60cfc7ec9ba5`

```dockerfile
```

-	Layers:
	-	`sha256:f7458f5cd029dd15250be64989219ff0060e66f629f01ec69155b00c98a01c93`  
		Last Modified: Tue, 04 Mar 2025 00:32:36 GMT  
		Size: 10.3 MB (10264285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c5af8c7e28f6de7c794c886b40c6affdd64f499a428857e9e3fb8823f0b163`  
		Last Modified: Tue, 04 Mar 2025 00:32:36 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:a837900a5d01c9547b57977ea1a02bf58b80e7511f11f4f8595c93e627175084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302321460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177e21b309adfd8889d84e4032513dffe79d27b718f105981f993bb5b4f31a1c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0260b683984b5458b67512624176ac3f678832da5b7aa4c808cea1226ddb01`  
		Last Modified: Tue, 25 Feb 2025 17:02:06 GMT  
		Size: 64.9 MB (64892946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a4732c96edfeab450050a70f02b158342482c6f2a5dcf7aeba30aac7fcc17`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 123.1 MB (123087551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae22e48255c2f697b9fca095191c64ef9ed4dbb370fe1ee1e80e85c90a5274d2`  
		Last Modified: Tue, 04 Mar 2025 00:37:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8ff83dcb1445d6d700113aaec774565406fde43d62e69d2fbb98ff8b91642526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10096678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb99ee7b198e22fdc19f464029a2f564537aa0ff0433ffdf56308d41f0b3364`

```dockerfile
```

-	Layers:
	-	`sha256:2efd8a3e8ff40d1c1e5d273a4866213d28071925f8b6a5ae36577dc650d9a184`  
		Last Modified: Tue, 04 Mar 2025 00:37:24 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6faa21ecf8ae7a6825db76764a993ca0287e4deee2f8bb42603a7c7ce0fbe65`  
		Last Modified: Tue, 04 Mar 2025 00:37:23 GMT  
		Size: 26.1 KB (26053 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e9da58c31852e94c9d6b192024d06896897f027441c926eb70fa4dabe93d1775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326682733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa2f0ba3e67dbb5bf8eb1eb1ddc3744d82e82d55f96b45e07f33998ae843585`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c63332dc2fc1cf0757c0675d81bf024aa3d2b601d0c397704255d7fd384be6`  
		Last Modified: Tue, 04 Mar 2025 00:42:12 GMT  
		Size: 81.4 MB (81413797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fb2f15af0e54e78387b98706e083a5882e5cd46c9ae24a07d9c9a7de13391d`  
		Last Modified: Tue, 04 Mar 2025 00:39:29 GMT  
		Size: 122.6 MB (122620567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b74e6d376969b3acea37d06a45e7f19217aef54404da6c16397c1abc7641bdb`  
		Last Modified: Tue, 04 Mar 2025 00:42:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2733037aa8678dc8087d1f4ff4372029af85d79e03f8e0d562442d047a2b4721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f817fe3d67c037f53a1a81bc3db8498b6d6827d4d0d68a924980162f7a08fea`

```dockerfile
```

-	Layers:
	-	`sha256:f9901a33ddec75ac40fe0245f768549b20fc3d1079993839e39b3a9fe6dbe998`  
		Last Modified: Tue, 04 Mar 2025 00:42:11 GMT  
		Size: 10.3 MB (10265857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5233ef641275bfb9edfe0bc133507135d9417ebd270c950c8e421d3d92dcf0a`  
		Last Modified: Tue, 04 Mar 2025 00:42:10 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:d63bb2e50e97e3f4c0ca39eca56af996e9814bb732c253259822319911e13f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340655963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea06bc112edc96fa3b019f641d5ddf2a319097cfe223d30be1eba6a80aaf855`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd643331f91c7ba21baa591ebcfb1698199cc44b0bb26546281af3b879239289`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 87.4 MB (87426512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c0d99ebcb8c5141b1cf6b2ed9074c140a52b0def862e573dd13e9a1e6bccc0`  
		Last Modified: Tue, 04 Mar 2025 00:33:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:16fbb571bbcf739fa9709b6b3bb82bbe8c42494bc123fadeb9a4d61d98d4a4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cab14f013fac636e393ddffac66c9d18a7038fe6c8237cc3bbb033fcac5cf17`

```dockerfile
```

-	Layers:
	-	`sha256:0b15dd9481ff505de4da3d48d15b3c6bf25f93c49e8b9c899e86868bfc1e5781`  
		Last Modified: Tue, 04 Mar 2025 00:33:44 GMT  
		Size: 10.3 MB (10254076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42abca9be7f6581df8a8dd516c1308a78fafc59f31aba4ac33525fedea3d8235`  
		Last Modified: Tue, 04 Mar 2025 00:33:44 GMT  
		Size: 27.0 KB (27027 bytes)  
		MIME: application/vnd.in-toto+json
