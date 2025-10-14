## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:1eae009dd3885e21ef76e92c1577c6ad776423b798f5e16e6f2425f8b290ff40
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
$ docker pull golang@sha256:af494ba338c342b103f66191f53c65d7840178107b8ddd9073eb389fe9ab7c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319944730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56eb0dec344869e69e4064e836f80778665be01dd261006dce6ed93edb80fe8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8128e4c16b0b9979543f149a581d9d2432c54d72a3eb8154e4daa816e56e27bd`  
		Last Modified: Mon, 13 Oct 2025 23:11:14 GMT  
		Size: 92.4 MB (92401891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5533a24a9e37fce0b0e949796f7edef8b1aecc8af44711d2767f0566cd2c9677`  
		Last Modified: Mon, 13 Oct 2025 21:02:56 GMT  
		Size: 90.6 MB (90638837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b658aa287dad55ae2a75ebaa9940c76ceee874d7c742917925c0cd7cb29ae67`  
		Last Modified: Mon, 13 Oct 2025 23:11:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5da62c22baa84852641c65194b48228031c2884a925e21a1ca9ab1396a63a12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba38e0d6361d96011426dd15796660fda8feec267e3aee69c176743f886be9be`

```dockerfile
```

-	Layers:
	-	`sha256:519c272d1eee5aaa6e58299839d7575692e0a07abecf3da7c4f58fec9025640c`  
		Last Modified: Tue, 14 Oct 2025 02:25:00 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa7f3860e83bc5d10b508b009acae57438856be42cadfa8a84a9b7775f969a8`  
		Last Modified: Tue, 14 Oct 2025 02:25:01 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:95b250cf5777520bd7c8cf8758bd03c91fae613abed8ce06b5beec3de6b97efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279108448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0744e0a97f4ad6d14bbae19bbb1f1dbd3b298e4c354a81b15b92d452d4efef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec7e66bfe48f30b687ac3edb8fb3a7c9ae8843bed67b4b693e8412e52069079`  
		Last Modified: Mon, 13 Oct 2025 23:10:41 GMT  
		Size: 66.3 MB (66254627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b3f77f198194af8440022630b5f3555d19874bc1b8dcfcdeb4ff1346ed16b`  
		Last Modified: Mon, 13 Oct 2025 18:23:46 GMT  
		Size: 87.1 MB (87074499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff393a1ea0e7bd587165e01246db5dfc5d843e09275b053ec111378065a78b`  
		Last Modified: Mon, 13 Oct 2025 23:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:af800567f271117028082657df93e45707a27211192900b81ef30cc20e6d8d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135926d0419fd1df80ee2b0491b7bd9e054b4e25ae4b36747813f8750c6feba2`

```dockerfile
```

-	Layers:
	-	`sha256:eba26fe6995ab8f008557c4a6b0720191380c08281f028f84994f81b5e7863ed`  
		Last Modified: Tue, 14 Oct 2025 02:25:09 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5fbc7923171996b223e4796eaaf52a123639e6e9f1ea6191dfd0492305693f`  
		Last Modified: Tue, 14 Oct 2025 02:25:10 GMT  
		Size: 28.5 KB (28540 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:696c6d98b6d87c6cab7e538faaeabc3123692bdcca95ab64e5e9ba79051d6bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308838990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbcec4166c81feee543891badae18f4301c1fff5b81983cc162d271cd972b75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158af010a5c1e134b368795d84236f5445c55384a7c3369b3b566615ff646ad7`  
		Last Modified: Mon, 13 Oct 2025 23:11:31 GMT  
		Size: 86.5 MB (86471882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad87b7b196d7850da55968ab4ea8d2e74337f796a2dda3e1e502c848906a7`  
		Last Modified: Mon, 13 Oct 2025 18:26:56 GMT  
		Size: 86.0 MB (86042092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e0a3f5cb456cd3731c57d104b112ead6dbb561f042416c65d8d441df8362f`  
		Last Modified: Mon, 13 Oct 2025 23:11:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1d3ff5469afbf0974e0e614f1b6adf24414c0bd40867cc1aef0b18a17f189066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2f4b08432d6928ef4e1019a371cc52a8b67fe81d7f45423a3f85e9535c0302`

```dockerfile
```

-	Layers:
	-	`sha256:85cf09e41795a7eee3a63791a456eb2465e03096aa51b131cab83086e5287903`  
		Last Modified: Tue, 14 Oct 2025 02:25:17 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3aa4ac182f321bcc67f8d8a66d6088573fadde6ad00284e7ebf2725be7613e8`  
		Last Modified: Tue, 14 Oct 2025 02:25:19 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:f14a9a0cc920bd9e2df353a2aa2cda08d0bb4f7671c7663060aa5fe03623176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319236359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63549faab5c65ccd83aedf09b4e722d0235ec12051b554f90f59797631db4c1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de08876415c14bb5e0aec9f6563839a0bab0d1ad10d2f06ac977312aa2ec04`  
		Last Modified: Mon, 13 Oct 2025 23:13:14 GMT  
		Size: 89.8 MB (89823384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc457dc23d2f2501ae16881398a5b91dd66079c5042a578bb1e723668e7c145`  
		Last Modified: Mon, 13 Oct 2025 21:20:42 GMT  
		Size: 88.9 MB (88852096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4d804668c09767afb00e3b406898abad99d900d8166148666dd9fa5d246def`  
		Last Modified: Mon, 13 Oct 2025 23:13:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fa79f3d33483164f5981f2da9f6c8325080f5fba8060e39954a40e29da80b7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8028b65755afc49ab860ab1204c9c6a836a43be0826c8f06ee57e549589e07`

```dockerfile
```

-	Layers:
	-	`sha256:f215112cdb47ad59437c20efa1acedbadc9dd39c0f77d61e0e773f372e3c5ddf`  
		Last Modified: Tue, 14 Oct 2025 02:25:26 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d258a1098f4f5caa3716fee1f4f7be36e5ce4aeed44766cb10de2c93e5507cf4`  
		Last Modified: Tue, 14 Oct 2025 02:25:27 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:b9bab26e14f6b5d2c67c711018a1c9055f02e08c648a2f3e869549e53c97f47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290407515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdf62acadc55a86c426751884b5e3dfe828ec00799a774890d753fd7257aeb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39be94b43c7b8fee0fdcf795208f91323ad52fb7cc0e21f16aaaac555d61b8`  
		Last Modified: Tue, 30 Sep 2025 22:53:31 GMT  
		Size: 70.0 MB (69997146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2278ae8aa2fd11576c5ca1eef2595396b385a8eb40d5115b743e671a726209b1`  
		Last Modified: Mon, 13 Oct 2025 18:40:42 GMT  
		Size: 84.7 MB (84728796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d66b2b1f451f8f83be259d3ff8a83bfa6b4ad1780b79e4758a802e709aacf0b`  
		Last Modified: Mon, 13 Oct 2025 18:40:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8003c98bcb8e37cd8e504af6cbf8d21574b4f5a8acefd636edf4b25107186296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2a15cae925a6e28a511c41c645fb506b93c1c8a399755a85d5c931bbcccf5f`

```dockerfile
```

-	Layers:
	-	`sha256:4511ab5bf671f54c8c62f7873c46cd0a981dbb4ce6c5d00fc4e895e8e91a2e4b`  
		Last Modified: Tue, 14 Oct 2025 02:25:34 GMT  
		Size: 28.3 KB (28283 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b6a0d76b5d65fe207b90768d7d1342589541ca4cfbf9b1c533057e236581232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325700836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b580afd04e9e547e94f70278ea88a65c19850fd63695d9f49215d6fc915b7ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc7393f12c50be43563a663d899f76ad97c089e8eff687160119c7058ff4c9b`  
		Last Modified: Mon, 13 Oct 2025 18:29:15 GMT  
		Size: 90.4 MB (90417562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb280635ff73067e450776ffb495ea1ad6245c60020ec72c47db59cab52504`  
		Last Modified: Mon, 13 Oct 2025 18:24:19 GMT  
		Size: 87.4 MB (87441889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a007ce122d8a235edf37f7fabcba8758064fe0dd473ab37132bd73d1d3ff8d`  
		Last Modified: Mon, 13 Oct 2025 18:29:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0321642ab0a888319525e6b07622dbd7ea82155fc951a6d2004fdbe639906443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f90751ac4056cbd90cca6b77cdba104a3503482ecfc75e67ea0b66ed5549720`

```dockerfile
```

-	Layers:
	-	`sha256:915e297b90c7a1a314a4db4735f3a3253002e6ce5b51ae6d4f310c0c1bc4168d`  
		Last Modified: Tue, 14 Oct 2025 02:25:39 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0b9f99263444523f6fa6de7a141b3fbf7b970af25534bcf34f960128941b07`  
		Last Modified: Tue, 14 Oct 2025 02:25:40 GMT  
		Size: 28.5 KB (28475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:821a9eb3fde59858ed77c1e881e0dcb1ac23ad0bd7901e2aa0349941b7d02175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292461182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8051b3bdcbd477791d43497ec75178e20216c267cf0df0581db1e2818afb46`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4dbf2eab022c30a4f1ad0d69bb0be8e9a7b59d1d848c5eb4bcf43acac22ef`  
		Last Modified: Tue, 30 Sep 2025 23:54:17 GMT  
		Size: 69.0 MB (69006320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9327917e2dddfe4111d470e54a510bc92320cf661a5e14b0ac90c62acacad6e`  
		Last Modified: Mon, 13 Oct 2025 18:22:35 GMT  
		Size: 88.8 MB (88792191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6b0afcb98c443477374f293a937859db74aef395f3a9e319f6b2f2340883ca`  
		Last Modified: Mon, 13 Oct 2025 18:32:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:644245b50de7f4212056b443a3fa0d5e3a4f6f18515c18a42a2baf78a0a1689f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebf12e8d6adccd6cabf571691cae4e52d347f1e7ccc3ae35e43cbf75c78b7dc`

```dockerfile
```

-	Layers:
	-	`sha256:a1357ed372bb4d0dc6a7abc27be9ee04894c06867a1c172399f60656b1c4d34a`  
		Last Modified: Tue, 14 Oct 2025 02:25:48 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd35ad073de62e1fe1b2b0f9e1e6c65fd5ad355855685fb2d66bf181acf2f8e3`  
		Last Modified: Tue, 14 Oct 2025 02:25:50 GMT  
		Size: 28.4 KB (28429 bytes)  
		MIME: application/vnd.in-toto+json
