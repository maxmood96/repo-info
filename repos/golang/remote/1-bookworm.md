## `golang:1-bookworm`

```console
$ docker pull golang@sha256:005ac726c79bed3f04c04b22665e945228ef287dfe3e240462a3c6cc98d77628
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
$ docker pull golang@sha256:5348c6b1f0a23fb5c5406af7b14de5598272bb50a7cad1f36ab63f0a16d69df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304022280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361d8b5c9aa59d977e4f74169823c096a55b29bfff49c12ee259db90c116a9df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627963ea2c8d5e7f344e68dce05f9013c8104d06e6e0d414fcbb261cc0b6bbde`  
		Last Modified: Thu, 05 Sep 2024 22:03:10 GMT  
		Size: 92.3 MB (92260964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ad979d054ab0c2824c196b59074e31870426326f3e359ca9ee12d0fcb999`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:13966d233353948cf8a2a17958f90620d2110a2717b8085f4129bdf3e884aaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b870bd861ecce4567841bc4bdba18bb9b65d42948e86a217a2b7425449a9a2c`

```dockerfile
```

-	Layers:
	-	`sha256:7f0ddc4b25be8c49bc1d9113f413faf693151f882dda9fa306afcef4573e8eb1`  
		Last Modified: Thu, 05 Sep 2024 22:03:09 GMT  
		Size: 10.3 MB (10257203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201b19ecdbdd1860a21ce2588ba0b3fc96d2b8419f7232ae3f0226c2d63d9007`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:e3e4449f4e4e7f740122cd1d6c63fe1fb8cd16d526f6c68fc90773111f5b89b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264541612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5841f7b583c0acb97645976c686f7192deaddbf3e8f50842d98fca0122149`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:26 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 13 Aug 2024 00:57:26 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:24:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bc24d45690a515d5d64aeaa7be5994f7db1e902b9e4dadf7bbc9b27214008d`  
		Last Modified: Tue, 13 Aug 2024 11:29:59 GMT  
		Size: 66.1 MB (66089195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6363114f7204e8b9cd3cb47febe5a3082ffb85a82d8c47efb0021f3f9323f`  
		Last Modified: Wed, 14 Aug 2024 01:59:55 GMT  
		Size: 72.1 MB (72127549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794e0e6bfe8897aa8d2badc883a93aacac284e36a2385b6f0880852f4a4296cc`  
		Last Modified: Wed, 14 Aug 2024 01:59:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f1245c4cae3a035d3b1881a66750e9a0bf7676ccad761e5cb01a4fd44c8faf0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10094203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f643c0307132ced133d3d5005838cbaf8efd4fdf6cb38e31da89d30dc3a11b82`

```dockerfile
```

-	Layers:
	-	`sha256:fa2b41aa169a4e07c7c4a3b02601d5d484457d94acd84e31649659a6fbcf52c0`  
		Last Modified: Wed, 14 Aug 2024 01:59:53 GMT  
		Size: 10.1 MB (10066549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1034f1ff9e7f98441fb650bf30a31f3b719c0df3467fe7d68c2ad051046a0afb`  
		Last Modified: Wed, 14 Aug 2024 01:59:52 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c6b19df41c8e5073a0a91d530741ff8768020b8de487b3f6902955322eab9d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294096120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2737b855c4589a4564aba00d16fc897fa4b8489ed918ec317ff872dc988fbbfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb27c98d5b9e78892d876693427ae0a01e3113b36989718360a5aa9e319fd80`  
		Last Modified: Thu, 05 Sep 2024 12:04:56 GMT  
		Size: 86.3 MB (86293965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355a3cac949bed5cda9c62103ceb0f004727cedcd2a17d7c9836aea1a452fda`  
		Last Modified: Thu, 05 Sep 2024 22:09:14 GMT  
		Size: 70.6 MB (70624628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f1399aa9166438efeea4696812a3fa3f3397ff114492577a919f9b09f3c1ea`  
		Last Modified: Thu, 05 Sep 2024 22:09:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9f8916cfbf54ceca3e1e604d00a6860dcc72849c58d9d64b78f08e89f7b13737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32de3080a6fb1a0c6332623176dc833ddf537da11c02635af62f30b1264adea8`

```dockerfile
```

-	Layers:
	-	`sha256:491b00f2ed10213b8ce100cdd319779d8e3ce065e4d776bca859fc472ca056b0`  
		Last Modified: Thu, 05 Sep 2024 22:09:12 GMT  
		Size: 10.3 MB (10285129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2aea2a57604ad14dbd86a0bea76171187abda2e739d1ee9ca6d20382a90fe2e`  
		Last Modified: Thu, 05 Sep 2024 22:09:12 GMT  
		Size: 27.9 KB (27891 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:d0aac08f954c29a6c42b8fa15f590467343aa44322b5fa059227d554b07d6e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302975159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f889b01b12deaf070506381da0038616a294137d6a7b292de92bf019c12bac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25df7d7205c7278d0ce0c357ebf605f53619a1f72c2e985b5b04563be9b22dd`  
		Last Modified: Thu, 05 Sep 2024 22:03:11 GMT  
		Size: 89.7 MB (89657864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5944571d35e19fa81ca655e6b7753cdb3e37418aa683e0c2a9c169e5d7256`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 71.9 MB (71856183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080f9c22972c331e5b0c34f2a64de5c7be8cc89ac39b2fc7ac5f7a0bb162ac6`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:022706e303fd2d3586d4e585fafe9d697c4e1ed08903a6e54658f8178e8105c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10264933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f58d7c1140c2b2064342800f0800bd173d938624a5542f2ec28312710cc9ac`

```dockerfile
```

-	Layers:
	-	`sha256:9340d615858ab4f34990893d54b60c8dd60d64837de014613a3e77cea42aee6e`  
		Last Modified: Thu, 05 Sep 2024 22:03:09 GMT  
		Size: 10.2 MB (10237459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf9c7e8086ece43bf53761a02c1132bda2a8f6e260fd3e4df450002c8722caf`  
		Last Modified: Thu, 05 Sep 2024 22:03:09 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:59838dca99129c64bee99b64e7f7a52002d5089fab4570d8e794f9614f81d5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274286095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6760f9828f19306064e6d88936ef76d8d1587800dc46206a039fcc51f8926bb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:48:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15bebfb1ce6517765581a89c1270a3039857497f5393a3a53eb55a6cf6c3b9e9`  
		Last Modified: Wed, 04 Sep 2024 22:23:29 GMT  
		Size: 49.6 MB (49562002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2220e2c6ab360be293a3568d8fad1b242e41ac727fbfd337305f9bda60d806`  
		Last Modified: Wed, 04 Sep 2024 23:12:52 GMT  
		Size: 23.6 MB (23647328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18258835940e3a6a6470cec276b968942cf166572cd7df8b709c75a6ae95f76a`  
		Last Modified: Wed, 04 Sep 2024 23:13:44 GMT  
		Size: 63.0 MB (62967111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88010f422507795f5659fe7a6f69ac5dd40524c2498dcb11b7ad8117cb7a4701`  
		Last Modified: Fri, 06 Sep 2024 01:27:59 GMT  
		Size: 69.8 MB (69831735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f92ff5c1684aca058ae9537bdbaf5bafd344391c0d79677375775ca94fc2195`  
		Last Modified: Fri, 06 Sep 2024 01:28:00 GMT  
		Size: 68.3 MB (68277762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb79cd972e07f6caf76c23c334f385c86da9881234a785bde6a22a16ac8e23`  
		Last Modified: Fri, 06 Sep 2024 01:27:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6f97ea5c76fdd4880f151d70a772bd6b2d7e94ed1df8f52bc2252644a845c62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c464ff278f10aedb3ec446376b62dacf8b63032181e33d4e981d0d41ae194c49`

```dockerfile
```

-	Layers:
	-	`sha256:9af2eb5a912e466a40441a6196537e34a26e46e101208199d87686347b23d7c0`  
		Last Modified: Fri, 06 Sep 2024 01:27:52 GMT  
		Size: 27.4 KB (27406 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:948b5272dd9d7527d66c0adcee0df747a378fd085750ed597bde7c5589de600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309891463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fe4232124f39574d08cd59901aff8fe8f77f5759449651f0c022495ffe9bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928db16ca296d9db3172ad8a2c21f034d363ea47bbebd05e5c085f52a9cae60c`  
		Last Modified: Wed, 04 Sep 2024 23:13:36 GMT  
		Size: 25.7 MB (25710210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39a679766d4a9f2fc4813eab194d4b11ed292163911e303c4f21bebad4be350`  
		Last Modified: Wed, 04 Sep 2024 23:13:58 GMT  
		Size: 69.6 MB (69588450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd8f872ceea67d0e302845bd02a8f847d8f29dee6e814576a90dbe61e77becb`  
		Last Modified: Thu, 05 Sep 2024 17:36:19 GMT  
		Size: 90.2 MB (90239717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5b8a4bec9158fc0bc52aa7bb2055ac421fd36de9ea98898a7188751ff7da1`  
		Last Modified: Thu, 05 Sep 2024 23:28:18 GMT  
		Size: 70.8 MB (70798979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c353ca765f344612c00173ace9310d1b9f4fd7783fd5b32d3e59d29436242685`  
		Last Modified: Thu, 05 Sep 2024 23:28:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:355ac7029c567ea213253496cc7fb526052f92beac01fb0d71653f3363e7092b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b138730893ef69b1b9e3d18853ced7f7d385bd64e0d56d4f9e762fcc4c6372de`

```dockerfile
```

-	Layers:
	-	`sha256:085da552c81d04d776b6463a86914582ef3e92f89416bb0a735c6808f3a40e9f`  
		Last Modified: Thu, 05 Sep 2024 23:28:16 GMT  
		Size: 10.2 MB (10230058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75d2fe8e2d4e73cd5d140843602c294ce8fee068910bd59eceabc5fbc067918`  
		Last Modified: Thu, 05 Sep 2024 23:28:15 GMT  
		Size: 27.6 KB (27593 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:3fe7af19aaf1ea1304e8ed10b83342240e9bf3ca0210536168a4289591b9d494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276808616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3e7b9c7f2fd198e4530349d3f1b2ff53b364c02fd52811fa1af2af797fe3ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb724644bd76f1a0ff54c043dd51ad35a7b4ac4ae889cf9d65db267bdab2ddf`  
		Last Modified: Tue, 13 Aug 2024 23:07:37 GMT  
		Size: 68.8 MB (68804026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766dfa346f9569deddaa862bfcc6c453c61295fa0688cff4cf096f917447678`  
		Last Modified: Tue, 13 Aug 2024 23:07:38 GMT  
		Size: 72.9 MB (72899210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb3533a7f134ba9070e272b22385b2101c1314d98ea5341a1eef2c75da2270f`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ef01b3291087d0d26345dcb2967f740188e19311e4aff4978422df4b96dace2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10121740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9db1b7342a289681cd4b098771c6efacb676f89c7454f3c972aeab705ae3de`

```dockerfile
```

-	Layers:
	-	`sha256:59950e2ac15ab44459da053ebd57341da30561f4b5160b34c822237d28604908`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 10.1 MB (10094213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f90a3137578e3c461351d1a0c9b730c7d45bf984fafc5ba56d2eb3ea7659e3d`  
		Last Modified: Tue, 13 Aug 2024 23:07:35 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json
