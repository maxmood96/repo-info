## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:6a05c4bb01534c7540ffe89e15eae23c5908aa6277a864a6118a73472e5fd1ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e7c3532646ff851410b71ef77592f72833192f4c43ce6332f027b4d235f56237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321567533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e63b3a5a835cb3eea498f1a0bf221c74c7d4db63e5d184c7cb9c88bdb74c20d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d9f854f908f28a433fd2d5b08b5e68ee58c9ec953dac233ca6864ced59f24`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 15.8 MB (15790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14034e66ee3f8bcfd399019612c7f333cc777166161c3dee1a945ac1f0659fd6`  
		Last Modified: Tue, 07 Apr 2026 02:43:11 GMT  
		Size: 54.8 MB (54760196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067d6a857ea26ea67633cd59e0209cb6a54e70a1e95d19e8ae6c6b0a15b3d8d6`  
		Last Modified: Tue, 07 Apr 2026 03:24:05 GMT  
		Size: 197.3 MB (197253868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a6519b1d485a037f547fba86380d94852fbeb42ec9da2866114c71eb69366600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6aa9c82c4d5cdf270628d4a61ec855ccf58fdbc3760ed2db9e0513d4638e0`

```dockerfile
```

-	Layers:
	-	`sha256:73ed5e2603c912b8076cc9cf51b010a9ac2aa9a833b5dbf047552cca137d66a9`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 15.5 MB (15471469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686bdb5706ae6b6c5aeec99a39a8c1104aa793812ec85c42b4c679fc4c5718b1`  
		Last Modified: Tue, 07 Apr 2026 03:24:00 GMT  
		Size: 10.2 KB (10194 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c9e26cba9c23da0b2f7fe76486e4306218e145dd4413e2bbfbeb8918fb985a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282328485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc713bda013e0c8300047aa755f4fae07326ef4795fd8a51102e2d6e62634a06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b7f7b3cfb222580c94a933dbaaabd959ea960847c9aff9c5d4daa21494eea44d`  
		Last Modified: Wed, 22 Apr 2026 00:16:47 GMT  
		Size: 49.1 MB (49055006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698f04c927addec960608562122b5f1c50ad262b50810e813b3046303555106`  
		Last Modified: Wed, 22 Apr 2026 02:18:42 GMT  
		Size: 14.9 MB (14905103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a451edd267f2ece592819d45854d958b47c98b8c4b25b1c98edd54f76d1bcc`  
		Last Modified: Wed, 22 Apr 2026 03:52:30 GMT  
		Size: 50.7 MB (50651590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c2c739d513064642e14c7fa1d4873e1e96ff1538ad1bd0b4769a3ea4bccc7`  
		Last Modified: Wed, 22 Apr 2026 04:16:18 GMT  
		Size: 167.7 MB (167716786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44040d682e7dfdc225bc1bc8fbe47356a4c9d8f5ddac17b8caa390084d081cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfa03a4eb93e6500fe420635961d73fd769ea98b2956406be7328f50128d158`

```dockerfile
```

-	Layers:
	-	`sha256:02f387c6b9851d25885dea82d203d44ae3b00ff2a00fa2a233e0cd3ed2937611`  
		Last Modified: Wed, 22 Apr 2026 04:16:14 GMT  
		Size: 15.3 MB (15270787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6a3b6f376a98d70f09250d78e1f40d606cf6e6b78e622aa32fa5610b993f95`  
		Last Modified: Wed, 22 Apr 2026 04:16:13 GMT  
		Size: 10.3 KB (10258 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cb5a3718feda064648abe1b7873c29837fa1b443aebde92637ee44d3737b6a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313104850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8fa6d9e5a441c31fc745e8d8cb97c67b33534d4fd3f9f6a36a5e45b6d1e02e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:17:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41762a69c06632f02d051591b8561619178cda30090272dff52f65c2d6157695`  
		Last Modified: Wed, 22 Apr 2026 02:32:20 GMT  
		Size: 54.9 MB (54886521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba12cf159babc02fc1c9dadaf51e2fca9d51183009dbc801190af3b460b98dc`  
		Last Modified: Wed, 22 Apr 2026 03:17:52 GMT  
		Size: 190.2 MB (190190591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c24169634e9ecf3ba104723f0b745f3999c9173d8afa5298c998fbaad512e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89747eac2101d8c2c6cc198299a2613947f7ab1d87cce177508b522b65f044d7`

```dockerfile
```

-	Layers:
	-	`sha256:d5a3c443b720a095f1883d617d66e6ee47b8812012583f5b29cf9e3db04f8dae`  
		Last Modified: Wed, 22 Apr 2026 03:17:48 GMT  
		Size: 15.5 MB (15473414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a14d0adcd1de85910e6889634a4528f088cda62a43b8f7c33892ca8f8bffb0`  
		Last Modified: Wed, 22 Apr 2026 03:17:47 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8600640d2234bd5b1b1011426d2162974d18baf1e4981c8e91302d6dbf0f8e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09019b22f9e3d2d7fa19865d4eba7b5e85b3f8d66199522063063780e56cc22d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d7ea2b68c41d012b622a11d60c4b7330f09ed012ac9774c3894afce154803`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 16.3 MB (16295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a70b77dc85f405fa11ace8b407313b02fa39bd8320ba0a6a1e2b1c856fb04`  
		Last Modified: Tue, 07 Apr 2026 02:41:03 GMT  
		Size: 56.1 MB (56058498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0d7578290272fe386be38c96d8e837c43979560544df34b91318fabc54ecb0`  
		Last Modified: Tue, 07 Apr 2026 03:20:03 GMT  
		Size: 200.2 MB (200171747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd1bd584434fb2e075e5004a5bb2aff2b783ec988ec6aabc1e3b9c51aa24ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc2e54085c8a69de997fbcdaab65a45229fa1d4726f16d89ab7980cacae79b5`

```dockerfile
```

-	Layers:
	-	`sha256:67538960685ba4573299fd6b1b3198d904bfdcffceab7660da9dcb7f9ee13a50`  
		Last Modified: Tue, 07 Apr 2026 03:19:58 GMT  
		Size: 15.5 MB (15459484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac8c5c3c6dfd17d38f9f94440cb68fa08e8276077537b81b11bcac7231970fe`  
		Last Modified: Tue, 07 Apr 2026 03:19:58 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
