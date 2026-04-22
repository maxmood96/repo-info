## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:1a0c902d56d92fe1b548f0adedb6a9291e20f7e39a38f7dac92a7c1ff29612f3
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
$ docker pull buildpack-deps@sha256:e5fc31d8fdca196a8c91485bb49be6dd7b72246db7389414fc18880a0c9d5098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350908175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c365d3e99163fef501f2f274a83f5b5773202d571ce8575b37dca66b5210104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:12:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e592cd2ed9323d51731ff2e060da4790d904454d4dd8c0f58dc124b12854233`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 27.0 MB (27008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68baee722d285caf3b4327e15b2205e5b417d177e480c8c55a3ed01842c26381`  
		Last Modified: Wed, 22 Apr 2026 04:45:29 GMT  
		Size: 77.0 MB (76969954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4074c68b5df515ef5d60615498c46cb043cf2a5598f4bbe4bc6e038a6ff427`  
		Last Modified: Wed, 22 Apr 2026 05:13:17 GMT  
		Size: 198.2 MB (198232568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:473fffcb83101ba916a9eb56c76ec0f6cee1645f47ec2cf48c2acf0182ca6595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16885861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f33e60c5f1fd2b95979c3382c8fa7e7d995b7d1921b0daa0ca5cb0b78bf979`

```dockerfile
```

-	Layers:
	-	`sha256:17ffecf7a55f0603b7665b5cbf8d2c152cfd01aa7154a7c38803df1a9bd09099`  
		Last Modified: Wed, 22 Apr 2026 05:13:12 GMT  
		Size: 16.9 MB (16875716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723ccb0e04d2df5148ec963c40a5b171c64aee540e77b1afdf0509386c241846`  
		Last Modified: Wed, 22 Apr 2026 05:13:11 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8daf3b4d79d4ca3fed6e52c40590fe745dec5b8536e1d9fdaba8a24c3e531d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296057782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a9ecba3729280267fa180289bf83a1c090e57b22d8a81a8dbc8c89087371d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:15:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616f54f84dee8932180832c344695078e63789301eb12467ca880323e3400586`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 45.6 MB (45622135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970639d217085f63010f6da0cad6e9f8e048924120803b4eb157ac1c2f651a`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 24.7 MB (24685888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2d4b24b5c349381f6b7163ca764f633bfc2f44c28abd2ae354570db164308`  
		Last Modified: Wed, 22 Apr 2026 03:52:38 GMT  
		Size: 71.5 MB (71474107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4c4d0d3729ec107c4dd6fda65a1ab42cf6ecdc0c47e064d8a152f4cd1c358`  
		Last Modified: Wed, 22 Apr 2026 04:16:29 GMT  
		Size: 154.3 MB (154275652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9518e0b53e6ee0320c38a6df3d10cde82be30d6f990c2fbef48b06390e5ee8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16639600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93421a98fe0eeaff6cbbcd88348ac99889b22abbb4cb4c4e6c367604f81a777`

```dockerfile
```

-	Layers:
	-	`sha256:cad1e5beb9a6a5bc398b0e2b13f4c4251201cf0c5e12c49c74e2327a93def404`  
		Last Modified: Wed, 22 Apr 2026 04:16:24 GMT  
		Size: 16.6 MB (16629391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759ead16d59a79c740f65bc748310de8236c5b4597d464e5485bedd975d5cc1b`  
		Last Modified: Wed, 22 Apr 2026 04:16:22 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cfcefe780f8f8e2fc8c548ba73b678c50aa70a7b19ca42b472935eef5a81099b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aedb9cfd6b81c184f80596271b535fbfeb66d29972261d506804b7d0222d07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7406cf4524d3710a69a6e4bbba357df8393b55da990695b89997aa04b54031`  
		Last Modified: Wed, 22 Apr 2026 01:43:16 GMT  
		Size: 26.3 MB (26289212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943416c03b0fa211b9ad3c070b785a9f8b5fea034656c1157181cce52e7b2b98`  
		Last Modified: Wed, 22 Apr 2026 02:32:45 GMT  
		Size: 76.1 MB (76104831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064597ae651da46ed5165c71083726ad4f216943ba9d4ee8d2e6554550ebdba0`  
		Last Modified: Wed, 22 Apr 2026 03:18:00 GMT  
		Size: 188.0 MB (187955109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c55da1d648639c5709ede2765715e6b77599fc4a00c69ceb25454963094bfc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16968328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec2fe728ac5180b588a8e6f37cd4b48750c3cd3f84cdf0dd06e165f90a5eb36`

```dockerfile
```

-	Layers:
	-	`sha256:678c1569df06023c2607d182bd264e416b928508768f76300f8c2c566e2c5e1d`  
		Last Modified: Wed, 22 Apr 2026 03:17:56 GMT  
		Size: 17.0 MB (16958103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f93aaa5cbcb688ee4427b3b3c760158caa38705d98de0b0ca3ce0b85cf74ae1`  
		Last Modified: Wed, 22 Apr 2026 03:17:55 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d6e0d77b9378976fe41c7d13c179d46d37c56c9f7a4dd7f7f19e5ae1d0143fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 MB (357808993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee448bbc92d9e12a7f0c1d7ea304c8b1101913b88e627316ca4b7ef8aaa1562`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:40:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74970d6f811b29c802a9f3c8d694bfd2f422255c20b66bcc271ba0c7bcc9dbfc`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 28.3 MB (28298911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d376180d010f10a41a07c62fb3fa00f2442ee96ea8b7248d80a02311ec598b1d`  
		Last Modified: Tue, 07 Apr 2026 02:41:15 GMT  
		Size: 78.6 MB (78591062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e8c7efd81c10b99e8acea59976a68692a3afa02433ab1f09c4e0b579ad085`  
		Last Modified: Tue, 07 Apr 2026 03:20:18 GMT  
		Size: 201.0 MB (201040631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06aad3fe0cb2f35fe08e320c5b6eddc53c67594abcc8c7e33f1f7b15009a4c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16795289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3896e91b40abd623263133a3c71e928d88f50eebfb30849299e75d7b7ad3ef07`

```dockerfile
```

-	Layers:
	-	`sha256:c4e0d079aeebd234a19c6742e8b13949ee301b0103d103791cf29377fd887ac2`  
		Last Modified: Tue, 07 Apr 2026 03:20:14 GMT  
		Size: 16.8 MB (16785167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae2db61b08e25ef9f0ce089c0261a2df17a81f23a5d2d94ab5898da67c6455d`  
		Last Modified: Tue, 07 Apr 2026 03:20:13 GMT  
		Size: 10.1 KB (10122 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3db41219ea4e659c61cb868438448ded1d1569fbe5fbf90a81e642eeabf58c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 MB (357835995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33745aafeea68dc6291071ef06bc599e57512ac272d52bef64d6ced10105c63f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 04:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:07:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82a75a893b6c64944c6f9a45687c1a1f96d90f40ac32f7359ffe0b6755458be4`  
		Last Modified: Tue, 07 Apr 2026 00:10:12 GMT  
		Size: 53.9 MB (53851237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b159d77ae23ff0a537f251333a902815f558c4d2eb7e7cb1124f2b5ba37262e`  
		Last Modified: Tue, 07 Apr 2026 04:22:08 GMT  
		Size: 29.3 MB (29318642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea75b9cbb530f46935065289cc64cf7b3ac3d21234960ebf989aceb6ac5630b`  
		Last Modified: Tue, 07 Apr 2026 09:52:53 GMT  
		Size: 82.9 MB (82862097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2d795e6ff7707d671b05fc5ecc31d2f80711d05221a6058197f2a8c33d04d8`  
		Last Modified: Tue, 07 Apr 2026 18:09:17 GMT  
		Size: 191.8 MB (191804019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb17d97049e1a08c46efc59b64aacd7262506b6dc8822d87da2d9488daee4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16777054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b867dfcff876f0e7d6cae0ac4d929fbc0d574783b134b80eb8b81b7ac65da0e`

```dockerfile
```

-	Layers:
	-	`sha256:8117fbf967aae7dea41ae953b7fe7bb621a0fa3a5ad2ea3eebde766a90224507`  
		Last Modified: Tue, 07 Apr 2026 18:09:13 GMT  
		Size: 16.8 MB (16766878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f0a6d59f6b31da63cfe65c03ac1d19ada0a216ffa0c43594308487c89a4a6d`  
		Last Modified: Tue, 07 Apr 2026 18:09:12 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58978c1e0e395f32d4aa30503e50eeeee22bb58b450cf4b8750a419d4eb8cebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.5 MB (465537536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a94587204091118de12a06c3ea926154a0a099272036176430a6f1b201693a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1775433600'
# Thu, 09 Apr 2026 01:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 08:20:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63b5561c308233dcf634aa914acd8af4b95568018df569d4d43c4791c98cc9ba`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 46.7 MB (46698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d867396e8c8691cbd2e099e7a0d3c7c33eed2261193868cfa5cfdebbe037af`  
		Last Modified: Thu, 09 Apr 2026 01:48:33 GMT  
		Size: 26.6 MB (26580851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d7c78d4e0f683fb07cd5e1493fc6c006352c3197e1c49758dde411d0f9d76`  
		Last Modified: Sat, 11 Apr 2026 02:49:35 GMT  
		Size: 74.8 MB (74755929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d88f1511eaaca7b7f47f40047169f69f4e64fada65fcfa543a682f3ee25d1`  
		Last Modified: Sun, 12 Apr 2026 08:35:59 GMT  
		Size: 317.5 MB (317502581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ee4778b4a936c7398b86181dea33be3ddb6699455cd19147c4ed53182f64e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16871754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019e9c71bdc3fabb430f581a2d129fae254a724a8c24c290ac2acd1d3c9d0128`

```dockerfile
```

-	Layers:
	-	`sha256:b5f2c2b51705664af18e232aee9489dca52b42b79e59f21eb442ebd4d25e6a70`  
		Last Modified: Sun, 12 Apr 2026 08:35:10 GMT  
		Size: 16.9 MB (16861577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50b9fb3b4e08782e4266ad2af612bf0d9ba5cb206fab41abf58aba6f0752ebb`  
		Last Modified: Sun, 12 Apr 2026 08:35:05 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5cd0d7b94edc865781b69e001cc26d5f0ee3539b77471b24c96addb00d7f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322688748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e47ef10472e91d7a27d2d493506e9aaa3911818cee007509de448ff13f901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 03:04:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d387cf27b8c74bb29905817ad867265b401af02fdbc21b522a98041e86095a47`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 48.3 MB (48291595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71640c6f0517962fef2d2cecd2252a1ad50dd36dcdfc5949b497510671693745`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 26.8 MB (26816201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d200d226dcb1e9ec18c10fb8ae6afd2e2e5f3a76506193fd7ffbd528f5de7`  
		Last Modified: Tue, 07 Apr 2026 04:55:09 GMT  
		Size: 76.9 MB (76879572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384dfb42b1fe626978c0fe2c478bf62e09ade9f0d508ccad09d28365801b200a`  
		Last Modified: Tue, 07 Apr 2026 06:01:10 GMT  
		Size: 170.7 MB (170701380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:327b60f036397618a25e6f1ce57a4ab54fa79db9ad67db03bda83bc19a81b2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16581169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2d3f9505b7dbb18755b6aa215e745be96632ee53c930e23455729e68039ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c496478fd18b9cf287fe256d7875870060202f6d2d89954646a01969268fe144`  
		Last Modified: Tue, 07 Apr 2026 06:01:08 GMT  
		Size: 16.6 MB (16571024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b1159b3f2d8a4b8a3e2d8a7b0aa614331d6be331c3d9d487a2815e19bbac96`  
		Last Modified: Tue, 07 Apr 2026 06:01:03 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
