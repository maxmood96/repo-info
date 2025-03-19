## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:b78be7e380a52320f674d5ea4ae13ea8a87708fbf8efbc870ff8e9c6edbeeaaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d5ea14e8042ec88cba63e993d4deec2b37203f9149007082a387885323103d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 MB (376824504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c6173e2a1c66528e7f6e61fd8288eac53359390cff23a06493a797ee32e58b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df0497091d0cfc8e931a73bef35cfd57d59f19322fcca6f87470d3b532a9d8c8`  
		Last Modified: Mon, 17 Mar 2025 22:17:40 GMT  
		Size: 47.5 MB (47542630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd1ca2661836ac2dcfb48519e1a1fcf2b3ddbc182b83cfd451a37cea0328fe`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 26.3 MB (26258246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149407641e16b36b863b091be42c587e870ccda41512acc3340e09ccd2a747cb`  
		Last Modified: Tue, 18 Mar 2025 00:19:02 GMT  
		Size: 67.4 MB (67446201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a4decedebacfeec59b12971bbde1c64d3bab386e1f9dc298e9e8c91a845fa`  
		Last Modified: Tue, 18 Mar 2025 01:13:50 GMT  
		Size: 235.6 MB (235577427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb9693ba0f72c748af9ba58a171f3398f0424b1a9418f7cd718cbecc387727df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16858996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dccb1a1e766ecaa873080703cdcd3c5a84ab4bb07af3725caa55e87765337a`

```dockerfile
```

-	Layers:
	-	`sha256:d1dba16e332f445a764471a28d9386d8c8a3a2239e391c0fd457604c122335f9`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 16.8 MB (16848820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94165f96cebfe46c5a0b403c96d805ee682f03d67431481564c2d9dbf7d76da9`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:be36f78fa8d3c2ffbddd0d22b54bda77db82f550b1b7b33c8266cdde1b461826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340992555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd83f01a34e9c731c3b39c6868bc6b330050d1560e3b5871a731e0e88bcb504`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404f8f7fc411f8ff4d9e0e372fba1e5c10c5194b11ce9185a2da79073a4ac30`  
		Last Modified: Tue, 18 Mar 2025 05:17:45 GMT  
		Size: 65.0 MB (65008424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f582acae5b75f91304b34b72f43c840e2a5f07e436f0e9a6d41fd49ee33c575`  
		Last Modified: Tue, 18 Mar 2025 07:46:58 GMT  
		Size: 205.3 MB (205257461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5c0bfd54b425c8610523669484b34cef6466db3380f8299d9f776d4fabe2e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16629074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f47f04cdf10c7345a742a3c45d6dad35478346fb2e1afc54559b844caedf4`

```dockerfile
```

-	Layers:
	-	`sha256:6663ae76a8fe50b96dcb176bc8671f55e4f7d7cc82e8849e08ed61ed5998f4fd`  
		Last Modified: Tue, 18 Mar 2025 07:46:54 GMT  
		Size: 16.6 MB (16618838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3c99dd9ef20911bdc5533d10ef060a796f305689df8720a1d984e915efdaa7`  
		Last Modified: Tue, 18 Mar 2025 07:46:53 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c413dfb73d37d812e369f945fe3eb52e70877f0842219dedeb0fd693a207cfe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323207909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137e16de4776efef9b6835474162cdc668da481700a979837ab1d2f452d1cad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d0067c75852db589ec6309ccaa1c2e508a0e7bb3c58863fcadae19a1c1537e18`  
		Last Modified: Mon, 17 Mar 2025 22:21:44 GMT  
		Size: 44.0 MB (43957597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d864355272bf90fd1144966fdc99f539dd4252af76ad0a5d7e1ee868d856d`  
		Last Modified: Tue, 18 Mar 2025 07:22:02 GMT  
		Size: 24.1 MB (24132404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef046ac7256a24a47a1208d1dca17bc5d10a76b0eec3d2cd94577b18be639d4`  
		Last Modified: Tue, 18 Mar 2025 15:31:50 GMT  
		Size: 62.5 MB (62515598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe008e013fa288b0c0b7e659668cb7168447ee9f0b8e9cec325638374c6f2f99`  
		Last Modified: Tue, 18 Mar 2025 16:21:41 GMT  
		Size: 192.6 MB (192602310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47683ecb0dd082e9a049428056b2fb871b610561995edcece07814c2380dfac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16628641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401e6bd59ce024e1a8d8ab60668091a9da4452faec0d6dea8f53ff544710a62`

```dockerfile
```

-	Layers:
	-	`sha256:28febfa389ce6ac3f8b59d09c13755247b148ab84f11a00d726d0c7573c21d52`  
		Last Modified: Tue, 18 Mar 2025 16:21:36 GMT  
		Size: 16.6 MB (16618405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bfe21e029a12e7aa2e50dde7163c115f3b1158dcf0dfb3ecf684d27fe13bb`  
		Last Modified: Tue, 18 Mar 2025 16:21:36 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6ea22783b50950e7a2ea2d32639243fb3820e4ee9604d4aa1a93d17f27c76327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367744114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cda23af725668f03cbb96806544a7d9497d3804ae80aeddc3ac02bec4487a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94a031aaac55d50c4495d8888a65973ac1a320a931aa0e73e9fb6cef43e2efd2`  
		Last Modified: Mon, 17 Mar 2025 22:20:15 GMT  
		Size: 47.9 MB (47916898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9c585ccfb21ec8756fd9ca6b5b83f6e36d0003a2342f6f55b3087ee0d0f4c`  
		Last Modified: Tue, 18 Mar 2025 04:59:39 GMT  
		Size: 25.7 MB (25697882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d5c4d521a51c32b5544ee4fd67c57ead31e48e0d9a394edb180d78318d630`  
		Last Modified: Tue, 18 Mar 2025 13:17:35 GMT  
		Size: 67.3 MB (67330212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39170df892cae0091dd72e23ef146630d9774bb93f5036c9b209b5235788849a`  
		Last Modified: Tue, 18 Mar 2025 14:38:40 GMT  
		Size: 226.8 MB (226799122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11099e4b4b75a0a776288bbb304822a79ef319800f35dca7afb0d173a2dc4512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16943937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d01eaaf8e7f1fa3f572c06f2edf18db33ca454350ba2eeb2ed779b0b2cd3b5f`

```dockerfile
```

-	Layers:
	-	`sha256:5a56a50ab788e181b17f9061cf1bad9976fc0fa2beca64efdcfc9fe20fab8a79`  
		Last Modified: Tue, 18 Mar 2025 14:38:35 GMT  
		Size: 16.9 MB (16933681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade512987613d912dc10069ccb247b43e03ec5fbb36a41f2484279df924d1135`  
		Last Modified: Tue, 18 Mar 2025 14:38:34 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b355c200602814e836e976a5335927264dfa0f291e1060f6e9711aa8a6e98d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385524543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244c110fc3c83aeb562ca8e9dca6d33b8736561d64332ca39ff3d6ef4d79e62e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f3d6c6a3aa49b126cd200d7ce5830c3bb8ef015d44bad711b523cd3cad501611`  
		Last Modified: Mon, 17 Mar 2025 22:18:06 GMT  
		Size: 48.9 MB (48863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888eee8ccf6b7f4f49c878caf4a23b48de26dc0c12d38b4a0f13ce0b7214d834`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 27.4 MB (27396309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a0a08d8deb9509e0c71bd1f0ab45d6576afc1729935f007ef7d9163649bcf0`  
		Last Modified: Tue, 18 Mar 2025 00:19:00 GMT  
		Size: 69.5 MB (69490332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd11aff3da489123f3789b2bc380d292cc91715d0b05066e40e8b5aca761f4`  
		Last Modified: Tue, 18 Mar 2025 01:14:03 GMT  
		Size: 239.8 MB (239774741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d47f60f4b9c1776140b569967909bcb4eee617ed9113baf40f48cebc8fd43797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16828499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dbd1701e06a149af87b6f6784522007f3c4bf534a4a1207b2d16450a789577`

```dockerfile
```

-	Layers:
	-	`sha256:c289d2766da2b7d90714bef04e17a5d7020b07e9a316d28984cd6beeb2e65a37`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 16.8 MB (16818345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeffef4e38e1157e8a0cc28d6c03e0bd370b48f6e0e4b28269b0ffad3dabcc3e`  
		Last Modified: Tue, 18 Mar 2025 01:13:57 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:63c2343097851d188b0ec81f6a553972aba44defea19638b7dd310bcd2a9d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358290493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d16b8d3b132920e1dcb021538fe92b52cebd7129474c8471ad9e38553b178`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e12542a0a53bb97cc352ca7ce416a009a12137a70b8b9c3e736be4923c559ab0`  
		Last Modified: Mon, 17 Mar 2025 22:20:29 GMT  
		Size: 47.8 MB (47750847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e581beb347f24f554e5f2cf2d1525cb47adbd2ebd171f2c46bd47fada5257b`  
		Last Modified: Tue, 18 Mar 2025 16:30:23 GMT  
		Size: 26.3 MB (26282283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3cc7353bb84ae34c688ff3596f801439d22635390e86e17ef4a03803ec818`  
		Last Modified: Wed, 19 Mar 2025 05:27:01 GMT  
		Size: 66.5 MB (66534135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6997771a7d9e486893b103ea01f09f7c8aab4497f51e63a06d87536cd35add1`  
		Last Modified: Wed, 19 Mar 2025 13:37:46 GMT  
		Size: 217.7 MB (217723228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50810e450fb8ccae9b440dd111e2899ee812de05ae45f3c37efe7e3bc9e9569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c84d0e7a0ca14099125937c67fb17f3ff8b4b267336c16ff85c9cda6c74c54`

```dockerfile
```

-	Layers:
	-	`sha256:bbea06d244cee2b98ff4aa2df8e7403236d91b4bb08ab453dfe4dce71862d7df`  
		Last Modified: Wed, 19 Mar 2025 13:37:27 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7ffd04fc02922cd48be44af9a83f47200796286a0a95011d4302db1dfff74ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382594929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a2132dd3da3db791fab5782ff3a90f1ee636fdb78a528e0df3d6eea984eb57`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1b9cddd723c4c8c3ec8dc918782516b3f18afb7b43c91515f8578d7f2ee55`  
		Last Modified: Tue, 18 Mar 2025 07:11:29 GMT  
		Size: 72.7 MB (72729373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd8a8fa31bce3f93e070ba7bb6840097bf447bf40a43360ce4dd5780bb2f7fa`  
		Last Modified: Tue, 18 Mar 2025 13:55:06 GMT  
		Size: 230.9 MB (230869967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:001d25f33df3f41f03a4ffa2b1dfa76b6a6f454fd8c2089d680019e62f6968b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16850362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd1c4e5fa2a380889aefe2f6ef3c80dec596ea8c41e5222fe70849447c9d26c`

```dockerfile
```

-	Layers:
	-	`sha256:b014d9720078f0d5e2b1d52d68a0112e9fe0fe1e54ce97978cbc4cae4e6538e0`  
		Last Modified: Tue, 18 Mar 2025 13:55:01 GMT  
		Size: 16.8 MB (16840155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08af760573c8a4f30aa596b209aa6b1363368e866d28cc5a26142191af39b8a4`  
		Last Modified: Tue, 18 Mar 2025 13:55:00 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5cbf508848c9f5185a0029b85942e9fed288a2282624261e3c964e83ad9ca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.0 MB (459981521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5bf7a214af759c473209401708b1c26940bd1c196ae17abed369e4607c48f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e088c063eb399e547ca6ed33d1ebd46f19289743d98703ba83311c2214184834`  
		Last Modified: Mon, 17 Mar 2025 22:34:26 GMT  
		Size: 46.1 MB (46065424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a540c8b69cf893a7a0a6c436d4761b79fd51f1845aa5b66555a58dc019b8cea8`  
		Last Modified: Mon, 17 Mar 2025 23:27:02 GMT  
		Size: 25.6 MB (25578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791930e93dca7c6cd366e9acff8ae855c1dbb03f800b05d14c315a184e79b1fc`  
		Last Modified: Tue, 18 Mar 2025 00:21:17 GMT  
		Size: 66.3 MB (66332717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdcfc66d4e097895bd9d0bc6be12587270f382144f35e4848ea98e916313908`  
		Last Modified: Tue, 18 Mar 2025 01:35:56 GMT  
		Size: 322.0 MB (322004615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd9e8283fea2b9a02fd18f174408808b28c49fbe64315961594a2c52a7977d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16914395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aeef60d164e8aa231fb79576c0136a835c6177e12d35aac676d4b8b2efe1f95`

```dockerfile
```

-	Layers:
	-	`sha256:e33bb8b1392b9e7beede2ba2399e1b58b7406fdb3c436ecbd5db0658500c9b55`  
		Last Modified: Tue, 18 Mar 2025 01:35:19 GMT  
		Size: 16.9 MB (16904187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4631d7101c67e19eef836d339a03749dbef394c0770cc6ee38085dea322668`  
		Last Modified: Tue, 18 Mar 2025 01:35:10 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1774c4c785a4a8ff60a1cca0f8535b5ef1f0fd4508a729d948069d5dd1bcacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355204087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ecacaa9f49d89f18ee6eeaf045844d3038f3f41ead448c693c268ae782f508`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e745d023c42b8954a78b55b72c865750f57f9ee36521990f6f841b155c5ea`  
		Last Modified: Tue, 18 Mar 2025 05:56:55 GMT  
		Size: 68.1 MB (68118368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a34e553468bdcb19c56bf2ff84b0dbf4cc4df8dc207ed19d676a58c343c971c`  
		Last Modified: Tue, 18 Mar 2025 09:28:30 GMT  
		Size: 212.1 MB (212111659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1600e21161f75dcd5caca8e79184ff099b5c120445f56922a862a09b0ebafd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16623516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ceba67566033ed1fc7dbdbf9f9f6f1c240f9f3aebaafb82c0b49fcc78db102`

```dockerfile
```

-	Layers:
	-	`sha256:8ee0303b501d8f7d891ad1d1201308a7050e8bf3b1e0477a5af87c56384f8fa4`  
		Last Modified: Tue, 18 Mar 2025 09:28:26 GMT  
		Size: 16.6 MB (16613340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3791f79efa336e03d9502c4b78fd4cf75bc6170d1f6bc0f2177a188663d100`  
		Last Modified: Tue, 18 Mar 2025 09:28:26 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
