## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:e50c770d84e74fba05202875719e16e1d55b8e6329f04348e548e9e6c358eb54
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb70d6818648004f52871153b3a79ba10a5f4f597159a9bd21f93c68fb7f40d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343262154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7d4d0d4ec058d30053e5af8f927286e0a1ee1a00d87ddf25c5eb21c28b3ea6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:48:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a867a2ba4f56034ba2804ac22169357a40437b8b6a997f3bb612def250ed9f2`  
		Last Modified: Tue, 13 Jan 2026 02:10:56 GMT  
		Size: 27.3 MB (27290900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55404ed8412e6a7f41ff3fbcda1b7f67ea69dcd921d832079674e3d1e96be46`  
		Last Modified: Tue, 13 Jan 2026 03:54:49 GMT  
		Size: 68.5 MB (68503999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbba9a5f70ca25634cc7fae217544ed798c52a03522938ea2d4ec4bd1041435`  
		Last Modified: Wed, 14 Jan 2026 22:06:49 GMT  
		Size: 198.6 MB (198625305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51bb5ed0a431c8c153383d8ed0461994d3b38ccc4ba0ae9636eb9dba88f1b43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16303017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6adbd14a08d36e79a9d461f7648ae38f15ffa0ba053bceddef0a3ee39faa47`

```dockerfile
```

-	Layers:
	-	`sha256:a859cbb1a9dc87b6f16f00a7515be9b75cd52bdd341306cb9151e528d5634405`  
		Last Modified: Tue, 13 Jan 2026 08:21:57 GMT  
		Size: 16.3 MB (16292884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e2185f20d098cc88c5c749f72721966163932933b4bee15c76cde670f703da`  
		Last Modified: Tue, 13 Jan 2026 08:21:58 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47c7b452f0890b36f4a44c4445f1b8654526b2ca0c5afc2dd9f21fd98f701289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290948076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e540664ce67371c52d57bbf55480ae165174a1031921ce6893418d25d90edf4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7f582255e583d8176a24d49b58b25ef2ab11e30f1f26c271dc02b42befa1ec`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 45.1 MB (45124955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363fb6b9543f81f86efd0aecc6d9e12898921b7bd5ed58e85c04a1426057dd9`  
		Last Modified: Tue, 13 Jan 2026 02:58:31 GMT  
		Size: 24.9 MB (24902123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b60fca82596286ecea5d47fc7f746d3aced8c889d5108a6794f889171c8a3a0`  
		Last Modified: Tue, 13 Jan 2026 04:26:12 GMT  
		Size: 63.3 MB (63339726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2bb1f25a793e276355c2fbecc2b7b644251bc7eaf70e1d4527651960cfebd`  
		Last Modified: Thu, 15 Jan 2026 21:19:54 GMT  
		Size: 157.6 MB (157581272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d6dfbad186a01d2070807ec19592b180b3a20ebce7da1662d540cab5d6d8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16058762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5f474e4e7be8b98fe5083c1fcc5c39979e9ce6d0aa79f49cab9c52f79e08`

```dockerfile
```

-	Layers:
	-	`sha256:9cbfcc03d0acb2241ec2617dcdeba1558c110504366d7a67a9f41c9e6eea66e4`  
		Last Modified: Tue, 13 Jan 2026 08:22:13 GMT  
		Size: 16.0 MB (16048565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b59a7b96361787ee8bb5d137ede212ba30a33107814e0c3eaa2afb577c0f16`  
		Last Modified: Tue, 13 Jan 2026 08:22:14 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee49b43bb96b9d4719f29d123b4be8a6e31f51619521618760c9a8a83806a639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332145770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1329e6425e63a4178d197da662e8b61a19b1111904daf8386bef225e142da264`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:51:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d83fa1af402d6122143d9e5834df76a1ce4536b0e53fa05dd6ae332f4c77b6`  
		Last Modified: Tue, 13 Jan 2026 02:15:12 GMT  
		Size: 26.6 MB (26552724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0863060b37c2073e502479262c55d34bd38dd8dedd4f04987613b3469d229d86`  
		Last Modified: Tue, 13 Jan 2026 03:58:44 GMT  
		Size: 68.2 MB (68203514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c042eca621e87d2accdd339187afcdb439707ea7e994122ffaeb9bf636f4de`  
		Last Modified: Wed, 14 Jan 2026 22:08:04 GMT  
		Size: 188.6 MB (188564814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e99f62738a9ce50eed5ac9b28e7a43db6c52118aff77ce09994f40955ee6920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16377645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111bf71e4db635b27d85f968917430a2b4d81898beaff1050e1acecee93caae`

```dockerfile
```

-	Layers:
	-	`sha256:49a43ab999795aa37dfe7528c4ce1827955786f62f580c76b061d6ab0d169f2e`  
		Last Modified: Tue, 13 Jan 2026 04:51:46 GMT  
		Size: 16.4 MB (16367432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:169e39566dfb3932e3bc8ffe0d7b3a8bbfbca7450284bd37a95e283f2f897c9c`  
		Last Modified: Tue, 13 Jan 2026 08:22:30 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e63237663b0943db535d4b300d62337713697697ec4a1262b4a2b381688d3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350331499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45622a3f20b9020dd6f0fa1d590128c09e147623903113f3e767da81a7ac5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ebc798fc10f8015cd27d3c8885c010f05e57b86cddfc6e327bc7f746362b1e`  
		Last Modified: Tue, 13 Jan 2026 02:03:10 GMT  
		Size: 28.5 MB (28474654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7a9609654b5ff3001c4a4b23c058f78703d8972ed2b4f3df257bb6cb1e211`  
		Last Modified: Tue, 13 Jan 2026 03:04:37 GMT  
		Size: 70.5 MB (70466208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d16d814db068f5b5ca803d4a81c723bf3721b606414e5dda8deaa9e7f3b0d0`  
		Last Modified: Tue, 13 Jan 2026 03:55:27 GMT  
		Size: 201.4 MB (201446821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65a9b8bfd3eadb1153f49faacd0fe18eb467cfc0941b6d3533e6f34ce590b79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16272757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5d5a84f66eb9df4607bceeb98882788b2e707f4034e9628f0df25f61bbcfc`

```dockerfile
```

-	Layers:
	-	`sha256:3e47b09eb66d440212b36fe03170cd0372343d9493a5d605a50af247c91f977c`  
		Last Modified: Tue, 13 Jan 2026 05:24:57 GMT  
		Size: 16.3 MB (16262647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41b8b2b2c44c81ea32b5eb8f0b337ddd65891f834abb282a925e3aeaca6fd3f`  
		Last Modified: Tue, 13 Jan 2026 05:24:58 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4383467c27bfafbf668b1db595690f03b5bda878f9d61f76b94cda63ce7413bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348116515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37a642ed1bc3fe4142a6a0f01b78ffd7c4121e173f5b1709a051b69d12f4aa0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1768176000'
# Wed, 14 Jan 2026 00:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 03:16:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 04:13:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3fc9cd4fe16c3d17cfa9014c31678a58aad75101c0db66189ea08efe999c1a84`  
		Last Modified: Tue, 13 Jan 2026 23:17:59 GMT  
		Size: 53.5 MB (53525434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197399fa4447d8fa115804ab3b4e02dac8c91312a2de42315098f7ba5379933`  
		Last Modified: Wed, 14 Jan 2026 00:59:19 GMT  
		Size: 29.4 MB (29433893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34eae56a8f267779d2b4c803a11c3bf71c8a6b9f9a6e12fa12e1722fb4de21`  
		Last Modified: Wed, 14 Jan 2026 03:17:15 GMT  
		Size: 73.9 MB (73938015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911b038d6e717ed090f9c3461176abfa8af2214f72883ede5a8a73f2ee77db8`  
		Last Modified: Wed, 14 Jan 2026 05:21:00 GMT  
		Size: 191.2 MB (191219173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:534c0f4ec0f12e375a4bb13519ab4dbe6eb4d2d31886f03b4eee924fa711f959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16275956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69829c7894381b8ec3a31a0402526db085ac23afaad5be097a9e691e88fbee4`

```dockerfile
```

-	Layers:
	-	`sha256:f04b2d384e59ed7b9e832d47850f339a57a0bd2585811b19c7bd3bd07b7bf8ca`  
		Last Modified: Wed, 14 Jan 2026 04:14:56 GMT  
		Size: 16.3 MB (16265791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc97153f6cee8fead45aecefffaf7471e1a046ae7f6c130d5f4e5f48942c94d`  
		Last Modified: Thu, 15 Jan 2026 03:24:42 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:39134a8719af5b4377a0fe47a226ce72bd94cdcb94ba7a6d98bf7d6e9eb85a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.7 MB (454699138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda8160f1621684f1dff8423f293e78b5e8c1a9022132540b4dbb6c40fe741b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1766966400'
# Wed, 31 Dec 2025 10:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:37:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 19:42:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:992d8af34d90a1736cf1953fc1b6a42478d3f56705880d255aceac14902fb105`  
		Last Modified: Tue, 30 Dec 2025 00:37:42 GMT  
		Size: 46.8 MB (46842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59f77af8fac6fe633c43cf8effbdd88f2374763db6aea46bfef4f1a063d920`  
		Last Modified: Wed, 31 Dec 2025 10:14:20 GMT  
		Size: 26.4 MB (26352545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfcf1a86a02992f6a6c9bf0cf2dd17b8a12c73c26f7604edf6b0a50cdda329c`  
		Last Modified: Thu, 01 Jan 2026 12:41:00 GMT  
		Size: 67.3 MB (67256815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d59080f72110044ef44e6be7ad52b3cfcb4e2e1c9f2de941b675556a6adb7d`  
		Last Modified: Fri, 02 Jan 2026 19:58:16 GMT  
		Size: 314.2 MB (314246938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29743d3b75f9533084becafbe278ef486808307caca1500207a285b9ea3beb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16327039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a391462719e6ed9b991c7839751c47f797ed6695a8e1a8426ed86fcfa251617`

```dockerfile
```

-	Layers:
	-	`sha256:03791360f3919c381923923ed5babca6587f10fab0e29eb963c45b023b21c66b`  
		Last Modified: Fri, 02 Jan 2026 20:21:30 GMT  
		Size: 16.3 MB (16316874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8426a6a8f2b84e0e334b443b047cdeb0c63e98bb22260e902b4fc823b9c793ab`  
		Last Modified: Fri, 02 Jan 2026 20:21:31 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e7b368109d15f0554329456a363187dc202ad791a661ffa179ebe5228fa60a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315668916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a817d2e387c7c0c20f349c397590628d296e39d00b69f92a8d29319e1607bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9a1f6e22461ab2a7c3b148cd7fd0131848ded4c904183b11402001b4c02c1f`  
		Last Modified: Tue, 13 Jan 2026 00:40:59 GMT  
		Size: 48.4 MB (48388631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023c3faac75568557121b3e0aa2c658af780e8a1a9143b42405a60dbbef8a126`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 27.0 MB (26996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8af6004b3a4bb44f014415532f591a277692d1804c8d47f715e1ffb386211`  
		Last Modified: Tue, 13 Jan 2026 03:16:06 GMT  
		Size: 69.2 MB (69226189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56476b5ea5eb457690e45ab37a809bf433dfdfd9590f390c524588409a87f0c`  
		Last Modified: Tue, 13 Jan 2026 04:19:12 GMT  
		Size: 171.1 MB (171058080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df98fe9dedf6d27fbe181915a83f5be5ad96cb34c51dba6144bf495529eda08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16080190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8af1f062d7768df3b401e4b70af3f53b117e29390eee8f0f0833e7eb535cfa9`

```dockerfile
```

-	Layers:
	-	`sha256:25724e792905f6c0bb6122f56cebe733b712b986b721aa5684a5b98e1ed952d4`  
		Last Modified: Tue, 13 Jan 2026 05:25:35 GMT  
		Size: 16.1 MB (16070057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befd65dd2273ff594308eeab92646c914e6ec0db82fa2b9c97d1fe9176631512`  
		Last Modified: Tue, 13 Jan 2026 05:25:36 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
