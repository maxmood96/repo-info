## `golang:tip-20250607-bookworm`

```console
$ docker pull golang@sha256:5ab83a3a0c31c8331496e7bb741ab8feb082be6ce3b7fd376c73596d7ed90806
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

### `golang:tip-20250607-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:d12242ac955672302b25e6abaf09d53efcdeda4643d3d58a817f19a9e435e2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312422564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ac1322336f794d660da4af688b115614c88ab5bd070b6e3a090bca12b389bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3077579ba53710f7b37fdd96ba0d126bddf31645f96cd52ef1932fdf1488f3b5`  
		Last Modified: Wed, 11 Jun 2025 05:58:27 GMT  
		Size: 92.4 MB (92355073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc635c4b2a5c576a8a73069e117f29a377ce38e81427c57d725fc1f78f5ae3`  
		Last Modified: Mon, 09 Jun 2025 22:08:44 GMT  
		Size: 83.2 MB (83157558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ed5bceb724fd0fcede7d0628b3f91d09bc1243121fe1669577b0db9019097`  
		Last Modified: Wed, 11 Jun 2025 03:24:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0a818ecb131eabaca0bc1963ce66589d13ca1c38303151366b300aa44f0e4afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e506a707567eb5e6b0a8a5bc0b06df64572f81a411a8c96868f030029f8e87f1`

```dockerfile
```

-	Layers:
	-	`sha256:c98ae5a61e0538173949d1e0008a07fe5e6c8ba48cbaee51a05fc91df6d4306c`  
		Last Modified: Wed, 11 Jun 2025 05:23:15 GMT  
		Size: 10.5 MB (10487389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bce456f3600445d9a0b36c0511c6622208f5befd0a01ff7161d72d315290d89`  
		Last Modified: Wed, 11 Jun 2025 05:23:16 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:3b9a4196663c72eaeda61879245c782e1ffeacb7a2c45016aa5735f5d8bfcb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272254157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628d1d1579ab9e7088a1dd1af9b0f35ded85ffe79a8a6d862d3b3ecc8054f68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0a248bc7fbf888bccbf6729078aec3b1f376d1d95c8ee77854eaa13fe0986`  
		Last Modified: Wed, 11 Jun 2025 18:27:12 GMT  
		Size: 66.2 MB (66208380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbba4495ee849a32b1868921c9f94170c36c552299b715ecef8d63f110b4be`  
		Last Modified: Mon, 09 Jun 2025 22:17:51 GMT  
		Size: 80.3 MB (80255849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21f261e19e03ede56ce5e828c5ae89a680cfd46d206b692b410e5893b298cfe`  
		Last Modified: Thu, 12 Jun 2025 03:34:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7272b0ce2104795f13630fcf30172a0f17a375a0287d4886ab837f03e4982c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c48e8287579357bb4ff51d969acea9166039068d34d127c869c022bf548e66`

```dockerfile
```

-	Layers:
	-	`sha256:c0f040084c86b06e6b039c8d2e407bdb18e36c944852fffc7e6fcb9ab47ed989`  
		Last Modified: Thu, 12 Jun 2025 05:23:20 GMT  
		Size: 10.3 MB (10294103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e944f9401ae6d42a8c31720dfa567d173eaba0dd1b7d5b27fd84cc5a933b18e`  
		Last Modified: Thu, 12 Jun 2025 05:23:20 GMT  
		Size: 27.8 KB (27783 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ac3055ccd2cd615df942ee420fd2af5696090081af041c9e253a3ec7d3e9edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301819783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f038aebb92e41e038aef0e416a04ce57be75b73c63c6355a186f0664ac0300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a17febfc3c309501dc6427821a98f0a207b994da4369bc17d53bfee0ec1e7`  
		Last Modified: Wed, 11 Jun 2025 23:08:08 GMT  
		Size: 86.4 MB (86425354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9018e4f62f0690ad9682f8c2f1f9edb62acf90f09cff841cc366e0feec33aa3`  
		Last Modified: Mon, 09 Jun 2025 22:08:25 GMT  
		Size: 79.1 MB (79141010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fe4a8d6af683cf67bbfdf892d21776e6aa87ff17ee28c1a21a5fb7e85637a9`  
		Last Modified: Wed, 11 Jun 2025 23:08:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:20b5d2c26576940c79b9d4d9a31f6eb6b28e464ee28c87c94c9328ee4472a93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcf313a5b237f500ef4672277701f0c03cd95fb25cddf92d1ca1885624b36cf`

```dockerfile
```

-	Layers:
	-	`sha256:562ab4dff474437bf5ac9fba0408a6350bbf265ad2d856e5ecd1f525c56df3a3`  
		Last Modified: Thu, 12 Jun 2025 02:23:23 GMT  
		Size: 10.5 MB (10515237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cbc16681d49aa30b156978c221712b6dccb785103d3f58a215d91f35c5f80b`  
		Last Modified: Thu, 12 Jun 2025 02:23:23 GMT  
		Size: 27.8 KB (27819 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; 386

```console
$ docker pull golang@sha256:709eb0abe91e3a2d029f425b685baab747790736b383bd30e3f400d8d7fd1b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312228875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05a223d164ed6350708e49509e0e0e19faf46717a90b25d0af3eec51735be75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f05f8b7fa9f11ce4088c4c2e37eb9df42bb9cdc437ed8b9c5379cd2306a6fc5`  
		Last Modified: Wed, 11 Jun 2025 02:20:48 GMT  
		Size: 89.8 MB (89774571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b4524b05c1706d1b72e8575c65245c59334a3e5a6eaa54af3aee803a8d9ca`  
		Last Modified: Tue, 10 Jun 2025 00:21:15 GMT  
		Size: 81.9 MB (81895727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0a4f8f0b10e38cdd3b532818352741ccba053078309a0a960b113997245119`  
		Last Modified: Wed, 11 Jun 2025 02:20:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:460640cd545bfeb4097ee198c2fe18384d2f7edbcf5503af0803895dcee1d047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754e7025076d3f44aa7b25e77b0cf0ab2bbd168c94df28463099a3edbc6003a3`

```dockerfile
```

-	Layers:
	-	`sha256:4d43cb3c10c722b08b83e240e4e3553fe1ff6d26784ebbbff4736d20ce0a405c`  
		Last Modified: Wed, 11 Jun 2025 05:23:36 GMT  
		Size: 10.5 MB (10466967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13999d5b2d180b92ec4b87e4eed473c955b4b9c8bcdd045447430fd959b42511`  
		Last Modified: Wed, 11 Jun 2025 05:23:37 GMT  
		Size: 27.6 KB (27616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:493e5b5fba9e8959109765603af167d3f740c990c7965825c5e202c7ada3c107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283527041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a724e212ea57809f1dc626d5327b0d46b8f433bb8a6b0de3616275ca4adbf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492b77d6bf957cded76e087bd45cb2dc99a21e61d8bf5a9dc72814542a2ff45`  
		Last Modified: Thu, 12 Jun 2025 08:23:42 GMT  
		Size: 69.9 MB (69945632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d3af848d50d9ea323fbb4774788f4092106f0c455c6c060c00477678619fb9`  
		Last Modified: Tue, 10 Jun 2025 00:52:23 GMT  
		Size: 77.9 MB (77898347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708243c168ac0b52b702fb835b1b8d5b72ea3b406d06966ab211a15a40541e0c`  
		Last Modified: Thu, 12 Jun 2025 13:09:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b605027ff8f4910bb3e39b3f0c38418a6857cb104aeb0289168655532526c5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd18e4ddfcf2d5ce873c044705f5bdcb753e358800412d6dd9eccf07ad5e098`

```dockerfile
```

-	Layers:
	-	`sha256:e0557931c3b2a83381f33bfe6ea413b0c0d86a13b4fa130bd818aaa589551fd4`  
		Last Modified: Thu, 12 Jun 2025 14:23:41 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:d010339fb3dd37365a50f679e716caf24f2947bb84728ba7fb743eaddf424dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318644125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdc0042422485866a2dda13dc777f102e8f822880f33aad743924a354384024`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04a97584b773cb2e3f5ef36cf5fd266e7a5329383a4acadeef6edef21349bf`  
		Last Modified: Wed, 11 Jun 2025 23:31:25 GMT  
		Size: 90.4 MB (90369172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4f9b76482449b9bca3b26be2809c20c3fb3bcd128ccaf98bfdc365ba993990`  
		Last Modified: Tue, 10 Jun 2025 00:22:53 GMT  
		Size: 80.4 MB (80440317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e6eb40294181eab51ab391dbf2e2004de48539bf6e65fd5c61ed1e1a72678`  
		Last Modified: Thu, 12 Jun 2025 03:16:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b76d8623365df6e18c01c9dc02c93fd07edde34d621df540893cf56948cdc26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b067370eb50f9ab301246aa7798786c0829d14889d94b36bdc6ddf697ad12a57`

```dockerfile
```

-	Layers:
	-	`sha256:c5658fbc7f944bd6d138ef7bb5b5bf67d14d9e4d663b44e7536b46c34be4fa64`  
		Last Modified: Thu, 12 Jun 2025 05:23:39 GMT  
		Size: 10.5 MB (10459872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bfe3ee1659295f66b3af0181b0ea9a1b6e7956543f4020254f80b2f079f0a95`  
		Last Modified: Thu, 12 Jun 2025 05:23:39 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9cced8fa777b06a3fd8c75420fb0fcf21b04bff1a47908f5ce7fea6646815e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285300414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8294eeb4ac231b910d61746ab64fcb50974953a77ceef61552cc324580f7f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c056714c54676358218cd75dc0c5d3298e3c0e7e53c127fdefd363c4380d95`  
		Last Modified: Wed, 11 Jun 2025 12:03:11 GMT  
		Size: 63.5 MB (63498247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d972cf1551f655df3a01c76dc6db428d58e500c24a29c3c7b92136f0ee2d23d`  
		Last Modified: Wed, 11 Jun 2025 11:13:11 GMT  
		Size: 69.0 MB (68957331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679ab8e1a4e56924d30bbad5d825514c9915a27f62262c60df5ad10b788d75f2`  
		Last Modified: Mon, 09 Jun 2025 22:08:55 GMT  
		Size: 81.7 MB (81680268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baf9026dd1eae02eb44e688686f9b3c2d5d614c500ef9241adb4640e53b1b0d`  
		Last Modified: Wed, 11 Jun 2025 18:38:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b9dff36700c87ebfcca4660ea11d1359e6840c79b92762e385dc663e326b351e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10346806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f727f92e6fecafb709628f4f623609a366836f5f51b4ec32c15e49ebd592c1`

```dockerfile
```

-	Layers:
	-	`sha256:84902b67e09d01c884045d877db5c169d21f4d80d4c01299c3cd5543cccf2e09`  
		Last Modified: Wed, 11 Jun 2025 20:24:22 GMT  
		Size: 10.3 MB (10319147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ba764f879173bfeaf1712371d58ff09c42f3578fa3da969c5a660b2d2120ff`  
		Last Modified: Wed, 11 Jun 2025 20:24:23 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json
