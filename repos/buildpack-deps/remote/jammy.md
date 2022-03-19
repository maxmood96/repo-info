## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:6e6d2d68ab9ff32e229c3e406e12f511df7bdc5589fb0afded47ec6188af7caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c26cb6a3f777f17987644f34bf80c6cdb600d791daaf2dfeee06ee7d603638fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250162543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77df891d53d0fdcc2dd3af6566e413506b4ebdaf65dc3d43d45f199a1aa7c406`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:31:09 GMT
ADD file:ce9bee138da151fa0b9e441f7ef06865e0171006e686f0dc5e1ca6a06e0a3d0c in / 
# Fri, 18 Mar 2022 05:31:09 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:56:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:56:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 07:00:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11581404396c9d08d16b97c64bb2fd043ef3216bd3e3ff3d1c6e03398dc8e336`  
		Last Modified: Wed, 16 Mar 2022 11:30:57 GMT  
		Size: 30.5 MB (30485551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1305491a76442ac63301690c078bd5fc0af516ba25fde9528a35db9188c4e2`  
		Last Modified: Fri, 18 Mar 2022 07:12:40 GMT  
		Size: 3.8 MB (3817797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a1be61110601cb14ca88a066963bb29f75059eac2b2f9fb7a60196a2c46667`  
		Last Modified: Fri, 18 Mar 2022 07:12:40 GMT  
		Size: 3.6 MB (3559491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3088901b32cf2cf377032e6f6ab00ecc65f56304c8695724970fb8431a29f8cf`  
		Last Modified: Fri, 18 Mar 2022 07:12:59 GMT  
		Size: 39.6 MB (39595788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e3cd7d9a1d3443fb84359f693cca507892bdcabda685d6bddc958515478456`  
		Last Modified: Fri, 18 Mar 2022 07:13:34 GMT  
		Size: 172.7 MB (172703916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4c04f4cde8dc534a12bcb982e8f998c9657abca6b81b496bd427175922ea9ad8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216968969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac357e0426f7740ddbc34b42e63d7c69139ade5d9c949ff32599432a5734f65d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 07:33:30 GMT
ADD file:19a0584ac22c220c1260894e828ead25579919ba2a0448fb8bcf90ba5dc4ca07 in / 
# Fri, 18 Mar 2022 07:33:31 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:18:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:20:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:559c58962576ae20efaf4338d13982a09d934fa524ef90330d051b6ebcb20608`  
		Last Modified: Fri, 18 Mar 2022 07:37:29 GMT  
		Size: 27.1 MB (27069048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2098a0e581836f2c68e2c4dcdf61d703be4f4ad972816519300cfeb2ff2bb8c`  
		Last Modified: Sat, 19 Mar 2022 03:49:33 GMT  
		Size: 3.6 MB (3568653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4415fb5c74607390e5a07fdef46a85e56c4f53013f42bbe83c307ac1ef516`  
		Last Modified: Sat, 19 Mar 2022 03:49:32 GMT  
		Size: 3.7 MB (3712132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b59541b72d3d146846e21d3ad7cd50615cfa031db874fb86d0abe7a2659953`  
		Last Modified: Sat, 19 Mar 2022 03:50:14 GMT  
		Size: 42.1 MB (42106210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a921e4832963610b6bde9e4de9879c5ff5ab2bee66e7933a76c3e882f4ccdf5`  
		Last Modified: Sat, 19 Mar 2022 03:51:49 GMT  
		Size: 140.5 MB (140512926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bcc37bb9edf0cdb7f4eb813b251e60ce8c6ca26a2a2d4de4e893ef5af504bc48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244176027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45a0cb485ae3dcd192c2c823499a5ab4263007cb7921ddd2a0b408c3a9f63a2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:13:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de81b8d223c70c2ecff8735f6588279de47e4a3c3266d19bf621c5c4ffc048c`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.8 MB (3792303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49986fba69bc0eae7347e2c6882c0b760ce11a31a258fb2694ff83665931577e`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.3 MB (3319390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8402a169943d97ded64a733fe9cd21896e521ec0e8b9fe4524d7ae817818ae`  
		Last Modified: Thu, 03 Mar 2022 20:19:59 GMT  
		Size: 41.8 MB (41760683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7204bb9af9b61fd248cce4031bbef049437307198afd72d7638a8e7a9e9467`  
		Last Modified: Thu, 03 Mar 2022 20:20:33 GMT  
		Size: 166.9 MB (166878947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9481ca66065ce339b1e01f5b8ff120cc8e635dd212b4baa9848b0e0f98178741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274967335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25958d2e5ce390a360a622c893b7fa82e578a48d54d2b51f2843aee2845b29c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:43:01 GMT
ADD file:5596c6fcfdc9d3c4b63db527cacb4cac548690f6631b60dee4972329037237c1 in / 
# Fri, 18 Mar 2022 00:43:02 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:12:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 03:15:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:22:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:779c5da60b9290c00c305c706d5d477b0647cc028035cc1723db7e437a962fd8`  
		Last Modified: Fri, 18 Mar 2022 01:01:57 GMT  
		Size: 27.8 MB (27792674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d84b474ce4102d31d6fd8cea63267bfece598ec610fe1f5612b795b0960831`  
		Last Modified: Fri, 18 Mar 2022 03:49:04 GMT  
		Size: 3.6 MB (3611244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4323e0585e69caede2372dd7a23853990eae0fe4e7d87d98456fda8e0f48e7ea`  
		Last Modified: Fri, 18 Mar 2022 03:49:03 GMT  
		Size: 3.8 MB (3775054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c642a2f1f533bed60af71d21875a89773835c6cfc32cd7a8e06aaa82d88f26`  
		Last Modified: Fri, 18 Mar 2022 03:51:17 GMT  
		Size: 42.5 MB (42450219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c640ee2b87d64cd1809067f733c2787aa22f0f0bde9c36a21dfdd7e6a5ea9a8e`  
		Last Modified: Fri, 18 Mar 2022 03:57:23 GMT  
		Size: 197.3 MB (197338144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e5e54e401ad574d43a0752256c91d1264e9aa40b8e7feae0f0134804569247a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224012927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed75fb7f5890d47c5b79142b489089bdd94020b76d2d1f9cf4f190094358678`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:36 GMT
ADD file:9b55d3d522028967302e5d3e4ff8f137867cafb44dde60f16cb4164bcf696f8a in / 
# Fri, 18 Mar 2022 00:37:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:10:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:10:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 17:11:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:11:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b1039ed94adda6ad2c358e44a4dcb6e55794a5ee68506bea2119c7395e92522f`  
		Last Modified: Fri, 18 Mar 2022 00:39:11 GMT  
		Size: 28.7 MB (28724094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8728d8dc15c76c2a67839b9755498323086446a2de1a879d4375058dfea3ca`  
		Last Modified: Fri, 18 Mar 2022 17:17:08 GMT  
		Size: 3.8 MB (3818549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0c8ad91f4becbc8656c8d445ef1d2d5bb25c41162f6742822fbf8413e86197`  
		Last Modified: Fri, 18 Mar 2022 17:17:08 GMT  
		Size: 3.5 MB (3470306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8ca7e1e2ff439e7af6e682827aa031061083e2d3913236790a2176b5cd5dd6`  
		Last Modified: Fri, 18 Mar 2022 17:17:20 GMT  
		Size: 39.5 MB (39539978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338f653b3eca32c2391303b3e77709e8f071998e415490557be9d276005e9d4`  
		Last Modified: Fri, 18 Mar 2022 17:17:46 GMT  
		Size: 148.5 MB (148460000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
