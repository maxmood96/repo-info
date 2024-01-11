## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:155ca60ef37f9fff8f977643a889e4a6370162deaaff0a2e28879f5192b8624f
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d8d1bc21ae3c5195e430ce0f60fbf48bf5937f9cea8fcc376c02433dcc546dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.5 MB (403457935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7937b42a8feba3bb0d82c587532be8df5323486dfbc150f73129d530b18d0659`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:34 GMT
ADD file:4c1ddd73138f061e46cb63a959e0b45e213bbe55a4e9859988b45cbe28c1939e in / 
# Thu, 11 Jan 2024 02:39:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:40:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:41:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f8012d8f125a645d98266e2a23733c0354f39eaae73d40ec23f48c12dac17e1`  
		Last Modified: Thu, 11 Jan 2024 02:45:14 GMT  
		Size: 52.3 MB (52267954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d4389e3b2cf1b1b5d2973b88c056f511579317121eba04eb993bb13d8092a5`  
		Last Modified: Thu, 11 Jan 2024 04:47:38 GMT  
		Size: 23.8 MB (23784573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb183d0010e4c134b94cbd70e63a2a8ec66d3c15e7101509e6f7f056182ff53`  
		Last Modified: Thu, 11 Jan 2024 04:47:56 GMT  
		Size: 68.8 MB (68774698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1184e4d1f2d4ddbfaca1915f5f1519986046e341964e7c9cca22dc2c929d3bf`  
		Last Modified: Thu, 11 Jan 2024 04:48:36 GMT  
		Size: 258.6 MB (258630710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3a4fa67d6308c9d11531802a1714b7e3a30f7a0e2fdda70c23e2ec9565eb1350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370914489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b521f21f6e40b32094690d87fef9846447df7e982f17cdf3775c7078d652fe9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:28:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1076957cedc8a5a67b5ef8a93c803e6193f70ae925dc66e3135d08c87986fa`  
		Last Modified: Tue, 19 Dec 2023 05:34:49 GMT  
		Size: 235.1 MB (235059785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a2d437465c678fdbeb26a1dc72dfe33c89f4c618e91462f65f39c6dd726bcd78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347264922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162db3a41fe9b99b8c862bda84608da82c27b7559ac215d2541c5d1a60ed19d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:44:19 GMT
ADD file:8fdf812544a777aefa5a72371aaae01c05618dad10c40d3f4c4535ab61effa5e in / 
# Thu, 11 Jan 2024 02:44:20 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:21:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:22:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:24:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:738b42c6f08e0cf326b2758999daf25b796a2257c832077146951a1871b3fa48`  
		Last Modified: Thu, 11 Jan 2024 02:51:44 GMT  
		Size: 46.9 MB (46880379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e28248858523a50531a4a4ba3120a7a3bed7f5d8f5e1532dbf70fe0e4abdde7`  
		Last Modified: Thu, 11 Jan 2024 03:32:57 GMT  
		Size: 22.0 MB (22032903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262aeb61dcefe26c7a021c6cbff21437816af99da1c465425a42a57695535cb6`  
		Last Modified: Thu, 11 Jan 2024 03:33:23 GMT  
		Size: 63.6 MB (63578121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9adec4ffd5656c654bbea826389ce450ba7de4c48755d423302c2fc11976f4`  
		Last Modified: Thu, 11 Jan 2024 03:34:20 GMT  
		Size: 214.8 MB (214773519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e20fa8d58f288f40a7caa444c147017beb16cb86bd5b9c6643c78f5987316dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389318431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3788047583bea1aaa8992313e98de6dc266c2a82f79c1190e19df2dc83ef745e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:39:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec939d1d3b6574ac3482db9be62850fd83b1612f01d44fb296af8ed464c33f1f`  
		Last Modified: Tue, 19 Dec 2023 11:44:56 GMT  
		Size: 26.0 MB (25983709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591136ec6e5960d51ec4ac04b638e9bb1afe645fd53be0f002e76e7d236d522b`  
		Last Modified: Tue, 19 Dec 2023 11:45:12 GMT  
		Size: 66.1 MB (66149784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5ad01f173df3982c94ba452286767ffb8a3e0e3eb42a4d4551877d1056860`  
		Last Modified: Tue, 19 Dec 2023 11:45:44 GMT  
		Size: 247.5 MB (247495152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:310896a51647634357c7df0de030674517d5cf73c1bfe0d206452e49c6204297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404237452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46441b1153f33d9aedd0364794a7f3e792b67264ec2f12e9d43a7fe5b8898522`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:20 GMT
ADD file:62936974dfc268ed9921277921d72e2fe4b8e316d02774bc95127ec6d56693e3 in / 
# Thu, 11 Jan 2024 02:40:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:36:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:38:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed5772f4773b25b36078212363dc2fec6143ee364938f8da48464f4eec8f182a`  
		Last Modified: Thu, 11 Jan 2024 02:46:50 GMT  
		Size: 53.1 MB (53117689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2db4548d8325ba0eeaa2762072b818997f0ca88e46fd790e170e60a67b1eae`  
		Last Modified: Thu, 11 Jan 2024 04:45:49 GMT  
		Size: 24.9 MB (24852383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029a70e763831146af2e2372d63eaf8bea93c65c5584418f84d97b2c06bec0a7`  
		Last Modified: Thu, 11 Jan 2024 04:46:13 GMT  
		Size: 70.7 MB (70696688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18bf31d5517f6727bd14630e3820783c8639eb811e253ef1c75fa54a1730dd7`  
		Last Modified: Thu, 11 Jan 2024 04:47:14 GMT  
		Size: 255.6 MB (255570692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:af6507b02c384a7b16d1e68f61f7e9cb976838edb32d618e14dd22834aa01ad9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.7 MB (375723942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec45878110a8b7aa46783d65d6121d7a53ee1a73f7e35f4fcaf1f499ae2744bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:14:46 GMT
ADD file:5f44d39d860d41ee2d969347a8ee97117d8464c5ba5bb8a7f437e02e02bfcb33 in / 
# Thu, 11 Jan 2024 02:14:53 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:07:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:14:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:44d8b0d43d4e86510a6929ab344b91638efe7be700303879a57bc650fbd84861`  
		Last Modified: Thu, 11 Jan 2024 02:26:21 GMT  
		Size: 51.4 MB (51364371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc4cda8e31359619d6ac6175803cf81d221646100de8856ff3c129b6c42d76c`  
		Last Modified: Thu, 11 Jan 2024 03:30:44 GMT  
		Size: 24.2 MB (24168147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48efcd41b3712a829c2841895c2c38d12027581f76d5f0d986fd20cc2f608c3`  
		Last Modified: Thu, 11 Jan 2024 03:31:39 GMT  
		Size: 67.6 MB (67579039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8969569160f2c5c6a8a65379d7ef8368582e88e65960a880e75dcdaae4d2b0`  
		Last Modified: Thu, 11 Jan 2024 03:34:18 GMT  
		Size: 232.6 MB (232612385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7c59c7b1d7a8d1ad9e1365acb6187cc0c56f7faf991c90e3f5b74c7e21601af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.5 MB (412493320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118e9cf52ba29c12c8b430e13c7830977d77914fe311c7009d7ff4db169b33bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:02:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:13:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:97954753acf4d5cb589b2a49219ffbc5c86834cb864ed80f516370017ea3c569`  
		Last Modified: Tue, 19 Dec 2023 01:28:17 GMT  
		Size: 53.5 MB (53455717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf9bc2559c9bc0dde88b00d18449e9a40dea5919313c9dba6b3a432f24542e4`  
		Last Modified: Tue, 19 Dec 2023 12:25:16 GMT  
		Size: 29.0 MB (28960588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bcb9d372effc2b9eed2bc00b534deeaf705ecf5a3705a53bce008b65768d0a`  
		Last Modified: Tue, 19 Dec 2023 12:25:37 GMT  
		Size: 71.6 MB (71584185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d68a49298b0a4e3725e9f200ab89754fd611e60f4a3da3511f6c2e48d2407a`  
		Last Modified: Tue, 19 Dec 2023 12:26:23 GMT  
		Size: 258.5 MB (258492830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e06f73b770a920fdfe28b7c1202a0dc92bc6559c46a992fbc97c4705eae8bb2c
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436257694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca4f6fd232056f9d6bf0854ad8ec0968c278ce7d1b97bd7815a79accd87f8e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:08:57 GMT
ADD file:2425f95373d17e6fdcc9fa7f49bb6c7911f6b90dc27b013c125e09c38c1691de in / 
# Thu, 11 Jan 2024 02:08:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:41:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4051c39033b0cb21a5a8e11e0cc7f40eaa9806ddc6699457c2f509128c3a492`  
		Last Modified: Thu, 11 Jan 2024 02:11:46 GMT  
		Size: 50.5 MB (50487871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680ecbf0470fdf287fdea90380971756e9423f13d45445f3c9b23000a0ace9db`  
		Last Modified: Thu, 11 Jan 2024 02:41:54 GMT  
		Size: 23.5 MB (23463389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be477d1b1316100dce4471ec2cd1633d4849b301db02472aa0f0b6afad63081d`  
		Last Modified: Thu, 11 Jan 2024 02:43:13 GMT  
		Size: 68.0 MB (67987875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dfe9ebe1ce7647a06ed30dc611cb2c666c6ee15d7ceafdc0fc5a900f77f93f`  
		Last Modified: Thu, 11 Jan 2024 02:49:06 GMT  
		Size: 294.3 MB (294318559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e11bae1d66d436b495174a0565e3d9971854799275db09bbf997cb5bb3c569dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378162989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d04c2a31a98dca05d74479ea9c7e90192cf778f8f46cd5cd93de5d61369e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:39 GMT
ADD file:8031754126dba92ceeddd0be53523bca85fa55f5859c83eaa57be2b0ba8f8046 in / 
# Thu, 11 Jan 2024 01:46:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:15:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce6f2c0c05e382af54def5b355ea9bda0f36bd689f9f43fdcd74463778010bc5`  
		Last Modified: Thu, 11 Jan 2024 01:51:57 GMT  
		Size: 51.7 MB (51672176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccdf962076103e72329069bf48fa3112a100d8a6deee506176beb22e27789a0`  
		Last Modified: Thu, 11 Jan 2024 02:22:51 GMT  
		Size: 24.9 MB (24850534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b64ba60f98b957715429fcc464c59051f469caba372893e922d41e0cf32bad4`  
		Last Modified: Thu, 11 Jan 2024 02:23:07 GMT  
		Size: 70.0 MB (70036818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c07749e7e6bb6c7e5d9ffb3f6ab89c6a03ed1299f3e901bd031fe7d2cfce9`  
		Last Modified: Thu, 11 Jan 2024 02:23:43 GMT  
		Size: 231.6 MB (231603461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
