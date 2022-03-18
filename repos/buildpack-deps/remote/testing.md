## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:63088cd81a081edc7cc2c6cc709262a1f8f762498e229a78ac9088bca3d5dbe5
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
$ docker pull buildpack-deps@sha256:8299681ff15fa4ebe729982a46f59a1680b5783ce1444cba976a3b05c8887250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337201132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f08df86bdce171fd263305a040e06de9a3362dca9a07dcb47a0932fb8f134c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:27:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:28:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:29:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeea17ea14a09712ca5b490a0c64f57af435ba10cdb9a1a7c56af17b85ac9361`  
		Last Modified: Fri, 18 Mar 2022 07:01:56 GMT  
		Size: 5.3 MB (5270513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b20718d5e8e4adb64ab4e1a41c30a4e311400c1e600e19792c50c1522420f`  
		Last Modified: Fri, 18 Mar 2022 07:01:57 GMT  
		Size: 11.2 MB (11186321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fce5439f6b2566f7bd6851706b38c1201c994ac1ec57ad8725cb0f08c28be9c`  
		Last Modified: Fri, 18 Mar 2022 07:02:17 GMT  
		Size: 57.2 MB (57186893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e2de6ca3450a7adef19d720dd7804f6a14451e0152d836741a4a7f7e72d80`  
		Last Modified: Fri, 18 Mar 2022 07:03:02 GMT  
		Size: 207.8 MB (207803108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:587a926780262f63f39fb96fabb1f24f2ea183a7fac5ad6fbae280f0b4134974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304946619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e1c9d28b076bfc39a562f7782dc53c252987243e9d7da0f3d8dd5dc43ef1f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:18:12 GMT
ADD file:990567084063731033d76e2ad1efcd558f47300ad1e9848197a4365f45d534b5 in / 
# Thu, 17 Mar 2022 05:18:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:12:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:15:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5c18c3be596e08b764befc1ff336d017f3a31c10bf139ca155094240de76a8c`  
		Last Modified: Thu, 17 Mar 2022 05:32:53 GMT  
		Size: 53.1 MB (53139012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0040329b3b511cc0d15a0ae2eb2bbcd344c2c8291532ddd0f333b1e142b464`  
		Last Modified: Thu, 17 Mar 2022 19:37:02 GMT  
		Size: 5.2 MB (5169031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800c571bbaa0a9c8eae64db9691f97d467f0bd06250b5da62e182b97753f497`  
		Last Modified: Thu, 17 Mar 2022 19:37:04 GMT  
		Size: 10.6 MB (10579460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11a7f3fcd6560f12b114a08e246f8b4f4e6893de096371b829d51f149731af`  
		Last Modified: Thu, 17 Mar 2022 19:37:53 GMT  
		Size: 54.8 MB (54813938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b97aefbe42ce0733ac3fc39364d8bc7d0eb5c2e03b80860cf73f2f70ff4e18`  
		Last Modified: Thu, 17 Mar 2022 19:39:54 GMT  
		Size: 181.2 MB (181245178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acbae2409d8ee8c88d0ef960365f776aee8a450548fa9b0506605f212a4aeaba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290124154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179997a54dca706a98fa38181b757a38c71db6c7f7aaad3ab4079fce4e889381`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:09 GMT
ADD file:b4dba23a3881b51ce93a5fac275db003c57e88fc4534625e4c57917ee7d15dad in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:25:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bac975da179fd2ec964b1f0a2374ae27456aefbe28014e1301872aaa7a545619`  
		Last Modified: Tue, 01 Mar 2022 02:17:11 GMT  
		Size: 50.8 MB (50787576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c6337247740872b2c547fe2c235240cb511f34f377358193108cc09d66ea1`  
		Last Modified: Tue, 01 Mar 2022 09:48:05 GMT  
		Size: 5.0 MB (5035170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1747c607a3fe8511a51023b984fd817a06b714e0a09c5028257ed90eebc47b0f`  
		Last Modified: Tue, 01 Mar 2022 09:48:06 GMT  
		Size: 10.2 MB (10241471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d3fa20637f40c1c0d555bbe24b09ee9dfe45ffa828cf0a24e2e432278157`  
		Last Modified: Tue, 01 Mar 2022 09:48:54 GMT  
		Size: 52.5 MB (52465949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b00a72b43e8f3657d5e5c9aaffd0cbaea84db01532fa5c55196727a6e494c`  
		Last Modified: Tue, 01 Mar 2022 09:50:41 GMT  
		Size: 171.6 MB (171593988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dc10872e9df18781834b0c42b03fe79668b23406008810d1e90621c64908d34c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326706748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a83c9cea35cc589e8ead2e17e227e9f428a2cb832afc7d20ce0fa18a6fd4c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:18 GMT
ADD file:c8087b65b6b61e4854699fe41f5bd7f307c0e0710204b586e85fd8176523d9bb in / 
# Thu, 17 Mar 2022 03:21:19 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:08:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:08:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:09:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:10:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:906df7cbb9fee5eb5d79c51ae55b6a857335ddd1b44645e3a59b3a50862f4317`  
		Last Modified: Thu, 17 Mar 2022 03:27:23 GMT  
		Size: 54.7 MB (54668239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bee854a2c1d4d436485263d8648a3eb5c0a4cdc26326102c680903b409889d`  
		Last Modified: Thu, 17 Mar 2022 22:19:48 GMT  
		Size: 5.3 MB (5256412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f88519bd8fe148fde1d5a9917fbea41afdd523e19fcecf2dc8f2f39c86cfbe`  
		Last Modified: Thu, 17 Mar 2022 22:19:49 GMT  
		Size: 10.7 MB (10676785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679d36783a2b174a0e8ee03bc292d3fdd5d57461299a881aa3561e5313ff763f`  
		Last Modified: Thu, 17 Mar 2022 22:20:09 GMT  
		Size: 57.2 MB (57222374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb92c1d1edb0bb67024b345c9e4455169845b0e4807004f036901c1a23c815`  
		Last Modified: Thu, 17 Mar 2022 22:20:45 GMT  
		Size: 198.9 MB (198882938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a148537ee74a0833c7a74556b6aa468858213de93497f17740debc1b8c86dab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335605243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83222059d3e7d2dc975d0b07c14bc99d3b0e1acad226e01ff2cd04b8756071d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:44 GMT
ADD file:2e2ec9677737b8bd29e3af438e4f72a00e4024d7771df47c835bc532f3955901 in / 
# Tue, 01 Mar 2022 02:06:44 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86f9569b4496bcb71f9a06eca983db008f228f89df9115b51deb7ba67bce86ba`  
		Last Modified: Tue, 01 Mar 2022 02:14:26 GMT  
		Size: 56.8 MB (56800248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc642b9c58ccfd6d24ba39de754790979cb5f4259049a1024063ce9ecd8048b3`  
		Last Modified: Tue, 01 Mar 2022 05:50:18 GMT  
		Size: 5.4 MB (5407350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03eabfe59d42c8a3ee934b6d80db7f1185e56951d5ec5a9561133731b6ff2d`  
		Last Modified: Tue, 01 Mar 2022 05:50:19 GMT  
		Size: 11.3 MB (11307416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf25e617660ac5db1f4151bbb260abc3f5330b37a67e7d43f48b6f5966bbb024`  
		Last Modified: Tue, 01 Mar 2022 05:50:45 GMT  
		Size: 58.4 MB (58393620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76570adf4796e6a45c9f30952a2243bd7ff6a21a66e4b0950f9434ad5b02150f`  
		Last Modified: Tue, 01 Mar 2022 05:51:41 GMT  
		Size: 203.7 MB (203696609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8f6292f02f373d2e88ef12a347efe3d21c19c870943c1dfe0b55173575547359
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313254729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b81c9962055c6e73881cafa36e718199604ef95298870c821f8a0b621eaf3b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:51:08 GMT
ADD file:550d1d8a058f07f217e9d0ec1e582f897b1cd24ad6c6c3697d5c89039c5ae265 in / 
# Thu, 17 Mar 2022 08:51:13 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:11:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:12:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:19:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4e5d74924161483e853a5bf08fcf297bf47b3124d7d1840e280c5f487a8750d`  
		Last Modified: Thu, 17 Mar 2022 10:41:21 GMT  
		Size: 54.3 MB (54339160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c2306400a47802f9098940358dd510c9d432998ff5d8b9ef4eb54da37c1b1`  
		Last Modified: Thu, 17 Mar 2022 19:47:35 GMT  
		Size: 5.2 MB (5225142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a35eaaf609861da62a9d25299ce8269925d4e205b08c5c62d7e99d19b7d6f`  
		Last Modified: Thu, 17 Mar 2022 19:47:38 GMT  
		Size: 10.7 MB (10654797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8024f4d3131917cacabab09dbe180853b42f8410b118be783211c6db8a987f9a`  
		Last Modified: Thu, 17 Mar 2022 19:48:25 GMT  
		Size: 55.9 MB (55928622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d422cf350e8c5ea52e6968d839aee919764de57d6f73ef0bd51d8e633c13a7b4`  
		Last Modified: Thu, 17 Mar 2022 19:50:31 GMT  
		Size: 187.1 MB (187107008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a5b8c298ba9fc35f9ffdbabf625761780304d6737bb7749489de6050f84b714a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342348288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3ca3a84d07b37a19d27cd4ce709aec3e0910f507b867a820b225f1552f8233`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:22 GMT
ADD file:08a06b615cc3142b45e95ffc03be0940c1aed49581fdb5c3a45d69c9ba65fcdf in / 
# Tue, 01 Mar 2022 02:03:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:55:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:05:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e0578def7e304114d931a4e4be85f40364b30cf0228e8360d7ec9d82b30f2519`  
		Last Modified: Tue, 01 Mar 2022 02:13:53 GMT  
		Size: 60.2 MB (60166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb379d336c1a24b02d5693d3a19fe1017d67c67f734a56c109c876bcf8547f99`  
		Last Modified: Tue, 01 Mar 2022 07:40:40 GMT  
		Size: 5.5 MB (5543531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a933c5a043de953ab3d5444edf590034fecf2a41084159c2ff91dcb57e349a89`  
		Last Modified: Tue, 01 Mar 2022 07:40:41 GMT  
		Size: 11.7 MB (11693203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0f79d5cc50dad2e31cae3c2ec67b9cfde06f4ead1e7e8f99141438474a7ff1`  
		Last Modified: Tue, 01 Mar 2022 07:41:06 GMT  
		Size: 61.7 MB (61676232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fc6ac6727fc8844e30486d606a1aab7f1a7cb8b264218aa5521ff271c2db5`  
		Last Modified: Tue, 01 Mar 2022 07:41:51 GMT  
		Size: 203.3 MB (203268957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee52198958ed6b43a532c277c17fe850360a88e61b71d69a48eeb2059133ca25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306360438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c4c96fd2d6a2a4c551ea765ad85ceced07b67b7b77234aa6c73b02d09d0a33`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:02 GMT
ADD file:82d5e48a017e9f867dce69500059071538b25dc5395a355bb79bfed992fb8cab in / 
# Thu, 17 Mar 2022 03:06:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:19:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:20:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc6fa8b00e7facc9855a15de9dbb6211a8692978d893a028e487ca7988379b`  
		Last Modified: Thu, 17 Mar 2022 03:11:59 GMT  
		Size: 54.0 MB (54000921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2c6272c85978c4b20b105a7a33a11881628bc38840c72128a526cdc6b709ab`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 5.3 MB (5250449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900da87743fe44ae1fee0a700fae42c07e9ade18d95f98fbace40ab318fb4846`  
		Last Modified: Thu, 17 Mar 2022 18:28:20 GMT  
		Size: 10.8 MB (10803619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f1b87cddc9e80df0130457e34d2b02b2e3a3700aab72bc40ee7ce09612250`  
		Last Modified: Thu, 17 Mar 2022 18:28:33 GMT  
		Size: 56.6 MB (56560505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d85dff32c741be680f86736f73847c567fc4f53dc0eb1cb045e3938bf1ed87`  
		Last Modified: Thu, 17 Mar 2022 18:28:59 GMT  
		Size: 179.7 MB (179744944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
