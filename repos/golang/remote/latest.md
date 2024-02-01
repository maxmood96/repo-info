## `golang:latest`

```console
$ docker pull golang@sha256:3c871baacaa9db01d5b7e26b6ae937b695fbc87287696d67341a4a0f29c31230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `golang:latest` - linux; amd64

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

### `golang:latest` - linux; arm variant v7

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

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:928ca508580b7c63890d25e4a31de8cfef35e9aa897365317e1706661b051ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287752060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4709b6f00d5e7f60bd31b425be6de9aee6b0d251a469bdea9bef30c11fa7e95e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
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
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0415bb1783d1a348827b100b0e918648a16b9be64e3af2d45b75d4996ff5b8c`  
		Last Modified: Thu, 01 Feb 2024 08:13:22 GMT  
		Size: 86.4 MB (86394350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7276b11ada40cb47372f79c1c868e56150546b15f0e734647b4337afadc366a`  
		Last Modified: Thu, 01 Feb 2024 08:13:59 GMT  
		Size: 64.2 MB (64160951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aeecab7f9bea6add3e567ff84eaa87f1f2da1e747d3b02674e0677be5c7c35`  
		Last Modified: Thu, 01 Feb 2024 08:13:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

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

### `golang:latest` - linux; mips64le

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

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:fd0a89bb72dfa6cd696c6835af91bfefa4d29ed6b29b4fb608f648cd97878a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303405759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817b54b955390f289642b01b4e4a9f30349e69abef4619bbb69c0718d61cd880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
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
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27c0ce817cf45ea009954445cec293495b0bb8726b147c6d45499b9fdab8a1`  
		Last Modified: Thu, 01 Feb 2024 08:53:41 GMT  
		Size: 90.4 MB (90353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0a72745538f5c4a3817949409e4a2c90386b3193222bef38589e081166ef79`  
		Last Modified: Thu, 01 Feb 2024 08:54:29 GMT  
		Size: 64.2 MB (64189624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da520c3e7f70a7a3276093fbf02aac31269728b1c0ecff03d19cd198e796a267`  
		Last Modified: Thu, 01 Feb 2024 08:54:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

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

### `golang:latest` - windows version 10.0.20348.2227; amd64

```console
$ docker pull golang@sha256:a377a5168eaa3a91f7a6ac41498e7def4d2f05f063672906ed3509fe70a97d4b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1995424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a16788a82413cdafb39cd62e24d101136ec7c8eb10b5ad24acd989868a7baf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jan 2024 23:38:31 GMT
ENV GOLANG_VERSION=1.21.6
# Wed, 10 Jan 2024 23:40:51 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:40:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c445c19b55c4b2442720623ffc2235a5ad02a0c71e9ca6c1c9d8c180cf9af`  
		Last Modified: Thu, 11 Jan 2024 00:05:51 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda5089bce9002bcf6bdaedb2288edee0d328ada4929e56ebf3991a0b829567e`  
		Last Modified: Thu, 11 Jan 2024 00:06:09 GMT  
		Size: 69.4 MB (69409123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b91ebf7e49130d7460d43115adfdd651f5dc4ad70244ab201a9c7669576f`  
		Last Modified: Thu, 11 Jan 2024 00:05:51 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull golang@sha256:a143f1046e28dc6c4185a8b23fb8a556c66bd8d4f6d34208d68f12c02a64ddae
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2165006372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013b50dd751da844b2ca3c3aa9666b1b148fc2eda0cb64eef05c5226360f8c72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jan 2024 23:41:01 GMT
ENV GOLANG_VERSION=1.21.6
# Wed, 10 Jan 2024 23:44:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:44:09 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1d59a6cfeafb1ae2b3334cf87c88e1266778eb7c183c2efba2255270baaea1`  
		Last Modified: Thu, 11 Jan 2024 00:06:37 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b14985e0233a59c6da1faf9301a83de7148aa08c6a82b04c4a0f17557c45842`  
		Last Modified: Thu, 11 Jan 2024 00:06:55 GMT  
		Size: 69.4 MB (69433202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23fe047bea89daa4ae69d6649b01880c3818b1bb1dcd9977e3362dc0952ae28`  
		Last Modified: Thu, 11 Jan 2024 00:06:37 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
