<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.2`](#spiped162)
-	[`spiped:1.6.2-alpine`](#spiped162-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:e3d39e73d6424fedca73f1ca85c21caa2ad5761d5e5158c694a0eabb04833795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:02fccb51b3a730618196652a12e3742185a8cbcbddf61a7e3c2ea67d45946793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38001731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac53ff2d9809b4fc230387d61cff0e5b37589998a790f14fba0420a4e908fd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c9031636414115a0bc8b844e9606108e85da9feb9e79941c5ec98c50c2455`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e87e282d4e28e003ee5b811b08b599c9e24e0a9f5987831ce99cc4038296e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 2.4 MB (2401338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9200e57c9bb4c71cff41ed342fdb72e7e5f6eaad2634e216ec7c00b1e4f771`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 6.5 MB (6470859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd10c6b252c12d89b5ff82b86f4ed0ee19fb19ec7075beecffcada0cd54366`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b470f07950abcef81da28ba78c167652ef0bd892184f999c730531f21d7e7fbe`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3bc99b75327213648a1d3a8e0fdaed76a80f5f6917cce02dff41ee99dd3ccf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16753d34e5841675e452ca01b40156651941389b2225d3adba65d3d7040f8224`

```dockerfile
```

-	Layers:
	-	`sha256:b47e02ed9917bdf537f10a957dada4a31fd5f846e8bb61cd9e155604ae39ce7e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 3.5 MB (3520915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3f446508a124780df57b8be6ecb3e69e8bebef18aac1f099d844b42740a6f8`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:1f94597a09c5420c2af2377b3f91f2c590b3edf749b3a9cdc5a51ecfdf09d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e615da381f04a7160c330896dc5e879fff71d3946b9662b2fc4da8f3ab72f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db87a09418d551ed1ddad877ac8fba0044c63c3c2b74bb92e6d39b704f87368d`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4802a9a513a6a3a3768043cbdfc03efd3df3f3345aa5716d2e8dffedc08b1143`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 2.0 MB (1997198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e01a4aea45f2a75c4cec3db156876d27e95e9fac2455efa8d24a5532bc153`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 5.1 MB (5138206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20d54d63366bdf7b998c915744fcdf90e8158cf8cba363fb032224370a3f94`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2a2efe8e9d736a954b2c18dbcfd99973f9f0cd63a5cb01264b50789e62d02`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b13824ee820b723b464a55b075fc9c973a7f0dffbdd29b252ee2ec6fd7131fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54edc359aa27b9794b1f7c96b2bb88705306ec22501a0986223cbb627fb59b47`

```dockerfile
```

-	Layers:
	-	`sha256:8355f8bfc3fe92b56fade2c4fb6d173f2d409335c9fe5efcf9d9905a4fc83361`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 3.5 MB (3491402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da14c75fd5a3d90ec434715c6a868e657f733f8c6f603acc1b569672306ecc1a`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dd743d8cfb2c799ea4231abec5c9c4ff7edff59975bbcda763a62bd260f83296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31456448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862b7a6b66d4482dd521688bae87c2729d769e3c0a8b6ea7cca01c5f312ca81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26454acc685f16ba00f0fd4aa30540425d42162300f007710673e52be043ec`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c3e0987721d924c02e5180d292ba237cd059ecbf6d1402a2ffcd226118a4f`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.9 MB (1855575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8b4d7f3bee254ed67cb250a5cb414d0fa5ada24a17992028795bd2fe059a0`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 4.9 MB (4880422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d521304bf740f64c097b0f4d3e998be7af8ab60044658ce8e2bc33582aeea562`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af1a7d1865356be7e9818a87cbecd35b86c542a33648a9be80f3a627398ff3`  
		Last Modified: Tue, 12 Nov 2024 15:30:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:143659b05d5fe1d19bbfd34eb0b0cfa1485dfea5c0caa853128d25d60d7825c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86032dd217b8c77185e386b22d6d332d4b6fd2cddf85c0a64df21f87fd1501c`

```dockerfile
```

-	Layers:
	-	`sha256:518b6630fbdb582debd5c4c46f8039b8f44195625f4400d4bb99b9401c419a1b`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 3.5 MB (3490893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6091081ed8d7f521ff0367b2fa7f66c5aa8240dbd8d7e712d30aeeffa79fb698`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8ef9312a0fdc8b92811d1d9657bf499db94d9b44ca98943e46eafa10cad58a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdfe29f5a38745b26b0a25ca56f43fbbddf727ebfc0b1ee7768601d7086f0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6c9a6dd794e1ed81dda37d02d3f23720f08189789c5f7fd0e17e046cf527e`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a914242a633c501864bccf609f0293d6ee4696ceac0bf74ccdc101b9c87483`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 2.2 MB (2247005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f56f562b230c429d639a172bbdbcfe017259e35e426197b4e9883b719fa93`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 5.5 MB (5481042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479dffbae58b3cdbe38bbed543f021e4299d588ae316f600104eca432152ccb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad01041c69cbbcefbf0a4ec453067f7db839dac2626d4f3f24adcc61e4f9bb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ebee9fa7e9afd48396302673a9252fd0fc7d56699c9316edf249f4e1f1b56e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50f7a69dcc7de28bec6996b147692958e6036b467ae55f6a170cb7fdaf0412`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5f6db1a11202d794574e24fece55d22205533180b9afdcf9e121468f1305b`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 3.5 MB (3492105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3374b525294173556b47123164944e536280773ae3ad1860af13f8bb426e3c`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:737e986d3ef60ed8830756931370aadbbc35c470cfcdbf3b37c1ff9495476128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38487066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015424fd76826195faac03d651002cf1171d9aca7cb6cac6bddb0d1ecdcdd8ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948637f4f555335bfea377215a90d164550e610058376f04c1b248876c0c47a`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b22510c35cc7cf8aedf1deee54533fd6b8d65ecd3bf49c80db67ece7a1edd2`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 2.4 MB (2398654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2800ed116932c0e846f7c7fffc55ace51d2b20e2254422a7966b44582f82f`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 5.9 MB (5941423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa575de140babafc47d340eeee5006016216aa9f50f5477cb2ce015a9f3218`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a2266b94596824891a07b27943af369135fb023a271e21e5bb20a946b2423`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:5518303d2b053e8128e0a806a12519370019e47d7b5b830bb54fcc4ad6ada5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d1558a4b6a4feeb09f779d05e60cb323dabd626bffb85f5816ec957025d03`

```dockerfile
```

-	Layers:
	-	`sha256:5b095849f6773c7c1ab56ad90a543e72da0ef69f0ecc27f6b248a9b5a2ffb3d3`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 3.5 MB (3514838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118929ccd9b9af5eaed5b240f4dbabd28b85fed458a3d9a12357d6295eaf20d1`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:0624ddac36d0a7ddbed7a4d1e96bc12408dede646ec00185081a40150d8d5d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36770390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dc63047f9926f6d2923676ff7656b5082713e12548f51058ddc50df5a3fd79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c77610d2c9af230e6e756e75398d01603d27c3467c884026c959f2ad40327`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6f8e71a2f1a37272bbdea88d14140c219a3e464d95cc27b2c975f187878ac`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.8 MB (1840578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4f114c249a163dcb9ee96873884c73f1c12e7b1e6c35e7d5ac56bbdd62c58`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 5.8 MB (5803489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0163814f8e0713ef82421f4884e0854c012d708bf4553bd4a79e43639fcce`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e644402e5e54bbfb5881f757e4329ef6fe334d20937810b832932b84a29b38`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ff1fe07cd6e788dc36a2521a7ba08d8d2e4f181b40c022e57cb202e95890535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b7576b893c384675fcebff96036ad796221ff2aa8c2b25fb235f2d52e3e7f`

```dockerfile
```

-	Layers:
	-	`sha256:7a509f4df839959f6049ec675b75f06e15d8aa1e9f25110d50d273e66eacdce0`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:1f2b0289f942ad1d147d7835b778fbd8dd009c4d7d217307d448d47dd342195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42131785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f62ad79133a652bc9b8924a9735bffedb08d5e7719e37c6d665e3d5afa92b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5932154388a6408863b1adb85966d65c76b1f1bb2ee20c1d3b10050983ebe`  
		Last Modified: Tue, 12 Nov 2024 08:07:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e2cd0d3193b040bbea27b493c8e6caf90148e2dc631373727d360e67cc00b`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 2.6 MB (2582085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4037acbb39d0315cb87be86e0494accb370f62b7e2920b332bc1b2a194872a`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 6.4 MB (6422808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d414ce94f9a23aa064a4a0c02f427e90bc63f56bf86f1e49d1f80047a678106f`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff03712da36b0fb092c45296793e1a6f86d62aa663929a9cd1b6a72119471ca`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:43eb28d2400ddec59bf666083b56fb75203ffd48eb075271990a43898c12fd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e5df906a8916e5ba51f60fca91067cfa1d60d46d91296bd4dba6241c4749d1`

```dockerfile
```

-	Layers:
	-	`sha256:2f91c23a45c50b096d8f809f5429a689c2b136c947fe447420b7f4874d3beee6`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 3.5 MB (3506557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d7096fa91901f54fa53ddd42d0638abba60d3083391dfc0efb5cf4cd4a101`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:0eb919bca91f6d4d9ad05b746086c59f9e22c3155c15ae4428890224ed68a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34947755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81952c610a5c6fc901a5ed261848055206cd195af1dc330c4ba02e209ac0101c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377dc54166a948ed8a9a616bfbda9d61e899b64d6f7daa2f89c45a8ad5fce7ae`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2102bd259c13530f5ebbd0eb2312b6abcf70ca2b36d47d204c5f476d4c6bfde`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 2.1 MB (2068739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a777b4f9aeecf100ba857234d9cbacc950a75e10ab1fa5bfd7e8447f5c6fce76`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 5.4 MB (5385847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3babab4816aee1453478ae8cffd3cb6af3af67e5ef97ea881e8d1320e8c09333`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a627a72dbe54e08097f9aa496b873b2fed610f1a4532679809379430c2de11`  
		Last Modified: Tue, 12 Nov 2024 08:43:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3c4caefe3199d7c21c37de5e12257c5deacf698116b1ef49283a3cd727c5cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dc0a4518739ee8324b44f9e5a5f24494ffa6d283c046b61945f61cd958d3fc`

```dockerfile
```

-	Layers:
	-	`sha256:443216e4433ea0db398eb6ca46f6cb144e31db38f69cfb6ac411580223065e2f`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 3.5 MB (3509088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6153e931e52aeb0af765bd5b8dc939721cbda80556d83fe7dfba13596f3543e9`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:879a585b679290d4e54c04e34fc629ccf897bd10d8a73f6412e18ae98247ffc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:fc73e7236b6bef7ae4e927b48b5f9664ec1649c147bea9f2a1c59a6873ba7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe942b3c121009cdd9974db0f5820e5602448acd7a0a008460216b96b9d45b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35a75d4c2c9ec2f11caded5eb8c328382a7514f10e36cd88d52b7833c72a43`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753ce898cf51bfb141701861e58962bcfbf488858498f19dfced7295ff1964d`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdeab123af8ffdd5fee87d27bba647137362da0d65b8e1efec942f7b9a4cf7a`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 214.6 KB (214574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3e52678b5331c28014609747ec3773ee7f655677938ee75bd7a9cba76cfa30`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1898347b383d4b061e159823944d559655b0436512cbadefacf4db2805911`  
		Last Modified: Sun, 08 Sep 2024 17:35:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f87ef4375f368e30c6154a357caaf21da5ebbabeac773e74984b92d4ec45af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 KB (86167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b718e7b3d1ec3e5cd424eea757ac306bac092cc4ff50649efa5c991ad7d4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:74ca122aff7cd1770a8f2ad1bbe9efd239ef1ef2fccf3f4238b761f6ba4efbb9`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 72.0 KB (72045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44c59ce40148f46174cd2792c75bf5cdba058bc968551a0bffedd77dc30ae7`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:e3d39e73d6424fedca73f1ca85c21caa2ad5761d5e5158c694a0eabb04833795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:02fccb51b3a730618196652a12e3742185a8cbcbddf61a7e3c2ea67d45946793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38001731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac53ff2d9809b4fc230387d61cff0e5b37589998a790f14fba0420a4e908fd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c9031636414115a0bc8b844e9606108e85da9feb9e79941c5ec98c50c2455`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e87e282d4e28e003ee5b811b08b599c9e24e0a9f5987831ce99cc4038296e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 2.4 MB (2401338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9200e57c9bb4c71cff41ed342fdb72e7e5f6eaad2634e216ec7c00b1e4f771`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 6.5 MB (6470859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd10c6b252c12d89b5ff82b86f4ed0ee19fb19ec7075beecffcada0cd54366`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b470f07950abcef81da28ba78c167652ef0bd892184f999c730531f21d7e7fbe`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3bc99b75327213648a1d3a8e0fdaed76a80f5f6917cce02dff41ee99dd3ccf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16753d34e5841675e452ca01b40156651941389b2225d3adba65d3d7040f8224`

```dockerfile
```

-	Layers:
	-	`sha256:b47e02ed9917bdf537f10a957dada4a31fd5f846e8bb61cd9e155604ae39ce7e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 3.5 MB (3520915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3f446508a124780df57b8be6ecb3e69e8bebef18aac1f099d844b42740a6f8`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:1f94597a09c5420c2af2377b3f91f2c590b3edf749b3a9cdc5a51ecfdf09d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e615da381f04a7160c330896dc5e879fff71d3946b9662b2fc4da8f3ab72f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db87a09418d551ed1ddad877ac8fba0044c63c3c2b74bb92e6d39b704f87368d`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4802a9a513a6a3a3768043cbdfc03efd3df3f3345aa5716d2e8dffedc08b1143`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 2.0 MB (1997198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e01a4aea45f2a75c4cec3db156876d27e95e9fac2455efa8d24a5532bc153`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 5.1 MB (5138206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20d54d63366bdf7b998c915744fcdf90e8158cf8cba363fb032224370a3f94`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2a2efe8e9d736a954b2c18dbcfd99973f9f0cd63a5cb01264b50789e62d02`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b13824ee820b723b464a55b075fc9c973a7f0dffbdd29b252ee2ec6fd7131fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54edc359aa27b9794b1f7c96b2bb88705306ec22501a0986223cbb627fb59b47`

```dockerfile
```

-	Layers:
	-	`sha256:8355f8bfc3fe92b56fade2c4fb6d173f2d409335c9fe5efcf9d9905a4fc83361`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 3.5 MB (3491402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da14c75fd5a3d90ec434715c6a868e657f733f8c6f603acc1b569672306ecc1a`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dd743d8cfb2c799ea4231abec5c9c4ff7edff59975bbcda763a62bd260f83296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31456448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862b7a6b66d4482dd521688bae87c2729d769e3c0a8b6ea7cca01c5f312ca81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26454acc685f16ba00f0fd4aa30540425d42162300f007710673e52be043ec`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c3e0987721d924c02e5180d292ba237cd059ecbf6d1402a2ffcd226118a4f`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.9 MB (1855575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8b4d7f3bee254ed67cb250a5cb414d0fa5ada24a17992028795bd2fe059a0`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 4.9 MB (4880422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d521304bf740f64c097b0f4d3e998be7af8ab60044658ce8e2bc33582aeea562`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af1a7d1865356be7e9818a87cbecd35b86c542a33648a9be80f3a627398ff3`  
		Last Modified: Tue, 12 Nov 2024 15:30:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:143659b05d5fe1d19bbfd34eb0b0cfa1485dfea5c0caa853128d25d60d7825c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86032dd217b8c77185e386b22d6d332d4b6fd2cddf85c0a64df21f87fd1501c`

```dockerfile
```

-	Layers:
	-	`sha256:518b6630fbdb582debd5c4c46f8039b8f44195625f4400d4bb99b9401c419a1b`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 3.5 MB (3490893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6091081ed8d7f521ff0367b2fa7f66c5aa8240dbd8d7e712d30aeeffa79fb698`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8ef9312a0fdc8b92811d1d9657bf499db94d9b44ca98943e46eafa10cad58a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdfe29f5a38745b26b0a25ca56f43fbbddf727ebfc0b1ee7768601d7086f0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6c9a6dd794e1ed81dda37d02d3f23720f08189789c5f7fd0e17e046cf527e`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a914242a633c501864bccf609f0293d6ee4696ceac0bf74ccdc101b9c87483`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 2.2 MB (2247005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f56f562b230c429d639a172bbdbcfe017259e35e426197b4e9883b719fa93`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 5.5 MB (5481042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479dffbae58b3cdbe38bbed543f021e4299d588ae316f600104eca432152ccb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad01041c69cbbcefbf0a4ec453067f7db839dac2626d4f3f24adcc61e4f9bb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ebee9fa7e9afd48396302673a9252fd0fc7d56699c9316edf249f4e1f1b56e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50f7a69dcc7de28bec6996b147692958e6036b467ae55f6a170cb7fdaf0412`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5f6db1a11202d794574e24fece55d22205533180b9afdcf9e121468f1305b`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 3.5 MB (3492105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3374b525294173556b47123164944e536280773ae3ad1860af13f8bb426e3c`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:737e986d3ef60ed8830756931370aadbbc35c470cfcdbf3b37c1ff9495476128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38487066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015424fd76826195faac03d651002cf1171d9aca7cb6cac6bddb0d1ecdcdd8ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948637f4f555335bfea377215a90d164550e610058376f04c1b248876c0c47a`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b22510c35cc7cf8aedf1deee54533fd6b8d65ecd3bf49c80db67ece7a1edd2`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 2.4 MB (2398654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2800ed116932c0e846f7c7fffc55ace51d2b20e2254422a7966b44582f82f`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 5.9 MB (5941423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa575de140babafc47d340eeee5006016216aa9f50f5477cb2ce015a9f3218`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a2266b94596824891a07b27943af369135fb023a271e21e5bb20a946b2423`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:5518303d2b053e8128e0a806a12519370019e47d7b5b830bb54fcc4ad6ada5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d1558a4b6a4feeb09f779d05e60cb323dabd626bffb85f5816ec957025d03`

```dockerfile
```

-	Layers:
	-	`sha256:5b095849f6773c7c1ab56ad90a543e72da0ef69f0ecc27f6b248a9b5a2ffb3d3`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 3.5 MB (3514838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118929ccd9b9af5eaed5b240f4dbabd28b85fed458a3d9a12357d6295eaf20d1`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:0624ddac36d0a7ddbed7a4d1e96bc12408dede646ec00185081a40150d8d5d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36770390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dc63047f9926f6d2923676ff7656b5082713e12548f51058ddc50df5a3fd79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c77610d2c9af230e6e756e75398d01603d27c3467c884026c959f2ad40327`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6f8e71a2f1a37272bbdea88d14140c219a3e464d95cc27b2c975f187878ac`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.8 MB (1840578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4f114c249a163dcb9ee96873884c73f1c12e7b1e6c35e7d5ac56bbdd62c58`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 5.8 MB (5803489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0163814f8e0713ef82421f4884e0854c012d708bf4553bd4a79e43639fcce`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e644402e5e54bbfb5881f757e4329ef6fe334d20937810b832932b84a29b38`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ff1fe07cd6e788dc36a2521a7ba08d8d2e4f181b40c022e57cb202e95890535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b7576b893c384675fcebff96036ad796221ff2aa8c2b25fb235f2d52e3e7f`

```dockerfile
```

-	Layers:
	-	`sha256:7a509f4df839959f6049ec675b75f06e15d8aa1e9f25110d50d273e66eacdce0`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:1f2b0289f942ad1d147d7835b778fbd8dd009c4d7d217307d448d47dd342195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42131785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f62ad79133a652bc9b8924a9735bffedb08d5e7719e37c6d665e3d5afa92b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5932154388a6408863b1adb85966d65c76b1f1bb2ee20c1d3b10050983ebe`  
		Last Modified: Tue, 12 Nov 2024 08:07:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e2cd0d3193b040bbea27b493c8e6caf90148e2dc631373727d360e67cc00b`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 2.6 MB (2582085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4037acbb39d0315cb87be86e0494accb370f62b7e2920b332bc1b2a194872a`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 6.4 MB (6422808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d414ce94f9a23aa064a4a0c02f427e90bc63f56bf86f1e49d1f80047a678106f`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff03712da36b0fb092c45296793e1a6f86d62aa663929a9cd1b6a72119471ca`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:43eb28d2400ddec59bf666083b56fb75203ffd48eb075271990a43898c12fd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e5df906a8916e5ba51f60fca91067cfa1d60d46d91296bd4dba6241c4749d1`

```dockerfile
```

-	Layers:
	-	`sha256:2f91c23a45c50b096d8f809f5429a689c2b136c947fe447420b7f4874d3beee6`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 3.5 MB (3506557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d7096fa91901f54fa53ddd42d0638abba60d3083391dfc0efb5cf4cd4a101`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:0eb919bca91f6d4d9ad05b746086c59f9e22c3155c15ae4428890224ed68a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34947755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81952c610a5c6fc901a5ed261848055206cd195af1dc330c4ba02e209ac0101c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377dc54166a948ed8a9a616bfbda9d61e899b64d6f7daa2f89c45a8ad5fce7ae`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2102bd259c13530f5ebbd0eb2312b6abcf70ca2b36d47d204c5f476d4c6bfde`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 2.1 MB (2068739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a777b4f9aeecf100ba857234d9cbacc950a75e10ab1fa5bfd7e8447f5c6fce76`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 5.4 MB (5385847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3babab4816aee1453478ae8cffd3cb6af3af67e5ef97ea881e8d1320e8c09333`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a627a72dbe54e08097f9aa496b873b2fed610f1a4532679809379430c2de11`  
		Last Modified: Tue, 12 Nov 2024 08:43:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3c4caefe3199d7c21c37de5e12257c5deacf698116b1ef49283a3cd727c5cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dc0a4518739ee8324b44f9e5a5f24494ffa6d283c046b61945f61cd958d3fc`

```dockerfile
```

-	Layers:
	-	`sha256:443216e4433ea0db398eb6ca46f6cb144e31db38f69cfb6ac411580223065e2f`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 3.5 MB (3509088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6153e931e52aeb0af765bd5b8dc939721cbda80556d83fe7dfba13596f3543e9`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:879a585b679290d4e54c04e34fc629ccf897bd10d8a73f6412e18ae98247ffc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:fc73e7236b6bef7ae4e927b48b5f9664ec1649c147bea9f2a1c59a6873ba7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe942b3c121009cdd9974db0f5820e5602448acd7a0a008460216b96b9d45b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35a75d4c2c9ec2f11caded5eb8c328382a7514f10e36cd88d52b7833c72a43`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753ce898cf51bfb141701861e58962bcfbf488858498f19dfced7295ff1964d`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdeab123af8ffdd5fee87d27bba647137362da0d65b8e1efec942f7b9a4cf7a`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 214.6 KB (214574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3e52678b5331c28014609747ec3773ee7f655677938ee75bd7a9cba76cfa30`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1898347b383d4b061e159823944d559655b0436512cbadefacf4db2805911`  
		Last Modified: Sun, 08 Sep 2024 17:35:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f87ef4375f368e30c6154a357caaf21da5ebbabeac773e74984b92d4ec45af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 KB (86167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b718e7b3d1ec3e5cd424eea757ac306bac092cc4ff50649efa5c991ad7d4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:74ca122aff7cd1770a8f2ad1bbe9efd239ef1ef2fccf3f4238b761f6ba4efbb9`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 72.0 KB (72045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44c59ce40148f46174cd2792c75bf5cdba058bc968551a0bffedd77dc30ae7`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:e3d39e73d6424fedca73f1ca85c21caa2ad5761d5e5158c694a0eabb04833795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:02fccb51b3a730618196652a12e3742185a8cbcbddf61a7e3c2ea67d45946793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38001731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac53ff2d9809b4fc230387d61cff0e5b37589998a790f14fba0420a4e908fd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c9031636414115a0bc8b844e9606108e85da9feb9e79941c5ec98c50c2455`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e87e282d4e28e003ee5b811b08b599c9e24e0a9f5987831ce99cc4038296e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 2.4 MB (2401338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9200e57c9bb4c71cff41ed342fdb72e7e5f6eaad2634e216ec7c00b1e4f771`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 6.5 MB (6470859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd10c6b252c12d89b5ff82b86f4ed0ee19fb19ec7075beecffcada0cd54366`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b470f07950abcef81da28ba78c167652ef0bd892184f999c730531f21d7e7fbe`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:3bc99b75327213648a1d3a8e0fdaed76a80f5f6917cce02dff41ee99dd3ccf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16753d34e5841675e452ca01b40156651941389b2225d3adba65d3d7040f8224`

```dockerfile
```

-	Layers:
	-	`sha256:b47e02ed9917bdf537f10a957dada4a31fd5f846e8bb61cd9e155604ae39ce7e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 3.5 MB (3520915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3f446508a124780df57b8be6ecb3e69e8bebef18aac1f099d844b42740a6f8`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:1f94597a09c5420c2af2377b3f91f2c590b3edf749b3a9cdc5a51ecfdf09d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e615da381f04a7160c330896dc5e879fff71d3946b9662b2fc4da8f3ab72f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db87a09418d551ed1ddad877ac8fba0044c63c3c2b74bb92e6d39b704f87368d`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4802a9a513a6a3a3768043cbdfc03efd3df3f3345aa5716d2e8dffedc08b1143`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 2.0 MB (1997198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e01a4aea45f2a75c4cec3db156876d27e95e9fac2455efa8d24a5532bc153`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 5.1 MB (5138206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20d54d63366bdf7b998c915744fcdf90e8158cf8cba363fb032224370a3f94`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2a2efe8e9d736a954b2c18dbcfd99973f9f0cd63a5cb01264b50789e62d02`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:b13824ee820b723b464a55b075fc9c973a7f0dffbdd29b252ee2ec6fd7131fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54edc359aa27b9794b1f7c96b2bb88705306ec22501a0986223cbb627fb59b47`

```dockerfile
```

-	Layers:
	-	`sha256:8355f8bfc3fe92b56fade2c4fb6d173f2d409335c9fe5efcf9d9905a4fc83361`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 3.5 MB (3491402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da14c75fd5a3d90ec434715c6a868e657f733f8c6f603acc1b569672306ecc1a`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dd743d8cfb2c799ea4231abec5c9c4ff7edff59975bbcda763a62bd260f83296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31456448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862b7a6b66d4482dd521688bae87c2729d769e3c0a8b6ea7cca01c5f312ca81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26454acc685f16ba00f0fd4aa30540425d42162300f007710673e52be043ec`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c3e0987721d924c02e5180d292ba237cd059ecbf6d1402a2ffcd226118a4f`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.9 MB (1855575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8b4d7f3bee254ed67cb250a5cb414d0fa5ada24a17992028795bd2fe059a0`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 4.9 MB (4880422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d521304bf740f64c097b0f4d3e998be7af8ab60044658ce8e2bc33582aeea562`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af1a7d1865356be7e9818a87cbecd35b86c542a33648a9be80f3a627398ff3`  
		Last Modified: Tue, 12 Nov 2024 15:30:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:143659b05d5fe1d19bbfd34eb0b0cfa1485dfea5c0caa853128d25d60d7825c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86032dd217b8c77185e386b22d6d332d4b6fd2cddf85c0a64df21f87fd1501c`

```dockerfile
```

-	Layers:
	-	`sha256:518b6630fbdb582debd5c4c46f8039b8f44195625f4400d4bb99b9401c419a1b`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 3.5 MB (3490893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6091081ed8d7f521ff0367b2fa7f66c5aa8240dbd8d7e712d30aeeffa79fb698`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8ef9312a0fdc8b92811d1d9657bf499db94d9b44ca98943e46eafa10cad58a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdfe29f5a38745b26b0a25ca56f43fbbddf727ebfc0b1ee7768601d7086f0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6c9a6dd794e1ed81dda37d02d3f23720f08189789c5f7fd0e17e046cf527e`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a914242a633c501864bccf609f0293d6ee4696ceac0bf74ccdc101b9c87483`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 2.2 MB (2247005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f56f562b230c429d639a172bbdbcfe017259e35e426197b4e9883b719fa93`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 5.5 MB (5481042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479dffbae58b3cdbe38bbed543f021e4299d588ae316f600104eca432152ccb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad01041c69cbbcefbf0a4ec453067f7db839dac2626d4f3f24adcc61e4f9bb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:ebee9fa7e9afd48396302673a9252fd0fc7d56699c9316edf249f4e1f1b56e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50f7a69dcc7de28bec6996b147692958e6036b467ae55f6a170cb7fdaf0412`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5f6db1a11202d794574e24fece55d22205533180b9afdcf9e121468f1305b`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 3.5 MB (3492105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3374b525294173556b47123164944e536280773ae3ad1860af13f8bb426e3c`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:737e986d3ef60ed8830756931370aadbbc35c470cfcdbf3b37c1ff9495476128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38487066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015424fd76826195faac03d651002cf1171d9aca7cb6cac6bddb0d1ecdcdd8ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948637f4f555335bfea377215a90d164550e610058376f04c1b248876c0c47a`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b22510c35cc7cf8aedf1deee54533fd6b8d65ecd3bf49c80db67ece7a1edd2`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 2.4 MB (2398654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2800ed116932c0e846f7c7fffc55ace51d2b20e2254422a7966b44582f82f`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 5.9 MB (5941423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa575de140babafc47d340eeee5006016216aa9f50f5477cb2ce015a9f3218`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a2266b94596824891a07b27943af369135fb023a271e21e5bb20a946b2423`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:5518303d2b053e8128e0a806a12519370019e47d7b5b830bb54fcc4ad6ada5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d1558a4b6a4feeb09f779d05e60cb323dabd626bffb85f5816ec957025d03`

```dockerfile
```

-	Layers:
	-	`sha256:5b095849f6773c7c1ab56ad90a543e72da0ef69f0ecc27f6b248a9b5a2ffb3d3`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 3.5 MB (3514838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118929ccd9b9af5eaed5b240f4dbabd28b85fed458a3d9a12357d6295eaf20d1`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:0624ddac36d0a7ddbed7a4d1e96bc12408dede646ec00185081a40150d8d5d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36770390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dc63047f9926f6d2923676ff7656b5082713e12548f51058ddc50df5a3fd79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c77610d2c9af230e6e756e75398d01603d27c3467c884026c959f2ad40327`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6f8e71a2f1a37272bbdea88d14140c219a3e464d95cc27b2c975f187878ac`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.8 MB (1840578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4f114c249a163dcb9ee96873884c73f1c12e7b1e6c35e7d5ac56bbdd62c58`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 5.8 MB (5803489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0163814f8e0713ef82421f4884e0854c012d708bf4553bd4a79e43639fcce`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e644402e5e54bbfb5881f757e4329ef6fe334d20937810b832932b84a29b38`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:ff1fe07cd6e788dc36a2521a7ba08d8d2e4f181b40c022e57cb202e95890535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b7576b893c384675fcebff96036ad796221ff2aa8c2b25fb235f2d52e3e7f`

```dockerfile
```

-	Layers:
	-	`sha256:7a509f4df839959f6049ec675b75f06e15d8aa1e9f25110d50d273e66eacdce0`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:1f2b0289f942ad1d147d7835b778fbd8dd009c4d7d217307d448d47dd342195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42131785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f62ad79133a652bc9b8924a9735bffedb08d5e7719e37c6d665e3d5afa92b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5932154388a6408863b1adb85966d65c76b1f1bb2ee20c1d3b10050983ebe`  
		Last Modified: Tue, 12 Nov 2024 08:07:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e2cd0d3193b040bbea27b493c8e6caf90148e2dc631373727d360e67cc00b`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 2.6 MB (2582085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4037acbb39d0315cb87be86e0494accb370f62b7e2920b332bc1b2a194872a`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 6.4 MB (6422808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d414ce94f9a23aa064a4a0c02f427e90bc63f56bf86f1e49d1f80047a678106f`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff03712da36b0fb092c45296793e1a6f86d62aa663929a9cd1b6a72119471ca`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:43eb28d2400ddec59bf666083b56fb75203ffd48eb075271990a43898c12fd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e5df906a8916e5ba51f60fca91067cfa1d60d46d91296bd4dba6241c4749d1`

```dockerfile
```

-	Layers:
	-	`sha256:2f91c23a45c50b096d8f809f5429a689c2b136c947fe447420b7f4874d3beee6`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 3.5 MB (3506557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d7096fa91901f54fa53ddd42d0638abba60d3083391dfc0efb5cf4cd4a101`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:0eb919bca91f6d4d9ad05b746086c59f9e22c3155c15ae4428890224ed68a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34947755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81952c610a5c6fc901a5ed261848055206cd195af1dc330c4ba02e209ac0101c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377dc54166a948ed8a9a616bfbda9d61e899b64d6f7daa2f89c45a8ad5fce7ae`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2102bd259c13530f5ebbd0eb2312b6abcf70ca2b36d47d204c5f476d4c6bfde`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 2.1 MB (2068739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a777b4f9aeecf100ba857234d9cbacc950a75e10ab1fa5bfd7e8447f5c6fce76`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 5.4 MB (5385847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3babab4816aee1453478ae8cffd3cb6af3af67e5ef97ea881e8d1320e8c09333`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a627a72dbe54e08097f9aa496b873b2fed610f1a4532679809379430c2de11`  
		Last Modified: Tue, 12 Nov 2024 08:43:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:3c4caefe3199d7c21c37de5e12257c5deacf698116b1ef49283a3cd727c5cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dc0a4518739ee8324b44f9e5a5f24494ffa6d283c046b61945f61cd958d3fc`

```dockerfile
```

-	Layers:
	-	`sha256:443216e4433ea0db398eb6ca46f6cb144e31db38f69cfb6ac411580223065e2f`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 3.5 MB (3509088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6153e931e52aeb0af765bd5b8dc939721cbda80556d83fe7dfba13596f3543e9`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:879a585b679290d4e54c04e34fc629ccf897bd10d8a73f6412e18ae98247ffc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:fc73e7236b6bef7ae4e927b48b5f9664ec1649c147bea9f2a1c59a6873ba7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe942b3c121009cdd9974db0f5820e5602448acd7a0a008460216b96b9d45b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35a75d4c2c9ec2f11caded5eb8c328382a7514f10e36cd88d52b7833c72a43`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753ce898cf51bfb141701861e58962bcfbf488858498f19dfced7295ff1964d`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdeab123af8ffdd5fee87d27bba647137362da0d65b8e1efec942f7b9a4cf7a`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 214.6 KB (214574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3e52678b5331c28014609747ec3773ee7f655677938ee75bd7a9cba76cfa30`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1898347b383d4b061e159823944d559655b0436512cbadefacf4db2805911`  
		Last Modified: Sun, 08 Sep 2024 17:35:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f87ef4375f368e30c6154a357caaf21da5ebbabeac773e74984b92d4ec45af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 KB (86167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b718e7b3d1ec3e5cd424eea757ac306bac092cc4ff50649efa5c991ad7d4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:74ca122aff7cd1770a8f2ad1bbe9efd239ef1ef2fccf3f4238b761f6ba4efbb9`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 72.0 KB (72045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44c59ce40148f46174cd2792c75bf5cdba058bc968551a0bffedd77dc30ae7`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:879a585b679290d4e54c04e34fc629ccf897bd10d8a73f6412e18ae98247ffc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:fc73e7236b6bef7ae4e927b48b5f9664ec1649c147bea9f2a1c59a6873ba7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe942b3c121009cdd9974db0f5820e5602448acd7a0a008460216b96b9d45b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35a75d4c2c9ec2f11caded5eb8c328382a7514f10e36cd88d52b7833c72a43`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753ce898cf51bfb141701861e58962bcfbf488858498f19dfced7295ff1964d`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdeab123af8ffdd5fee87d27bba647137362da0d65b8e1efec942f7b9a4cf7a`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 214.6 KB (214574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3e52678b5331c28014609747ec3773ee7f655677938ee75bd7a9cba76cfa30`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1898347b383d4b061e159823944d559655b0436512cbadefacf4db2805911`  
		Last Modified: Sun, 08 Sep 2024 17:35:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f87ef4375f368e30c6154a357caaf21da5ebbabeac773e74984b92d4ec45af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 KB (86167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b718e7b3d1ec3e5cd424eea757ac306bac092cc4ff50649efa5c991ad7d4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:74ca122aff7cd1770a8f2ad1bbe9efd239ef1ef2fccf3f4238b761f6ba4efbb9`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 72.0 KB (72045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44c59ce40148f46174cd2792c75bf5cdba058bc968551a0bffedd77dc30ae7`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:e3d39e73d6424fedca73f1ca85c21caa2ad5761d5e5158c694a0eabb04833795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:02fccb51b3a730618196652a12e3742185a8cbcbddf61a7e3c2ea67d45946793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38001731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac53ff2d9809b4fc230387d61cff0e5b37589998a790f14fba0420a4e908fd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c9031636414115a0bc8b844e9606108e85da9feb9e79941c5ec98c50c2455`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e87e282d4e28e003ee5b811b08b599c9e24e0a9f5987831ce99cc4038296e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 2.4 MB (2401338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9200e57c9bb4c71cff41ed342fdb72e7e5f6eaad2634e216ec7c00b1e4f771`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 6.5 MB (6470859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd10c6b252c12d89b5ff82b86f4ed0ee19fb19ec7075beecffcada0cd54366`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b470f07950abcef81da28ba78c167652ef0bd892184f999c730531f21d7e7fbe`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3bc99b75327213648a1d3a8e0fdaed76a80f5f6917cce02dff41ee99dd3ccf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16753d34e5841675e452ca01b40156651941389b2225d3adba65d3d7040f8224`

```dockerfile
```

-	Layers:
	-	`sha256:b47e02ed9917bdf537f10a957dada4a31fd5f846e8bb61cd9e155604ae39ce7e`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 3.5 MB (3520915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3f446508a124780df57b8be6ecb3e69e8bebef18aac1f099d844b42740a6f8`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:1f94597a09c5420c2af2377b3f91f2c590b3edf749b3a9cdc5a51ecfdf09d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e615da381f04a7160c330896dc5e879fff71d3946b9662b2fc4da8f3ab72f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db87a09418d551ed1ddad877ac8fba0044c63c3c2b74bb92e6d39b704f87368d`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4802a9a513a6a3a3768043cbdfc03efd3df3f3345aa5716d2e8dffedc08b1143`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 2.0 MB (1997198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e01a4aea45f2a75c4cec3db156876d27e95e9fac2455efa8d24a5532bc153`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 5.1 MB (5138206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20d54d63366bdf7b998c915744fcdf90e8158cf8cba363fb032224370a3f94`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2a2efe8e9d736a954b2c18dbcfd99973f9f0cd63a5cb01264b50789e62d02`  
		Last Modified: Tue, 12 Nov 2024 06:27:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b13824ee820b723b464a55b075fc9c973a7f0dffbdd29b252ee2ec6fd7131fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54edc359aa27b9794b1f7c96b2bb88705306ec22501a0986223cbb627fb59b47`

```dockerfile
```

-	Layers:
	-	`sha256:8355f8bfc3fe92b56fade2c4fb6d173f2d409335c9fe5efcf9d9905a4fc83361`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 3.5 MB (3491402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da14c75fd5a3d90ec434715c6a868e657f733f8c6f603acc1b569672306ecc1a`  
		Last Modified: Tue, 12 Nov 2024 06:27:16 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dd743d8cfb2c799ea4231abec5c9c4ff7edff59975bbcda763a62bd260f83296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31456448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862b7a6b66d4482dd521688bae87c2729d769e3c0a8b6ea7cca01c5f312ca81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26454acc685f16ba00f0fd4aa30540425d42162300f007710673e52be043ec`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c3e0987721d924c02e5180d292ba237cd059ecbf6d1402a2ffcd226118a4f`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 1.9 MB (1855575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8b4d7f3bee254ed67cb250a5cb414d0fa5ada24a17992028795bd2fe059a0`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 4.9 MB (4880422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d521304bf740f64c097b0f4d3e998be7af8ab60044658ce8e2bc33582aeea562`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af1a7d1865356be7e9818a87cbecd35b86c542a33648a9be80f3a627398ff3`  
		Last Modified: Tue, 12 Nov 2024 15:30:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:143659b05d5fe1d19bbfd34eb0b0cfa1485dfea5c0caa853128d25d60d7825c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86032dd217b8c77185e386b22d6d332d4b6fd2cddf85c0a64df21f87fd1501c`

```dockerfile
```

-	Layers:
	-	`sha256:518b6630fbdb582debd5c4c46f8039b8f44195625f4400d4bb99b9401c419a1b`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 3.5 MB (3490893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6091081ed8d7f521ff0367b2fa7f66c5aa8240dbd8d7e712d30aeeffa79fb698`  
		Last Modified: Tue, 12 Nov 2024 15:30:51 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8ef9312a0fdc8b92811d1d9657bf499db94d9b44ca98943e46eafa10cad58a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdfe29f5a38745b26b0a25ca56f43fbbddf727ebfc0b1ee7768601d7086f0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6c9a6dd794e1ed81dda37d02d3f23720f08189789c5f7fd0e17e046cf527e`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a914242a633c501864bccf609f0293d6ee4696ceac0bf74ccdc101b9c87483`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 2.2 MB (2247005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f56f562b230c429d639a172bbdbcfe017259e35e426197b4e9883b719fa93`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 5.5 MB (5481042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479dffbae58b3cdbe38bbed543f021e4299d588ae316f600104eca432152ccb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad01041c69cbbcefbf0a4ec453067f7db839dac2626d4f3f24adcc61e4f9bb`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ebee9fa7e9afd48396302673a9252fd0fc7d56699c9316edf249f4e1f1b56e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50f7a69dcc7de28bec6996b147692958e6036b467ae55f6a170cb7fdaf0412`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5f6db1a11202d794574e24fece55d22205533180b9afdcf9e121468f1305b`  
		Last Modified: Tue, 12 Nov 2024 10:29:43 GMT  
		Size: 3.5 MB (3492105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3374b525294173556b47123164944e536280773ae3ad1860af13f8bb426e3c`  
		Last Modified: Tue, 12 Nov 2024 10:29:42 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:737e986d3ef60ed8830756931370aadbbc35c470cfcdbf3b37c1ff9495476128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38487066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015424fd76826195faac03d651002cf1171d9aca7cb6cac6bddb0d1ecdcdd8ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948637f4f555335bfea377215a90d164550e610058376f04c1b248876c0c47a`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b22510c35cc7cf8aedf1deee54533fd6b8d65ecd3bf49c80db67ece7a1edd2`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 2.4 MB (2398654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2800ed116932c0e846f7c7fffc55ace51d2b20e2254422a7966b44582f82f`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 5.9 MB (5941423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa575de140babafc47d340eeee5006016216aa9f50f5477cb2ce015a9f3218`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a2266b94596824891a07b27943af369135fb023a271e21e5bb20a946b2423`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5518303d2b053e8128e0a806a12519370019e47d7b5b830bb54fcc4ad6ada5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d1558a4b6a4feeb09f779d05e60cb323dabd626bffb85f5816ec957025d03`

```dockerfile
```

-	Layers:
	-	`sha256:5b095849f6773c7c1ab56ad90a543e72da0ef69f0ecc27f6b248a9b5a2ffb3d3`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 3.5 MB (3514838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118929ccd9b9af5eaed5b240f4dbabd28b85fed458a3d9a12357d6295eaf20d1`  
		Last Modified: Tue, 12 Nov 2024 02:11:03 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:0624ddac36d0a7ddbed7a4d1e96bc12408dede646ec00185081a40150d8d5d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36770390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dc63047f9926f6d2923676ff7656b5082713e12548f51058ddc50df5a3fd79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c77610d2c9af230e6e756e75398d01603d27c3467c884026c959f2ad40327`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6f8e71a2f1a37272bbdea88d14140c219a3e464d95cc27b2c975f187878ac`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 1.8 MB (1840578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4f114c249a163dcb9ee96873884c73f1c12e7b1e6c35e7d5ac56bbdd62c58`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 5.8 MB (5803489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b0163814f8e0713ef82421f4884e0854c012d708bf4553bd4a79e43639fcce`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e644402e5e54bbfb5881f757e4329ef6fe334d20937810b832932b84a29b38`  
		Last Modified: Fri, 18 Oct 2024 11:33:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ff1fe07cd6e788dc36a2521a7ba08d8d2e4f181b40c022e57cb202e95890535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b7576b893c384675fcebff96036ad796221ff2aa8c2b25fb235f2d52e3e7f`

```dockerfile
```

-	Layers:
	-	`sha256:7a509f4df839959f6049ec675b75f06e15d8aa1e9f25110d50d273e66eacdce0`  
		Last Modified: Fri, 18 Oct 2024 11:33:15 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:1f2b0289f942ad1d147d7835b778fbd8dd009c4d7d217307d448d47dd342195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42131785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f62ad79133a652bc9b8924a9735bffedb08d5e7719e37c6d665e3d5afa92b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5932154388a6408863b1adb85966d65c76b1f1bb2ee20c1d3b10050983ebe`  
		Last Modified: Tue, 12 Nov 2024 08:07:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e2cd0d3193b040bbea27b493c8e6caf90148e2dc631373727d360e67cc00b`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 2.6 MB (2582085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4037acbb39d0315cb87be86e0494accb370f62b7e2920b332bc1b2a194872a`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 6.4 MB (6422808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d414ce94f9a23aa064a4a0c02f427e90bc63f56bf86f1e49d1f80047a678106f`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff03712da36b0fb092c45296793e1a6f86d62aa663929a9cd1b6a72119471ca`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:43eb28d2400ddec59bf666083b56fb75203ffd48eb075271990a43898c12fd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e5df906a8916e5ba51f60fca91067cfa1d60d46d91296bd4dba6241c4749d1`

```dockerfile
```

-	Layers:
	-	`sha256:2f91c23a45c50b096d8f809f5429a689c2b136c947fe447420b7f4874d3beee6`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 3.5 MB (3506557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d7096fa91901f54fa53ddd42d0638abba60d3083391dfc0efb5cf4cd4a101`  
		Last Modified: Tue, 12 Nov 2024 08:07:19 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0eb919bca91f6d4d9ad05b746086c59f9e22c3155c15ae4428890224ed68a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34947755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81952c610a5c6fc901a5ed261848055206cd195af1dc330c4ba02e209ac0101c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377dc54166a948ed8a9a616bfbda9d61e899b64d6f7daa2f89c45a8ad5fce7ae`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2102bd259c13530f5ebbd0eb2312b6abcf70ca2b36d47d204c5f476d4c6bfde`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 2.1 MB (2068739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a777b4f9aeecf100ba857234d9cbacc950a75e10ab1fa5bfd7e8447f5c6fce76`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 5.4 MB (5385847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3babab4816aee1453478ae8cffd3cb6af3af67e5ef97ea881e8d1320e8c09333`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a627a72dbe54e08097f9aa496b873b2fed610f1a4532679809379430c2de11`  
		Last Modified: Tue, 12 Nov 2024 08:43:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3c4caefe3199d7c21c37de5e12257c5deacf698116b1ef49283a3cd727c5cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dc0a4518739ee8324b44f9e5a5f24494ffa6d283c046b61945f61cd958d3fc`

```dockerfile
```

-	Layers:
	-	`sha256:443216e4433ea0db398eb6ca46f6cb144e31db38f69cfb6ac411580223065e2f`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 3.5 MB (3509088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6153e931e52aeb0af765bd5b8dc939721cbda80556d83fe7dfba13596f3543e9`  
		Last Modified: Tue, 12 Nov 2024 08:43:00 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
