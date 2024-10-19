## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:f9736689b5f3de513f841e1679ba4a4ac70d697d54a2d6ea41b26df57afc0404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0357130b032ae0c854db1dc21229137704ae206a83f05daf23ffc95712eecf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367984491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a39104e33d7cad4c9c9d85b3127205c321bf8353351b6730a4181a98e58027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62683c6ad6022c8249b2258dcace69634541663e2eceb81fb4c1c2e36d49de26`  
		Last Modified: Sat, 19 Oct 2024 02:53:50 GMT  
		Size: 227.9 MB (227866497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49b2368a3f95d6e910307e3c9f69f87deb7c2d3354b778e2874705c3bb4d5ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16507570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0df43ec87be3e27a39b4d13c738ef559f245755c425d593b205930559792820`

```dockerfile
```

-	Layers:
	-	`sha256:92f3ef1413b81322d8f5ea466d1cc9afec312eb414214d83c7c9cba360fa6bf1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 16.5 MB (16497377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee48f91490aa5f9944f1624c3f85bbc3f0562946751903e3d5c114b1e114b1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dfb638ac11b12fef8510bcd4e28a26e5f4098a2d1414b6b5718ceca4300ca23a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336055761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164af35a4a2654f15149ebbe020f83269d27a6e0fccba1b295239d7a0590c776`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:33:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881241cc914c17be2c506105e054bfcf46ca5dc3a2c61b399fb49563a725f97c`  
		Last Modified: Thu, 17 Oct 2024 01:37:57 GMT  
		Size: 19.6 MB (19644443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cc8728e864cc21d996b1238d79456f457c2d6f8c5d26d74916564e44abbe5b`  
		Last Modified: Thu, 17 Oct 2024 01:38:20 GMT  
		Size: 63.7 MB (63741533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08102b561e7767bc425138ba99beed9786e26ab88c0b070d2835c1c29a5044`  
		Last Modified: Thu, 17 Oct 2024 01:39:04 GMT  
		Size: 202.5 MB (202523688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:54125fe0eca21864407bcc5465626b7b25012068ec1cd2387efb6bc127ebad95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317481868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c0a305057a0e790d5004feb9ec9b00b36af5f837395a3d959ca76d7ce6614`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:25 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Thu, 17 Oct 2024 03:05:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:36:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b14885f9520938c577e16ecdfccbd10cf46510a9c0149d0d479ccd879d93d6`  
		Last Modified: Thu, 17 Oct 2024 03:40:06 GMT  
		Size: 19.0 MB (18974054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebaaebd3fa818b1b4bafe8e7f26090da3811fd6c155b2f7f73dc8875a3a905`  
		Last Modified: Thu, 17 Oct 2024 03:40:26 GMT  
		Size: 61.2 MB (61233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884e2f9eb216cf208e6169a9d6d8edb9392a7ce4982869962011c53fb6f91d88`  
		Last Modified: Thu, 17 Oct 2024 03:40:58 GMT  
		Size: 189.6 MB (189614810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4a38f49d0091a4e29280f14a38096f5f1099c0cf22ede3cd23325ba805631f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361333988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f530ebd9306ef5feceda1fb5383ad5d2ac5f7a5a1461680639651f171a94057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:19 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Thu, 17 Oct 2024 01:13:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:34:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:35:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc979a58041d0ca8e5deac6b7852b9a756f65c5fde4ed5a01b9ab02ba82ff2a8`  
		Last Modified: Thu, 17 Oct 2024 04:38:39 GMT  
		Size: 20.4 MB (20385295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f53239df6d74ac78e3ea17ce45a2e39dfce24b675fc31f8f4d6cf9bb4b4e1`  
		Last Modified: Thu, 17 Oct 2024 04:38:53 GMT  
		Size: 66.3 MB (66305737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7481d379b4107b6f999b57394ad368f476ac3b244f21a8fd4fcdbb47e6854b5`  
		Last Modified: Thu, 17 Oct 2024 04:39:21 GMT  
		Size: 221.0 MB (221043231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee56890ed8d6f91cba4394aa3f5083c5123400202ab7d096522a85a831f612f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372586202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcecdf46d089364cbde632cfb8e3b506ec37ff689e40ba870fd8b365626314c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9067ce74b0ad44714f9fcdde6e1e80ccc5ea632bd70cc38760f160485b65493`  
		Last Modified: Sat, 19 Oct 2024 02:53:44 GMT  
		Size: 228.7 MB (228713750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2795e01efc42f3f6e6dec027b25de27f203b53cb39ba0bf807d31e1d8fda2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16477955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8734bfa35aa50645b7863013835b368e0353dcea699cb346e1e1c5a7d046a558`

```dockerfile
```

-	Layers:
	-	`sha256:f840f39bb756f2de1a67ce2157b37a9f49eb73423510632741ce767af0764190`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 16.5 MB (16467785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de718ffef3484dc52d3236b9e93a9bbcfb9884f51c7d9cde604bc6d4b99c1d2`  
		Last Modified: Sat, 19 Oct 2024 02:53:38 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:25eab8db5e0fac52c8246295fd5f054b693548c5b4c48cf3140a9f06be463754
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345215162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d84b1e19fc528971a6245468bd3defca3f2af877b4d5c6a6f34dd718ad316`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:07:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3136c2a952f0ce80aeca2b6928afe3f03863f57c7fa1a03ebd2f7c0be5923c8`  
		Last Modified: Thu, 17 Oct 2024 02:15:26 GMT  
		Size: 21.0 MB (20965665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8f48a50ba530f6de6ffd4fea12c7a1881ea25592c7713fae880299f80511d7`  
		Last Modified: Thu, 17 Oct 2024 02:16:17 GMT  
		Size: 65.1 MB (65075286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918b279067b0d9d3b75423dc4f7c0ec8f715830135aff70d1d449bac131e76a`  
		Last Modified: Thu, 17 Oct 2024 02:18:32 GMT  
		Size: 207.0 MB (207045743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c1c38533b14a5bfa7c72de8bc53e0f27ba26f26081f394f36c3df35723273da
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13637603f1051994f2585a17e7ff16d6ba6ddb533434905b593d7b7e5c41fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2644f355ce42082bdc3b0fffe0d7e95a4d8ecfcb7944e76a2d5fdfa12edfaef9`  
		Last Modified: Thu, 17 Oct 2024 01:54:41 GMT  
		Size: 226.2 MB (226153671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff2315a159e26c773bde3e416a35ce0ed9d4879c4a50de17da0589c3b92a54e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342774272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a95637bec4073de581503c4ecea9334cfc150932106b7843177ddf1f4e0649`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:48:13 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Thu, 17 Oct 2024 01:48:15 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:46:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e49835389a5b3be307cfcaee824ac271d1c990968ebef582d739387fe8cd1a5`  
		Last Modified: Thu, 17 Oct 2024 03:50:19 GMT  
		Size: 21.7 MB (21658714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0166b7d6671ccc810cbc6335bc33f3a6c82e87668bb0dee7a3abc097ff3d1`  
		Last Modified: Thu, 17 Oct 2024 03:50:34 GMT  
		Size: 67.3 MB (67337716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b8b77d7a85513a728feea2661f7073ec071f3c4b10f104596ac74c52221ccb`  
		Last Modified: Thu, 17 Oct 2024 03:51:06 GMT  
		Size: 201.0 MB (200968998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
