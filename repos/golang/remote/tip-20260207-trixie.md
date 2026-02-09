## `golang:tip-20260207-trixie`

```console
$ docker pull golang@sha256:bc05592eddf863dbc95855eb3aec3729ab95a5f60865dbeec77692c5b58a076f
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

### `golang:tip-20260207-trixie` - linux; amd64

```console
$ docker pull golang@sha256:731215e7e88f2c261e18574a62c0493fe4678f96dab56bc8282cd9212b1cf68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338315341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d083f0a51e2d4794cda9d81fa10c2bb56d68bf085531c542db605d222a984f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 20:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:03:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:03:27 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:03:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:03:27 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:03:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:03:30 GMT
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
	-	`sha256:ca7009b37cd8d7156c9eb11e3c33913f3c71523ac4263169cab919dff656fac4`  
		Last Modified: Mon, 09 Feb 2026 20:03:56 GMT  
		Size: 102.2 MB (102158839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8851ad447646491f8bdf177c504eb9cf9f7fed22219bb80245af458d33cfe6`  
		Last Modified: Mon, 09 Feb 2026 20:03:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:babdcd1e146bf628dff9302f74dbf5de1bcf00069a5affc176a30f791a991ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc1d5d42869cdaab260fa51507e2814dcd8dd7f98353d573ec2f0134c1a74df`

```dockerfile
```

-	Layers:
	-	`sha256:b2af02191d7a8df434182f8563c23a89ebf8fa234264393cdbb6af862a242297`  
		Last Modified: Mon, 09 Feb 2026 20:03:54 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0329162ae25d643c00a2a6581ea83189581102a5ccecf0bacda9484046ca37ec`  
		Last Modified: Mon, 09 Feb 2026 20:03:53 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:4d9ef9f512d03dc6058b274d720f53633a94fb108d3cdd0c0a242a35062e4f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294453031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72fa8dd0bf2af78f55d93fdbfa98e7c28098d137875718662e1b3ad4473f87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 19:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:58:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:58:38 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:58:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:58:38 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:58:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:58:41 GMT
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
	-	`sha256:332c449d2c94158c741e05e410d31402e392a771400ee7bfca27e9c71f9f2cd9`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 72.8 MB (72802350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ab22e08e9698f4f1d950c2f8cdbab80681e412632c369a2d8464d7065a769f`  
		Last Modified: Mon, 09 Feb 2026 19:59:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6d2a7319ca37e7ea8f3d73e8737233fcde780ca67a0803f85f8e0005d58abafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b74bc31970d5b9d2767f5c8ffa677bfd0bb0bf7a65bbc8a73359def14c0fb8f`

```dockerfile
```

-	Layers:
	-	`sha256:889959caa777d2196a177f6002879693d03cbe9225f66996f41dacd33a0f777a`  
		Last Modified: Mon, 09 Feb 2026 19:59:04 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1856e776c2569cf3ca0413da31f698f6c51f2b4242c9fc12edb0920fded1dbef`  
		Last Modified: Mon, 09 Feb 2026 19:59:04 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:31c87f613aac4b6bc9b50aeadacc7351e8cfad97745ee488408f817efbed073c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329046378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a979f4216658e3dfe5874da6fbdad76671ad02af9a7350c56189e26f1a2d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 20:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:02:58 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:02:58 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:02:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:02:58 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:03:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:03:00 GMT
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
	-	`sha256:d9c730ed8c3dbe1b27e0124488f26a4ddd89853ea34283961ff1503f2efc5587`  
		Last Modified: Mon, 09 Feb 2026 20:03:27 GMT  
		Size: 98.3 MB (98304389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d50b7e1a084b500d2e0bf5ffd73c1f93858010ee6cdbf96beed2ec5fb6238ee`  
		Last Modified: Mon, 09 Feb 2026 20:03:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:df150c887c6169cdfb7243a7072d69ae94e7d8599c0c8d28b5305c347fb20350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3b48fb3e3c08409951d836f60627aee899697c7c38963e2ac817c321ccfc67`

```dockerfile
```

-	Layers:
	-	`sha256:f9944fbfe88ff759d9b17afd3da4fd457bd1dbba4ccacc9640604d626c0d49b7`  
		Last Modified: Mon, 09 Feb 2026 20:03:25 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1f8a9a3c7b1aad2144f2d3b9dc67aa17a549792982953590d549bacff20b56`  
		Last Modified: Mon, 09 Feb 2026 20:03:24 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; 386

```console
$ docker pull golang@sha256:6b49a6c5e79688d9ee238ea549301e905b4ad1b5ab2b565d194c7fb7a119ed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b61ef72bf0d5e15c12bfe4487efbfb4281b7287c83e5f4ad7aecb9d3f830c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:58:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 19:58:08 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 19:58:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:58:08 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 19:58:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 19:58:10 GMT
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
	-	`sha256:24054e0758c481a536c5d316469c1259e8fe6e0c6bfcdfbceba8fda49ff333c5`  
		Last Modified: Mon, 09 Feb 2026 19:58:39 GMT  
		Size: 100.6 MB (100606781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60246b25c84dadfca6d9f955dabbaaaa097e2533e0c132c2bf762689b40f0469`  
		Last Modified: Mon, 09 Feb 2026 19:58:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8939254b2d93bb4941aa4e486eb74ad999df048d944dad0f09ab1f642b2526ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a3886b485537ad6d0b64dab0cb6f82f3a6cabd1ea2ad248cbc55fac504ba84`

```dockerfile
```

-	Layers:
	-	`sha256:b741fcab935741c95d96201313147ddff2595b8d1e51bd44ee7698122d25c94f`  
		Last Modified: Mon, 09 Feb 2026 19:58:35 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f249d986a06e59a6ba4cbe4bd8aa0a601172e6fc0e28cad1c20c5125a9fbddc`  
		Last Modified: Mon, 09 Feb 2026 19:58:34 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:32290ef7c6e2c11f91ee033219f27a88b8c74717cde6b3a45de309986d3c5b1d
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

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a8a91d82a6e320a22fe315853ae87298170e3a7a9b6702ba8e359fe734adf5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2655dfe6334751adc2fe4125d1b648476e7e8054d0586e13490866dba3f144d2`

```dockerfile
```

-	Layers:
	-	`sha256:df00ccb8322d9f2fa14353362219d9b7a640d5b1e4a7def5e61d840fd62535d6`  
		Last Modified: Mon, 09 Feb 2026 20:28:04 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bfd03c2f3f9e890ad29b8686ee672d7379d7d95360b03aaaeefc25c72490feb`  
		Last Modified: Mon, 09 Feb 2026 20:28:03 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:de519e0ddfda64a38387915ea9453c1524b84b0517caa4c4991357c05566cccd
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

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d51d98b648a28b8dabbc19b9f6ee5c5fc03ddb35fec9764ffc1a581b673f7ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d6762f6d72e6601e392980a48955f6768fcd2761342af415fcfb7ce0beb4f3`

```dockerfile
```

-	Layers:
	-	`sha256:7a5226b096d2b4b8587b3bf217203a5c01463f29dfd8ecdf3979e4cea893da26`  
		Last Modified: Mon, 09 Feb 2026 20:43:24 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4de3933e15c993a1933919490eb509baa30d35ede97968e875ca0bad16f4404`  
		Last Modified: Mon, 09 Feb 2026 20:43:21 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-trixie` - linux; s390x

```console
$ docker pull golang@sha256:83e5625ff1f01773f60d54a74a49641781faf39768f1207dadf3af8895d07e89
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

### `golang:tip-20260207-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c89ac5a5c831a9fa070d7d45739b5518de97d4c6e8239bf7951431791b1b733b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae3e871946962841ea5a4407352fd085c3b6e64a5ed5d542d857da94ba3dd39`

```dockerfile
```

-	Layers:
	-	`sha256:a451a6fb60e7baf1cb44e562d27588586f84c4a5580f84da29782f1b51017a61`  
		Last Modified: Mon, 09 Feb 2026 20:00:42 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70ecaaf54968cc7d3f167a736424682ab02bac54ad151b12161718ad2a8ee66`  
		Last Modified: Mon, 09 Feb 2026 20:00:41 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
