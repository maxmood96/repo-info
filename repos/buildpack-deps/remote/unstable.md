## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:12a3126d9556da17e7bc2461a487a75e8a24ec3d2e76824af4151f77a8cba0c2
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
$ docker pull buildpack-deps@sha256:80882520b36b209536046f3f88f96d3c608333a002de5cbbe1972befbae06543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343168565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a286c9960c46898daa20ee31ff72632668bc39c4d9721a08a1bf1588aff6e710`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:14:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f19ac06db907fa72eecf21fa150fd26d99a092e409ed5349cff34755befbc8f`  
		Last Modified: Tue, 04 Nov 2025 00:28:38 GMT  
		Size: 27.2 MB (27195269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ec5cb615961fc44dd0a7c713d96d2a3966c5c0893d5d0298b8055415ec4409`  
		Last Modified: Tue, 04 Nov 2025 04:14:55 GMT  
		Size: 68.5 MB (68451097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907ee23dba4a7a5d75a14a8a6c29c878d8242ab766174bca91e1309e4ee76b0`  
		Last Modified: Tue, 04 Nov 2025 14:30:44 GMT  
		Size: 199.0 MB (199036559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e59ceb5778d005df99246ce464d1ef35df2d4eed83b55fc56b7f6b99d5c315ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16265316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9218b6ab9bce8bf7355069ba1308e04b8527c05215db5c8d09f049ba85b37972`

```dockerfile
```

-	Layers:
	-	`sha256:d420574cd1bcadec301ae7ef80a29121b5602e351f045dc1c1b3385d17bbd278`  
		Last Modified: Tue, 04 Nov 2025 11:22:49 GMT  
		Size: 16.3 MB (16255183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57688ae21eca80046ffaebcb0c506daab67666b7555b6c37c5b583cfb1169f39`  
		Last Modified: Tue, 04 Nov 2025 11:22:50 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c0dd9aa770a0f15fc5f4285d4c9b3e4d6c9fd3f2f1003dd6499cbc823d3c4279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291493609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb455e4bce3c14f4b59e7d2ca3285529fde8fb524f46218e0460ff214370d520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 02:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:21:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cf40c8870d4fc31c85e1981d6e2ac2787a589f1e553cccffe9aca41df353fd5`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 45.0 MB (44990635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb447e96331843e57f9f8c2921b90731b9e4529a8a58e3def300ae395aa899`  
		Last Modified: Tue, 04 Nov 2025 02:19:17 GMT  
		Size: 24.9 MB (24929773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a2af30582e54ebd41ab69f1a6aa5dd01e372deffa02d94d9a43958a0d3d77`  
		Last Modified: Tue, 04 Nov 2025 03:21:54 GMT  
		Size: 63.4 MB (63360418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bf9c635af3265a50f4b01704a4e39f3af45fd6a665315a801ea453925f19a`  
		Last Modified: Tue, 04 Nov 2025 14:30:38 GMT  
		Size: 158.2 MB (158212783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23ca5df5391b0e5c73fb6b08ef4ed9bcf0331da4309e5541361d20efa277dc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16022327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f05f5c0dcbb3d052e4997034c099293addc4fabbf830d344d9ca9f41f47fca`

```dockerfile
```

-	Layers:
	-	`sha256:37eeb8de390f4e1c834ae4cf4cd706704ef7baa1a9802faa4972be2c181ce953`  
		Last Modified: Tue, 04 Nov 2025 11:23:59 GMT  
		Size: 16.0 MB (16012131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18f3f01a64b7d49713648dd17f34b7df19215755b1a82f0f0db316fbfe516fe`  
		Last Modified: Tue, 04 Nov 2025 11:24:00 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f5cc923e324587f30d37a74e9164074774f26fd36144122878c0ed5365283379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332362715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deecf73d4c551ebb41eea82fb42b344eef20984cb19330c9806596ad55591eb8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee2464e4f33b113343bb1ab557ca8f41d3b10032adfee93dfe6afa6fc0c4b0`  
		Last Modified: Tue, 04 Nov 2025 01:30:07 GMT  
		Size: 26.5 MB (26462272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaec26cc42fbd50193073025d81257d88d937883055aad460dae174f544107e`  
		Last Modified: Tue, 04 Nov 2025 02:21:08 GMT  
		Size: 68.1 MB (68112770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab38f637a03b54502352976fec6cd773ed316db9cccb36cd0b5e4ed670558b`  
		Last Modified: Tue, 04 Nov 2025 13:52:51 GMT  
		Size: 189.2 MB (189201655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:438d43875b8c5da664b01e99514e7cf3a37e7d77800cf0c6145ff08b2ab85202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e029ad1c03ecf08ee2f4b1fb58efa2b2d9caa27d4ca2a826ac4588eb495babf4`

```dockerfile
```

-	Layers:
	-	`sha256:9c66cbd09fd6a41aee2957211766c4d4524794f967103ad25d3187b6485d5502`  
		Last Modified: Tue, 04 Nov 2025 11:24:13 GMT  
		Size: 16.3 MB (16329732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad243c1c86d9fe4689ae7da9e29fdd9e6e66c1a71479d42dd774b56a065cfa77`  
		Last Modified: Tue, 04 Nov 2025 11:24:14 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:30338d67480456afae4ffbfb8128c5d1b73fc7796e916d5af18ba276ad7000c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351105760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1738ad218550576aa47911bedce7173d62284048fd182b121fcb536deb1a7966`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:31:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e227b380623fcba2d9150034228fcc8257fa11236e7ccca0e2f9cad3a24c603a`  
		Last Modified: Tue, 04 Nov 2025 01:32:02 GMT  
		Size: 28.4 MB (28436262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02a601986dfbe157c15ec69c5f585f418cc3b60d6c2afde0f0222a7f25d5930`  
		Last Modified: Tue, 04 Nov 2025 02:20:39 GMT  
		Size: 70.4 MB (70357090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abd1257eda02fe96b5b7333fb0318918b52d072e868052badf432bd609c8833`  
		Last Modified: Tue, 04 Nov 2025 14:30:35 GMT  
		Size: 202.5 MB (202503401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9fc478b5ab1543cdf4900a593bccf9087050b91f0b7428aa3b850860c3160ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16235073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf8332498ab881f4bcf3ae29d6200e95fd64d15b15359b765814dfd4f2025a0`

```dockerfile
```

-	Layers:
	-	`sha256:8d1905da73f962530f7c3158381b951def97c44ed2cc0bd31004a11551213237`  
		Last Modified: Tue, 04 Nov 2025 11:24:26 GMT  
		Size: 16.2 MB (16224962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cf396e7ae3ca134035fed99af022c075b5328f613b6e830933839e552ed84a`  
		Last Modified: Tue, 04 Nov 2025 11:24:27 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4ce0380ab5f82a6bcde6506976825a8f87a888bb404f5df1d0bc91f392d2f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.1 MB (695062585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8ae6a340b710367227e9d97eccda2342df427006146c928be74ee879445af2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:573dcf794048f7c1a04d7e5caace5a2fd1f7290004272bc4f3dfd960a096f8a9`  
		Last Modified: Tue, 21 Oct 2025 00:23:18 GMT  
		Size: 53.2 MB (53217563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d66ae6d7a7d4ee86e6e6ff963fcaf8df404ad10cfa1d1fd6e312e128f220b4`  
		Last Modified: Tue, 21 Oct 2025 07:45:26 GMT  
		Size: 28.7 MB (28740070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce499c900f022c6bd64723f2ec0116e5a84c4bbd95c63b9450125c67c0d19d`  
		Last Modified: Tue, 21 Oct 2025 17:34:21 GMT  
		Size: 73.8 MB (73816162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915d8deb9f6a59a9c424d0aefaa481574d74b7770297b9849b8f777d2f14a11`  
		Last Modified: Wed, 22 Oct 2025 05:30:00 GMT  
		Size: 539.3 MB (539288790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bda4686170737f9067b2b2ac15871f5afe97b5c6c4838bb76b5289add96667b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16234144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae69a2334bb505b2f59478550fa6ddfffc8eddb85a9fb80e703723bd152c4df`

```dockerfile
```

-	Layers:
	-	`sha256:96041df0dedd459eb2d1b745e792e8df1e46a7cb81039848f0d695a5f672dd50`  
		Last Modified: Wed, 22 Oct 2025 01:21:49 GMT  
		Size: 16.2 MB (16223936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463d4ec8228ccf677704926e8eb4922daf874dc8e01751691f186632c742b848`  
		Last Modified: Wed, 22 Oct 2025 01:21:50 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f3e6e7ed0547b93c323d1fd46c9416b597b57a5ec82811786a829b942781a1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076967476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3484203cc637ba6864d80602c5869c8dcad7aa0d9fe3004c2dff500f214a54`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2be9bed11e9fd66165d84261d66ea19eb2c82eac8e67869aa7908bd19fd9be21`  
		Last Modified: Tue, 21 Oct 2025 00:25:21 GMT  
		Size: 46.7 MB (46705170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36f6ee73a964ada5e4d7f0d2e62741259e488dac65675b450483b9da2f329e7`  
		Last Modified: Thu, 23 Oct 2025 03:09:49 GMT  
		Size: 26.4 MB (26407261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc35f74b34686aad819559de052ea77a9f2e0919e8f484dd33fc417af8df1ca`  
		Last Modified: Fri, 24 Oct 2025 21:26:55 GMT  
		Size: 67.2 MB (67214490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b970122751e6c33ac9c3075cebf6e42cf2a355842fcd4dbaec860e67f7710b`  
		Last Modified: Sun, 26 Oct 2025 14:22:43 GMT  
		Size: 936.6 MB (936640555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c975370dda1fcefc6d0676342a3a68fe5ad6e81eea80fd18e94db177690d4607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16305977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc462cddfab90e2c1097405475a9b94aa4778b4e597e9b8998c70ee0816335c1`

```dockerfile
```

-	Layers:
	-	`sha256:cfc33141eab91aedb88110e3619fd3a186db601fb5381b97fe176f2db3eaa3da`  
		Last Modified: Sun, 26 Oct 2025 13:21:40 GMT  
		Size: 16.3 MB (16295769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a628f5000436c0b6ff091d0e7ff34fdaea99e0a589c97fb1ab5887f96e53eeb`  
		Last Modified: Sun, 26 Oct 2025 13:21:41 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dc44beecb5d3948f9e1f1201bf176701993a925357b9d226fa66213fff814848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311385121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97454f7580357edda1d6a16f6c7b34473d81a23a5d60553d4292d2f3fbbb1323`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 10:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:28:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ee07654f71bb163a06c3532a844efe8d75683f4dd53a88a8109fd9ed1b66fc1f`  
		Last Modified: Tue, 04 Nov 2025 00:16:26 GMT  
		Size: 48.3 MB (48346444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e24f5b3ee730a867fae54f44e0b43c0311d9bd66c565a7c2a2b0d7a887c220`  
		Last Modified: Tue, 04 Nov 2025 10:03:07 GMT  
		Size: 28.3 MB (28324175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137dedc8726298d18bf0cbb080b8d89391fa9483e0163fecf362cfc0f0c4e9a8`  
		Last Modified: Tue, 04 Nov 2025 14:52:14 GMT  
		Size: 69.2 MB (69187515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f5346c1e59fbc781c938ac583a768412fb4b756c403402f2554b1cb24d153`  
		Last Modified: Tue, 04 Nov 2025 17:29:08 GMT  
		Size: 165.5 MB (165526987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cbbae2a74b33a279d5696b55388d0fff4052e6fa98a546e2642dfecff09a4075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16031980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedeaccfc067afed430681d2d02a2091fcdccf05047bf5e617b8adb3609d62c7`

```dockerfile
```

-	Layers:
	-	`sha256:628f765237fdba55c86092221e6d8eb6a4300e9875a213abe1da95de43fda825`  
		Last Modified: Tue, 04 Nov 2025 20:22:00 GMT  
		Size: 16.0 MB (16021847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677b41396d500c6b5bd20019db7eaa8d26800797095caebfdf6fc81eaa8c4e45`  
		Last Modified: Tue, 04 Nov 2025 20:22:01 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
