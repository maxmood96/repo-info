## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:3d99140ece58ce94929d118902ae459ff23b8980a4d3c7dce106c9779b22116c
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
$ docker pull golang@sha256:9d1b41ec88cf511cdb941d0d1f8fbc14c299b79a2cf0b8173967a7b432cb2573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336110014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96807d003a7365a4e270957a6695a1fa03f39d9cc1b344861e7eeca0ccd22d73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6894e4e0bad9bfe3bb7cdb1da477418aa8139a8849893360666243be489b951a`  
		Last Modified: Tue, 01 Apr 2025 17:13:43 GMT  
		Size: 86.0 MB (86000897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdcf0ac50c31370559153f24cee269e765f93f7d9caa55e2923550ee66d79`  
		Last Modified: Mon, 31 Mar 2025 17:35:08 GMT  
		Size: 126.1 MB (126057009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1332644f21d5550a5ce7b01431b44fbc07e5f43eb724c89038192dc7381e11`  
		Last Modified: Tue, 01 Apr 2025 17:13:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:dfced00e85fc732e04585fdecaf81b25918c74de08122e929be0fa3bc2228ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e9f30e6198bdfb3e9a157fb30fe1dc7ade1b64c733b5642d9c60251b2f5e38`

```dockerfile
```

-	Layers:
	-	`sha256:baf97bcb6833b4a502a8ea3775a66b3e102dc2c37581e18e7aac963d3b454f5e`  
		Last Modified: Tue, 01 Apr 2025 17:13:41 GMT  
		Size: 10.3 MB (10264429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb5d31debb9ac7e6a5528a0f06cfc41e9fc218f382854e3fceadf2636137509`  
		Last Modified: Tue, 01 Apr 2025 17:13:40 GMT  
		Size: 27.1 KB (27060 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:8d7412116dc181924e5c369fd2031e77eb9e126e839b10282e6d3a9b0de21171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300254343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1958dadaccf411f7ebaa298b55aab30c9ad9e259cb8ca9ea3eba90f5261e88f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:5df465922d4d37689f205f8db79322885e1b2a4fcb76bc9411e873e87dc4d228`  
		Last Modified: Mon, 31 Mar 2025 19:49:55 GMT  
		Size: 121.0 MB (120990498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c329c7b5153305a69ebf9b5630b2d6333f38e9e495e0944e07fe9b9288a5534`  
		Last Modified: Mon, 31 Mar 2025 19:53:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7f2d79ffee13bf12a344c68d57d2a00c629e4211e5c9fbbc3db76a759ad7b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128965a13ad0a40260595e644f27a3093f0191de1ea9d9213dfec888be71b11`

```dockerfile
```

-	Layers:
	-	`sha256:150726ede89c0e326cc09b99fcd903a23afdf19d1374a058a41bcaab8cf4a007`  
		Last Modified: Mon, 31 Mar 2025 19:53:23 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39de4962e6bd21d8a872b3491b6dc74d13ef50273d205e71ceb88dd414ccff77`  
		Last Modified: Mon, 31 Mar 2025 19:53:22 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:251da55adf94c29928ee914dd130abfa61988c1d33772901ef1c831198242835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322666084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf2426d5b4f1a898028ebd3c049cb69c8de30a66f9e23b6ccba60ee04775a82`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
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
	-	`sha256:15331666df650886c34693df6448a24027e3a0aedd81057f599d0c56087566f5`  
		Last Modified: Mon, 31 Mar 2025 17:54:53 GMT  
		Size: 118.6 MB (118604354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9451cf184a259f3c92da5640d0469867f48871a2c45cde4fc9dca2aa614c2ad`  
		Last Modified: Mon, 31 Mar 2025 17:57:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1bad6dc753349405e95c2ad9dc88ab61bdc57c03a7a282bd0b041a844eab0aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061407434495fcb468ecab3b8cbb963972118b7695bf39fe7f7b60253429682f`

```dockerfile
```

-	Layers:
	-	`sha256:9133969e24814bf4fdb28d366eb1d49c110248248d83f333159733fce7708fd8`  
		Last Modified: Tue, 01 Apr 2025 17:16:02 GMT  
		Size: 10.3 MB (10266001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35c503c6aa7bb25a6ecfb57cf3f0d529d1aea09a339b8f08f9a8b027604c7c5`  
		Last Modified: Tue, 01 Apr 2025 17:16:01 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:6678a55deaaf4ed1077420df8fd5a603d01babdc01309cb3d8fa0e16a0bfa697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338343970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2574da9d3485bf857337bd749464c0a5866db031c50329adb646eb34ebe63d2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c2eab8b6f365228928aad3bbb42fd90b5478d79bd93115b3cc56284271adac`  
		Last Modified: Tue, 01 Apr 2025 17:14:31 GMT  
		Size: 87.4 MB (87426505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20357d85d18b3e3e63dc269591697947f7bf020ba7021f1f8a7b1b769a804fe`  
		Last Modified: Mon, 31 Mar 2025 17:36:49 GMT  
		Size: 124.1 MB (124146637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332e15615e6f2febf5eb6d6927bb69f87c1a40678883beb27dd4701001a4070f`  
		Last Modified: Tue, 01 Apr 2025 17:14:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5e4c95a6caf978221b313f580db78b75943284321bddc218ccedde5f087acc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd39410f3df5b2917891a88f349266a0eced0b14499a961c2199d1b4c616ea2`

```dockerfile
```

-	Layers:
	-	`sha256:3b94a28f9d5435904df9ab9ceb6cc3d1ce3eb64528deaca239e485e465c57556`  
		Last Modified: Tue, 01 Apr 2025 17:14:28 GMT  
		Size: 10.3 MB (10254220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fca9226d810a8d341dafa0787dcab6496344604514815e5ab96c62768f99fb4`  
		Last Modified: Tue, 01 Apr 2025 17:14:28 GMT  
		Size: 27.0 KB (27026 bytes)  
		MIME: application/vnd.in-toto+json
