## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:f4c85455fd264f4cfb3a678a3073c1dbd5420e9797839154bffbc902610f4ac9
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
$ docker pull buildpack-deps@sha256:94af30e4fa8fc36d343d3068df7f4efca85d0689bd1c3f003eb6afa2ba8302c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323266908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb58058885a7ad019ca5028096650773f07325e333f8c6a76b85d150f32e1f7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:19:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:34:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe71fa68737bfefafea69e4a0c5b69941285043380076279a4d65e82b5973e`  
		Last Modified: Tue, 24 Feb 2026 19:19:14 GMT  
		Size: 15.8 MB (15790747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa00cf3a9efb63d5aec84c5357f82990b3f70ca32d8a41f639c98f03b27f20`  
		Last Modified: Tue, 24 Feb 2026 20:04:11 GMT  
		Size: 54.8 MB (54760461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61055c62b574d5a6764367e9fbc48e9e83de485bf37a6ef2da4e942dbdce75a`  
		Last Modified: Tue, 24 Feb 2026 20:35:36 GMT  
		Size: 199.0 MB (198959266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49e248b944c165c32e15618c7bf08cc82693054ab8eab04c650f5c172208167b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f10b669a7b6178a3370b045179843acf9e1856e8c3c7cb33c438afad5c3965`

```dockerfile
```

-	Layers:
	-	`sha256:2e25cfb6553f216d9e3587e6445abec3a595931a88582b17c9147163b5291256`  
		Last Modified: Tue, 24 Feb 2026 20:35:33 GMT  
		Size: 15.5 MB (15471443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd00c5558fc825957cf0e38546916b56e23566298575d53f8c982cc7930d79b6`  
		Last Modified: Tue, 24 Feb 2026 20:35:32 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:651510ef0afe46dffd1342da646452238cb59fb51ef5113e1505a04baef26c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282214857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0838567e839a589f7cd201850ca2798065924c08df5e4e46bc990f8f6f08688a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6ca5f53d580fbc72887807a74d2d1c2f8900fc3f535a8082d3df4fc3f9e84caa`  
		Last Modified: Tue, 03 Feb 2026 01:13:42 GMT  
		Size: 49.0 MB (49047418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b496e431ca97183650bec266004dde0fc1c85e5f1c690d4146afd2ea94035dc`  
		Last Modified: Tue, 03 Feb 2026 03:30:31 GMT  
		Size: 14.9 MB (14881625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466cdd399272acbb9a1e85ac72634d24be95fda0a3f55eab1a8ce1da5fc02bb0`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 50.6 MB (50640186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba49f5c360bcba7b6578f214e17256eea46d67b7e8abcf8e38cf1ecf5201962`  
		Last Modified: Tue, 03 Feb 2026 05:22:13 GMT  
		Size: 167.6 MB (167645628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36423975ddbf93513ee7b7f6300357c713c9fc55488ce0e612e59173a2218be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15272600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6ead679df2da4d146e45db2e621be99e9e90544c17f9fab1836743bbdb8bc3`

```dockerfile
```

-	Layers:
	-	`sha256:6b2712a7be07811894a9f3cee1a848acd45ba83e8306416caa2a71d93e395fd6`  
		Last Modified: Tue, 03 Feb 2026 05:22:10 GMT  
		Size: 15.3 MB (15262341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b7404fa8fa015ca9bf5d2e330a0271cdf1b207463b5bea05e209961c19ef82`  
		Last Modified: Tue, 03 Feb 2026 05:22:09 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:19aadc66a7743fa0e8433d705be3c5b7ab43db5d9cfd9b1d735ca9973e60999e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313019916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cce2b424a71641e8ae4f08563c2f02be1233cccb9f344352fc7da9710f7eca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:18:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786fbba60dc8d61eaf8fb6b0cf5291a807641e61a5c761e1cba765ef879da43`  
		Last Modified: Tue, 03 Feb 2026 02:45:17 GMT  
		Size: 15.8 MB (15751646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1a0324220213f9a9398a3adcfcebda6418d2bd83212c762c2bb386f570200`  
		Last Modified: Tue, 03 Feb 2026 03:46:49 GMT  
		Size: 54.9 MB (54875010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542cddbf58e2123886de78abce1dd6b3331f337fa011529952f26928803a5ed2`  
		Last Modified: Tue, 03 Feb 2026 04:19:07 GMT  
		Size: 190.1 MB (190134940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c24f91ad6f6529802c050e0cf303e1107322b4912246e016de0bbcfe9884354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc58560234be8ec0290db72fd7bdbebb93ba71db87fd2856eb3430d2b9e9127`

```dockerfile
```

-	Layers:
	-	`sha256:b3b0f8e42be38cb2c5ac826e367297d4f23ad18f609b168fed5dc0ba659fbfa9`  
		Last Modified: Tue, 03 Feb 2026 04:19:03 GMT  
		Size: 15.5 MB (15464968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da77e9c0e4c0a89c338621c290fe09f285c61a0f63bfb0964f99949ce1e5d0c`  
		Last Modified: Tue, 03 Feb 2026 04:19:02 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cdee3c27c36c84ad0d8d5989e2387327b07b4af1c3193bb326a1669a93795944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328919386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00523f9bb01db304b0ef6ebed15a4adb2e0a93c566682085ba3b897134263b0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ba919300e8846f159f61d3dad9bc45f102d2250de1dac9da8674f83e4e628`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 16.3 MB (16295541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c2152f88d25aaccd0c582b343220b4ec754827f272c5f5df677301ccd082aa`  
		Last Modified: Tue, 24 Feb 2026 19:57:01 GMT  
		Size: 56.1 MB (56059516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6625ec994fabcd7117e021e5be81d2a5a9ea5e5d29586c9171c29085646c2474`  
		Last Modified: Tue, 24 Feb 2026 20:19:35 GMT  
		Size: 201.9 MB (201864545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88bc85a43346cef8ed6e45c6dbd1d390f4827044efb962d7c77fa714f0a35bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4e5b082f3bb4c45572ef742eb11a7090fd7e2b7fd0c7f4cc9ff39a09df3a3a`

```dockerfile
```

-	Layers:
	-	`sha256:89f1082ad0ba92665d63761965989c247ec11619a99c7b1b085582303fbf092d`  
		Last Modified: Tue, 24 Feb 2026 20:19:30 GMT  
		Size: 15.5 MB (15459458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9a5b0b4042abf1fcce1c703bdf8149dcdb9ed2fa6d413c87e0152663cc4c66`  
		Last Modified: Tue, 24 Feb 2026 20:19:30 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
