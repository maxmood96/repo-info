## `golang:tip`

```console
$ docker pull golang@sha256:7310d6e7cae063d3bdc13a7ae9aecc15456ce7e9383dddefa25be177914dcebf
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
$ docker pull golang@sha256:2402b2a09fb293e9040282d191f9f24c77a335181d101be4eddc8cb360cbec5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312458037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9870304d103ed732d39b396f5b37876f1a4c8d8bdcc514831a13872b9fc147`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:4ed99bad1d974c902851eabdc47d99abfe540fe95df411d9f5738d89f403b218`  
		Last Modified: Mon, 23 Jun 2025 17:36:25 GMT  
		Size: 92.4 MB (92354956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553943e6d01c9acd45d693254df521c1e8dd5f2af99f49bd85cc6c44cbb632b8`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 83.2 MB (83193149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c2e874612543b8e9d2970f32d780a420f5b8510a85e9b4020418d582f0d759`  
		Last Modified: Mon, 23 Jun 2025 17:36:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f925f0fd299d2f6208d966fb5283effeaee51bffe1f7f2cce6a64c10972d7a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3785d68ad59c0e9945a0df2a3c1fc2d8b703509c72690806734924fab82509`

```dockerfile
```

-	Layers:
	-	`sha256:8cf9718b33d7a691e8f5656a3f37a0657bd9e8af2297e6e9bcc507f7a4b281be`  
		Last Modified: Mon, 23 Jun 2025 20:23:53 GMT  
		Size: 10.5 MB (10487389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7357cccb3e9a0ac957813ef263ee6caadf45e82c0d345ff1cd682421b17c2747`  
		Last Modified: Mon, 23 Jun 2025 20:23:53 GMT  
		Size: 27.7 KB (27658 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:2bb99c0ba3b748bbb443f6fec005ba1925d70cfc5b7cb481aac93abd8a1d1d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272274750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaaabfb3be5a77f7fd9d956e2eda10df8cb9722dc63a5a8da355cbf4f3c1e3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:9f2c23b36edc595b524e22ac037644488010f16b51c7c2741b5377b0b7319594`  
		Last Modified: Mon, 23 Jun 2025 17:37:09 GMT  
		Size: 80.3 MB (80276441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10bbfc7839c0e56df7b9cc2c830b58e4ef991186eef66170aedb7bff8487f34`  
		Last Modified: Mon, 23 Jun 2025 17:36:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:63649ddb53c85fc6310c9395464064b70557ef03b64b8c024eb781fce87a5ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91414b80495857189c33ca1607549c158f58aabee7fc9ca8c29f06aae65d2163`

```dockerfile
```

-	Layers:
	-	`sha256:069e86552dd996aeb02be31400171b169ace02b695a79a440da070e7d1c42420`  
		Last Modified: Mon, 23 Jun 2025 20:24:00 GMT  
		Size: 10.3 MB (10294103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7039b663fe7186f804364dae41b6464c422a35c1481761b35023f94703b67093`  
		Last Modified: Mon, 23 Jun 2025 20:24:01 GMT  
		Size: 27.8 KB (27783 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c7c0bd415341bca3a03803a8096e8344fc26ec6043124910e7b19174a2f819b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301847187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a2eeaacce1886af85cc69237843a6b1ccf9d10869fec81d0df8b71763af289`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:c5b77692401f3ea137343bd9363ea145d89603d5742a3fff804ed8b3a2b6ef06`  
		Last Modified: Mon, 23 Jun 2025 17:54:19 GMT  
		Size: 79.2 MB (79168414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ddadf55f5bbcf73c9ea9c30a28ae6e7f304a176c9919a5ca815104d7e35776`  
		Last Modified: Mon, 23 Jun 2025 17:54:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7960bf71b8946fb911cc2cad231a5bb163b679eea56557ae4d8358bd9451bbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93019f9e6938f177455d3230ecb06ec5a9e0241261a9205731d6804e6535b12`

```dockerfile
```

-	Layers:
	-	`sha256:c39b001033a1c2f9a92e9e0e0f5106450483dae645f5180bdad9dd69e0dd7777`  
		Last Modified: Mon, 23 Jun 2025 20:24:10 GMT  
		Size: 10.5 MB (10515237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b26835b70bb57545a45f51956634f9a41f48c7033667a9a714860edb0409752c`  
		Last Modified: Mon, 23 Jun 2025 20:24:11 GMT  
		Size: 27.8 KB (27819 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:e3dd2eead26a803987904a00fa8cc4b6c494f78dbd933de2e5669ebd3ed72609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312261292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c894ede51f8046c045a9fd2538186f6064849ae34b589ab0103b9e96c3fa40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:f262b8183e5ffdbd13958fd3c3cd83cdbaa5c5762db98f428c2d413727767299`  
		Last Modified: Mon, 23 Jun 2025 17:36:29 GMT  
		Size: 89.8 MB (89774374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c3a68cf208e712d48fe5a3cca6178d38afd0dcfcac42ede03f6220d712b15`  
		Last Modified: Mon, 23 Jun 2025 17:36:27 GMT  
		Size: 81.9 MB (81928340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7491e6096ac15871bb7b885d51e990dad12b9ece53d36f06ca7be2cd6f6f3b98`  
		Last Modified: Mon, 23 Jun 2025 17:36:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:44c73621e0c0a59130df3e8735f31d5b70e1fa8479974dc6fe94d8c9a2252334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253a7e12ab0ad8a6d1d44d3fc975188a1c0f7d0f0c7ddb96c506ec6bc8ce30af`

```dockerfile
```

-	Layers:
	-	`sha256:fe5b79bdfcd8b790debcfc804d9830a318f4126cf64cae55f2a654f42825c0dd`  
		Last Modified: Mon, 23 Jun 2025 20:24:19 GMT  
		Size: 10.5 MB (10466967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6271391fa40a86502f6b833c32ca0011fd9dd3f3c33e1312ac216e740d6b55e`  
		Last Modified: Mon, 23 Jun 2025 20:24:19 GMT  
		Size: 27.6 KB (27616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:ba469d1a808c20e41bd434215f0c85961245a28e7e6468b038dcc3e748000c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283557530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c1b29e76083f86a54f69894efb6f85e2a4f32c1ab464ceccb26d97fd232ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:c06cff9b3645e89e43bdd9c12cd42ee3720afcd0df12be5f9dc945f24a13dff7`  
		Last Modified: Mon, 23 Jun 2025 17:53:28 GMT  
		Size: 77.9 MB (77928836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e284d55d001b374708b20c741a753b9f5a386ee403eef69dbbb6374f471163`  
		Last Modified: Mon, 23 Jun 2025 17:53:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4eeecb1b952e85077dfb7d227a5de859db6c633a071a362e7f74a9def450ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f223b7ee28512c5e73b5c2e7e8bfcc6f4a76117c4824dcf00980de5e4d727122`

```dockerfile
```

-	Layers:
	-	`sha256:db8873229f1d939fad0fdf6c85c300bd1eb3d74dc383294b7f3b46525fcecaea`  
		Last Modified: Mon, 23 Jun 2025 20:24:25 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:5d23d09f5881f697d3716ccc0d8e10804c0a753d78979d46f4c291daa089d1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318666964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d64b6bdfc6c011928884881ccac2e88a70e1f80e44584386b5b1e63215522a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:a51f6a9436457535ac561521e5803267cfa96280c8bee442d726995d270b958c`  
		Last Modified: Mon, 23 Jun 2025 17:51:06 GMT  
		Size: 80.5 MB (80463156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2829bd85df58766c34e6fff185029fb4b393f51c61b3e612377e366b9f735b7e`  
		Last Modified: Mon, 23 Jun 2025 17:50:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:55b1ec4c27170da3a3c467ccc7280a77956e54dfb8445de19238bff1d71b4300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70257516e54c90263c9e498e1c840bd588a6428646db2e07738602b412a6f622`

```dockerfile
```

-	Layers:
	-	`sha256:bb61709d974dd1a697a1721d43ee452fe4036f6780c1599884496c57a99e3afb`  
		Last Modified: Mon, 23 Jun 2025 20:24:30 GMT  
		Size: 10.5 MB (10459872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2901c61285899e56eb7cec55bed604835c551c78c430c4947267ce44fb12731c`  
		Last Modified: Mon, 23 Jun 2025 20:24:31 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:0d7250192b96d76f8495e44905abf1eda8c05bc92ff262f4131a264432e3aff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285329155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2992f5374e450bfa71fd129c7928ff515d1da1a2cd53bd2c77405160f5dc6cb8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
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
	-	`sha256:87c4e9ad813ce53948d9016f3d50242da725640f347f8b2bb02b8db89e7d0980`  
		Last Modified: Mon, 23 Jun 2025 17:41:29 GMT  
		Size: 81.7 MB (81709009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb672e1333619d30046ff959be91ba178e30369a734dcf665091d55caab11ea`  
		Last Modified: Mon, 23 Jun 2025 17:41:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:76d871fc94ec461ccbeab41732e34ffc6eab3a665e82f53a4aa71ce253394da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10346806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d934c8c77787cf85dab10815844c8e549bd787b10c524b8bf3c2f015f9db8754`

```dockerfile
```

-	Layers:
	-	`sha256:b9320f66dff6e3bd31f686d2e60af5ecdac09c7d720eab94b47f1cb736c6676b`  
		Last Modified: Mon, 23 Jun 2025 20:24:39 GMT  
		Size: 10.3 MB (10319147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004846556a2037c6eee447b97372c7803af138024eb2c14fd4efaecc159eca7a`  
		Last Modified: Mon, 23 Jun 2025 20:24:39 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json
