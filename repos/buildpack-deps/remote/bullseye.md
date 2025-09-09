## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:741602876acf9b5e782a9db9533f68e35d3e4c82cd065a7f2ee6cb268a58fe9c
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
$ docker pull buildpack-deps@sha256:f5cd04225720b3d1ebaa5baff6cf2501d90a461c94f51091365e7d92448db131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321424518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505165507572b84e4e3177efb87e26489aeb55ab233c7025ee0a1b5810978488`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b969d43370836ef53860df2c53e721ccfdd06653f3db3f7100570314bf509d12`  
		Last Modified: Mon, 08 Sep 2025 22:13:40 GMT  
		Size: 54.8 MB (54757246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6412c7204557d8c521d4b9da4c0a744f9cd8038936537301a90b9395815640`  
		Last Modified: Mon, 08 Sep 2025 22:39:07 GMT  
		Size: 197.1 MB (197146531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa09fb86b577ea44ee9dc835f1c70592a59a23681da1653de242737921ab2223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6235d0db4268fb3922a99d2512bbd3b9aa3eaae345d57e9409621e3f496eb4b`

```dockerfile
```

-	Layers:
	-	`sha256:b2e43046da97ca7b4e7c30fc4a20f06149eee3b47f00189f01c759060fa1a9b1`  
		Last Modified: Tue, 09 Sep 2025 01:19:56 GMT  
		Size: 15.5 MB (15462172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88cdf83fa0817eaeb3bd61aaa2d9828e35f4fad6505dc4f5449dfd6ab315d8f`  
		Last Modified: Tue, 09 Sep 2025 01:19:57 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3828d38d0bffcd622057abc8cc7981b54502edc7ab246563b8e7583f9098bddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282147777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f5bdb8162f92ba9d4fc6662b318478d8ca470fe3da35e6114ed431b8c535b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3c82b80881167fea789bb8cf043d4de732e7b062431e2c261928679dcd3b3`  
		Last Modified: Wed, 13 Aug 2025 00:15:42 GMT  
		Size: 14.9 MB (14880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e2d995d706697c0af2f117145d4dbab9dacbc5f34e7d500b3d99b0062c6f`  
		Last Modified: Wed, 13 Aug 2025 06:47:54 GMT  
		Size: 50.6 MB (50632440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1442f1d0f4f434d42cc2cb968a36d89906e276d8e6a54625dc785435cff2500b`  
		Last Modified: Wed, 13 Aug 2025 13:54:09 GMT  
		Size: 167.6 MB (167590147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54ce9ae59ee46d1d50a79c94313e1ab6dba6c42d8178b29f2f8b85e584a769f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdecd51cab6a44d315eb683d400569c907b6c52b7335b597442332170f8a6187`

```dockerfile
```

-	Layers:
	-	`sha256:37e837f8a3eda4173c33f13671d714a2b11372a586e4c9f4eee847b85fcea397`  
		Last Modified: Wed, 13 Aug 2025 13:20:10 GMT  
		Size: 15.3 MB (15261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977e20a180b57de7b274834623c2c58caa0d93314cbf62a77a9c55018052895a`  
		Last Modified: Wed, 13 Aug 2025 13:20:11 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4605779299163f8f0ae30616558089c99dedee0c8f27923ccf9c9257135a0de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312913588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076c44d57155df958702dadd3f71226d3c9f65eeb9cd73245e60c803883fee46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06836ab0250fb74efa819c381a3a62f540817c74a1d0468d4e03f53c6b03758a`  
		Last Modified: Wed, 13 Aug 2025 15:28:22 GMT  
		Size: 54.9 MB (54856134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d454c8e58c4069692ce41e243c84f24682d348d8667ce5764628f03111249d`  
		Last Modified: Thu, 14 Aug 2025 00:15:27 GMT  
		Size: 190.1 MB (190058369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aec7b4f7ffbcfda84ae56133ec50cb1b05536523585c9c9be2ea558708ef72ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baccaf5cbf4726c86b60a116a1940238e5a36bd49973e658407f339b3d1e0196`

```dockerfile
```

-	Layers:
	-	`sha256:04d0deb9576be4d90292c6c33058cfc4008921be95dd0c916a75664c89f1b0c8`  
		Last Modified: Wed, 13 Aug 2025 22:20:05 GMT  
		Size: 15.5 MB (15464117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e2cfb730de4a249115e76ab9b4ebf029e0cec6992c998814a92d1cd8da11be`  
		Last Modified: Wed, 13 Aug 2025 22:20:06 GMT  
		Size: 10.3 KB (10318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7da14ff11aea6fa012e5aa66c78c6bcf2e3bc933bc1a71c15512b0f069b289a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327057256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b922b353e4624ee18caa5c4fdcb0b5cbd07f1e8f0ca5d561300c34967ce80b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956db1fbb0de06709cacad88eee1a92edcd3eb326031290d4f6e321e68d7c6d`  
		Last Modified: Mon, 08 Sep 2025 21:55:16 GMT  
		Size: 16.3 MB (16268970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8151bbc2095026ddf31b19dbad5daa6653efd5a630af32432a4736a4ce7bc56`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 56.1 MB (56050010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0f4fdfc6cc8075bf66208e6134f6010af73c42995332cfaabb80108c050da`  
		Last Modified: Mon, 08 Sep 2025 22:40:00 GMT  
		Size: 200.0 MB (200047763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3da1a797dfe8a0b547bee1a28c19212084ff92a91e07f042e5f12bf7d8e8f2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d68a560e7542b271f5991d20189d86216febd0c372a5fb53091f0395bf2ef7f`

```dockerfile
```

-	Layers:
	-	`sha256:cdfcb29dc7d2eec970317606573b5863ede338dffdd393d8defe1f8e35e4eead`  
		Last Modified: Tue, 09 Sep 2025 01:20:31 GMT  
		Size: 15.5 MB (15450187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f754b3016b602c603700ba425f14f8a5fa8bfad6e5cf683d7449aee853530dd`  
		Last Modified: Tue, 09 Sep 2025 01:20:33 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json
