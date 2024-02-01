## `golang:1-bookworm`

```console
$ docker pull golang@sha256:cf1c8a7ab34b4f478f43174c5135b3d057818e3dcb4b753e8de0f8a07eeb6c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:5c7c2c9f1a930f937a539ff66587b6947890079470921d62ef1a6ed24395b4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297175266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b429352f944d3ceb37f26112e11f74b1fcab851cbe6fc611c024c08cfff5bf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d85599795460b2d9d24c6b87c53ec60555b601705cc83bea31632240500980`  
		Last Modified: Wed, 17 Jan 2024 02:00:06 GMT  
		Size: 64.1 MB (64139892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223fb869183bfc381cf4d382255f5d41b2687e9741e697b70fcbbcbe02094ef7`  
		Last Modified: Tue, 23 Jan 2024 19:56:54 GMT  
		Size: 92.4 MB (92365572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc4c1e5efad6a5c46177991a1853a03068d93b8be5343911ef95f5536a78294`  
		Last Modified: Tue, 23 Jan 2024 19:58:18 GMT  
		Size: 67.1 MB (67061612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c516ddd64fde35c3441eca3a60bfe44b635e70933d0ed8f426830065697caa79`  
		Last Modified: Tue, 23 Jan 2024 19:58:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:18cd793ce60cc77a541e9e3941cf2df61f52f047cf31f26ce3649d01f2932714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258402807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9a20099abc5121f149b5b43d430e638f4794febac9589b311cb8d0794bb55f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca9b1f8d7860a719d7975578d676d9027aa7b6bbfaeccea30b3c58c1a727ba8`  
		Last Modified: Thu, 01 Feb 2024 05:44:18 GMT  
		Size: 66.2 MB (66222162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac6aa58af0b8e4bf5eea04c91b0a5d0793c14ed4e0741772096e4fb7dbb82a5`  
		Last Modified: Thu, 01 Feb 2024 05:45:09 GMT  
		Size: 65.8 MB (65832095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e870905788bd1431bb1716e6bab64ee0fe40e6e4cea5f5b867d2720d7bad009b`  
		Last Modified: Thu, 01 Feb 2024 05:44:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ea3f343e515dd6d4c39e82757c186040f2838ea91e935670433b0849f0813ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287721004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3dc2467dea348a59112ac390d5b688c39c86d1646039137d565635ecf4ab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b4f1810f998c1f1580e2404b2e7fed8e264902d898bbe531443ea9789b7641`  
		Last Modified: Wed, 17 Jan 2024 02:58:02 GMT  
		Size: 64.0 MB (63991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece61d3d983cb71f3b959313708a475ae29034ee4d69f2bb84e46daccbc065a`  
		Last Modified: Tue, 23 Jan 2024 19:45:10 GMT  
		Size: 86.4 MB (86393901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302f5869308ee3050467084d0c29506dc1abb9a4fdfef48515837d880754dd73`  
		Last Modified: Tue, 23 Jan 2024 19:46:51 GMT  
		Size: 64.2 MB (64160910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4819c57d0a3c3f911b34050c353f8ca997e418d2c0986332b146789397e2581d`  
		Last Modified: Tue, 23 Jan 2024 19:46:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:7fd31c31aab449c1cc9a6a4cd498ab20a018de2f64b7ed151bcef3305270dee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296746574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a3a30c65125b68fd75b8a731dd93bdd28a61639c5716f7e5d872c56c361a49`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:28 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Thu, 11 Jan 2024 02:38:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abfb5cb040b6af10cb1e9ac26bb34229604ca8c2cd52ef5bf19c4b933dd6600`  
		Last Modified: Thu, 11 Jan 2024 04:41:29 GMT  
		Size: 24.9 MB (24884306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02d03ac10f8c192e0b06aa689206512609710cce15b14a04e9b07acdfcabed`  
		Last Modified: Wed, 17 Jan 2024 01:50:18 GMT  
		Size: 66.0 MB (65986657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0f00a89f647930e6472185ed67f0365f8a20cefc3b89471a443d14d9f520cb`  
		Last Modified: Tue, 23 Jan 2024 19:49:18 GMT  
		Size: 89.8 MB (89771977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001c537c195a9a5459c2ca7a074e5047f8d89a6144c28c7b494510319d03103`  
		Last Modified: Tue, 23 Jan 2024 19:51:28 GMT  
		Size: 65.5 MB (65521452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e80d09cd48770672aebcb471058f72f77b6f492d1155dda87c5d88cb9a7eb2`  
		Last Modified: Tue, 23 Jan 2024 19:51:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d217c9e073f2b3fc9eab3c28ffe2a67824e53bac877792a49cd4bbb46b2c9830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268069973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ba511ef51672f3c99addf2cb15015edc2017dc82f531a842fdf087e9ec580c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:06 GMT
ADD file:e632734e8c2b1e7594b8a79fefe3b2790d6e662e647019a7daa2713f4b1aa7be in / 
# Thu, 11 Jan 2024 02:11:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:48:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32de429a78b4633d08d4ddf9cb62b7ff44ee9ed79fafe52b6d33ec4e772c2beb`  
		Last Modified: Thu, 11 Jan 2024 02:21:59 GMT  
		Size: 49.5 MB (49548641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdc39b4d6447f4b14a9d2668a4ec5e5cf44bb6dd0d7958fc882ba5d7297cd1c`  
		Last Modified: Thu, 11 Jan 2024 03:24:15 GMT  
		Size: 23.6 MB (23630453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db1512d660252aea394ce778a64b88e7f0b13cc6560953b1615531e4e266d3a`  
		Last Modified: Wed, 17 Jan 2024 02:47:38 GMT  
		Size: 63.0 MB (62965856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74183cb45ff6e86232af49111c9018053f1e2c781a871f765b2dd3a7822cef17`  
		Last Modified: Tue, 23 Jan 2024 19:54:02 GMT  
		Size: 69.7 MB (69722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c23c496b71fca14a2525b688e625c103878e08bdc27e053c4533e102bbaad2`  
		Last Modified: Tue, 23 Jan 2024 19:56:18 GMT  
		Size: 62.2 MB (62201909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcf2045ce3ba66cb32e011e431a47504acf5342057f960ce054b5371edea23d`  
		Last Modified: Tue, 23 Jan 2024 19:55:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:063516f1507707ac49112c2bfc70107b4593a09a4cbcfd4d31e1a46c3cda91e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303377582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c642dd50c359d513091f2c6951935e4ed93fdffb899effada68f096eb0930bf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:11 GMT
ADD file:181ff897280683d4e2f512551aa99c5bca9823305859ed4620c8ea3bd4d95cd5 in / 
# Thu, 11 Jan 2024 02:34:14 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:62296c33e75415de6ebf7e20132da876513ede04af94472801e60452c0a295dd`  
		Last Modified: Thu, 11 Jan 2024 02:38:58 GMT  
		Size: 53.6 MB (53557571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08c7f22c453d0296f7b3aac215dd01664f85d00e83a734e65de9f4669b9b11`  
		Last Modified: Thu, 11 Jan 2024 07:23:16 GMT  
		Size: 25.7 MB (25696347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b4b3bd26123c050bfca2111b37a82d4c385c67c129372b0688d3bea5051428`  
		Last Modified: Wed, 17 Jan 2024 03:24:46 GMT  
		Size: 69.6 MB (69581529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960166212959538186baaab8a7daedc177f4cc318035b81791f0874aff417d31`  
		Last Modified: Tue, 23 Jan 2024 19:35:33 GMT  
		Size: 90.4 MB (90352284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abc5b6a34af5d058deb847cf47336c9c57296a719ddeba6cfb18f9993183721`  
		Last Modified: Tue, 23 Jan 2024 19:38:09 GMT  
		Size: 64.2 MB (64189646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d890f7605f4624d4602b2ea8f7acc2e8b894e6d185dad966075e63f26b7db4f3`  
		Last Modified: Tue, 23 Jan 2024 19:37:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d7e15462c9ef917e095b051c44afd3aea4650e8de34370b4f7d4035e45bcf656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270300761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f699abec31b499a73bfae22a6f7580b4f269f02a9beff39067a8ce90590567b2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:44:46 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Thu, 11 Jan 2024 01:44:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:11:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Jan 2024 21:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcda5a31401318d38b94cd36426844d1953c0561252561b5205f9b95c442bac`  
		Last Modified: Thu, 11 Jan 2024 02:21:00 GMT  
		Size: 24.0 MB (24043257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed6bc65286743fe499d9acd1b031ec55623990da97c0b8c5a36e90e5efb4f45`  
		Last Modified: Wed, 17 Jan 2024 04:03:37 GMT  
		Size: 63.1 MB (63126558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7171751e7a117fa828bc3e6f03ea58203fed1567e63c1fb1ca164f80133378d2`  
		Last Modified: Tue, 23 Jan 2024 20:43:53 GMT  
		Size: 68.9 MB (68928403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d80eaaf290dd2428e0daee1f3a78806350ff68b1c4d44b46182c50de37eb4ca`  
		Last Modified: Tue, 23 Jan 2024 20:45:21 GMT  
		Size: 66.3 MB (66284464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2853ea0f85ec6ae37e2128182bfc1d9a5828923e5f412c4987cbc1b32b4027`  
		Last Modified: Tue, 23 Jan 2024 20:45:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
