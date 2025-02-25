## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:bb715027a2d4f569d898f94b2405ffc593564b81c8aa2bf15d53d30467d8d0ee
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
$ docker pull buildpack-deps@sha256:d2e93687f21da5853e92d5d2394b09c22c04252f3cf160684f835ca1a616f0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321121810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246e22f571a0f5c491769a43d42a15a65de640fdb1075fdba4c2f3ca90722ebb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d32181a1ed55cf7269c27a7a18858d7a4679d9fccbc616d5d878b6ddded25b`  
		Last Modified: Tue, 04 Feb 2025 06:14:22 GMT  
		Size: 197.1 MB (197072749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c20b6d0d8cf0bbb5a04f01ad8cd51019ec51de92a5f18c0de949f2e61d1189ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15081760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66acaa1540629854cd364629b821d7ce5c76de2a55eb5d7a1618e1d5ba5a3adf`

```dockerfile
```

-	Layers:
	-	`sha256:dc4a6b5f744e6d3c4ceaaae6439e7eef4457996ecf9f57bb36742af7b5636be1`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 15.1 MB (15071528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f76a037f50e1f86156c2121d6d9be40001cbdbec315dc9419f83848a2851e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cde95ac46ba8ac7242f07d3320c9b53e32d974612dbadd63ee1fde773a5faf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281867583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c1abd34b9a94833380f7c95fed29f23bae62b21cebc1b27b484df0a8673089`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Tue, 04 Feb 2025 16:21:50 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d22fafd29a9973ab48a06b7cbf9416d9a431926127f18d024a23698bb7846a`  
		Last Modified: Wed, 05 Feb 2025 00:19:43 GMT  
		Size: 167.5 MB (167528902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8aba3369c134e5380e0e38832cdb8f956cc40eaa85810adaf9230efe7b67e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14882585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ecb90a8f76f95ac0ad4c85bf345fd7ad35766c956edf208ceeeed26d7e3397`

```dockerfile
```

-	Layers:
	-	`sha256:22d4f4afabc5e17cc7069af4c9f7a36a1bb7a13d4501ad9352f5fdc2c0f51a45`  
		Last Modified: Wed, 05 Feb 2025 00:19:39 GMT  
		Size: 14.9 MB (14872293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b86e39b006f3491ba761348fa7ff7b787d5586f6bbcbc5b1462e54f93d0212`  
		Last Modified: Wed, 05 Feb 2025 00:19:38 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2d7dd3bb2e678f4ac5efe0f6dd9b422125d1735658d015fddaa35abdd88f341d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312625808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66399a2ca0c4e6bc423eaddcde565f254b12be3da5b6f991ad5bb1ed6c064e9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cae5cdedf5465f9b64d9afa67592e36727e50a811baf4a0d35508744cd435c3`  
		Last Modified: Wed, 05 Feb 2025 01:39:50 GMT  
		Size: 190.0 MB (189983362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f7ce8f56b9bd572e5a86b90048094e12f0e06892aaa369b9091bdb739295961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bb5448e55579f471395fc165fc01a95fedee319d933d48413199ddcff8be9`

```dockerfile
```

-	Layers:
	-	`sha256:6201e1b1cfac8601a21cabb87248640a56084226232c90fdcefc3d9f1cde2a8b`  
		Last Modified: Wed, 05 Feb 2025 01:39:46 GMT  
		Size: 15.1 MB (15073762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ec28d4f74e1a883a777017f87c15501d36cd5001bae75c06a920072ea9d232`  
		Last Modified: Wed, 05 Feb 2025 01:39:45 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b515dd8b23b365afa8c7f48d5188a5a0ec7e7554375b6491a913f5287b32b9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326749201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2bd6e4ec4913368395b20da8db55b72a1a932fe0d11508017ac51a7d83453d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f28cf5e794f0152421ac3105b0a494099546b172c842c1d39e2f90f3bf92f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15070078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0abc2579fe0b912e55deee4d21fd2330cfd79524a33acb41f9032f92d64ee7a`

```dockerfile
```

-	Layers:
	-	`sha256:13bb7b58926390013828051fe96a7df0f4b5dd2ba864c135b3905d766acc1f84`  
		Last Modified: Tue, 25 Feb 2025 04:18:01 GMT  
		Size: 15.1 MB (15059868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf387e464379a7e10e012a6efaa66eb301070d438f61a98fa2ab1b9e68332eb`  
		Last Modified: Tue, 25 Feb 2025 04:18:00 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json
