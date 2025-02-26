## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:9206db3504830246f49dead6c0cccdb275b265ed15059ca5a01e778fafc482d6
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
$ docker pull buildpack-deps@sha256:32b7fa5013a5923bec01926453448712665a92eb2ff6ae9564c2e22d80d79cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375182269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccb8174ff8da569b4476052a17287e1b535a8471256c38ba122014b6024c752`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:950923b83892d84e409583fe8acab5a43a4ded92172eb9eeccc75b10012df546`  
		Last Modified: Tue, 25 Feb 2025 01:29:43 GMT  
		Size: 47.5 MB (47450585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8896ab25253a01ccf34a69a21881e74b41a25ff808e9b6217bda2404edb01961`  
		Last Modified: Tue, 25 Feb 2025 02:12:39 GMT  
		Size: 26.2 MB (26209855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41757968bd034488636645b2f5f31edb844db8e61d6402ac8aa7b5539e2ea59`  
		Last Modified: Tue, 25 Feb 2025 03:13:39 GMT  
		Size: 67.5 MB (67525915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a1a4e23340835a04ef09e5f4656568fe2151171836ce4da5cb8c5f591084f5`  
		Last Modified: Tue, 25 Feb 2025 04:17:56 GMT  
		Size: 234.0 MB (233995914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c120871908811bbb78fb17c39c2427cdf825b337c58156f1732b88eeec79eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16843595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e3d14518a25ba350d50f8d06cbbf5806778516fd27dacbad1d9400b37a9367`

```dockerfile
```

-	Layers:
	-	`sha256:1f2eef29b60a7bc80f951d1aebd883cf4a2393eec7b1933af2f2c254092765d5`  
		Last Modified: Tue, 25 Feb 2025 04:17:53 GMT  
		Size: 16.8 MB (16833420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342ca8555505e6efc76bd136ec1542b988530d97ce02532dc7bab281967b0ec0`  
		Last Modified: Tue, 25 Feb 2025 04:17:52 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8524881567c0ea12b50adba3b8d7e49e038605efebc73f705bd4fd5a32c52a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339530775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51caf8637d3c87d38635483756ed5d0363e838d7c139d121eef02cc78ec460bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aec04388a5500e40b5b47dc94d28a38cfaac08b914f818d50d6fef28b32d9a5c`  
		Last Modified: Tue, 25 Feb 2025 01:31:20 GMT  
		Size: 45.7 MB (45691956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7909ec64897749d066538d04d73bf65a5bcacffc48c9bca80514cdb519fe3782`  
		Last Modified: Tue, 25 Feb 2025 05:16:49 GMT  
		Size: 24.9 MB (24906569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27f57f665013eafdf01b5a42494dcb8116446bfe558f079982977e9c2514fbb`  
		Last Modified: Tue, 25 Feb 2025 08:37:57 GMT  
		Size: 65.1 MB (65144391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78c22d30ce41478e91b76174bb3434299e02855fd96c2e7b270395dd49b68f8`  
		Last Modified: Tue, 25 Feb 2025 10:16:11 GMT  
		Size: 203.8 MB (203787859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12c8aecf965ec64766f7205f3ac0064bc8554f0e31d3b569f0ddd815ad7855d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16613045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fa74cc2a490f2831ae206fe816748efaad00d7c69319d0bd3b6010ec49bef0`

```dockerfile
```

-	Layers:
	-	`sha256:edb5b64564bc98fc49ca7212b383a0cb89290787cc19245fa2e4710b4f53ecaf`  
		Last Modified: Tue, 25 Feb 2025 10:16:05 GMT  
		Size: 16.6 MB (16602809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e366b16cb5f9d7816f350015de632f5a5e32301a1a9902cb34dee76f2b0817`  
		Last Modified: Tue, 25 Feb 2025 10:16:04 GMT  
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
$ docker pull buildpack-deps@sha256:493a3f9d9df7967068cf147483504cf5e4a8e27f6b2ec063b3646e26ca5ca11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383380651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378edff4eb7fe64a9d51929374368fb2b09f21f5c70a8bd3c1b33a17f3b747d1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aae1e98269b26509d10518853922a459fafd0d625e12a0e3bd33654e86d19bf9`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 48.8 MB (48759296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75db5fe14e7f8d4a4352afc6fbce8a608d64e144a93abb709938695801d5f5c`  
		Last Modified: Tue, 25 Feb 2025 02:12:27 GMT  
		Size: 27.3 MB (27342554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f104786b18cd811e268777c977024df12ef2dfaf94dcd9d61ac70c26e3948f`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 69.5 MB (69478544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a0e67a40f4a4a344859e9e53173ec951925487e717e76ea00daf95e194253`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 237.8 MB (237800257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b253bc9bdef13c31292ee7a8d1ec54bab1e1a8cf702d9926c5085bd56950b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16812439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bacb96da9fb111e75e5243ca88675e62f9e834921378964e8794577f772396d`

```dockerfile
```

-	Layers:
	-	`sha256:7d9c8586fef526e5aa1381f2e41622679197c6cdc3884add0afdbc6ae22663cf`  
		Last Modified: Tue, 25 Feb 2025 04:18:01 GMT  
		Size: 16.8 MB (16802285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e62ab7e1e080923bf1038f594b65d68b150c954b79c321cf5a4d432c309c106`  
		Last Modified: Tue, 25 Feb 2025 04:18:01 GMT  
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
$ docker pull buildpack-deps@sha256:6fa8e1a3d617cb3c34ddffdb4aa2936b54176778c8a7bd18e2e25aa9ed4ddd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.8 MB (457840823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130b927270b3d61b68a4faab1cb2fd1c6f6c4aaad45a1fd08c3309e76f0a43cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f390d4530b68a73e13f0b8647d2db7253fa60266e1fb90ae3f587c71a006f52`  
		Last Modified: Tue, 25 Feb 2025 01:32:10 GMT  
		Size: 46.0 MB (46003542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542aac923569c10399fd56cc5e2363a56a89b5180e2dddd54f84754ded5a213`  
		Last Modified: Tue, 25 Feb 2025 02:36:30 GMT  
		Size: 25.5 MB (25547766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770a9d99da8ffce3a0f64384e37db6e3b77d3cebe38de8bd53a185b9f5807f6b`  
		Last Modified: Tue, 25 Feb 2025 03:19:47 GMT  
		Size: 66.5 MB (66548209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d429c7c22de7d239aaf5bc264c266988193b373194b25b4954e878d42d4b56`  
		Last Modified: Tue, 25 Feb 2025 04:40:39 GMT  
		Size: 319.7 MB (319741306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9bc149ecdc53e2e1f3365605f22200d8cdc12523604a42628fc85f00f1044479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16899698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddda1fe5fd2f60e8acdabad9f2ff6a2fcace1bf6c35e8b5d939e283a55d12a7`

```dockerfile
```

-	Layers:
	-	`sha256:efdd58314f05f9be4b3dfff53fb16ba87d15fc6864419668ccc6e06f5db65e51`  
		Last Modified: Tue, 25 Feb 2025 04:39:57 GMT  
		Size: 16.9 MB (16889490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e4f71b5bf5ee511fad4a1980d87eb67d00fd170375fa771f2813cf9d2954b9`  
		Last Modified: Tue, 25 Feb 2025 04:39:54 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:49884309c547165f7fcf016a26b51ab8bfe7d34a986c67e35ac09f42f722d02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348186727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8121c76b75050fc365431cc1a3591e75301090ccf62084f3c9b85537f8b6f62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb029d344ac2942bf1f98be4221b2466495c100c4662a25e8e6338cf9c0f606e`  
		Last Modified: Tue, 25 Feb 2025 01:30:43 GMT  
		Size: 47.5 MB (47498543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a284e667f853bfd37a5b5f735f1448b941efd88d6ca35d51858f3d1bc02320`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 27.4 MB (27368553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ea831fd4fc9eb25ca53ba663df8f3da6dd8286d4c4b7fb35d757ed455e00f`  
		Last Modified: Tue, 25 Feb 2025 07:17:55 GMT  
		Size: 68.5 MB (68496754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453d0cdd242fa8b418b3ceb8b6c88133916368a3d61e858677d6946b943970a`  
		Last Modified: Tue, 25 Feb 2025 09:24:08 GMT  
		Size: 204.8 MB (204822877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49e7ff470fc407ece5cf783ed04917823baaf3fbb88930bb8f885f793a3403c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16628017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaf65b725b79ac6fde72400395735fbb047d74fd12c4d89a478506a25ae187b`

```dockerfile
```

-	Layers:
	-	`sha256:63785f207070057176accd478deac84a6844906a15fbfc9ed7a9b54b697cd5e3`  
		Last Modified: Tue, 25 Feb 2025 09:24:04 GMT  
		Size: 16.6 MB (16617844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee576a74578fe0ddf4dd29bacc954c31fcb29a23cba9c20a31e3e8a45d142ecb`  
		Last Modified: Tue, 25 Feb 2025 09:24:04 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
