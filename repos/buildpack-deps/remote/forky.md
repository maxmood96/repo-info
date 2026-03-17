## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:09f8e6f0ca1de6f6bb1ff15c4c84c5c1e2b31c746dcd3fb9d6c3cc8e87c50fe9
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bb51e0333b4881f6dc46023cdb49294c0d25157e2520d25917db2febb0c55c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349790543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d8f210977bdac2275f1fd2079d9e193c049310e4f7626d0ebd3e0ffb153025`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544a38ddd1390105762bdf349d1e32b7cf1a9f82dddf930c31b8042b03c6965`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 27.0 MB (27048499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60232b2b35a4cd7a3c869ce028715219f655956cb40f5462e6fb4439cc2e05f3`  
		Last Modified: Mon, 16 Mar 2026 23:25:44 GMT  
		Size: 75.9 MB (75947432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ecf9ee25a68bf8b76aee8bc662aa505146e114f6e617213bdad99978d47f2c`  
		Last Modified: Tue, 17 Mar 2026 00:20:49 GMT  
		Size: 198.2 MB (198169521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88bfaeff4de17eeffa6d08acf0bb95273c1be80337f9e99de986f8414e4c6828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16802702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74299d89a21acc3f7c951e7af0d5807ca675163456490c556bf860052d6f4eae`

```dockerfile
```

-	Layers:
	-	`sha256:c20a6957753a9cbd0e0dec07f9743ccff13fc07c568e69c73b234e2973aa9835`  
		Last Modified: Tue, 17 Mar 2026 00:20:45 GMT  
		Size: 16.8 MB (16792557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6a69073fddb90e06d62b2ffd92c49b2fb5ed04b882259b6a0f555f4749eb40`  
		Last Modified: Tue, 17 Mar 2026 00:20:45 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8cd6198cba8f4dae6db2cacf3867b0cfce2393baa912a32780098ca5deac3292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301821371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958aad2cd61c7ff36fa324cac352f376d113c27ec691f847e5ba6128db13017a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:04:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2692d078b62360ce66efa48798cce1ada6ffaf0e61c3560fb4e15c2ba9d74`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 24.9 MB (24920360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25208c70da66ab3bb8d85158eb796fdadd82a017ba00747c64f1e57f5bb9ee99`  
		Last Modified: Tue, 24 Feb 2026 21:35:08 GMT  
		Size: 70.5 MB (70451873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361c9a8435117b262175d66e39e3c547c91d72dc70c01581d1cabdc179abe0b`  
		Last Modified: Tue, 24 Feb 2026 22:17:31 GMT  
		Size: 160.8 MB (160796090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3db7239a1d75acf2fb6ba91ade7aee080711e42362e99dc4838bca9d721d154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16611210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ba45b840f64e4c2a2a8b363b2ae327015f2664305ca209c8649e190eebc46`

```dockerfile
```

-	Layers:
	-	`sha256:c9cc7fa08b949ad2671d13e2c2708eb226da44b44dd7b9bff6e36fbe6f182140`  
		Last Modified: Tue, 24 Feb 2026 22:17:28 GMT  
		Size: 16.6 MB (16601001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855b8c362f0d400dc02d50ff61bd31690b5549e0f59ba9853943d9f76e2c1fd9`  
		Last Modified: Tue, 24 Feb 2026 22:17:27 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:811dc8e8d9aaa58446119d0a6b45366caff1cd4ad796565a8b05a82e14090be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338020783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891c237582fb4c9051be3eca7743624b8feb09791781a83584102123cf3a89cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873916964a227a18ebb04ec1f407f168a33886e300682cbd4848c61bc623f448`  
		Last Modified: Mon, 16 Mar 2026 22:40:19 GMT  
		Size: 26.3 MB (26344588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4fb7d902f3cb9bf3e0daa77ba127ee8230f61ba12bbb5d9f7dcefc084f7373`  
		Last Modified: Mon, 16 Mar 2026 23:31:17 GMT  
		Size: 75.2 MB (75222389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6719eb5de4a05a7626a3b66f236c500c85db4d56169bd8486988d9eb1b4c289`  
		Last Modified: Tue, 17 Mar 2026 00:20:34 GMT  
		Size: 187.8 MB (187794745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3866399cec38aa5f1d5e69404273d8cf5488a394e8278c09cda1a02bab24182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16888337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda236def5714df193be53360a84c8f8a18fe9bbf12457a2e3da282f2a919803`

```dockerfile
```

-	Layers:
	-	`sha256:4cfa768cb5d711b96b2e39b5c31f6c21b0da048a43ff1cdb1b90dca962d5c06d`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 16.9 MB (16878112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0634033859063264c581959d881d1855a0de90fc6247b6e3af17c0fe135f06b`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cd7409d7abf16f56af908fafddf55934fdc507c14d4256b34f3fb681840bee6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357226204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ad77696485d1b2f977f4ee67f683387d90c8ea16d3e7ce55018d173602859`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63597877e9ce45a8d644c87f2edaa1b6f60b392c0f8a5049196e27710801057`  
		Last Modified: Mon, 16 Mar 2026 22:44:13 GMT  
		Size: 28.3 MB (28310412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b32036cc7858dc14c7d8b709498aa52c52147bbd4f9cd24a39c522f264cf55`  
		Last Modified: Mon, 16 Mar 2026 23:42:04 GMT  
		Size: 78.0 MB (77964507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6614020f7ad970a65a6139fcb8b9913066a1c5f4945ad804e2c0c2271693d3`  
		Last Modified: Tue, 17 Mar 2026 00:20:44 GMT  
		Size: 201.0 MB (201031414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6523270cae55b10f237ecbecaf56491648d9581be8eea24ec942a396977703f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16771749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1346df970287a83a9ddc7d0bd89b952fc96465101bf77d399a78851138f2b09`

```dockerfile
```

-	Layers:
	-	`sha256:3b690647eccb3ded83f61f9ba7e63c5f83158bb53bcdf19d2850e32350bdc561`  
		Last Modified: Tue, 17 Mar 2026 00:20:40 GMT  
		Size: 16.8 MB (16761626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b3291abcf222678cf875ee14f784288200fb3e5b132ab21d5fbccc7a842ce8c`  
		Last Modified: Tue, 17 Mar 2026 00:20:40 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:748fd37df666ae003407b04af603cef02f5c80b6494f41353151a628d6a377e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362027964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0176afa3c9169cc86f0d1ff3d6a04d23b5a71255dcd8b731e8282bc604888311`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 21:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:56:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 06:17:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa31de94cb423730059f9604b4ef3f6954ef0ad086f5d48144efd62317b2c2e`  
		Last Modified: Tue, 24 Feb 2026 21:20:56 GMT  
		Size: 29.5 MB (29513933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930837d0aa6df8d34e08c85803ff9b80030a83f236fe93d9e1ea4d7134b958c3`  
		Last Modified: Wed, 25 Feb 2026 02:57:28 GMT  
		Size: 81.9 MB (81942342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d73cceefa5bd4d8a06262c2034e237feabf6df22280dc171af731959b407ec`  
		Last Modified: Wed, 25 Feb 2026 06:18:38 GMT  
		Size: 196.9 MB (196929902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7040a61a3dcfac5fb066bf230cc51f933f48453cc4c0c43f80a9fa5e8ba72497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16807529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09408b21b30828860ad5879c2c4fbfc979c62f46a7cdd2f7fdc12cd8070d8130`

```dockerfile
```

-	Layers:
	-	`sha256:83a88d668ebc5f3c235e4ce7bb968b3dc9b3f5f2a662f055ba4c9e34e6f7d023`  
		Last Modified: Wed, 25 Feb 2026 06:18:34 GMT  
		Size: 16.8 MB (16797352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4abc4788eaf5e708445d092ac34a53694004810cd34b6e99ec01494b7d5c63`  
		Last Modified: Wed, 25 Feb 2026 06:18:33 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4a07117c40a71eeafa1f067471830ee9ccb74bbfb1ecbdfe13343c477789d153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.6 MB (468648172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5eb31e6cb42fe103ddad7a3bfee8af7c4702874d08084e10bf4d7c95a1bd75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 26 Feb 2026 21:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:33:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ea7a6a4533bb42137b98ae7cf7eb86a1fd6eefe9d713522264d613c05e62`  
		Last Modified: Tue, 24 Feb 2026 19:09:30 GMT  
		Size: 26.8 MB (26774378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebef486f83ee0c702c262a6d5550673a0f1b78368f99bd1ce71d5e966d05ab`  
		Last Modified: Thu, 26 Feb 2026 21:38:15 GMT  
		Size: 74.4 MB (74379205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b16e39d37471c692ac6df897b04bb474eee60d703290f4752935fdc10a24d`  
		Last Modified: Sat, 28 Feb 2026 19:49:17 GMT  
		Size: 320.6 MB (320580185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9c0e5337687790a07200eaa00aabb33cf8944c46444832b572dd6b2d85efb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6b0f3fdfb70563f37211e755d59a2be7a26138c5c9864d87d89778a2e301a`

```dockerfile
```

-	Layers:
	-	`sha256:92c278ac18d4279c06690a127db5174d7096668ba4c3c52040137a99c5a1957b`  
		Last Modified: Sat, 28 Feb 2026 19:48:33 GMT  
		Size: 16.9 MB (16885046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173fb54d825398d0145365446ef33f196c28634bbdfc9c52cd0bc87d9443c491`  
		Last Modified: Sat, 28 Feb 2026 19:48:28 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:335b3335f4d8360f00c28bf66c700be02143a00d1e0101ba1a37655062b66064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326314477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a152d0b3c1b0031ec18178927f97728106bd3d0186e06e1f5fc7abc57b9e7dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:14:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc3d23a1ad94963e56617c5ddcf27c1a360185386d60459632a29eefc99c91`  
		Last Modified: Tue, 24 Feb 2026 20:58:20 GMT  
		Size: 27.0 MB (27005253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96339ee6032387e57235bad6fbe6a63b35d2154d0ed8853524ee337a527c18b6`  
		Last Modified: Tue, 24 Feb 2026 23:52:57 GMT  
		Size: 76.4 MB (76433018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970d5e9476197853dc258a861178bcf66850ea686e04fa4b573683a2fd87c4`  
		Last Modified: Wed, 25 Feb 2026 02:16:04 GMT  
		Size: 174.4 MB (174427854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b31b4c156f6ad13de5cb0bdfede20293b8ec0cbb96e8cbf9368b938e2697d6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16609992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c5aee1bb6eeb6eebf9ac23ead06e41d5c7f97451dc5dce167e8d8c04eaee9d`

```dockerfile
```

-	Layers:
	-	`sha256:ed66a42a8a64c7aef04c433d6f13024c2ef2d61cb6e7e216e148435e119f9fc8`  
		Last Modified: Wed, 25 Feb 2026 02:16:01 GMT  
		Size: 16.6 MB (16599847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28447f1f73823925c0ffdf309e57974701c8add19b813d288e34f9db7c650886`  
		Last Modified: Wed, 25 Feb 2026 02:15:59 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
