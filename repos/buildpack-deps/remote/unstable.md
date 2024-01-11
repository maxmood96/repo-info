## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:64fc9947a34727d9cba2f16d3eeb553157c45386b554f8a544094776ab476bec
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

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5c1f5bd5e9e24eddc0f490c84a78c0407ccd76bc033eb7f6eccd3e8d4d9eac46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371353285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1705dd6d3c3223baf4b3c598de337fd5ee8ca684023203e652bc55ad8a9ec6e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:50:13 GMT
ADD file:9151e08b2e412287dad7d69ba24534b298db5f003230d2502a6ba98cec1ebd47 in / 
# Thu, 11 Jan 2024 01:50:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:58:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:59:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:02:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b1b81c0298ff01b74292896351d56a8bab04cfea53060a06c7a5a819fcaccaed`  
		Last Modified: Thu, 11 Jan 2024 01:55:53 GMT  
		Size: 49.4 MB (49383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3596882ba4d789b2748d175d36c81d47be0b31bcd840be1acdcd1f4f8e0dd`  
		Last Modified: Thu, 11 Jan 2024 07:08:29 GMT  
		Size: 22.7 MB (22727696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9c40a74a9cdc4bcbf9e60c299bf24612ef99ae8a4e0ff4c0774d9fdae77a82`  
		Last Modified: Thu, 11 Jan 2024 07:08:52 GMT  
		Size: 66.4 MB (66376638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94086a87540fb712cdd71fdcb626b02d1f55a6311196aa3e52ceb0c8277740a1`  
		Last Modified: Thu, 11 Jan 2024 07:09:44 GMT  
		Size: 232.9 MB (232865820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

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

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:69245b548ca491164b8f79a59ed9f132c590f0451c5d135a5a083a157e24296e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389750539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced53c9b7074b8ea302783196f8ce9dd79af5f97a6e5bf7ce1ed009eea808d63`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:49 GMT
ADD file:41d0336f9211d4665c98a2ae6d92a97885617a6f3ef646ad5e96e1c505887f36 in / 
# Thu, 11 Jan 2024 02:41:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:31:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a6d440355d1d93856497f93e287cec8381a68287949dd140442830cc02425a8`  
		Last Modified: Thu, 11 Jan 2024 02:47:08 GMT  
		Size: 52.1 MB (52148723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2daf712adc807f54f8b2b64a1df5a3955a5a93666ac193bb4074a1d18ee8d3`  
		Last Modified: Thu, 11 Jan 2024 09:36:43 GMT  
		Size: 23.5 MB (23530411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3fd6ed3f8d38e910bb159ceb062013c7c1ddba4294b092d803454c6df4d781`  
		Last Modified: Thu, 11 Jan 2024 09:36:59 GMT  
		Size: 68.8 MB (68839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c288fec57f4945c661eae06efa8174cbd03149cd286a4c0d81d679a147bcad0f`  
		Last Modified: Thu, 11 Jan 2024 09:37:30 GMT  
		Size: 245.2 MB (245231428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

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

### `buildpack-deps:unstable` - linux; mips64le

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

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9b3a38fe80a279ce74af308b73a20a3ae93a513930ffcc383e88a212d7d5309
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.8 MB (412839044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bda82009c1989f6c73b4c951dc08f0d9b02566a4739f5b2c7110f881e317df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:35:47 GMT
ADD file:c2cc792d0e48795239ba8948f28a31a458128e8d2dade2ed88a7cc1830609097 in / 
# Thu, 11 Jan 2024 02:35:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:13:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a12077db2f3238d1c66f5358bd931ff537264797def7be2c14c9e9cd0ac05402`  
		Last Modified: Thu, 11 Jan 2024 02:41:17 GMT  
		Size: 56.2 MB (56185653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25800b978411714d00508bd5510f9f780d186fe5a4b83794204a9ad4f6eb6bbb`  
		Last Modified: Thu, 11 Jan 2024 07:25:41 GMT  
		Size: 26.2 MB (26179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5849bf0a86283edbb330815a50679f0e541585b82098279c61a8bedd8a86f8a`  
		Last Modified: Thu, 11 Jan 2024 07:26:04 GMT  
		Size: 74.4 MB (74434454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d3c92b2c4fb2b60d5a67d474e1a478746d30627f98e595048676ff200feb4`  
		Last Modified: Thu, 11 Jan 2024 07:26:50 GMT  
		Size: 256.0 MB (256039591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

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

### `buildpack-deps:unstable` - linux; s390x

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
