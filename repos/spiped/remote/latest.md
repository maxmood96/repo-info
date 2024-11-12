## `spiped:latest`

```console
$ docker pull spiped@sha256:db003b67d75c11bf1bc8dba9dc8fee814967cde439a55f7e6e6f9ed2f762bf50
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
$ docker pull spiped@sha256:e1ee4001dfded202d0df94ec3a4222e900df84398c08072124bccf4f545e701e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31455113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbedd4910f1d4859586b96b2c804a9d6275a9a827f9abe808e0c3a6685c1315`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
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
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab09031d24b116812fb7c499839a851cdba083c720131aab46be0bdcbfc4193`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784432647c7f15b17c5ed863965e5dc5c0c82c6ef4605ca3f784700b3e627b2`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 1.9 MB (1855252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3878bd0cc3b53195940572ec6aa05f63c96f777f5df88b6f22275f0005093835`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 4.9 MB (4880127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b219a7ab77ef82d2ca0774c5ab7d009089d417850a516a9488172689ed40006`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dee28840daf3d46b335273fa0d8aa4a6fac22e1fb0954f83dcd698ba8fc5d7`  
		Last Modified: Fri, 18 Oct 2024 02:10:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d98b2207247c2b307b8aad8448541445f3694be5b7686a02791e8343f93ca9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3492424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f75d853d0b527f93f9311fe0173e8672827eea9679446e6479ea651b8409fe`

```dockerfile
```

-	Layers:
	-	`sha256:a68a19b8e3966936d970f60c2ad262c44234d7dc42b6622ac6191514b28f93da`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 3.5 MB (3477444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54de5b3f61d1f708f1cc788d4b7865041d9621ce4d9410e5df2716683d59455d`  
		Last Modified: Fri, 18 Oct 2024 02:10:22 GMT  
		Size: 15.0 KB (14980 bytes)  
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
