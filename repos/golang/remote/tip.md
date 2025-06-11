## `golang:tip`

```console
$ docker pull golang@sha256:7269e735f0e6ca0b2b35cf300a45d335eea3c613a60d6a80a01c7d35ba1e0730
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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:39470fc5889513bad73832a7760be1fa5b2963282ea99b63b432e9f9db94241a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272250203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e0dec9c1761d108e302ba7ba8d7904192d7243da9d687e799c0c9e2b28f00f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:cfdbba4495ee849a32b1868921c9f94170c36c552299b715ecef8d63f110b4be`  
		Last Modified: Mon, 09 Jun 2025 22:17:51 GMT  
		Size: 80.3 MB (80255849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00c5d753d09c9ba992f867ee0aa50a0c3cc88b75dfaa25b29deadd6898ddc03`  
		Last Modified: Mon, 09 Jun 2025 22:17:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:11a532d273ead6bc11e6186da1eb08c96889191f5f090a263f26cc384e582998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43d0d13a98b6556db7d853f803c1343a460c3e8f6b6e41a54634c88b36e0187`

```dockerfile
```

-	Layers:
	-	`sha256:ceb68023e1feac853ee1a03cf710d3349f06d3d43737a3e4c08c2ae4ae4b99d1`  
		Last Modified: Mon, 09 Jun 2025 23:23:36 GMT  
		Size: 10.3 MB (10294103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0981eec9c3f7d16b3faeffcc261d6e396a212b8893d219dc8fd9d76537043e`  
		Last Modified: Mon, 09 Jun 2025 23:23:37 GMT  
		Size: 27.8 KB (27782 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6739299f10e76b6c6eb0f7fe0745f59aca196db9f1527c663c1c86be8f9dd4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301790858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87a9de54800741847d92a978d99a10584148c01a37c5e599147a9ec5b9b3d4e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:f9018e4f62f0690ad9682f8c2f1f9edb62acf90f09cff841cc366e0feec33aa3`  
		Last Modified: Mon, 09 Jun 2025 22:08:25 GMT  
		Size: 79.1 MB (79141010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516510f64bc68aa745299de17d9be1acfd1b37165a22717b56e18486bda5f786`  
		Last Modified: Mon, 09 Jun 2025 22:08:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d13245a24b715e378a2b5e11158ca878a9926903f07672d54f1f80017e0242d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086ed887d0aea306d4c8bc161d0f44883cec7401c9b93062ab0a4c881f484a0`

```dockerfile
```

-	Layers:
	-	`sha256:69eb0bc20a82fec6163ef0b952ad0c76fcd9c8ca907ca6ef17ae402fea9f1042`  
		Last Modified: Mon, 09 Jun 2025 23:23:44 GMT  
		Size: 10.5 MB (10515237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24af529c993d8ea3335a03b5fe745c80c5638dd7dfb998121ea29c1760ade75a`  
		Last Modified: Mon, 09 Jun 2025 23:23:45 GMT  
		Size: 27.8 KB (27819 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

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

### `golang:tip` - unknown; unknown

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

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:cceed687a28ec129a2ed02390df90bbac12b17075b1efcf8f6db31be9f831de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283525526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d593649dfb9bc225136b2a233401491f2959eb5c22c5eb8c5ebf4d731291ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:a8d3af848d50d9ea323fbb4774788f4092106f0c455c6c060c00477678619fb9`  
		Last Modified: Tue, 10 Jun 2025 00:52:23 GMT  
		Size: 77.9 MB (77898347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b159a39789fc955c04bd00abbf5a43b8c428adae6dd844cf3ab5d077bce06e`  
		Last Modified: Tue, 10 Jun 2025 00:52:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:39f55f994ec1b20819e15676b832db27e96162a46e69fd6d468c7e14844677b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5f6836138d77d8cea60bf477ba4b55cd3acadeed2659f0a9b62525e5c7009`

```dockerfile
```

-	Layers:
	-	`sha256:cb9200466a6534abb1b96e3d0553806701427d05437e3b023bd5fdbd0c8b54eb`  
		Last Modified: Tue, 10 Jun 2025 02:23:32 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:82f7f0fbc5a1273dd4873b5b046269a46cc5e741f0b078a88f402cccd1bb1657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318623789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d6868bdfee6082237bc7dd19f3d85cb0dafa7b96c6fab0ef2b038692d094f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:db4f9b76482449b9bca3b26be2809c20c3fb3bcd128ccaf98bfdc365ba993990`  
		Last Modified: Tue, 10 Jun 2025 00:22:53 GMT  
		Size: 80.4 MB (80440317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8617fc2f1dbe02117d28e2590cd5d4b0527d74db4b10965404fd514a5ec199`  
		Last Modified: Mon, 09 Jun 2025 22:09:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6f4e17c113ab9d8fcef8ad2932f2f076d290344f3fb561fb274390baa1020fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791c49517eb7bd2e216dc45c775c891f1e9ca69a7d7e7caafcdbea0d8e19128`

```dockerfile
```

-	Layers:
	-	`sha256:1b802f6eaf786d25606889ddb85e72fe907d03d5f867a64fb7098423e8b6e32f`  
		Last Modified: Mon, 09 Jun 2025 23:23:59 GMT  
		Size: 10.5 MB (10459872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74e42a1c1941da25295850d196346dbba9141b221bcf27d97427754b94c4a2e`  
		Last Modified: Mon, 09 Jun 2025 23:24:00 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:5477c18d4c2de7c05ca164510bda9ffaf0ac13c5d2a51bc23292db8fdb1d2e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285281343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bce1eb7b9522c8d265c525b04c2797550c732a6fe3d0cc11f3a0fd74838be1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:679ab8e1a4e56924d30bbad5d825514c9915a27f62262c60df5ad10b788d75f2`  
		Last Modified: Mon, 09 Jun 2025 22:08:55 GMT  
		Size: 81.7 MB (81680268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c40da347e768c56ba2214345a55f4c48e186f11e29b7d7537382223062d7c`  
		Last Modified: Mon, 09 Jun 2025 22:08:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3ac46e8f2753ba265173dd922424c359b49f1f99bbac51a395284ea653db2015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10346806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c243c2ae5487aade9c2a75057ef703c0a08acfd079cde07ca8072b115287ff`

```dockerfile
```

-	Layers:
	-	`sha256:4fa48cce564253747c2008148c699a72edc5d365d2dd6647e1c629cb2dd64c9a`  
		Last Modified: Mon, 09 Jun 2025 23:24:07 GMT  
		Size: 10.3 MB (10319147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ee6e4b42ff9a67e8f67af51c7d57d33bf82d26b807d0b81a7f0b394d7430dd`  
		Last Modified: Mon, 09 Jun 2025 23:24:08 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json
