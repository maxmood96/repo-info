## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:d345de3e270abece7f2060cc0e9ba3cc7fb38b8b131a7cd25e3c0fa6f93c25c1
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
$ docker pull buildpack-deps@sha256:9fcd96aa16e4b5b878c41b2c8a7e947727bf33c0624bb76a15932f01596ab0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324669920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d79e6840ec104aa8e0c522b8f9449cdf1b0ef57d4cb0feca5d83880d73fcc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b9b505d2f2f0a849a74a095acfe5025f5d72fb01d82d04f1365cd960707119a`  
		Last Modified: Tue, 25 Feb 2025 01:32:18 GMT  
		Size: 43.9 MB (43880302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd562fc242f36f82e6cc8e66ce3b8e9aacffd6f2c454b8c1521cbb050ded690`  
		Last Modified: Tue, 25 Feb 2025 07:17:52 GMT  
		Size: 24.1 MB (24088476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f19655c88ddc6bc9f7163357a30ca6c32e0e8136a77199ab4041d2b3ad565`  
		Last Modified: Tue, 25 Feb 2025 14:19:56 GMT  
		Size: 62.6 MB (62622433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd31e9a72d836dc9855e23d0076b28aaf054002915002cd4cc64b2c020e842c`  
		Last Modified: Tue, 25 Feb 2025 16:56:57 GMT  
		Size: 194.1 MB (194078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07381ee77f15e56d49cf67c23670000c67c5b053f34db7d85817b2690ceb4d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16612630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb134f75135b1f552387cb779a38d5f363efcb28da8501881f3dbb5f366b0b8`

```dockerfile
```

-	Layers:
	-	`sha256:87a680b56280e030ef51364879d43d5a25bb876b3762ac57843829403521f284`  
		Last Modified: Tue, 25 Feb 2025 16:56:53 GMT  
		Size: 16.6 MB (16602394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db5b9168ab40ca0d4c3c2366b68ffde87a9e1b595c07cb126b25d446066dc9d`  
		Last Modified: Tue, 25 Feb 2025 16:56:53 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6433d7b7bd5eb9edffced646491465af269a1ab1f9a2b5e3999b213338d0bf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.8 MB (368834759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d53dffdde403238f012e04beb5e4dc3d6b1aad4c84cffa03c594befb79b9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82dee3ca1e84a7a17d41ea99cc856a25e454e910360ce904862612b751069507`  
		Last Modified: Tue, 25 Feb 2025 01:32:16 GMT  
		Size: 47.8 MB (47842599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fdaf1ee62a1e8985dc4f6dd94f1ef4b21fdb86969059a5e1bf8b87bfc3b6ca`  
		Last Modified: Tue, 25 Feb 2025 05:42:44 GMT  
		Size: 25.7 MB (25656066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b361fcdee5d50fc8a582c25e48726784dea4601570e0bb7149e796c01faa8`  
		Last Modified: Tue, 25 Feb 2025 11:55:29 GMT  
		Size: 67.5 MB (67530634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4152b2963830cdb8c0e41d6026166f1549d76a3afa9e6365568d8db2601cdf84`  
		Last Modified: Tue, 25 Feb 2025 15:25:28 GMT  
		Size: 227.8 MB (227805460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00f0844cd7d5fa5aaee20dac0283e2f729ab528d5ee648627da0a44076890fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16928546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79b93a235ea4a618aeb4ab1cfa2d37910c02b27ad295b4d7a5e083ef22351a`

```dockerfile
```

-	Layers:
	-	`sha256:c92dce7383f9cf40817e734d6dc0e24da8beb05cf748ae2d6696a4d8c883f676`  
		Last Modified: Tue, 25 Feb 2025 15:25:23 GMT  
		Size: 16.9 MB (16918291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29d11e9b4cac96eda836997060223e3fa96cea4014426e3f2eb95fcef6df437`  
		Last Modified: Tue, 25 Feb 2025 15:25:22 GMT  
		Size: 10.3 KB (10255 bytes)  
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
$ docker pull buildpack-deps@sha256:73fd056c3dd267ebc58edcbbb33e1fd7894658853c2efceb66ae5777e844adaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358998443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e706529e5be2e20ccf17730016e6e597416b5fd576372e39e9d822bc2c61a151`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34ea8e316aa47eaa9617f1b9a35d3a8120ea53cd407c4add1aafff37c0381edf`  
		Last Modified: Tue, 25 Feb 2025 01:31:10 GMT  
		Size: 47.7 MB (47672872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d13ce39ad4744d80777f693b612839d6935dc5ee1e34838c927f4fa9839112`  
		Last Modified: Tue, 25 Feb 2025 14:50:38 GMT  
		Size: 26.2 MB (26241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f7abeee55e42bf6af8399f8945e651d4fb037fbd0f0edcba9023eb4a7ed34`  
		Last Modified: Tue, 25 Feb 2025 22:29:34 GMT  
		Size: 66.7 MB (66682191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546786252f2fa0873d27f3942813f6c9f80a75a64f2b32da62711c0853fbe3a2`  
		Last Modified: Wed, 26 Feb 2025 02:25:13 GMT  
		Size: 218.4 MB (218402233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4c10f06c387dcb8e80dffab712c5963a015e190ba87be53b532b74b4b6df41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c0331d73ed35dafc0e9f3e9b96de6e06615f97ee8f9add014cff7d221f60a1`

```dockerfile
```

-	Layers:
	-	`sha256:bf0f369dbcf081b7ad0c3bc8db2c6c631abd5a280dabfb81474c02e262fbf6ee`  
		Last Modified: Wed, 26 Feb 2025 02:24:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c568e0f79b86d6dfd6b0691fa6ae869d4796972c467144a1f7203b8173b3f1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.2 MB (381158660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db03b137216949408928eb5fab4abd637d465735b2b5fc6c459baad47d050a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9370c4ccc640520942cbaafa9d1bba72d3a14bc22c93d4c585e6cf8f83d65274`  
		Last Modified: Tue, 25 Feb 2025 01:31:22 GMT  
		Size: 51.1 MB (51109956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a14d42f5e429844e608bdea207bfc8db8bb3a74d08ade67bcacfe19c5fbf8`  
		Last Modified: Tue, 25 Feb 2025 04:33:25 GMT  
		Size: 27.7 MB (27746070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aaea582b8b7ff6324c9b146d200160cd89f84b7db9c384d8893b333eac8a62`  
		Last Modified: Tue, 25 Feb 2025 08:21:01 GMT  
		Size: 72.9 MB (72851519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfe2f6f333e10f7540804d77054d6a4092aae35fad07a48523698c116e42bf0`  
		Last Modified: Tue, 25 Feb 2025 11:53:21 GMT  
		Size: 229.5 MB (229451115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:909ff248adbb154f7cba2e543d8286e6cef6212c889f6b9640b19fe00859c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16834378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57018b5179c3ddbaa7e62c7e95e6779672333ae6d2ec3e6830cf128097c772b`

```dockerfile
```

-	Layers:
	-	`sha256:620350a3044a6c2f2e5dd507e63b20703f6caf49515425c07027189606e601b9`  
		Last Modified: Tue, 25 Feb 2025 11:53:17 GMT  
		Size: 16.8 MB (16824170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352f44514a0baf72719d09119597f49de84aa6a28d58c281ddf68c6f7676040a`  
		Last Modified: Tue, 25 Feb 2025 11:53:15 GMT  
		Size: 10.2 KB (10208 bytes)  
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
