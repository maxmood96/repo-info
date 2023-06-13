## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:7f3c28087275931fd8a693e62f5bde35fc72abe26d24af6cc4756b71ff907942
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
$ docker pull buildpack-deps@sha256:528b5311a9ae6696bcd00391123c4bc54f3b31b58c58e64d74bc86267eb03278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351457721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9832bf13f8edec5c1794ddc2768c54640f872d1d3ba82cf610164cf5a2e673`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:22:34 GMT
ADD file:8ed2c72091b90575b320038c2ad715760d6382aeea5c416dd16f7ed04e955217 in / 
# Mon, 12 Jun 2023 23:22:35 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:34:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:34:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:35:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e79cba44192968ca6ea42058e67723ae58bebd2ea54b31f432b1ffed9fea9d9`  
		Last Modified: Mon, 12 Jun 2023 23:28:29 GMT  
		Size: 49.6 MB (49551965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cda7b25305de24c8cc4e88d990c3c3c70e109b190f7411b9d3237528081a161`  
		Last Modified: Tue, 13 Jun 2023 03:39:26 GMT  
		Size: 24.0 MB (24019326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c71d2bfd3c86199eb06493b2f6d0258d7576aca3f851198b940bb3b1505989`  
		Last Modified: Tue, 13 Jun 2023 03:39:43 GMT  
		Size: 64.5 MB (64535333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75a9b221ba575bef197107054a01083b3dc2b0d4bedc07f7e6c3fcbde4df462`  
		Last Modified: Tue, 13 Jun 2023 03:40:16 GMT  
		Size: 213.4 MB (213351097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d5ef570688e4f0c744103ca53619ec64eee27efd1f62001d9f82e4789453c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316547689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc039e7d985e709264f02129c6b6bb1ba748f7a391ae26c6da11f79e7f75d34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:49 GMT
ADD file:bbdd13db0e090d7d928a2beba57e3c1340342d05e5c15f7b7377c9791a5cb4ba in / 
# Tue, 23 May 2023 00:48:50 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:19:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:20:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d14a321d144fc48aa438b2364b0f1a5667979322ef9cada9309bca48584a11a1`  
		Last Modified: Tue, 23 May 2023 00:51:36 GMT  
		Size: 47.2 MB (47154613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af911895fe3f6120ef979a3b5dbd9bac4de6b4d900e6ad8ddd6b28ccb19a7746`  
		Last Modified: Tue, 23 May 2023 01:22:48 GMT  
		Size: 23.0 MB (22951581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc480ad84aad81f48b8427943b9e4cb119ca2f0562152d578d98f45ff47a69b`  
		Last Modified: Tue, 23 May 2023 01:23:06 GMT  
		Size: 62.1 MB (62144202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c909aa5b0b4faab46fd295d7d46adae7941a4443bd61771ee5a16f726e7e542d`  
		Last Modified: Tue, 23 May 2023 01:23:41 GMT  
		Size: 184.3 MB (184297293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bc482d01bcfba9d59704601f01b9f3890277671f0f5ae65064ffc8bfd8a092bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301978210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993c7c66f179e1f8a499111f4da05a053490bbe72ab3e5d29a35162ec157f3cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:00:33 GMT
ADD file:82567bde3caa9ad83c0c12c0525e6fd51cc833f0b29e733c2da572ed00150220 in / 
# Tue, 13 Jun 2023 00:00:39 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 05:00:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 05:00:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 05:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1d80e7ebc54969ad575378cf66dc58999cbf341e0d2a92c9ff0bfd5b3b9fb1c3`  
		Last Modified: Tue, 13 Jun 2023 00:06:30 GMT  
		Size: 45.2 MB (45234838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26e461ec0e64583c2acfbef48942f57c9de9da65ff1a078a62e910baf3ce05`  
		Last Modified: Tue, 13 Jun 2023 05:05:32 GMT  
		Size: 21.9 MB (21922951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da543e1cb7517b023e6ef07f0f0385da6f0c3f832cfd7ade1c7381c2ffe580b`  
		Last Modified: Tue, 13 Jun 2023 05:05:49 GMT  
		Size: 59.8 MB (59799388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a6dd7ea367162c4002f5bdde6db8bbbef4671fde6486cf888d7a0bb5c07e29`  
		Last Modified: Tue, 13 Jun 2023 05:06:19 GMT  
		Size: 175.0 MB (175021033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b1e52d6511e5cfbcb6ad379788c4aba30e2dd9ab3e9909a0843477506f3d785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340130427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4578dc30c4d05d7a1fed527a3d742d540a2f37c1cbac255db25eb945baf702b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:41:38 GMT
ADD file:94f1432513f9a03b38028af02b1d1720fb0558559faf3e7f9d7097cf6b962056 in / 
# Mon, 12 Jun 2023 23:41:39 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:05:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:06:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ba9ab3e6f12b9702649c2e0c7d78e22ffb9183f68c288b9edef2387bd8d4efd`  
		Last Modified: Mon, 12 Jun 2023 23:46:36 GMT  
		Size: 49.6 MB (49592096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393fb89bae1d5f0307a283cb7c3b5f54cc63fde2e90b7b65ceae29bcd27126f5`  
		Last Modified: Tue, 13 Jun 2023 03:10:09 GMT  
		Size: 23.6 MB (23558237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4483fcef438011d245d9be3906ab5e6a92c139027fe4286dc7e46b975299183`  
		Last Modified: Tue, 13 Jun 2023 03:10:24 GMT  
		Size: 64.5 MB (64490917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cddf934afceb08172df763ffcde92b9665c3c8ae9c4810b008715669ad3d58e`  
		Last Modified: Tue, 13 Jun 2023 03:10:52 GMT  
		Size: 202.5 MB (202489177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b4764a5e07b05e2bdd8d6d90fa4ff2e34c122e475fc4aa317242bebe454cba77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.6 MB (353591470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e185958c518f02129b840a8ea93d9703f29c31e0bb0ee3ca1e71acfb27d11b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:42:10 GMT
ADD file:209e3bb955801ad81eb18a280f9fbd5500a0e1f04565e6c94c9cd24dcba4c0af in / 
# Mon, 12 Jun 2023 23:42:10 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 01:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 01:10:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bce10b6f772acc79b03d87add4bd359f98c767e3599f82d8e351cced14c1a11`  
		Last Modified: Mon, 12 Jun 2023 23:49:26 GMT  
		Size: 50.6 MB (50562699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d6b7d433b6a8b07b01e4b262b82f2b882380e41bcd3a6e8b88ca32ea66321e`  
		Last Modified: Tue, 13 Jun 2023 01:15:14 GMT  
		Size: 24.9 MB (24858532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c9493cccdfcd2c44a013f62ecc08283137f3fd2d7a483cf56387dc987b536`  
		Last Modified: Tue, 13 Jun 2023 01:15:36 GMT  
		Size: 66.4 MB (66355536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e30574996c34012fa193dace0f01bb334e773810647079cb6d2a76b7945342d`  
		Last Modified: Tue, 13 Jun 2023 01:16:23 GMT  
		Size: 211.8 MB (211814703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0d42590a778653226abaaaeba3e4d95d9f165e2cb3520044566e699afa0f811f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326264556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732624570cf9a1dec3651b64baba5195328bdb63e629cb11fed831a9a8341e59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:12:52 GMT
ADD file:b2a9cefcdd223b4cbf9b1abac81e8c0c158a24f9c272910a8822619ea9d55ae9 in / 
# Tue, 13 Jun 2023 00:12:57 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 02:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 02:13:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 02:19:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65733d4f161a7d2fd9cef6d80eb7fe00897e936eb78d018361809f7384b08c28`  
		Last Modified: Tue, 13 Jun 2023 00:25:52 GMT  
		Size: 49.6 MB (49561285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cac982d96cd0724a1a282faecd42ae997cf2e6c468441bdcf2ce718f092f4d`  
		Last Modified: Tue, 13 Jun 2023 02:26:09 GMT  
		Size: 23.6 MB (23606470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec621985ebc463298904a643b89d8805cdefe9a156edc65db797295bf5ce37d`  
		Last Modified: Tue, 13 Jun 2023 02:26:58 GMT  
		Size: 63.4 MB (63449697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43067e7ef8f78b7740cb05aa82b22965d78ae240348e6c33c24dca2d27e8f056`  
		Last Modified: Tue, 13 Jun 2023 02:29:12 GMT  
		Size: 189.6 MB (189647104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4180f83bee8862f62e34b242a6c4676f055a0f07f919efc59b95ea783f28b947
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363209518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7746abe0792125c6d07981a17bf7eddf421fc2d3b4d85176177bb5470447ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:52 GMT
ADD file:cffada1d28fb1dc246127e193bd218b3c76450667fe4cd380f04a5caf5571be9 in / 
# Tue, 23 May 2023 01:17:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:55:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:57:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d914d1b8acfde6dc74b2fb48f95f7aedafbe4e4ad3b6ea21aa9db007eee47739`  
		Last Modified: Tue, 23 May 2023 01:22:29 GMT  
		Size: 53.3 MB (53302061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfd02567bd019328b094640438b56aa8ec096d625eb4dd7646bad29dc33d703`  
		Last Modified: Tue, 23 May 2023 02:02:41 GMT  
		Size: 25.9 MB (25928691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bffe3818ac84f2da95782d45c9d0ec1ac2686d474eef4dd224cd8a76dca7a`  
		Last Modified: Tue, 23 May 2023 02:03:23 GMT  
		Size: 70.0 MB (69960094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fadd7c17d6fa307406898325a872ede82ab292ef5fa12394c40c221c7eb9c3`  
		Last Modified: Tue, 23 May 2023 02:04:21 GMT  
		Size: 214.0 MB (214018672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:319c5404529b1b4a4850bd19828fad92d8f15ec12a9b212558e3c33420e79be2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360337704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3401bd1aa4e446fa792354fe3a7a505b7987861b1373581c3a8fcad8acc678ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:05 GMT
ADD file:a70ed7f2a74611e58dff0d33cfe5096adda0510365aa0e8d263a6b37246bc262 in / 
# Tue, 13 Jun 2023 00:09:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 00:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 00:34:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 00:42:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70731a0001323eb925eb073dd2d04510ef4700ac6f50030dfda993464aeac07a`  
		Last Modified: Tue, 13 Jun 2023 00:12:27 GMT  
		Size: 45.7 MB (45744069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cd3aa3980443f31b6ef037bb0103dc68fed3f80d9dad50456dfc523c6e96bd`  
		Last Modified: Tue, 13 Jun 2023 00:43:27 GMT  
		Size: 22.2 MB (22237741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c649750d7b93709631b4e4968c598a571877e20cf0c740450004c294ba0fac93`  
		Last Modified: Tue, 13 Jun 2023 00:44:49 GMT  
		Size: 60.0 MB (59982046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9b379ec8367526584e03bda3262d3295316d6ef7f3221aab8d5e7450aab8fa`  
		Last Modified: Tue, 13 Jun 2023 00:50:25 GMT  
		Size: 232.4 MB (232373848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1bbafd5378397c3d7f47f2e041f2819246b08b6702b86811c4784aa230ad45ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318590113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83de6025398ecbe1b08015f53e1a1c50da9f422fb2d44a672de0159a898f550f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:35:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6242508e16648c81ff21ed8251d1dfbddaed438084bbcd6c7baf639349cf592b`  
		Last Modified: Tue, 23 May 2023 02:39:32 GMT  
		Size: 24.3 MB (24275724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081327490bfb5677aff76324903d283fb120712a9f911ed52f6d4be91df47e0d`  
		Last Modified: Tue, 23 May 2023 02:39:46 GMT  
		Size: 63.6 MB (63609047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46eacf0032042bf63c931197525f86388a95920b01b4b1a56fb4cf0331d60ba`  
		Last Modified: Tue, 23 May 2023 02:40:13 GMT  
		Size: 183.0 MB (183040727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
