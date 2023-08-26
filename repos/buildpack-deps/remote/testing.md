## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:2b2b32a0979f9e778c61e71765f325d65143dd33061844b359c3e8509b18ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:48e1e62eb8eb8044cc53ea454162d6a6e779a54a7655738df3ee0e33c7c2f6d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366777858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757cf9bf2ab015c3bc903fea576bf2f11750326fbcdaa0865559866ee0629179`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:02:32 GMT
ADD file:1170cd4ff0eb634606742ce298b7bef45db4b76df3573e41853850f4bb1fab87 in / 
# Wed, 16 Aug 2023 01:02:32 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 03:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 03:51:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 03:52:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c74a9d7ecb9b51b7ca655015e97fe63c4c4643adaf35c9af51956deead7d037`  
		Last Modified: Wed, 16 Aug 2023 01:08:58 GMT  
		Size: 49.6 MB (49604152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2680ce991d97fcdc7ea794a58be8b5d9d19b0e51227bc662513d81e46b8554`  
		Last Modified: Sat, 26 Aug 2023 03:54:07 GMT  
		Size: 20.3 MB (20253933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d10c899bd7b7762b1c066a8550a6fabead446586a5eed878ad4256aa32101e`  
		Last Modified: Sat, 26 Aug 2023 03:54:24 GMT  
		Size: 64.7 MB (64676288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f13e4edff26f2bdfad30ccbe165054d0395fa89543262917fc1857fee4c49b`  
		Last Modified: Sat, 26 Aug 2023 03:55:00 GMT  
		Size: 232.2 MB (232243485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:45042aff5955087fb42e7926e5083662816560e204c9ff9af10b2ef86b86a776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338618864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63d0113d6c9154f0b72cbd751734f94e9b70d06b00c11d2ae26092f46e40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 01:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dfbc5e6b18e516ad072378c62dcfa42e9981f0925b16c44303b5c7f6424eca`  
		Last Modified: Sat, 26 Aug 2023 02:00:57 GMT  
		Size: 62.3 MB (62298697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76154f4b1c42c402e154efcbbb3b3594eaa5766589d7938250f678a4ccbc7bac`  
		Last Modified: Sat, 26 Aug 2023 02:01:34 GMT  
		Size: 208.7 MB (208674771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b913b10427d3e82d26dd3ea433c2613283b3bbb42ab893ec72cc49c595c75818
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320858320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17804165ece3cb9207424a6d9805a08124bd9b53f8650d3c50786f4084c211a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:19:37 GMT
ADD file:fcc6e87e54bebf4c148573f42bb67ddfe40bbb89b37b0c88d5a5ac8074852e50 in / 
# Wed, 16 Aug 2023 00:19:38 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 03:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 03:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 03:24:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00b7ed9deba9ea7ab64452a4e5dfd73f0f68e2784fb8cd589dc15932edf9a46b`  
		Last Modified: Wed, 16 Aug 2023 00:25:41 GMT  
		Size: 45.2 MB (45176042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ab9b63e935a21ead032541d64b9383f6f790c568ab43af2005788226208270`  
		Last Modified: Sat, 26 Aug 2023 03:25:56 GMT  
		Size: 18.6 MB (18600069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ecd7980980da55ee9bc438363e46299df63de50e1a11bb324c2d4ed527fc0f`  
		Last Modified: Sat, 26 Aug 2023 03:26:14 GMT  
		Size: 59.9 MB (59934994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627466e8d4d61f81e88f6f89395ad01aad5b1bc79ff76036d2dcd8805a41a1a6`  
		Last Modified: Sat, 26 Aug 2023 03:26:47 GMT  
		Size: 197.1 MB (197147215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bba68de9470e314bcffbdd624ebefe4533b899397d8332cadc6749b6f8b5a6af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359810640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c38aae7342dfb0f93091faa3c969e46aae5cac0d3a49f8e46630190515b5eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:42 GMT
ADD file:16621389c05de9ece6b8d40e6c62ca81465940296cc58f7f1c56571fac05b33e in / 
# Tue, 15 Aug 2023 23:41:43 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:58:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5fc9f67522f8eb1fc65844ccc91e1d93595f85d410842d334c85f7e0a15d841`  
		Last Modified: Tue, 15 Aug 2023 23:47:22 GMT  
		Size: 49.5 MB (49521978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c849b78c27f87cf11f7bfc3a6c274880955ddcf718ceae8fe425a331d69fb`  
		Last Modified: Sat, 26 Aug 2023 02:59:50 GMT  
		Size: 20.0 MB (20038140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d90315047ca31a048692ffac9ca9412c3013153dff0ae8d9d7fa6d3dc5fc787`  
		Last Modified: Sat, 26 Aug 2023 03:00:07 GMT  
		Size: 64.6 MB (64638758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee57ed9b60282d375d3ac783ebedbef80f927e70ccbc8fed583b68a1e5d7df9`  
		Last Modified: Sat, 26 Aug 2023 03:00:37 GMT  
		Size: 225.6 MB (225611764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3d0aa40e31daf90f34882c964a7e88bf77f7ba88105a0b77218e52eec3077468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351278231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70893e3a566643fb18e37fe78bc6a178372ea9a8888b1a4621f8398b437ea51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:38:43 GMT
ADD file:4d14207b5cf935fa2b9de70132f41a0eb90a8b5200ed3d27e60b766fc6131e13 in / 
# Tue, 23 May 2023 00:38:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:54:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22e40771358829b6817b47cb2d682b51257385478c18bb1ec96251a68a9c75e4`  
		Last Modified: Tue, 23 May 2023 00:43:23 GMT  
		Size: 50.3 MB (50323189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008bf109a603c637e9a80a5a8fe46353089a5fb8c6333eced350af89d7298576`  
		Last Modified: Tue, 23 May 2023 02:03:46 GMT  
		Size: 25.1 MB (25110482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39204aa4c310e5b428093f5182d87e2f302dabb686c85507aed2372505156242`  
		Last Modified: Tue, 23 May 2023 02:04:08 GMT  
		Size: 66.0 MB (65969876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489790d665a9caa11ab395ed735a1f587a230f693c4468d6ee11b6b885e5259c`  
		Last Modified: Tue, 23 May 2023 02:04:53 GMT  
		Size: 209.9 MB (209874684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5059e71ef0c84126a195ad39d3c58db8326dec7189d1e742b8d004b91ca5071a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347255735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ff0a632ec3ce7f042f8da658ee0deb0a11f4c1dd1066fb70f764d83bbcbff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:15:24 GMT
ADD file:21a0349f8818b8dfb23d9795ca922c9828660ac081ba9db3e4fe08efddeef0dc in / 
# Wed, 16 Aug 2023 00:15:29 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:39:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:45:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b01e2a8b457425ca543dc2e5fd0920c4c1baf753962560010906ca5d157fb3dc`  
		Last Modified: Wed, 16 Aug 2023 00:26:31 GMT  
		Size: 49.4 MB (49449783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b7568185112b7ae667741ad45f90e22219bb33f27fe4b15461aea0fc1766e`  
		Last Modified: Sat, 26 Aug 2023 02:46:44 GMT  
		Size: 19.6 MB (19559201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3389ac306ca24c2ea9675ac7442b509e039a22dfb231109ea46f541dc045bc66`  
		Last Modified: Sat, 26 Aug 2023 02:47:35 GMT  
		Size: 63.6 MB (63589900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f399df345c500b2b335c292621381de1af8e74300782f1ca6a13766e5146f6f`  
		Last Modified: Sat, 26 Aug 2023 02:49:52 GMT  
		Size: 214.7 MB (214656851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8a505e6a396f5f035dcbea2cf46d4bf41c257478b4e9329f0e1fdfe5e17bf53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362786127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5942d86ca7e84bea64a7b2e9c57641bb32edc3da17a4328ef6facefdf6814015`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:16:38 GMT
ADD file:28e774b3554d274fc742feac48f78a3bf6f120cb729e2824007dd94d5c414156 in / 
# Tue, 23 May 2023 01:16:40 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:46:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e109feef3fc6307cd9a880958cef6624de9c2c6f054987e479461a1ae51c7503`  
		Last Modified: Tue, 23 May 2023 01:20:49 GMT  
		Size: 53.3 MB (53312324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab84a55cc084469df8b38ab6a01658bfba2b29b7410a970ba6d9d2864846672`  
		Last Modified: Tue, 23 May 2023 01:59:19 GMT  
		Size: 25.9 MB (25923867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfbe0bc6dc85168e7da83a7be20c9913921338417e0c639a93ff1cdc5664403`  
		Last Modified: Tue, 23 May 2023 01:59:46 GMT  
		Size: 69.6 MB (69566996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab2c83c92e0bca392c1c98be8c27bf6a116f567d39ba305e515f7e3f013e2bc`  
		Last Modified: Tue, 23 May 2023 02:00:44 GMT  
		Size: 214.0 MB (213982940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8a8f70eb549c97383a810947ec358766cce1c1a6198c2886c9c38c1fa6a916e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340067645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c3baf1b430712e0da9ac65beb55ac8610cddad3cb5d9f57ee1594f3e64f186`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:45:32 GMT
ADD file:d99fe1ff201690fcb871123822de04002451af1e06ae75e1a18fd80ef531de86 in / 
# Tue, 15 Aug 2023 23:45:38 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:52:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:53:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73c53ccb564b87caad8f214df94d16496ce4754e4b20ee558b3c8f3ac938e41a`  
		Last Modified: Tue, 15 Aug 2023 23:50:14 GMT  
		Size: 48.5 MB (48539809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a53bb03e6b4b7d81815de0b07a64fcbe6daba956f76e89e89d7b363f2792c8`  
		Last Modified: Sat, 26 Aug 2023 02:55:22 GMT  
		Size: 19.9 MB (19924635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e76065e4595f9d0768d5101fdd6a014761c6b1ebb18d266a2d788cc3e717e`  
		Last Modified: Sat, 26 Aug 2023 02:55:36 GMT  
		Size: 63.9 MB (63914401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa4c05f57d5430bef4b7dfce9f82a955350acb992b1207d40585842d2ec12d`  
		Last Modified: Sat, 26 Aug 2023 02:56:05 GMT  
		Size: 207.7 MB (207688800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
