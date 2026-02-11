## `golang:tip`

```console
$ docker pull golang@sha256:fb784252363c7415d16d5470ace131f1e38811cabeb3f42e02208c73ac16c8c7
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:a978f3a671c2bbed8a95c2b13614d67c3c55d38188470f7ad78aec82a01ae579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338315996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928ebf3bd10a03f6424023bb38a05720aec9b34baae699ad0e916a2f32643aaf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:47:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:47:47 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:47:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:47:47 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:47:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:47:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b15f7f7883e2fd3305a5396600f157bbbdffd169684311da14965ac0674d`  
		Last Modified: Tue, 10 Feb 2026 21:48:18 GMT  
		Size: 102.2 MB (102159493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab3e19e6c8e8831458d5c634ec4fc50390cbaa761a3a0d1041089a86cb5630b`  
		Last Modified: Tue, 10 Feb 2026 21:48:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:e0e15ae594c9b090343df1abe245413ebe588950215bd48fdbb5af638162b930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7106abac1bef833f9a2b5fd45e65bd41c02a662ae9024ba39029b8a2d31edf`

```dockerfile
```

-	Layers:
	-	`sha256:2c5d558aa3ebead159b53aabe4ac28c5396d15500d72680b094451cd960f40a4`  
		Last Modified: Tue, 10 Feb 2026 21:48:16 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f503464a79b210bc1cda347e8c2e0081c9764d1ece252c4d74693357880e5a`  
		Last Modified: Tue, 10 Feb 2026 21:48:15 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:459fed5e2410f8429ae0ce11220c1171c865bfa322a598bf5b338489a2f7fc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294452905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb8c5a6de83f24a980494c698e07df6447b7b71c3794aa57e88027de7f3bb06`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:46:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:49:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:49:22 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:49:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:49:22 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:49:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:49:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74387350d2cb71494f8cd51684a1223fa4d67c2770958430649aa3d99f0d84`  
		Last Modified: Tue, 03 Feb 2026 03:32:37 GMT  
		Size: 23.6 MB (23628323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eaf2b8f43157ee85fb0c9ace18005d09181f51842f1543a4a0e4d1072f633e`  
		Last Modified: Tue, 03 Feb 2026 05:01:35 GMT  
		Size: 62.7 MB (62713563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e5b6cd881eac2120f5a26a8c68092076693337c5cb600a4440497b95ac9421`  
		Last Modified: Tue, 10 Feb 2026 21:49:50 GMT  
		Size: 72.8 MB (72802223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556fc7018113e82fd09e740c69a5e6e4bd8be46931e49f17f4584482e5044c2a`  
		Last Modified: Tue, 10 Feb 2026 21:49:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:1273ff2abdd084a1c0ce8b1f4ef4cf7f73443e635ca1e2c741136fb2d7423815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70384c8ef7320e723ef526be67151a49b8971740c44b87c8f0c379249a9914ee`

```dockerfile
```

-	Layers:
	-	`sha256:9d139b20dc48fe59dcd9795679c6f6bba7c0a329f04613d7d6db822bc9ca4126`  
		Last Modified: Tue, 10 Feb 2026 21:49:48 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf4d9cf157c35c5bcd1662ae191a378bcaac64daa28a622f5daa0831242e3e0`  
		Last Modified: Tue, 10 Feb 2026 21:49:47 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:205120de9f14d175deb0446d719d0711ce8e5d08bbada3fc72ea43e148f33f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329046607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b20f66d9f7bbc7167df5e7b00ae1212659b7abdd59c90ec7199fd3c8cb5070`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:47:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:47:05 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:47:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:47:05 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:47:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:47:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3fdeb7a131c9adde07efc725346d649eb4f0a5fc2dfc49161b789e8c921fae`  
		Last Modified: Tue, 10 Feb 2026 21:47:34 GMT  
		Size: 98.3 MB (98304619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b18ec627d4b16c5684e8395778c2a2c228bcab71f46f5cac12d5a2b50e49c17`  
		Last Modified: Tue, 10 Feb 2026 21:47:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3a32ac505b6c9d49df552ae898d8fdf6d7f391b8698a9920be33bb8bacd5d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6230c0b284de2b0435b265598a7cf3695757cdbc514628a6e2aab014158b8a7f`

```dockerfile
```

-	Layers:
	-	`sha256:9fabd1a570e799c89673da18063d706d9b3152c8e30fa2b62314e37ef22c3615`  
		Last Modified: Tue, 10 Feb 2026 21:47:32 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59acd2874a651a34ae0654b0a4e9951ab9f44000561b7c5e4ddbaef6d222d9f0`  
		Last Modified: Tue, 10 Feb 2026 21:47:31 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:c4eb139accce9129f934b5863db09b3cf2f35e574fc6eaf1973ec9a8c402159e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339513068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98208d03cc0e668b645d0f6c153d67f511f5e03d80874d75970c195afa5a3016`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:48:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:48:25 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:48:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:48:25 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:48:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:48:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82aa8569021d347e27d65aa0b48a5747ad08b2dd9fedb936660291f168eeed9`  
		Last Modified: Tue, 03 Feb 2026 02:49:59 GMT  
		Size: 26.8 MB (26778421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa32f4c52b58b9468e88e7cde44c8447ca98c8e3cdb99900c08bada90da980a`  
		Last Modified: Tue, 03 Feb 2026 03:25:16 GMT  
		Size: 69.8 MB (69803143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b60c04f38d57a09496545675fa7b09c335ff9cdd38c88e4b989ebd594ad752`  
		Last Modified: Tue, 10 Feb 2026 21:48:55 GMT  
		Size: 100.6 MB (100606961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d305d93d1464ab40a9a4413029dc95fde7d86a380aa00918f65e5ec5e6ba3b`  
		Last Modified: Tue, 10 Feb 2026 21:48:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a384a3a5ea006933da2fc1638b7b26ba6486bc00888206106b1dce08c258698f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c1617b73681b4d00878220890eb6c4a61b922838c3a92f30a04b119c7f200f`

```dockerfile
```

-	Layers:
	-	`sha256:f7c2656d8786cfb9de51447723541963303285522e0090cb375c17d160fee21a`  
		Last Modified: Tue, 10 Feb 2026 21:48:53 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873492de2e8445073e8b227d922e752687cb0153f18420d97e74c9464a5b17c7`  
		Last Modified: Tue, 10 Feb 2026 21:48:52 GMT  
		Size: 28.9 KB (28925 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:1c9deb9b30b1aedec589802c5b34e3245d8853a3001550ebbc9bcfb58b51a7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336113593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8578bec40a771a0576fa531b42e60c38ba12f88c1336c3cd314eeac13f563ef5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:26:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:26:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:27:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:27:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee79ae595ce83805d9060f1c610385dfe6280391251ea73a1f48c7cf8bcb3f09`  
		Last Modified: Tue, 03 Feb 2026 10:38:14 GMT  
		Size: 73.0 MB (73032214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81524379358b3926f0db2698f1a9540fee00e644691faecc926ca8a022dd0762`  
		Last Modified: Mon, 09 Feb 2026 20:28:09 GMT  
		Size: 92.9 MB (92864222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f34b281626db46d13e5a751b54221f74b1d0be2bfad3701f6dc696782f8809`  
		Last Modified: Mon, 09 Feb 2026 20:28:07 GMT  
		Size: 90.1 MB (90106742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f05dfb1c1a5f2e312cea04d536814c4e786127ff3c20d3923b13a92539d9cf`  
		Last Modified: Mon, 09 Feb 2026 20:28:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:beb04c5d3cf6ebd3cf6260c62900f7e0c9809111e5281dc3ddf1c7f44873a7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf52d31ec8765ac356c5f460ae2295239d4b3624e181342750ab8a9e4871704f`

```dockerfile
```

-	Layers:
	-	`sha256:530030d71492d863615012aa93bcaad4edcbaf02676c71f9de5f13f92943e4e6`  
		Last Modified: Tue, 10 Feb 2026 21:49:34 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf504c035ae65b38a4523dee764cdcadd52bde472d17f04e7fb759880b501ebe`  
		Last Modified: Tue, 10 Feb 2026 21:49:34 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:700103b8437ccf73af38c6133fbe6424e50b0df61dbdd9ef4fcd92134a306ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361659037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bcb37eeac33bae464a8eb1f55695492ed6928056118fb12de3efa22ebb44ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 08 Feb 2026 00:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:36:19 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:36:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:36:19 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:36:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:36:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518328709aef2ec161ee90f4be9eea82346936a41f7fadae6c748b8ca89b81be`  
		Last Modified: Fri, 06 Feb 2026 08:00:06 GMT  
		Size: 66.7 MB (66660429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30992833d130e4aed39434931ae478a9ff84677bfa5deef60f6f4f9de9312e34`  
		Last Modified: Sun, 08 Feb 2026 00:50:26 GMT  
		Size: 131.6 MB (131627094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23894c629a08e6202ce12c965a7b27818d87e5582941a612a4ef5200db7436f`  
		Last Modified: Mon, 09 Feb 2026 20:43:36 GMT  
		Size: 90.6 MB (90641431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb24371fe911fd27e73a6af24c04079366a9d08e90d424a76fb9d3f10e6a768`  
		Last Modified: Mon, 09 Feb 2026 20:43:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ae96010fdddc6d2877e8c9af2a0223a8f4d6ef3a44f1755f2cb587ce7746bc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036b6d0a3bd55dc36790fc2bb7f5b220d18344839a9fdd2b68566f1b77a20500`

```dockerfile
```

-	Layers:
	-	`sha256:ce25161092a7e3444b2af3d4a3e55b492f580b57b624594d87be76e7ba2dcf20`  
		Last Modified: Tue, 10 Feb 2026 22:29:08 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e41bb1eb104339cf979eb19312f0bb253731e9d5857b12c8d3586b57144f66`  
		Last Modified: Tue, 10 Feb 2026 22:29:06 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:2d7d1f8d1522ef251facfc15ca92b9db278a7f4849de6d16093b9afd9a646c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313391767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30c9c423c91737ef72d23b45c676018a79b4e95f259139da6d5704572b85892`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 19:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:59:44 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:59:44 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:59:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:59:44 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:59:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:59:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3c6a3ae754d274216ffbec3754da469ace4e7c5b6e8e123969f0516b4a968`  
		Last Modified: Tue, 03 Feb 2026 05:29:44 GMT  
		Size: 68.6 MB (68623115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f527bed626ba0462f7683e31f92506f4c89898f125e450022182ab02dbac44eb`  
		Last Modified: Mon, 09 Feb 2026 20:00:42 GMT  
		Size: 76.0 MB (75970510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec9ce8a3837e5750bcd10b11df694113758518fac79cbd3aa70f831f2db7`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 92.6 MB (92648889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ccce570eb121e903694c14b671b10aa139f4a64c9ff8dea9431c239fb2a78f`  
		Last Modified: Mon, 09 Feb 2026 20:00:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6abee40fc89f204a6413d51c15c665bd1bb345fb0925c57ccd5aa3ba9d61f316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdadb392e8f183c52bcf30fb3213d805e6238302d7cc5cd305e81dd70bdbf98e`

```dockerfile
```

-	Layers:
	-	`sha256:97326ccd12b9fa2d08141f962f0e8a4a3c047b9c44ee0d5c23b3f04b6dd0f12e`  
		Last Modified: Tue, 10 Feb 2026 21:50:00 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a0e641df5583a0d45299caa33aab4d7ae53ade50c5afdfd0301c4d6b291ce3`  
		Last Modified: Tue, 10 Feb 2026 21:50:00 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
