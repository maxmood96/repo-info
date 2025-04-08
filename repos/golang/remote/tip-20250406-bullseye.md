## `golang:tip-20250406-bullseye`

```console
$ docker pull golang@sha256:14b453658a266847ee303ada4ddfd374dcae51f821d5b1d057519025c5f25c80
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

### `golang:tip-20250406-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:4702761d9f99e42f1d8d61cc9b0734728babb872bbb219e30d83e30de5b88bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336313972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c0548863aa386126f12b92f3db1c7954b555d2e78b3b70a71c71f5c21261b8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81325b5a8ac55eb1e30d55aa8624ae589097cd375904cdc30341d2e2998c531`  
		Last Modified: Tue, 08 Apr 2025 04:14:12 GMT  
		Size: 86.0 MB (86000808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc044b4e18e8d70a1ecc203412289673855869397177339cdff79099bda4d2f`  
		Last Modified: Mon, 07 Apr 2025 22:40:51 GMT  
		Size: 126.0 MB (126045817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d84ef1f6824a204f7d56d23e8677f7d8ab52feec1d1d46a7bf6048d3db76ac`  
		Last Modified: Tue, 08 Apr 2025 04:14:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250406-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ffa41959aee2c5a4faadae22d8f4329b1d08bdae5397062d378388e00e73e19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ca1b17ddc4342e5a6eb900292edf0bd6fdf8fde08c8e930560ee8e0a4d1545`

```dockerfile
```

-	Layers:
	-	`sha256:f025a8280c31b3524efcd58eec93e58facb426b665eb89f71e649548830047c5`  
		Last Modified: Tue, 08 Apr 2025 04:14:11 GMT  
		Size: 10.3 MB (10266343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e95b58d14b2f58179a62334b5e3d5f1347da27fa6f338b306561a565979ef98`  
		Last Modified: Tue, 08 Apr 2025 04:14:10 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250406-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:b7d3192e96bb00e4bcced86c85c5ade4e195096597492224d6f224688e09a533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300324737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef3f8076bdc259473c80476061cf08f3ef680f02de0dec4dd255a625c18f86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192ce451b4bc1458959a86a1dd55f46cf5148c4d3e016589a215f847b4e66ae`  
		Last Modified: Tue, 18 Mar 2025 16:49:06 GMT  
		Size: 64.9 MB (64922890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1290dc10baba6632fd5e083ce70494036c9bdcaeb42c9719e7ebc2bbe45fe3`  
		Last Modified: Mon, 07 Apr 2025 22:57:05 GMT  
		Size: 121.1 MB (121060891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ca0b05717cf5d62c51f595085ba15909b2b52c26749fd473b74abbd5d32aed`  
		Last Modified: Mon, 07 Apr 2025 23:00:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250406-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:168daa70d6430340893ccc0048d99de1c663e06d8afcccddb373d181d6556b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb87d4d681f083477222d557b52da54fe10f64b19c55a37d24194bef94b227b7`

```dockerfile
```

-	Layers:
	-	`sha256:f42ddf148b618b3b905c620ef394939935db6968d5b758c1d43a8da0743a1036`  
		Last Modified: Mon, 07 Apr 2025 23:00:30 GMT  
		Size: 10.1 MB (10070769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3073632250271145ef99f4e346d7fa8880f02fcbfb65e0c27936495620cc986b`  
		Last Modified: Mon, 07 Apr 2025 23:00:30 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250406-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:958fab45e7fd0936e7aae7cd7c7793d32638269686e3f40e1f4780793198f1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322805453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f2000650e6993211a5cd7c7b489e345ad6e76889cf12f1966ee7b5dea6588a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852072c6d90387d6d845e4f9e792adafa4579fd943cc48eacd0405192508786`  
		Last Modified: Tue, 18 Mar 2025 18:56:37 GMT  
		Size: 81.4 MB (81413745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c040252f366631b10d12c85c56edda99c15cbe025d4e4abe3b2a7e0736ae53`  
		Last Modified: Mon, 07 Apr 2025 22:45:10 GMT  
		Size: 118.7 MB (118743723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a6723d52e4d9c6b2a1ef9ccd332fc5d3fc88d236fc2d204ac20b990590f21`  
		Last Modified: Mon, 07 Apr 2025 22:47:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250406-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e0aa86c5372d961f218c46d1f9496cbbec78e5941ed8b601af265a6816a86401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9a8d3dd60d8006120a1522d1de20193634a05b23bcb8711c35909b9f917ea8`

```dockerfile
```

-	Layers:
	-	`sha256:8de69d46ed3880fda107e9faa68176e9dbc3722612129f49903ad20a06fb072e`  
		Last Modified: Mon, 07 Apr 2025 22:47:22 GMT  
		Size: 10.3 MB (10266001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893ac8b36a0f9a25a51e61c5dea4b40715b98adf6a73c593b39163785e517ec3`  
		Last Modified: Mon, 07 Apr 2025 22:47:22 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250406-bullseye` - linux; 386

```console
$ docker pull golang@sha256:701306941df1b983457eac96cc54d5852ccc69e654783ab33ebf610775af6d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338620760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae90f961a667ec28416eb6b72d47abaa86a138725452194ceec1afb14c2a8a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e7acde6705212f18af900a6b0c78cc5b1d37e0a66454795758e7a06a75b390`  
		Last Modified: Tue, 08 Apr 2025 04:14:28 GMT  
		Size: 87.4 MB (87426577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae3c30c1a3e04c667c09570d32c4fdc5fb10965c2ae3c7c8d16fb2e127e055f`  
		Last Modified: Mon, 07 Apr 2025 22:41:19 GMT  
		Size: 124.2 MB (124195306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9956403858ec96e7e2ae7b6338318bf57e6d23cf9d0ae012ca6ca04cacee8ea3`  
		Last Modified: Tue, 08 Apr 2025 04:14:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250406-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:3fa5e6328d91defedf2057217e3d9358c974f305a269282776704b1757f491b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea91016967bba8c75881ddb87c788442caeb4f714c97419b538364a12ebfa731`

```dockerfile
```

-	Layers:
	-	`sha256:925b43c11b122a434a214dd910a86eb8624fa9c734461a484b5e780bb4a2bfe0`  
		Last Modified: Tue, 08 Apr 2025 04:14:26 GMT  
		Size: 10.3 MB (10256134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97016052704484aad89d5f17d60a4008d5e001b6b0a0f65ac26afc9b2b2d15a2`  
		Last Modified: Tue, 08 Apr 2025 04:14:26 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
