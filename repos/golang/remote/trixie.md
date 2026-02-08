## `golang:trixie`

```console
$ docker pull golang@sha256:dfdd969010ba978942302cee078235da13aef030d22841e873545001d68a61a7
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

### `golang:trixie` - linux; amd64

```console
$ docker pull golang@sha256:7af63db8d8dc56289c8fa6d9883ad9d043c332755343a243dbb5d91984343a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304990159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4741e2c519579d44a174a5e64b4104dbd1ad73b7a9c53733131db4838ae3be3e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:03:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:03:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:03:41 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:03:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:03:48 GMT
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
	-	`sha256:d3b37a8f89c93c2b56d4f2cea38e4d53f9d7f8d10f0241ae1a526dab622bdf05`  
		Last Modified: Wed, 04 Feb 2026 17:04:16 GMT  
		Size: 102.1 MB (102138701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdf71b47847e47b44531d019e8eed7d243fd7189fe6b14cf6754724b04fbdd6`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 60.2 MB (60156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac7b480234dda467a567c0327f68728ccf10a679b4f797393e9b61161862427`  
		Last Modified: Wed, 04 Feb 2026 17:04:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7a61191dc198dc2b5da5fa76f0ee225b09e96981210700df73f7769f95674f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b8d881a9e072e5c4c7437aa03b378924253f9190d336e85c51d2403109b3d5`

```dockerfile
```

-	Layers:
	-	`sha256:8885891d139252d037afc3924c9139f4db157ec1894aefdafb62f5c2531130e4`  
		Last Modified: Wed, 04 Feb 2026 17:04:13 GMT  
		Size: 10.8 MB (10785503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e772ed12e235a2821e1d27e9637fedcdd613dab7eb39971509b28adbe1a7a6`  
		Last Modified: Wed, 04 Feb 2026 17:04:12 GMT  
		Size: 29.0 KB (28953 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:ddc844ca6dccfe63281d917d6bc253c5022003bf731fe11c9b0457fa9af14900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263926746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5f620a9a223c38017bc79b3f83d3a6743b97c39e6855b5903273c84aaa4e4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:03:24 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:03:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:03:24 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:03:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:03:24 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:03:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:03:27 GMT
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
	-	`sha256:5161545f852095383489ccc08abf3541bb88511e2f5ab6121bf74211f0c1e5c6`  
		Last Modified: Wed, 04 Feb 2026 17:03:52 GMT  
		Size: 72.8 MB (72783573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b7e6ac913cf5db56d036aaf335904f49acbba9f9a6464379470983dced635`  
		Last Modified: Wed, 04 Feb 2026 17:03:51 GMT  
		Size: 59.1 MB (59076165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4ef91856cd4d091e8186f1e6303293232301fd531c03b38194a5ba484c1497`  
		Last Modified: Wed, 04 Feb 2026 17:03:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3290eb8143e4facf5c0c0ca056e2242af9b70c9df7d53d2f221d6e2c07087898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f5b7d722f743809e5695b22d8d01a0d6b416727dfdb077e9fc457f21ffdc87`

```dockerfile
```

-	Layers:
	-	`sha256:b16c42613d2e3de3f09baab22de3dff22919f2ee9b6740a4dfaeeba984b022d2`  
		Last Modified: Wed, 04 Feb 2026 17:03:49 GMT  
		Size: 10.6 MB (10581424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74a3156e0bb22100862d01732d8fcefbb058a4edd9b9708f83f0c8d19731b41`  
		Last Modified: Wed, 04 Feb 2026 17:03:48 GMT  
		Size: 29.1 KB (29086 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:faf9b3ab3226a8296b9ab352a859c075519f2c17016dd5ea773445c27f6893f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298204814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9435d0bf0acfd6ff285521eeab2cc014fe890ede255b1608a67a0874bce6ef25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:04:02 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:02 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:02 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:02 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:12 GMT
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
	-	`sha256:d2293ce4668c8cbb74640605d57aeeb460396b307529fc68cff5b1fb674c2265`  
		Last Modified: Wed, 04 Feb 2026 17:04:42 GMT  
		Size: 98.3 MB (98283497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fac6022b2ee873ba16b3704e4dc9dfb3d60a32c4c3577bd7c9d971bdb2f1f7`  
		Last Modified: Wed, 04 Feb 2026 17:04:17 GMT  
		Size: 57.7 MB (57653449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cc7f1016b827ec42444f762792cbe7e6e8aa261c637657eb00b6107e6f4015`  
		Last Modified: Wed, 04 Feb 2026 17:04:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:75be4cdb2b169afe00676f4c154bcfd91b59006cdc5239c60a62ce6f4ff16bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76e2a2fa75dd6d68e298b41d72c6038889a0d217bdf13b930cd79604bc60266`

```dockerfile
```

-	Layers:
	-	`sha256:be126afa7de9c3b632a703125317f39003c7b5c71c4e7bca091d974aa71b56e2`  
		Last Modified: Wed, 04 Feb 2026 17:04:36 GMT  
		Size: 10.9 MB (10906006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0036bcc1fcee8de50cbaa8ce10da404c9cccf0280b1183d94d7c363dfd417b5`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; 386

```console
$ docker pull golang@sha256:11dcd46e924310d4a38f4994c5783eeb2baf99e3999312bec1160185cab8980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306842547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126ce41f963e513f18a9aa5aeef1faa0ece3ef708b4f0f1a10e9a583c1d0fb32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 04 Feb 2026 17:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 17:04:12 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:12 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:12 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:14 GMT
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
	-	`sha256:c5c5b1c5ad6c8ec98b0ff35759eceb007db6ad8724489f49164587e0cce1f197`  
		Last Modified: Wed, 04 Feb 2026 17:04:42 GMT  
		Size: 100.6 MB (100582783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5c0b9aa7ecd0690c22b5272d78803efbb58eb70a587a69b65a9a3f03d3f902`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 58.9 MB (58872907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49288bca90fcc725b89f889465490f86b741b7c60bb71ba394db7e1df0d184`  
		Last Modified: Wed, 04 Feb 2026 17:04:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c08ed2090c9196a31080da8af865740a1263829308df160a8361f6827b894959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ee5b947b93edc737101a29a1fc47615f6d7d4c258b1c9a8da10e74754689e9`

```dockerfile
```

-	Layers:
	-	`sha256:9072270a6e631b8b15d33e4a92a16f87f0b36bbe1dda59377b5f194eb7b34d69`  
		Last Modified: Wed, 04 Feb 2026 17:04:40 GMT  
		Size: 10.8 MB (10756748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04383b7bef5e920e86815d5cbfe18fcc937797d5b12b13011a6dc47a06765f95`  
		Last Modified: Wed, 04 Feb 2026 17:04:39 GMT  
		Size: 28.9 KB (28897 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:68ac89068b9f63f6f86f0322e9da589d298080e24a418832511c62c31cabb396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304124048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e82edad132b2d95ed1ae29ee68e79a4657c99b4b022a0682266e64d7ef41fa`
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
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:05:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:05:37 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:05:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:05:42 GMT
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
	-	`sha256:7d69879181021786809c25fc5c953b51116d19e9c3c6d50663a1bdc3a339c1bd`  
		Last Modified: Wed, 04 Feb 2026 17:06:35 GMT  
		Size: 58.1 MB (58136923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ef0f4f59f5de676ffd93a9d7ec216ba9d36c7d98f09aeb42f2a7ce73cc1a5c`  
		Last Modified: Wed, 04 Feb 2026 17:06:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:66b878efd4fa8e268e700476c623c9026a4c1cf32d8fea08ca7a175d1c0d9d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf76c2f3470426c12092cb9dbebf502228a281abe46e1a935ba5dc3fd913eac7`

```dockerfile
```

-	Layers:
	-	`sha256:c850ebfe393bb00c85cfaa37bf21a7526497cee896c6f7e3394dd9c05f23aa4a`  
		Last Modified: Wed, 04 Feb 2026 17:06:33 GMT  
		Size: 10.8 MB (10781313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34fd09ecb49aba2b2426df444bf486d3e3acecdc61d0b9cf9c56efd7847b5fc`  
		Last Modified: Wed, 04 Feb 2026 17:06:33 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; riscv64

```console
$ docker pull golang@sha256:cf18904cb3841d8d62b295d4f2d25eb675ae6905e8927ece4fee1446dea44833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329691814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a926bf93d77dc586d84c34064eab9d9f0aef4a912c14fbe6b1db704243400c`
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
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOLANG_VERSION=1.25.7
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Feb 2026 12:03:30 GMT
ENV GOPATH=/go
# Fri, 06 Feb 2026 12:03:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 12:03:30 GMT
COPY /target/ / # buildkit
# Sun, 08 Feb 2026 00:52:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 08 Feb 2026 00:52:03 GMT
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
	-	`sha256:fcc7a4defc6ed5152e9b8491720ca46efa70b0fed648253c440f39924818c17b`  
		Last Modified: Fri, 06 Feb 2026 12:06:30 GMT  
		Size: 58.7 MB (58674209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31e9a8e4f08a1e49484a35d10be0a8df1cefad6561e89a6b25b0cc8798ac4cc`  
		Last Modified: Sun, 08 Feb 2026 00:56:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7a3c9ae7b0b3f364aca5e43368c0ec53a5d8217dc0262c4185251590ef64e68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4072213a8e423594b5825097cb675a291db7456f596dd2bb554903203d11e4`

```dockerfile
```

-	Layers:
	-	`sha256:e5fc7a8b791a09965a015d0b9ac5c88a5bdb6473fab144058882335fee3a62cc`  
		Last Modified: Sun, 08 Feb 2026 00:56:41 GMT  
		Size: 10.9 MB (10855146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad56992321040ab7cc174e99253c091c6b8c8b0141959bcc56eec45890f67098`  
		Last Modified: Sun, 08 Feb 2026 00:56:39 GMT  
		Size: 29.0 KB (29023 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:trixie` - linux; s390x

```console
$ docker pull golang@sha256:1a8691df9139ea421b9656bdff2f1a7b0dcae905b890368bb366ec978c9f861c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280216075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80b741b8349ebac16740d83b2e7c5a348133e686123711a89c15274c48fefcd`
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
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:03 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:07 GMT
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
	-	`sha256:22f8f0a3fdc9e8378ae51ec0652c2aa7b3fe566439364495bae28720620458ab`  
		Last Modified: Wed, 04 Feb 2026 17:04:51 GMT  
		Size: 59.5 MB (59494139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e1653a8456391f7e1d1dedf3d83c022179955432539021f81e7e83724f062`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:trixie` - unknown; unknown

```console
$ docker pull golang@sha256:80be7ea875229e20f97cc40fc54cad4a1d7f166fbb9fede4eaa2f6a0b6824d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775b8ae022c9c4e6b9f4673ab44bf96a83dd61191b8a95747ab4b3654d4eb302`

```dockerfile
```

-	Layers:
	-	`sha256:7beecf1288550083875f0f8c7e01c7de613a0f19fc747c98cba12b1be3272273`  
		Last Modified: Wed, 04 Feb 2026 17:05:03 GMT  
		Size: 10.6 MB (10595903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bdd0d37055e8fc75e302c0a2e2743a04cdcf8c1c8d1d26a87fd031efd03a90`  
		Last Modified: Wed, 04 Feb 2026 17:05:02 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json
