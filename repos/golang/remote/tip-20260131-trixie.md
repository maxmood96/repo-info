## `golang:tip-20260131-trixie`

```console
$ docker pull golang@sha256:64a1dd4eddceefa997f6197fe69ffd7e724c9402a1f0ebb21f1b79e9e383100c
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

### `golang:tip-20260131-trixie` - linux; amd64

```console
$ docker pull golang@sha256:d4f83d2c4b961f22a2eba4dc9d4f38afa618a19bae7e951099c74d91c288782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338166500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6912be2ec510c355ea5654cf74e1448c1022d2805920afed47df57501cded5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:09:32 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:32 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:32 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:35 GMT
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
	-	`sha256:cd6dc5808f7d73635c6b2ca4ab30e0ccec7b407e227cee6a5f4f6e05e08b2c6a`  
		Last Modified: Wed, 04 Feb 2026 17:10:04 GMT  
		Size: 102.1 MB (102138608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d77c5071552ccc1b498b00d6bad89feb028d4ca1997f547fb5b93cbfe4679fc`  
		Last Modified: Wed, 04 Feb 2026 17:09:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9d041159110c15620e22ad8955b5f7a034017cf188d3836978c77e2333ca3758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d97df7d339a807752d35a0a79bcb9ed270a0c6af2b8ef4b0304b322033e422`

```dockerfile
```

-	Layers:
	-	`sha256:df3f82ba455a5b2c926a60e52197d2ad4fc33ffc5ca9403a3b5710ac5decd7fd`  
		Last Modified: Wed, 04 Feb 2026 17:10:00 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ae31d5d064e359fe4493b22ada2018f0730d9d6fb1e6da93fe8b2358581f73`  
		Last Modified: Wed, 04 Feb 2026 17:09:59 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:25efe47ec21eeb183b38527f7bf1206682fe353503410b9171ab2d9e052bbdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294326875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1a76b02cb2dc8bb9e5ff67ce919a02c7a9b95d7376b47a56761b22108eaf59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:10:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:10:12 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:10:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:10:12 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:10:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:10:15 GMT
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
	-	`sha256:0e23b0d7b9d54babadd489ce63d7e1f601a70f4fd724ebe8b9a1f2cbd548742e`  
		Last Modified: Wed, 04 Feb 2026 17:10:40 GMT  
		Size: 72.8 MB (72783436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28b215068e64202938b2a62c7ca412e57076257ec09960f740933fc899542eb`  
		Last Modified: Wed, 04 Feb 2026 17:10:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:87a57a68c4fec1db99e0cab39bacae1b84ea970ef18f103735651b892767712f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d835b565b695b984843165b70d2e9be888bac9f6b960467d10ea841581c0c317`

```dockerfile
```

-	Layers:
	-	`sha256:ecb3eea81e92f04e4fe120e1098adab1afd87004c4c2542a4a942f5bd6613a8c`  
		Last Modified: Wed, 04 Feb 2026 17:10:39 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd64a9a6e4e497dd98e7c2047d741cfb33643d82542a28297df9c36792ccf2b6`  
		Last Modified: Wed, 04 Feb 2026 17:10:38 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f31ceee578de12a170ac703c201c285f8c039f9219aed453ba2f45f3ff8d76cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328926925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e51866e6b5abdecd0f142f3cb0032d4d460d54e4f6b898145d9d185e0e3d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:09:02 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:02 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:02 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:05 GMT
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
	-	`sha256:baaced121a795f2fa99f69c2fa8cc51de1a85679619a61aa4b2470dc9dda4e58`  
		Last Modified: Wed, 04 Feb 2026 17:09:31 GMT  
		Size: 98.3 MB (98283358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61441411465bbcdd86b79a33db2baffe3c247f2cf9fabbab970f0e323e8211e2`  
		Last Modified: Wed, 04 Feb 2026 17:09:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:81564ff3541d9db02ac6392220fb8ae7aa2604730ded83f36e4eac0328d676ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc0a80546acf90ab0bce80ffb01bcbe5abe90d6c087deb21d04992370d1b81d`

```dockerfile
```

-	Layers:
	-	`sha256:2fd00a9bc024b76e06673caea36d93bddd1f7c002f1ed521b5a6e6dfe78e50a6`  
		Last Modified: Wed, 04 Feb 2026 17:09:29 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44af320d791f44364abacf5e356859eaef2d687b08689c7634cbf40f3c0608ac`  
		Last Modified: Wed, 04 Feb 2026 17:09:29 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; 386

```console
$ docker pull golang@sha256:2053db20d582a2ba9819be3b0e989fed9134567e0d891bbd2964896ae1010dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339375728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dea7257ca44523ca9170f7c5d06a369e9dd6c082fa9adeefd7f00f6613d3a3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:09:21 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:09:21 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:09:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:09:21 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:09:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:09:23 GMT
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
	-	`sha256:8ce7c9e96632d28e28137c517d7dfd17e9f2c321128a9ed94068847afc6c4f23`  
		Last Modified: Wed, 04 Feb 2026 17:09:48 GMT  
		Size: 100.6 MB (100582635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc715818892651794fdd6223f7b454d2d5bd467f00808211e471843ac2a1d00`  
		Last Modified: Wed, 04 Feb 2026 17:09:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9bd533514f63b4fbbab27ef469d88dce7c26599dcd18cd2aa675929aba1c97a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611fb6eecf829d0102867ce2d4d93764af0e5ec44d3f6e86175281fe7538226b`

```dockerfile
```

-	Layers:
	-	`sha256:3574d43b0cc2916bb0db2a5b3f0b6bc7ab557f659c2b25c8477331b83e6328fb`  
		Last Modified: Wed, 04 Feb 2026 17:09:46 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b781093c5ab3f653ba8e90ca9d0841a5a480bca2100246fc6c51b970393cce6b`  
		Last Modified: Wed, 04 Feb 2026 17:09:45 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:98d5731feb912688e115ed6e667d0002384ae661859fd0688619fd8545f199b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335994491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0716c4983d479027f6efb05364062a1e9f5f13a54a50a71c0c0dc4beac482466`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 12:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 16:29:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 16:29:19 GMT
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
	-	`sha256:36e28e1c3e5fd5ced8c9244f622cdb6d1cbf2cd8214985f25bb15c5537fedafa`  
		Last Modified: Tue, 03 Feb 2026 12:48:55 GMT  
		Size: 92.8 MB (92844494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2de6609bbb9f6cd18291a04a70351eb545ee9a938442a3fb3b53ee46981209e`  
		Last Modified: Tue, 03 Feb 2026 16:30:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4165e84d158fd8bf09b6eb3e607ae9d3db9d0093364d23c7d378ab6dffd1b630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ae08e8f1d88d58a8e22569740fe3e081131b6bbd4586c0eea5e0fe56d3ed5`

```dockerfile
```

-	Layers:
	-	`sha256:da2ea886fdddb2fd9abb5f80bde97c11652b42d833dff18ad51194ab83abb033`  
		Last Modified: Wed, 04 Feb 2026 17:49:14 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b792b5385cd38a073ddc677d3aaf36300379448e46fc87ef05b2a1954c2891f`  
		Last Modified: Wed, 04 Feb 2026 17:49:14 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:3032dea10b94523915b6f8be596c9acd91d49177bc0b792f5d1a0df6b983230d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361574905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc366c12bee0a45980907b38d7291f1e4ee3ca5645f85959181e09bee7da953`
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
# Sun, 08 Feb 2026 01:41:38 GMT
ENV GOTOOLCHAIN=local
# Sun, 08 Feb 2026 01:41:38 GMT
ENV GOPATH=/go
# Sun, 08 Feb 2026 01:41:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 08 Feb 2026 01:41:38 GMT
COPY /target/ / # buildkit
# Sun, 08 Feb 2026 04:53:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 08 Feb 2026 04:53:48 GMT
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
	-	`sha256:dc3c8f3022c37addebb7f3bba04877b6aa3acbe5feb276f525d0db506f58caad`  
		Last Modified: Tue, 03 Feb 2026 08:06:29 GMT  
		Size: 90.6 MB (90557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2d735b153c1f47b0527c3e550a1bf46fdb976e88bbdfbb57c67e6183839895`  
		Last Modified: Sun, 08 Feb 2026 04:58:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:05869f460e0a886213a0772058ceefd2efc67af997ec4015b9080fffc48eed4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71351b975f068745d373b8afb06fcd981c6f7b7dd25d49c9a062f8928d041870`

```dockerfile
```

-	Layers:
	-	`sha256:113aa16db950c5bc47c1534e21b8ef415217611fe6ca8a904200c7949e914ba1`  
		Last Modified: Sun, 08 Feb 2026 04:58:41 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af74f3ce25b6ffc46d19b241627169ee4dfb9719cbf612b52aeb4364e186c2e4`  
		Last Modified: Sun, 08 Feb 2026 04:58:39 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260131-trixie` - linux; s390x

```console
$ docker pull golang@sha256:1cf1c527e424f71653494a01e4510e5db742ab5df2bbcc47841b58918e24158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313292378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6343d7fd96d0eaf88b02f5d80ae5efc53fdc2e8fe12c0dde59d17ca2697c0c94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:15:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:28:52 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:28:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:28:52 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:12:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:12:51 GMT
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
	-	`sha256:4214fb4364cd89307f3d3f0f8973196d093c5d30f95042cef1760cf1ccaa7c41`  
		Last Modified: Tue, 03 Feb 2026 06:16:15 GMT  
		Size: 75.9 MB (75949568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3998cbda3cc399aefd41fad17e120e7a6bcfa51d205283ee13315b1e3c7306b7`  
		Last Modified: Wed, 04 Feb 2026 17:13:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260131-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2246a6909e41aeb97154daa8664e0bdbb62f398b8d31b6309a0165cc25a0c1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc22935e4c3f20917762e6ccadb368ef8b2beefb72efedd6b5e4617f9ecf382`

```dockerfile
```

-	Layers:
	-	`sha256:68c5c3f4b1415c793ce838710d938d720bf6db24ae6f37416beee654597fb517`  
		Last Modified: Wed, 04 Feb 2026 17:13:19 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f6c5e18a4c59d9353543092f40a96ae33ad231bf88ceed4dc4fd149c29ca75`  
		Last Modified: Wed, 04 Feb 2026 17:13:19 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
