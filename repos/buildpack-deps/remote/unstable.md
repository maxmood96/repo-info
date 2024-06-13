## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:8224ad404883c97eec11c4487defc24f4a135f8ba2db20d2183d45517b3b21a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:510629bf7ce9533a231f49951f789b23afdf54922c1505c96da14394e0222d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 MB (390247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f61a281502e7231809486544e2dfc46a5b2be4dd982295d8a5670aa527f4445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac544ac355064026ba785eadccce3f97f0eaf50205a8f46a879294788785684b`  
		Last Modified: Tue, 14 May 2024 03:08:10 GMT  
		Size: 246.6 MB (246637499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:23742a24d183ff420647512e78ce459cb89eb479cea30d180cdec0175fc077b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345912159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c42b3df689e76f103c1d1bb86546c10817577f7bb4471423d09c057e1f925b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:21:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae581ede8f2c1d7302c93ac10d87cd470c5a5641bdbc563bc1606c09aa60177`  
		Last Modified: Thu, 13 Jun 2024 01:27:28 GMT  
		Size: 214.0 MB (214025639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:477914b6fbdfc2a5308d84f4d0557e828580fc5fb583a97d294638388eaba72d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326696137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794beec7cc73358bed5b7ff44b555cf6e4c8f21b8bc10dcce4f2f234d5cc7644`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:30:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e48a8a26ae4b39d549817d9f6485a412bea366150e0b4cf93a1dc2ff4c20c`  
		Last Modified: Thu, 13 Jun 2024 01:37:23 GMT  
		Size: 200.5 MB (200549606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daa240adc3a26e2cfccc8f82dd71f77925f6e95bc18d608dd874c8899a15943f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369902961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9399dafa2937341b2f8e58f15cff1becc501382148d41cfe86b2f9edcbdb6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2611f13f4ded7c5c4db9cec62d32aa647f19b894c8d49a71181242d891cdaa`  
		Last Modified: Thu, 13 Jun 2024 01:33:37 GMT  
		Size: 231.5 MB (231457189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:333e240091ae3ba55acd6c3de0b1975631a7acd0458fb0a447556bc4617a26b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382952788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aeac83bac56baf8646254d28495861d39e591245e6bcc85a9fc2cf80e0079`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a44d02da26a64e916b188437fc3eb829bf06dc211923352addff42906c24621`  
		Last Modified: Thu, 13 Jun 2024 01:23:52 GMT  
		Size: 241.0 MB (241023248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84e1d4e2b5b3643c67a7dec4bb189b32e2cff2f9c9500de31a98e0bf3c42f3df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867490fd8a8761f0b11b7e2ead79189e24a94657b0d08b60eecee6681c4a1d8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:27:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0b2c691a41774071c0d9dd21f2ac31d580543d1b70cd9eb6e4ca27aae33b3`  
		Last Modified: Tue, 14 May 2024 11:46:47 GMT  
		Size: 217.7 MB (217669143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44994ebe239276f8c148f94904212fe0e082dd7a6a06509a0b841baba3204e9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404129957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c27e94800d6d03b5ef7856567848c95031b762ed4d0284cf0eff3b0c9d93ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:05:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666e37da3df3c94824cb116466c272922f2a7c733cad8460357b2504dc816849`  
		Last Modified: Tue, 14 May 2024 07:13:53 GMT  
		Size: 248.9 MB (248903741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a8a6cba424fbb8acb65e7459c95265712378982cd5dfbbc849ab2fc0d182f18f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.2 MB (425163913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c9e1fbf05033a4f4607b05de62de26b589467a64610c4aa368e44ed99ad6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:38:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe41b9eb8f07e9c6e67c4cf4ae6b4fe894f733f429286173f646100119905c`  
		Last Modified: Tue, 14 May 2024 01:45:57 GMT  
		Size: 284.5 MB (284524499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bc0f1580f7da7dd52f12f0fb6a45bc148ad7a5b1f37094d065634e86715364d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371563717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14b04d8b3d5f404a739ef30d225977273df38f670b35a7cdb00df85d22db2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c512ee7e60445e2908d19d2738b076dfc41b764ba56a3e9509b8e8a8319a68`  
		Last Modified: Tue, 14 May 2024 01:31:53 GMT  
		Size: 226.3 MB (226268942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
