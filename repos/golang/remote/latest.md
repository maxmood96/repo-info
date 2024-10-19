## `golang:latest`

```console
$ docker pull golang@sha256:d7b4cfdee0b5e884694c08fbb61e0a1c3788559977dadb6051f45aac75d4bbdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:db933bde327ab6b27f54c29b092ab3bf9276738432ed1bc730b5c9bd98ff33ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304282114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f4a873f3508262a7dfb2924949f7f9056ad3001bca21453453fdba5cdfe8af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09bd0f8c72b1f7a4ca636b5aedb92a1eabce22f4608ea90f57daea57e43663a`  
		Last Modified: Sat, 19 Oct 2024 02:53:21 GMT  
		Size: 92.3 MB (92279470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f1163629431c9f488c4d6ff6afb5c73021839723b50bafe245663ad3d9df`  
		Last Modified: Tue, 01 Oct 2024 22:18:51 GMT  
		Size: 74.0 MB (74006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29d27dc8b2154be83283c4791da25b0264a9dc8484dfad644d065af56c19b72`  
		Last Modified: Sat, 19 Oct 2024 02:53:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:7a1b0b66e1d8aed47553745b7511fb1368914c5e9640f0c71366d3fe88ffd0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fac087af780356ae2902c70b0df254c3425f3c71ae482ef791d151914b31303`

```dockerfile
```

-	Layers:
	-	`sha256:fff466621aeb3cba9e5fa5bca9299d4e872de1d3d6e55182d9ebf7106357e6b2`  
		Last Modified: Sat, 19 Oct 2024 02:53:19 GMT  
		Size: 10.3 MB (10294068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47775835a6f7ebba12f8ca4dc561f74300078ed8def15a8fefdde4ae84bb0612`  
		Last Modified: Sat, 19 Oct 2024 02:53:18 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:64b8e7db71d3d8b782d3d302171a33d7c3778321411359393c2ce42bbefb79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265043030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb871db0fb171d4853d4733c7f34a78b5a0f44349d9c2294bd7695c1f88457d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5090fcc20b9d13d954de99341bf220366e38db6469372eb93dc48232374cc51`  
		Last Modified: Thu, 17 Oct 2024 13:14:29 GMT  
		Size: 66.1 MB (66136617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832285c268d03f9079f25d645da4f232d333a236aca4f5406f4294d01f183`  
		Last Modified: Tue, 01 Oct 2024 22:22:37 GMT  
		Size: 72.2 MB (72161385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c1fd473e218c0b8a0732a98bd6e72be69d819b9a02000b5b53bd6fb4c3578`  
		Last Modified: Thu, 17 Oct 2024 13:14:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:0c0364747f6287db982fbee3165a1d78e62d0bbe7fbd82033744b0e5e8312bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10102525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b419f53ee5bab0a2819ef6dda1ffcc58570993e25556d48a8a06ea4ec0a4d6`

```dockerfile
```

-	Layers:
	-	`sha256:ba05219e5f4c3684bbd003582f320d535cc4389f05ca37a3e37853cd8023b9b5`  
		Last Modified: Thu, 17 Oct 2024 13:14:27 GMT  
		Size: 10.1 MB (10074832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e986edca7f0e878053ddde6003b2bfa618ea82150bdc0fb77ba35366c6898ae5`  
		Last Modified: Thu, 17 Oct 2024 13:14:27 GMT  
		Size: 27.7 KB (27693 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:aff7e7cb65b9061cb71588ce4ff47eec12fc1f172ff2439f1372c2575b273872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294484106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59223b9b6312e87b1983eaf572d771ef2f58c2c9542147a3abd24a3b3a69d8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9409b189f55b977b4478384cf7a6f1b3af23b6c051231231ea12b993f04bc683`  
		Last Modified: Thu, 17 Oct 2024 12:29:55 GMT  
		Size: 86.3 MB (86311137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a00ec5f007d0ae73647c82b7d81d98a44fb7d073d06e633d656bca79db62a`  
		Last Modified: Tue, 01 Oct 2024 22:22:17 GMT  
		Size: 70.6 MB (70644133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81722acdba27c77df7dc3dc8e704c3770a5c9711a5156ef76640bdec4fe4d450`  
		Last Modified: Thu, 17 Oct 2024 12:29:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:6101dad26b371ecd12e9340bcefd534a75eb7a5e4ced69240d32cfbaa5866781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e851b3712fa8bd7225834bffd5f5afac15c4612ea5fbee5ed4ed1283402b470`

```dockerfile
```

-	Layers:
	-	`sha256:a1d1968998227e9f1d2a164af6d4f0fd84768e0f76b79256aa76635f95e2691a`  
		Last Modified: Thu, 17 Oct 2024 12:29:53 GMT  
		Size: 10.3 MB (10294023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7767995489c6915fb94417164351b9b79e27e40807f8fbc64dc2f3e8cd4e161e`  
		Last Modified: Thu, 17 Oct 2024 12:29:52 GMT  
		Size: 27.7 KB (27741 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:7e708a1ab8fe0cc0a164a929b08d69fbe940e5c918cbd5de6908218392757e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303233667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0544b7ad1fdd74b7a3273b225748ea2e0def97d07483399d424329aa9015f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118b4d3aa7d5b42c90f2dcf856bd26bfe40949f5a30646fbc676721418903875`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 66.2 MB (66208418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bb5d742356e83d569902d6ccabaa1879517fd88c0b94d236bf2f8b045fea32`  
		Last Modified: Sat, 19 Oct 2024 02:52:53 GMT  
		Size: 89.7 MB (89673106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d4de23fe72666a7f8131049dc36e9aa2ba3bb48644c246b44b0b9d60e95bfa`  
		Last Modified: Tue, 01 Oct 2024 22:19:00 GMT  
		Size: 71.9 MB (71880213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5416ab8ea99c95ba8c01e5675914b1caf016932e9396bfc0bff7c62fd18c5ae2`  
		Last Modified: Sat, 19 Oct 2024 02:52:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:964b11ca18e3d9dc8fad463fe6229c2cea022ef3a3bb182d96bd680eab4c7150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5070af050b6e1c8d234518011dd24b31ed953c1a7e1f2aae13df22b7061e68a`

```dockerfile
```

-	Layers:
	-	`sha256:8909c4f48ac617d2c54b703ecf28f8b099fe8e1e46c5e22e98a8d7c4ebab717f`  
		Last Modified: Sat, 19 Oct 2024 02:52:51 GMT  
		Size: 10.3 MB (10274112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db68e3bac4a8f7d0a93e33c1e0352429965ec8429c1579861ca8e4717a1161d0`  
		Last Modified: Sat, 19 Oct 2024 02:52:51 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:6858b38bd6ef95cbfa4e7803dcc51b480760948abab0bdb211602c4e1e5fa06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274623574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fe5bca50072347799cac0dc6638c90c42208325e2bacab5a10da01486d98f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36a8c8304278444a69b45df3237dd325d03c14c930d7ebbb98b5b9bb4f45a`  
		Last Modified: Sat, 19 Oct 2024 03:21:49 GMT  
		Size: 69.8 MB (69849953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2578ebc4d92fa9b48e166d34020f08e2f073e7d8c3e096d5341af707aa9d38d3`  
		Last Modified: Tue, 01 Oct 2024 22:27:29 GMT  
		Size: 68.3 MB (68279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9e1143cc06412137708334bc4dbdd8ea2ef9162a7fef60a26105d61cd59c6b`  
		Last Modified: Sat, 19 Oct 2024 03:21:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5e3efa72caafac25fee6dd965b3bbcdb0a0fecaaac69ef07b62da70907b74a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e475f91ee60b555d771d607f452018953f2cca196c5062cf4af1575b3d5eaf7`

```dockerfile
```

-	Layers:
	-	`sha256:97d222df2f711b2dda36e1c60dbfec6db5a3a7f83c8956c5f47911e647169e42`  
		Last Modified: Sat, 19 Oct 2024 03:21:41 GMT  
		Size: 27.6 KB (27569 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:55999989ed1ab2c60c7790f88947119895ae7794d62a4b51e25ef937a4429b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310163309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4384e5dfeac3c21f15217c1155bccd70b666b21c2b8f17f177834a74a7a11b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb83b0c632f5b09e3c0c89a2090d917f0df7037accb580247402249e170f80`  
		Last Modified: Thu, 17 Oct 2024 08:24:57 GMT  
		Size: 90.3 MB (90257243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc178eefce949e69fe38c13cce1ba17fa50a129169fc4241e2ca8280bdbc6c`  
		Last Modified: Tue, 01 Oct 2024 22:25:17 GMT  
		Size: 70.8 MB (70810506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366df76a4e6d890eb52e8482317306a774558bf2b2bbc724515371e5c8c8d54a`  
		Last Modified: Thu, 17 Oct 2024 08:24:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:9b021e91900032f73dada2895a5774fe9e6fa36926a89f03bddf3141dcb473a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a642293037b634a58a3c52ec4112397e2f69e778ef49235f836d6331cb2d991`

```dockerfile
```

-	Layers:
	-	`sha256:ba38927a66f0288f4ac80e898c2a25618c8e1745b2d971b0e63c530ff5d892c1`  
		Last Modified: Thu, 17 Oct 2024 08:24:54 GMT  
		Size: 10.2 MB (10238952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7af5c960ba91ef340b28b074c1f749a8ed21d0cf7c42706b7e8d40f5378bfc`  
		Last Modified: Thu, 17 Oct 2024 08:24:53 GMT  
		Size: 27.6 KB (27631 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:851f7650fa768b5b3dafe166a5c7730f8bb4f414d7a2edc51c18f82b1e8921c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277267388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25e61b04b9f8329da0141702a971f4236f967ec45c9461e128b1cee12e33c6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba66dca1247069bbe2e2adfc1cbc055a99250a0e8c3ec2bfbbb419a1f58e5bb5`  
		Last Modified: Thu, 17 Oct 2024 03:48:39 GMT  
		Size: 24.1 MB (24051978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236e9b4fd4c23047a10cb64d0cfc027a005094af65d82f927b8a39dfe85c14f`  
		Last Modified: Thu, 17 Oct 2024 03:48:53 GMT  
		Size: 63.5 MB (63494989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacd9d4630c15e3813e836fc8752cba1c05c6962f9bda5973c262f8ec41713c4`  
		Last Modified: Thu, 17 Oct 2024 12:55:34 GMT  
		Size: 68.8 MB (68846165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb0f3540aaee2844fb7022ba44453797a29663928ffe252ed090c5b51b28634`  
		Last Modified: Tue, 01 Oct 2024 22:21:50 GMT  
		Size: 72.9 MB (72935651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dd952b1d2a8cd5abce25d9bfd09e0fe9c0a2a6a3fd82ffc83c46992674b539`  
		Last Modified: Thu, 17 Oct 2024 12:55:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e43fa6babf4b6a32b668347e1d749d3d31f582da1852fc80f9aabd6d939c31f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10130060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452dc7cdb0d67cfa92f6592d70fec6de0a5431a6b7049e5199153076fcdb4487`

```dockerfile
```

-	Layers:
	-	`sha256:d55ccc6fa0c077e993d33d8517a4612b7a0809465110d7d094ae14f0d5164aaf`  
		Last Modified: Thu, 17 Oct 2024 12:55:34 GMT  
		Size: 10.1 MB (10102496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32314d2226233e108c00e00c4706a990624646e77e8026ade697d5968d5d1256`  
		Last Modified: Thu, 17 Oct 2024 12:55:33 GMT  
		Size: 27.6 KB (27564 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.20348.2762; amd64

```console
$ docker pull golang@sha256:67fc9f9fdbc9791a990ed4c7884ae6ae0f8307807c13b357441c63e29a427ace
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902581230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35af519f2a81290d7577c119cb68c94f587219186b0f3f207ebc41c769bc3a8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:00:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:00:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:00:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:00:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:00:08 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:00:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:00:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:00:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:00:35 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:01:52 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:01:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5ee69cc7a7c00cdf4c7f1dbff132533631d0ad0ceaa5b5ff3db486c5b53c91`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cbbe74f967f0f9a9ef684fce9a9aa625821acdbfe105c34435074aef0d4d18`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf92431dccc391f1ee38a98f1ca77b1097bda8214d7419e6969cb3abf8430c4`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eaca868705c9e05560d53495acf3d495d0b7a06c6ca9b329fbd507d7d6edea`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba929dd024b4609634374ae5172ba04b23b9a0d30aa37a2b7ca3d881d55c2b6`  
		Last Modified: Wed, 09 Oct 2024 23:01:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1298a5450abb7290201ff8c77efe56187bfa7a3ebef66eff603c77c1b506b6fa`  
		Last Modified: Wed, 09 Oct 2024 23:02:02 GMT  
		Size: 25.6 MB (25565156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64778e8a77ed158cfedca607e2abc463e88daa09877472b22079c2d7bb486626`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce14ff8404e31e6ceaaaaa071eea060149cdb4568c12d3539669a2744c2fff`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 335.7 KB (335731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b91e7a00fd9533319ca369401b4fe2dcefda3dfa70aa511d56ca40081abd57`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6e8a148665bc2d68668af00265458e6f605be340e500fc302c1c9ca4e7437`  
		Last Modified: Wed, 09 Oct 2024 23:02:09 GMT  
		Size: 77.3 MB (77328388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da972d21cb88b99cb078df72e224aff083f94475d206d2cd1f1536774545cd`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull golang@sha256:297687d686b8a28bd06de3cf4c8c232f43eedc77c5b889d2c40a13429d17496f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005229032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8e81ecaa31896c5c040f3942d8ca486e031e1836e6161268c78a1a28da232b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:07:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:07:08 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:07:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:08:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:08:17 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:08:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:08:24 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:10:26 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:10:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0b69ce3049c27995588e18993ed09137752980cac80c4663648f5089cd9275`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba7602ffdb33cd282009cf1d68032a22821a3999cb542a3ad983d4d826621b`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85184f815a4ea0c2d893d89869ca572c31fb105c4c70b03706bd4f58ca4aaf0a`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc241ab5ab4740281e28481724541dcc6e188f2ffa28e4861f5648d630ace57`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c76426ffa00c2faa295c3cc1b31156e15134b0690e4a1b629a64fe729e7056`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c03c0444578ea76cd2a730e33886d9c2ec957c31c4341bddd62b67f34508c3`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 25.6 MB (25566436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fe3d482d8c7ec1f9a8be4b592907ad8c05d338a0c9edb4a4b734a79eee532`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ed797d603bcaafab01b729f9f4997af2b4b044ee40a85449f400aead10eed`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 324.8 KB (324810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630601fb93553af5e9d2e83bb1e0d212cce73f4bea992c668aef743868d62d`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc433f483b37ead71df015348df3261600f715ed35293715ecb7153d8b78a20c`  
		Last Modified: Wed, 09 Oct 2024 23:10:43 GMT  
		Size: 77.5 MB (77501886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2af687eb62f54159437b2fb0cf416cb98e217cc5a67ef09d2f3dfbf072c95c6`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
