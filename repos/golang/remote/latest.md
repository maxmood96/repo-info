## `golang:latest`

```console
$ docker pull golang@sha256:75ca321c953ce0572c709fa186cff872a510a22d6dad515291c6eb29edb9c849
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:21d68a382b318dde54771baf5e04393e0930d077583c8010e4fd83adae328eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312030533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364310d5dd6d53f87952897019b2147ed0aeafa58d4b5c7207d45c581ce7a6c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:25:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:57 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:57 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:57 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:05 GMT
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
	-	`sha256:132b23345fa8206f1493a3f4a33a96c348176e4598f5bd75e8ba3a662bec063e`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 102.2 MB (102159378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656857beabbec31d8624216a277a98542a9fba0685c0d5e2965d60646c51f96a`  
		Last Modified: Tue, 10 Feb 2026 21:25:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:ad7318a6fed35953ba4c290975396857febb01a55869694444a11474306a7258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10815928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3d8a67e76535d80ffc19e882e7ca7116a6ec232f8ed67254672d5509c9d7ab`

```dockerfile
```

-	Layers:
	-	`sha256:b1aed07a70480df40f9fea3c29b14f1020f9d27044ce2c1a90b0e0e72c283363`  
		Last Modified: Tue, 10 Feb 2026 21:25:31 GMT  
		Size: 10.8 MB (10786975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7999dd527cff96d4d923b32f2fdc7608a6ca4424fa532173c2cd4ff58b53b67`  
		Last Modified: Tue, 10 Feb 2026 21:25:30 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:76e4ea0469de2f9548d6ca33be9fb8e9a21af1b331100e8c93acad9041b4d1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270602119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919614fea859085c93f0f2620586f983e6256e12ae046a9a4a57ffcc72cdce21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:48 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:48 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:48 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:54 GMT
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
	-	`sha256:f4545da495a95354686dc0238a92b34aa7866efee7c6a78e1aa02b572230b570`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 72.8 MB (72802225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af767d3bb84f3c7207d0e6fefac9e0951d10fc2f90d9d7c3d6f40bd2e301f7`  
		Last Modified: Tue, 10 Feb 2026 21:25:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5c93705e5617667916d5f05933c980db73167dba125e7752a0c32ed9f8f47917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10611981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ea40f61cd606942e199e75f9c025b7b8ba9146b0b54eddb6e13c8e6ee6b646`

```dockerfile
```

-	Layers:
	-	`sha256:3141a86b6e5373c5f8c031de6b13c2da13b6aa3a2aeea770661b4110b82128b1`  
		Last Modified: Tue, 10 Feb 2026 21:25:17 GMT  
		Size: 10.6 MB (10582894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6c16eabce6ec901213c80849861abe757261a1e3eda5bcb932d9e6af99bc84`  
		Last Modified: Tue, 10 Feb 2026 21:25:16 GMT  
		Size: 29.1 KB (29087 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:01c1cc836c799e8464815ffe6b4c17b4008fd5efc96d47511d78d2d1846049b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304656473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf57f277dfcb5ca2f2aaf22d7a4e1ac62661788e29fae795d21fc84d1f78879`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:01 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:01 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:01 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:11 GMT
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
	-	`sha256:e42862b12367ee1065711c0ac8df9327c9ab509758b30b8728d6213cf3e9380c`  
		Last Modified: Tue, 10 Feb 2026 21:25:39 GMT  
		Size: 98.3 MB (98304602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad77e9b09f8dfb42f8d398ade734f2c73fc1b86187a7db331b79c980d8dd12`  
		Last Modified: Tue, 10 Feb 2026 21:25:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:d414828240ab859b58694d72baf126a046adcaf51c53ff5379fb699a000f5f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10936609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f3eb59656b60e60909ad2b64660cdf35c0575ee9662be2c649b3977e47855d`

```dockerfile
```

-	Layers:
	-	`sha256:d66dcc0e20e359d28ce711bf30870710b6b1899c4bc1df254843616d4875ff35`  
		Last Modified: Tue, 10 Feb 2026 21:25:36 GMT  
		Size: 10.9 MB (10907478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248be2bcc72856cd97a6a4380a4aa5a2906ea1e32960d1126efcd5da62dd6258`  
		Last Modified: Tue, 10 Feb 2026 21:25:35 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:8494453c2fa061fe6e8d5816650cc946ca59b7fc84a4177c4b1c40fc4d737287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313515660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956edfca6cc8306a4d6b5314a1c4574845ac62484f4716e0134c3aaec0ed76a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 10 Feb 2026 21:25:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:25:00 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:25:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:25:00 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:25:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:25:00 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:25:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:25:07 GMT
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
	-	`sha256:9d7723434b921aaaec3ea1761a30320c459565456ac6eba1df267d5ad01df5d9`  
		Last Modified: Tue, 10 Feb 2026 21:25:35 GMT  
		Size: 100.6 MB (100607065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbfad3c600a3a9c8302db25d37648349b37e769601e5490f9bfb9f615fe5677`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 65.5 MB (65521738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b636bf3bcaaf03c4b26c55591e8cc54bb40b410d26c6027ae375223b808a264`  
		Last Modified: Tue, 10 Feb 2026 21:25:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:7de6c36ab4be7d5a5a6ed4524e3a3e819db14813f231fd752373a0c2413b48dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10787115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb053fe57c222504bf1a961024ae27a3fafa3871976496aab689619730a2f08`

```dockerfile
```

-	Layers:
	-	`sha256:a8f07ef9b7e732b2d98d2f7f8a40cfe6a2dbf97e9369cca4650a5f92b410a37a`  
		Last Modified: Tue, 10 Feb 2026 21:25:32 GMT  
		Size: 10.8 MB (10758218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5b19f1f717f11065ee55a6d6f58d37cad130c08385fc5809ab2e488d6117da`  
		Last Modified: Tue, 10 Feb 2026 21:25:31 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:070b53d204b97583a205770c0d91a1658f7e13b95acf5a62ddc5e2eae7eb6d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310737455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a7b0b0f072a5e330be08819a40ee72acde45abe8b999a6071bf1c220b960ae`
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
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:36 GMT
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
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ec2ea4c7ecfac088e7f60c9c0bcfa17286ead05e35ca5655100798438ff4c3`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:1455518987d85fd17793a7ccd519e2bf42e839c6487ceaf89d981ff7b8efa33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdd5746331ffe11ce5e6a51f2864250431fe4d1eac6813da7db44a212452019`

```dockerfile
```

-	Layers:
	-	`sha256:85a462ebd6942e9c50ec68c77d524e3f60ad4586a500c94161f43bcfed983f31`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 10.8 MB (10782787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530f56e5c958bbab8215173aa04a60acdf54e29cd630e3f3b5fda48b2fdea2bc`  
		Last Modified: Tue, 10 Feb 2026 21:25:49 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; riscv64

```console
$ docker pull golang@sha256:6273d0002e0dd473a4f372597aae20c530fba172144f45372094df38133b7e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336073217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c97355d7647f19a8da80a4dad4d41880803085c7f2116f58eb57337d52a0876`
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
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:26:13 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:26:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:26:13 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:26:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:26:30 GMT
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
	-	`sha256:b0e59666da981e3405c1b7fd86ade4932c92816496358034a16d9db56a3633b7`  
		Last Modified: Tue, 10 Feb 2026 21:32:56 GMT  
		Size: 65.1 MB (65055611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74afc761e2a6a2434adf94d57ef14b4b8dbd95715c17a65d6b2fbff8a076d852`  
		Last Modified: Tue, 10 Feb 2026 21:32:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:d00626367dc16a3fc6e4ec71240cbd2cce9205cca99cf7e2019687f5af7ca3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d833f524fa0697ff6e6f79e00c78c79ed58c6bd7e4f7f80a490ad159fd16d4`

```dockerfile
```

-	Layers:
	-	`sha256:59f057ecefd5d7c90c89bdf34e5e019712b3caf66f0bbcc8ac445c6e681416a3`  
		Last Modified: Tue, 10 Feb 2026 21:32:47 GMT  
		Size: 10.9 MB (10856620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e1569a8156f3f91196a9f60bd66360960ff76f54ec9d53b344a37e2d3e1b1d`  
		Last Modified: Tue, 10 Feb 2026 21:32:43 GMT  
		Size: 29.0 KB (29025 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:50c7a5797d9a727136c17f6bc0cae88f228a3b653adeeeb1cde3547028eee3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287145634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad2219bf4c085a7a8c4cd0405b0e42ef58b058cdc3c744027fab5816843eb7f`
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
# Tue, 10 Feb 2026 21:24:18 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:18 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:18 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:25 GMT
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
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c4a1280c9c86b709579683bf7dfbc2a5eace4c6bb785296310e038ca2c88c`  
		Last Modified: Tue, 10 Feb 2026 21:25:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:d1b794f68853ddd474b43eaa0c8a1992404e6d35a47cf3c3bb6c69aea6ea6746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10626151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b51590c7cfd1a09e5eded9423534968e6033d1b430b56a4a4ddff90ea69c7c8`

```dockerfile
```

-	Layers:
	-	`sha256:b5c37e986ec4a32905e73f96fe0c00eaf622910a0f1fabffb7736285ea4c6a80`  
		Last Modified: Tue, 10 Feb 2026 21:25:08 GMT  
		Size: 10.6 MB (10597375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d1d15a03f0239f21c7a28abbf56e0343a157ea53b4efa38acb26f5b09a9ade`  
		Last Modified: Tue, 10 Feb 2026 21:25:08 GMT  
		Size: 28.8 KB (28776 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:2225d7c7c0cb9d23f6f3e5eb77284fe9e017fab2a77074d88665c918dbd9eae3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1617274557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70b500467b8263ab259ede71703c586a43980218edcdd7b00c828e4ab222665`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 21:26:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 21:26:46 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 21:26:47 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 21:26:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 21:26:49 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 21:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:27:42 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 21:27:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 21:27:49 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:29:18 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:29:19 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f0ce23bf20e4e4b723c48737da5a809eaa74eaae29a6baa0c98c3a7aaf662e`  
		Last Modified: Tue, 10 Feb 2026 21:29:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5701c59a7f8317bd28e0da7cfa531b9eb5d25b8a9b98d6b7047db31ce46d33`  
		Last Modified: Tue, 10 Feb 2026 21:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7b7d3ea42a0e191b8407a1b5b569e0b161fc76c0ab8011088b51b9c833623e`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c79d245bad43d9d1c5771497a6134a98623f4fb016628394bc9ba8fabbe243`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d030477899e7ce381c5decec028af460368c2cc35145ae71cb07c3dd1b77b1`  
		Last Modified: Tue, 10 Feb 2026 21:29:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f55fa67d9c26d94e30082d3a9ae25c258190674c0814a9cd9852948b469b33`  
		Last Modified: Tue, 10 Feb 2026 21:29:33 GMT  
		Size: 51.3 MB (51263578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514b7b61912d146534043f561a8897989b1194c2118d2bced912590ed91adde0`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aec0225718c7856de0bc21f0aa9fbae0ea63d27564ad4199d9c5a11b7aefd4`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 398.3 KB (398324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ef57c9d89a0c311d8d894f68dcfe663719e915ef6782371e1645c1a22598a`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e285b7425b87af7e90a0d0539cbe391eb639586a7f533cef5f335da2e3969f6f`  
		Last Modified: Tue, 10 Feb 2026 21:29:36 GMT  
		Size: 69.8 MB (69841755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734603d9c9b5b37f9a3cb2516dd133366febab9cf9009d77e74aeffc5eb4b81a`  
		Last Modified: Tue, 10 Feb 2026 21:29:25 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:dfb3c1c79e23b69db93c647c6793e06ccc715aa6b0a1160e39453165e0c361ae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1957120180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59967a9aa2da2ee497b5517e38aabc8bfe85412336c10eca66c75b20bee3da00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 10 Feb 2026 21:23:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 21:23:57 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 21:23:58 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 21:23:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 21:23:59 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 21:25:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:25:33 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 21:25:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 21:25:43 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:27:56 GMT
RUN $url = 'https://dl.google.com/go/go1.26.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9bbe0fc64236b2b51f6255c05c4232532b8ecc0e6d2e00950bd3021d8a4d07d4'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 21:27:57 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9eeaa033510bbb49e86b8e5c86ba6e2e3c41cf872197eaf0a832fa9a68818`  
		Last Modified: Tue, 10 Feb 2026 21:28:18 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d43ab923e491d94833c68135fa0b29225e8c4d52c3199042ae814776854e0`  
		Last Modified: Tue, 10 Feb 2026 21:28:18 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b949b25637b2ea3dc38a1dd78388ad42dff48bca222d2f36935f4ee151251f2f`  
		Last Modified: Tue, 10 Feb 2026 21:28:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82572f5145421944e9cad4c198e839084d05bbb4398cce64597323493b4a948f`  
		Last Modified: Tue, 10 Feb 2026 21:28:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ebcc75e773c2d9c3c6b8a50f297687a87150757789ab3c85fce9ecb3c84c3`  
		Last Modified: Tue, 10 Feb 2026 21:28:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90330c474435ee119b07d0622302f6456772d72602675939a88db9142b9d26e`  
		Last Modified: Tue, 10 Feb 2026 21:28:23 GMT  
		Size: 51.4 MB (51358086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1d1e60122490a9014ba270c438730ca66e0e6f35d9b084de82a2dd70d467e`  
		Last Modified: Tue, 10 Feb 2026 21:28:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf78431b8e76c0c2f6005203db91007a979d4c06bb146e852d3c8dff901b785`  
		Last Modified: Tue, 10 Feb 2026 21:28:15 GMT  
		Size: 320.0 KB (319974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e03edd7c687d6f960a1bedc7893f4c212d33199309abbf62d74327cb0bfbd3`  
		Last Modified: Tue, 10 Feb 2026 21:28:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21680441bdcec6f871db151d910b8651b29699e811c1cfd6d13fa194f7d5b591`  
		Last Modified: Tue, 10 Feb 2026 21:28:27 GMT  
		Size: 69.8 MB (69772231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb573656e84a78f28b826e7d1937b89cc6273d0202e656a4a7279469477deca`  
		Last Modified: Tue, 10 Feb 2026 21:28:15 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
