## `golang:tip-20260619-bookworm`

```console
$ docker pull golang@sha256:36d1096d190b8e694f70b4e9ac77a1c15a0c81e7b23e544de76a93e0527e3656
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

### `golang:tip-20260619-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:8583e6c7d83bc85a9ea963c1314e47d56291007245f71c92f8adc26c7297a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.0 MB (331991075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54075a14db2f3fc1d3d64a3c5efc00257bbf5fedfec1c2a70fd1eb476e164853`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:40:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:42:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:42:40 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:42:40 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:42:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:42:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaf204ab2ba2a5abf35cdd70baf16338a2cd33e61cc125208d72d0c381e80d`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 92.5 MB (92481370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ced9bfc2a0ce47376a0e89056fba2dbdc199ef992671e729f2b29cd85c5af1`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 102.6 MB (102559388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da86442dc9a1e09b15a1948c5de29d85837b5c2a883fd4d307f156da6442f30b`  
		Last Modified: Mon, 22 Jun 2026 22:43:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6412de43e0b42ceaa02ecb1b70a93a186982e459d83ee5b06091f6ae77543017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb5d04c82b5672347b5b682717c524b9ff3d9dd4985ca2e34744d8b5d1f2ae7`

```dockerfile
```

-	Layers:
	-	`sha256:aaa268ec6f1e14fea5c3d92cebef2fe1cb0a6f1480a020b60d535155bcfe24d2`  
		Last Modified: Mon, 22 Jun 2026 22:43:05 GMT  
		Size: 10.5 MB (10497073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1065d27ac0a5f1b5254fc6923f508f0db3fa594fa05be0c2ac4cb6d65d4cb81c`  
		Last Modified: Mon, 22 Jun 2026 22:43:04 GMT  
		Size: 28.4 KB (28389 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:4ed5a6ec2b2768822f4a96fea356d66f5eba40bc4694f6746411ad4717ce4e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290434800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7cf5a89f5555b6e64ac86513b5677b112ce1d8f50e306bee1bf56611ec6dae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:45:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:45:56 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:45:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:45:56 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:45:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:45:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f7c68aa5629a37a99de2287c5dada27c5ba0cd553e5b4f28471c0e6c213`  
		Last Modified: Thu, 11 Jun 2026 02:43:46 GMT  
		Size: 59.7 MB (59661587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0a5b775c24135768821753ea7930abdfefd3cc8d54d4c3673cb876a4d1429e`  
		Last Modified: Mon, 22 Jun 2026 22:46:25 GMT  
		Size: 66.3 MB (66338954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6c0ac1bf1a1f35e41966874d41949d2c8d30b471f4a54f05d28249cc12bc`  
		Last Modified: Mon, 22 Jun 2026 22:45:14 GMT  
		Size: 98.3 MB (98276162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92783259ed87e1fc5ed33fd76e6ffa1afa5df36fca1cb0c4e1aea39cf3532c25`  
		Last Modified: Mon, 22 Jun 2026 22:46:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3b454342e550ed1146f74eba2ef5ca1415240148b4ea1591642664083343153b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2a79a49dea6dc3e41a98d7ed0628a40d131c543395554c09d4fc6ea49e313c`

```dockerfile
```

-	Layers:
	-	`sha256:7b70ecd6e20b9f00a446548d8882b345a645cd1d2ad2ac458ee5d41414fb9392`  
		Last Modified: Mon, 22 Jun 2026 22:46:23 GMT  
		Size: 10.3 MB (10303769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb52aa25883bfd8286d1d48b14c80b981dd12f038b676114058b3583e7924159`  
		Last Modified: Mon, 22 Jun 2026 22:46:22 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c54db2927786e8b0b27a91de1268117ef6e77d7e9379fbcd9961cff071415119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320004428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767c6e3b5c2d83bf554a6a45084622c5b791eb586c6b1870db28730820745a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:43:04 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:43:04 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:43:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:43:04 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:43:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:43:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facee36d345fd6c445d32abfad05ad4ec65d96287f212cf00d5b64734bb029b7`  
		Last Modified: Mon, 22 Jun 2026 22:43:33 GMT  
		Size: 86.6 MB (86554635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4f06fe9b49ab2b0e448e3bb545bf0083fe0a192a188b8354bf30a5042489`  
		Last Modified: Mon, 22 Jun 2026 22:43:15 GMT  
		Size: 97.0 MB (96959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963094e05ecbc625f451b77b2fe1fb9061348a40ed5f03895de6201761bae19e`  
		Last Modified: Mon, 22 Jun 2026 22:43:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7997ac8d8c73101fb33370dea34b76409f48602b0e965cb85f888a7fc23a0e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99529c802615c8abbe16f3d58df7745e25d378e491d9bbf60c9940c3288c507d`

```dockerfile
```

-	Layers:
	-	`sha256:0cec0a7d73f1202caac19a657c1610757ba67db09491fc2490f33bcdf0471f33`  
		Last Modified: Mon, 22 Jun 2026 22:43:31 GMT  
		Size: 10.5 MB (10524897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7583bc3514befc254b7a9fff832c93a9c221c638740fa7d3ec42bf4a7ee7cca`  
		Last Modified: Mon, 22 Jun 2026 22:43:30 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; 386

```console
$ docker pull golang@sha256:87e5a42394e3beabd8c404f9b723806b666327aafc93f0a33448ac9bf01792bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330857874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454d471161c05c504230c2ee4f9f85f6b938accfbf40851fbb94ac788f7a6db4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:39:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:42 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:42 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:41:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:41:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1abb617cf69e81d401bea3de65ddcc50a1ac250e94890ec9ab61cb42a18679`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 24.9 MB (24879714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc4b12d03ab32e6c96be6bc5f6e0fc347b431b1f7686aa5f92f4cd1a5cccbc`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 66.2 MB (66244000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f17833cc373f891f2096f8c0dc90c8147e092437dcb288fdd227a835ddfcdc`  
		Last Modified: Mon, 22 Jun 2026 22:42:11 GMT  
		Size: 89.9 MB (89903801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675e2fd1600788af1a6ae5db185dc20a1f52bf11f13c9afd16f6795c307c09a`  
		Last Modified: Mon, 22 Jun 2026 22:41:13 GMT  
		Size: 100.3 MB (100338995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac93ac05baafb4dc6ff4277fbe332686edf969b60efad0371bcef77c819a9bd`  
		Last Modified: Mon, 22 Jun 2026 22:42:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b3d2bf24772032ae56e55b642e45708ddefc46738abf2e2e879c5e4c28000ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46b4065396a5344344a9a51202383e755a0f3e11c0e125e6aefe05f428e322f`

```dockerfile
```

-	Layers:
	-	`sha256:99fa3e14b6a038153b53ca7ae55ec5d2dd4c4594e91c57259baa8008e111d197`  
		Last Modified: Mon, 22 Jun 2026 22:42:09 GMT  
		Size: 10.5 MB (10476653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c8302f7cbe0af06f73a2dca1e71a8a8d76dd7c398202d035432050af2ce98b`  
		Last Modified: Mon, 22 Jun 2026 22:42:08 GMT  
		Size: 28.4 KB (28357 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ea58a99235fd33176bcdadcb74dfcfbdef0d786b567c81e14296af522daab202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301746966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fbad091c8e6e0413fc2933e298f0315e728f4e19e8ba91aa7a0a4c5f84a978`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:02:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 23:02:50 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 23:02:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:02:50 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 23:03:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 23:03:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c086020bbce3335fe9eece6ed9bd8f5bc1e45eed6579e81e64181addffb83`  
		Last Modified: Fri, 12 Jun 2026 01:02:23 GMT  
		Size: 63.3 MB (63315954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914bf280b1770cc8113eb19527c59fbb1740e0ce824cec4f0fd9e76670a4b8f6`  
		Last Modified: Fri, 12 Jun 2026 01:33:02 GMT  
		Size: 70.1 MB (70083997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae066d545f3a63cd46644c3d9678ba433b4c9aa20eb87d43ba7557e769fae2c`  
		Last Modified: Mon, 22 Jun 2026 23:05:12 GMT  
		Size: 95.9 MB (95930107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de9a358cc10d54f5f7fd269d1f737210b0b0d2587fcda60b5d39bf02fdfe741`  
		Last Modified: Mon, 22 Jun 2026 23:05:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c8d329c9aecc1f0f4daeaa5e81b5a513414893c7075dfa1538ead1facb054cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78633b8b0cbed93e7eca133416f243981a147bd8f78f2a5a563c59457864bb5`

```dockerfile
```

-	Layers:
	-	`sha256:c66160855df8e01b53cae55c62320f8e9979a04e3ef09839890eb0e8eb5a7425`  
		Last Modified: Mon, 22 Jun 2026 23:05:02 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:163e3ed6c69c933b8371c40d2ae17b6e23b225346cdd582a4f5870439b3f9e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337328086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466199ee8b57fa35592f5c8d89919ffb4a126c578c5f38052a9363987aac4d5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 10:26:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 12:51:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:41:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:41:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3af7c755dce470b1c44918153cc71bc2ea3bed1cbf9108bce1ad1d4579fb5`  
		Last Modified: Thu, 11 Jun 2026 10:27:04 GMT  
		Size: 69.9 MB (69853632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b4dd1efdd40c916f72d9997ac4a377751a99e14a9001e86722f39f10877da`  
		Last Modified: Thu, 11 Jun 2026 12:51:56 GMT  
		Size: 90.5 MB (90495547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70a3316b3905923ad611a6c49ef41a8febad5f35cea9ec0a2d4d25d3ae02c6`  
		Last Modified: Mon, 22 Jun 2026 22:42:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5250e629e55111bf3dadfbfcd8b0eabf7e6703d1ad75a3473a4a55e3eea4cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04a12d46f620fb39b447151d8f66f151648749666ed76548a994f7adbaeb37f`

```dockerfile
```

-	Layers:
	-	`sha256:d9b56348e0c52519ab5ff9d4d5a184c41e82aeec69028d75c820f3485b7408e6`  
		Last Modified: Mon, 22 Jun 2026 22:42:18 GMT  
		Size: 10.5 MB (10469558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1705c10a473990577df4fc30bd0fbcd7cf802699f12f16f56f901cdb531360b`  
		Last Modified: Mon, 22 Jun 2026 22:42:17 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:59dbed03ffeeb026d906721f67f8dd558ec3306e42a876dc9e73840051552635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304796572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c908d8f5bb1119b3f06371e1896fa2de3024427edbbac263a5ed5ecc770c638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:44:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:44:37 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 22:44:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 22:44:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0f0bf9684619796dace2f15b323a1fcec3fdfd4a5712e33f82ae28ed815bf`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 24.0 MB (24038950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33cb3e3ab28182d2640ab8d60069099e6c4d1dd9ee3f806d20e366f1901797`  
		Last Modified: Thu, 11 Jun 2026 03:26:38 GMT  
		Size: 63.5 MB (63498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c669866eae6f37d02e4b465a54f7bec5bd6570587cb07cda52d79b00b44f6e`  
		Last Modified: Mon, 22 Jun 2026 22:45:27 GMT  
		Size: 69.1 MB (69087950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf953c950bf774a1558a2610c27217993faad44f113fb37ad0ee60aef8db0d`  
		Last Modified: Mon, 22 Jun 2026 22:44:49 GMT  
		Size: 101.0 MB (101009813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7716d2e1c7d779a4a0edad051d112063d47ba4e8e04118f663cce720c2a0198`  
		Last Modified: Mon, 22 Jun 2026 22:45:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2bf7b824d4b1c30add8c6f2faa9816e41da24bc2e5a8120c71a3167030a967fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b731f87d170e08657fa779e1020565112d62c33f96803e2b780a388f31c45d3c`

```dockerfile
```

-	Layers:
	-	`sha256:e8cfd651964296c1f7de5e9d388adfccedc74ba7fa3c7004778eafabdc2c30b3`  
		Last Modified: Mon, 22 Jun 2026 22:45:25 GMT  
		Size: 10.3 MB (10329579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd171a4bf9fb1204150d1c5b3607fac4b7a7deb66e5ff845e5343dbe9caa69a`  
		Last Modified: Mon, 22 Jun 2026 22:45:25 GMT  
		Size: 28.2 KB (28216 bytes)  
		MIME: application/vnd.in-toto+json
