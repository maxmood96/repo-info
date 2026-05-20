## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:3b121fa33fd869e0b9a112fdb5248b2e1326bcc41503c1a7304f3d6c98d3aa27
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fd174c41d20d187e3118373909d7d6f2bd98448fde7e56f049143e9b96a870b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350727347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6f7631dab124a9472f4b5110d133ba454991b18ee48c9ce803dd03a540700`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:23:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2642fa4ec2a9746c709cd3ea129863f7b5d0a1937a5b2a2f95a75245bf1fe8`  
		Last Modified: Tue, 19 May 2026 23:23:23 GMT  
		Size: 26.9 MB (26891116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4107cf9efb8684cd0abf2860b1e6b4e583e2c7f47cdcfb7a25f6b4e3148e16e4`  
		Last Modified: Wed, 20 May 2026 00:26:36 GMT  
		Size: 76.9 MB (76901260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc2c38535548f1fb4b8f31af5eefbae1af2d74fe687f918202b0c03e36a1521`  
		Last Modified: Wed, 20 May 2026 01:16:31 GMT  
		Size: 198.2 MB (198237765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2e01ae6bb1d777ae767c29e85073cc7f496e4a80a6d7c40548036bd7aa5fb5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16906644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733493bf2c2e1096de15a0f5839b3d2dea1aa4a1e21bc318d084c99ae72f3f58`

```dockerfile
```

-	Layers:
	-	`sha256:3f4f55aaf6f1341fdbd64b2382dc1ef09c3e13f16a500b8c96edce18cf6804a3`  
		Last Modified: Wed, 20 May 2026 01:16:27 GMT  
		Size: 16.9 MB (16896499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7dd3e8923e0ccc5d502b55c48756ae61753b72cb33ca582e00d01df4a0b80d`  
		Last Modified: Wed, 20 May 2026 01:16:27 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b9a9dc97b24c9bb05ebdf4a50185b5672ff14edf253d8f8893124d2d5258837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295951056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f482b9cbcc679dc25753a86550272c585ced85a9d419e7b548b9c7cd349b11f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:15:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b6df9d4a408084133e98c8d6c8e0e3de38b9e95851bc2206e09b39135c71bba1`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 45.6 MB (45603185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd97129e166740f6b7d385932f0e29058407c0b25cd1d04df0d94fe382e494c`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 24.6 MB (24602913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f41170f5eafbd474b965f1d2e3462304d25531cc0394b9f6f241c79cc0af46`  
		Last Modified: Wed, 20 May 2026 01:34:40 GMT  
		Size: 71.4 MB (71417301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f79a69bb2e08f703854b98371463dc47464eed61c939bac687fcc5e3eed3779`  
		Last Modified: Wed, 20 May 2026 02:15:36 GMT  
		Size: 154.3 MB (154327657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:579a02f43d1b191dd73b17a58ff6bb2a19b0590662a9a123e37ae9d3f8557352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16662658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d396258692e6c618478015b811e626035c65762755f9c239b5394ba2fcbda0b`

```dockerfile
```

-	Layers:
	-	`sha256:0dd143a60965f83e8d93f9d84708e4e06ed9d5e2eb037f9b14453ed44f0d1b83`  
		Last Modified: Wed, 20 May 2026 02:15:32 GMT  
		Size: 16.7 MB (16652449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791deeb3bfdcddc2570b6582ed4e22364e0f3ee749f1bd45900447a9c5df1ad1`  
		Last Modified: Wed, 20 May 2026 02:15:31 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6abdae09c38420e9c24a4754d9e17e517eaf277edcce3781d5f72a78d8bcadb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339190370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e5d326aa43aba4d5f440f6eac285b364e7f7b5a72de79adc05a452a5f8dd94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6efa7756521280bd54091d885e5326bdeb8ff205564db4dd0b7c81ed203199`  
		Last Modified: Tue, 19 May 2026 23:27:03 GMT  
		Size: 26.2 MB (26170165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c09d09dc4bc7143e7855d920786955805f4275e7095dd6a2b7367a2b39b19c`  
		Last Modified: Wed, 20 May 2026 00:27:51 GMT  
		Size: 76.1 MB (76065993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba71f02bd1fa651b5d44b98f49e7ae38ab4a2a50ee989c6878ad52e39ea37558`  
		Last Modified: Wed, 20 May 2026 01:16:40 GMT  
		Size: 188.2 MB (188234181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dcfd23636681df0cff70bd95601dfcee5132ef45c97033cbfc931fd159bfe65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc85b91ad884c2dc846df41576c978fb353dbdf974a30f93eaf39e6f89cd1bb7`

```dockerfile
```

-	Layers:
	-	`sha256:a1b11c3f4f4873765e3041d9abe6fc8059bff55139649382a4332ce65cc59629`  
		Last Modified: Wed, 20 May 2026 01:16:31 GMT  
		Size: 17.0 MB (16977607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0a6493f6c9600d8d485657ab4f6ba7c8b14a9fcd104aee089df873d375b844`  
		Last Modified: Wed, 20 May 2026 01:16:30 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f980bf0f8056609614e5559924710d338a4dc3614cfc3abf8eb1009b0777c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358546785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aee13394c1049baf6d99ef470fce0f912153079feed94a76c9cc6544aeeee4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:03:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497fcbfcc0cfec531a77167884014e2e81ee738aa6aca34516d78ed1b945bdf`  
		Last Modified: Tue, 19 May 2026 23:25:23 GMT  
		Size: 28.2 MB (28207970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b7c5b17f8f533e68966e1ba0cf608f2e2d4de56a6745dbacaa12f28dbc238`  
		Last Modified: Wed, 20 May 2026 02:45:41 GMT  
		Size: 79.1 MB (79073049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307abf1d89103be33dfdafa843632d3f05cb60577acee621e11d13ec591ebee`  
		Last Modified: Wed, 20 May 2026 06:04:29 GMT  
		Size: 201.3 MB (201263822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa89470f0b36a552492ef9cfe0094072d7fecd09b8439ee1126452939fdfaca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16874042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d353502036cbb986bd4defec3f4ac57b20935d96c0764c17d6ecfc3de312e6`

```dockerfile
```

-	Layers:
	-	`sha256:af96ad2a9178a037d60454a1139cf73d33dde543a2da47b82fab46b6bfd8abdc`  
		Last Modified: Wed, 20 May 2026 06:04:24 GMT  
		Size: 16.9 MB (16863919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52b34368c0a9a9b72c2ba70cc1c09efeab8d88b73da882f62afb5a5915cff4f`  
		Last Modified: Wed, 20 May 2026 06:04:23 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5a087f0858bc7ac6519bf4b9c696ec3d9fe5344777a6b145601fbcd4de9d3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358772875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fccac5c5835b4dfa3a6aefb39b4a31565eb3058ab605f27f15225bac61f0905`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 01:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:51:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:06:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5564b9da7290f7430ffd86cfc5f2b22a68586fade0aa81c8610704c43fd41e`  
		Last Modified: Tue, 19 May 2026 22:35:40 GMT  
		Size: 54.0 MB (54021281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24877c775bac285836892c60f877392eff4299b16fa48a35fb91c222b64558d`  
		Last Modified: Wed, 20 May 2026 01:13:54 GMT  
		Size: 29.3 MB (29285894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc79d08e369fda0605c037025da8b1333ff074dcf4bb801aa3f65c8ba0a35`  
		Last Modified: Wed, 20 May 2026 06:51:44 GMT  
		Size: 83.4 MB (83444053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f31e2d21d5ecbf134461766a5322e4d3a509a7d626e322d58c9445eecd1e98`  
		Last Modified: Wed, 20 May 2026 09:07:42 GMT  
		Size: 192.0 MB (192021647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:26e363b71ccbbaa7ceb5fed373f76204a9a77845480717667c6843df2fb9994e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16855197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8d5ffae2b965c8fb4fc845521b308df70f7daaf91f8b6594aa12f598a90a9a`

```dockerfile
```

-	Layers:
	-	`sha256:0b74db684ccf6d59e5b445db3029f1fc6d39e24f8327566d9263347d7f3ac976`  
		Last Modified: Wed, 20 May 2026 09:07:38 GMT  
		Size: 16.8 MB (16845020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc103aa1d79d78551d906a1948a7c3b376be3403544850d34acaba13ca98bdb4`  
		Last Modified: Wed, 20 May 2026 09:07:37 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7285ea772fa87e904daceb724faa2254873ecb640b8c69ba5745ed41af8ada7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.8 MB (467818041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad76b1ca0dfe2e8388f68a5662e5ef177ac008449d1151d627871d6636f09896`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1777939200'
# Mon, 11 May 2026 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:34:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 13 May 2026 12:42:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ac0cf25d901b0f78c05ace03b84988d685b5007a5c2ecdb859ecb56d3b46f4`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 46.8 MB (46773178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3f17a612f2a3435e0c1ae9abad061b774e7306b25478218d81e34d30f64a36`  
		Last Modified: Mon, 11 May 2026 00:50:05 GMT  
		Size: 26.5 MB (26492191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d7c25eb5f654458e4aad845eb30dee96526bec66f681e9ed9963f8a04e964`  
		Last Modified: Tue, 12 May 2026 00:38:40 GMT  
		Size: 76.1 MB (76093814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2505df158515b72049e6c42029270741f6e11e042a1a56742db9566ff3fe8f`  
		Last Modified: Wed, 13 May 2026 12:57:36 GMT  
		Size: 318.5 MB (318458858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b665baa5aa55ab92d9aee997bcd329f49b63c636e7899e266872c9c7f32bbdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16940615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447c637b54fb26c7bfbc9901ec7b9599a1726a9f45d691f3e7f4aa03af068f10`

```dockerfile
```

-	Layers:
	-	`sha256:c7cf639241f9e85c72c475ce136e6fb226ab37a31441bd0a6f362e4a5a4018cd`  
		Last Modified: Wed, 13 May 2026 12:56:53 GMT  
		Size: 16.9 MB (16930438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c361cce277f5b11733d00a74e5dbb9e06eaeb846d00013809dd282bd79bc00aa`  
		Last Modified: Wed, 13 May 2026 12:56:47 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:98a4e234a1e928c3eaae52b8b9ad426ce65e9a7a5377e01aa9f2ee8622158be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323512557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c66235dd138a16db3c4a9d2f3d627ce22de4e1ecf7537f2b2f4a3b7bb941cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:05:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7394ea10bf5bc140ccf55e31841e993aa40f4cd465376d373dbae4fff2479c30`  
		Last Modified: Tue, 19 May 2026 22:35:35 GMT  
		Size: 48.4 MB (48440526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee0ef4f478ac4a827949260fdd413d25005b05e8864d837f644813aef5311a`  
		Last Modified: Wed, 20 May 2026 00:18:29 GMT  
		Size: 26.7 MB (26688667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee9f47b39dcfa33283603429ed1ce4fdc019feaebe8a99bcdad2e79cfa369ab`  
		Last Modified: Wed, 20 May 2026 02:06:10 GMT  
		Size: 77.4 MB (77423573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bb0b3c97ca4befc75c74d30c6589b39c14cc55397e7c24a8410579c37c8a8`  
		Last Modified: Wed, 20 May 2026 02:46:13 GMT  
		Size: 171.0 MB (170959791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cce27da7350f4045bd76d7cf573f7d2f8a7e8eeb17654543d6037f0a91feee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16659168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60d59dc7477f3e70276082644e4876f360567441fea5b1f1dd855bd9ec2295`

```dockerfile
```

-	Layers:
	-	`sha256:445648f7b5450b2388c7b08b7fbae5f88152de73545c4d5784efc2a648329048`  
		Last Modified: Wed, 20 May 2026 02:46:09 GMT  
		Size: 16.6 MB (16649023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed380b859721bf45dd66a441ef8397ea5907aa5f972600289821b8826e47da6`  
		Last Modified: Wed, 20 May 2026 02:46:07 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
