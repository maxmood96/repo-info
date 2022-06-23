## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:9409fbca35a0afe8961926f1ec0144c24eaa6ee70e33b5a8f0268b7bff058337
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
$ docker pull buildpack-deps@sha256:e3ceaa559f55d3ef7143e6f5e2c7deb45373a14f66d78337c98275cf7e3dd43e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338982342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f655195eb67b40fd8f6edcdb2ef14478a4b6045bcb64aa54c10803217e372c0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:19:54 GMT
ADD file:7e968e6ae38ede120a52f1d2e734b4fee4fd4ffd6e5f747edc8190d2a8bc6a52 in / 
# Thu, 23 Jun 2022 00:19:56 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:48:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:48:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:49:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8849e73adf621df4a443e9ac4eec9b698476e4f14f8ed894806f302d5b33156b`  
		Last Modified: Thu, 23 Jun 2022 00:24:12 GMT  
		Size: 53.0 MB (52993983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a3004561e732519f3aa704178d4bc2d97eae3c1cc556af0ea0d3e66e28ba24`  
		Last Modified: Thu, 23 Jun 2022 00:57:33 GMT  
		Size: 9.3 MB (9291497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0f93f12fe636ab6b9beed73979390ba6a1aa6fdcf7bbc5cb403f683142a0e3`  
		Last Modified: Thu, 23 Jun 2022 00:57:33 GMT  
		Size: 11.3 MB (11264030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c85c343cd3e553d90219aa415a28525986ebdcf4ed151ad763eea350150fd70`  
		Last Modified: Thu, 23 Jun 2022 00:57:52 GMT  
		Size: 57.7 MB (57719551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d4709f8d9bb7ab97a241ea8a07159919e2c1d3dfab03b8cb8f554c6c1e690e`  
		Last Modified: Thu, 23 Jun 2022 00:58:26 GMT  
		Size: 207.7 MB (207713281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ae5ef8803d802343739802077ea7787593ae9eb0f714e3b3fdb989927e415e9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306699238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58feab16e6ccb7ccffacbe2e2cc76947864fd30e0fc61b0f4f26c09b42b24f61`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:01:33 GMT
ADD file:2980a4070352ee6798cd5240bc8b6e068815aed3d8bbf85b426005ece7d9872b in / 
# Sat, 28 May 2022 02:01:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:02:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:03:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:05:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:234035d78cc15d2308af9cee32306959cb61c14372c60047e93d7b747c05b2db`  
		Last Modified: Sat, 28 May 2022 02:16:30 GMT  
		Size: 50.7 MB (50735045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0923a0d0cdbaffd32ad4dcaea3669e9e3de65fa60085e77bb3b3e8d4b4eb3fa0`  
		Last Modified: Sat, 28 May 2022 03:27:27 GMT  
		Size: 7.5 MB (7537455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d2efe917b364518c9ef6d14325dc6cfd07776bdf28eec8971d46617ff1d524`  
		Last Modified: Sat, 28 May 2022 03:27:28 GMT  
		Size: 10.9 MB (10927507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d389a3875812c86b94085d0e0466b0416949eec9f33a61dea888cf39f8c419`  
		Last Modified: Sat, 28 May 2022 03:28:19 GMT  
		Size: 55.2 MB (55173534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cb03957b29b9525c45d6e5acc64d7e12e8f50601032df3848fa467a4c18850`  
		Last Modified: Sat, 28 May 2022 03:30:17 GMT  
		Size: 182.3 MB (182325697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:588356fe3c961469c6cc63a8a834a9bc371a70c26ac0ade6dfa07a17dd02d2e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293725407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e3593988d2a9693c318443d2a4eddfa6c880e4559add96d31ece6389fad8d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:58:07 GMT
ADD file:8f129729b10afccc69a16674ae2d85afe02706c13f7c3177672040ce01dc34a2 in / 
# Sat, 28 May 2022 00:58:08 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:38:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:39:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:41:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:138713cd49f1253cc6e27f92b0403100f0c5966f7a66077fd4d7c6ab6a6799df`  
		Last Modified: Sat, 28 May 2022 01:13:41 GMT  
		Size: 48.5 MB (48476343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db436db30438e10e5eeb35827787a5b8ed355db8a9ecf271097bb255dc415b5`  
		Last Modified: Sat, 28 May 2022 03:06:08 GMT  
		Size: 7.3 MB (7269071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926a3169136786c87319557ca5d830b8821949450e41d7405b1167918ad0bb4a`  
		Last Modified: Sat, 28 May 2022 03:06:08 GMT  
		Size: 10.6 MB (10572917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21dd0c806bffa44c59273211fcf9fdb67feabfaa2c4c33867f7d24f3e25078d`  
		Last Modified: Sat, 28 May 2022 03:06:56 GMT  
		Size: 53.2 MB (53179627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034cff7e5ce28ba386399b69a9bae8fba466e9aa22cd1d4ecb2756b054c709f`  
		Last Modified: Sat, 28 May 2022 03:08:43 GMT  
		Size: 174.2 MB (174227449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39537ff6fa2874d82dd2303e1bb631bde9ac3f92d705b1b72ac90ed6953dcb5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653b279d5c793b8369b188bf37d263d691e39e0ab86fa035d3cc78f9d8a30d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:05 GMT
ADD file:149d923f098f33a347aa57ca673aae5cc103628b202337e4ff2ea5ac278e5c18 in / 
# Thu, 23 Jun 2022 00:40:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:09:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:09:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e34000263ac838bb9254930c5e34d9fa4b486f544707ae0aa508bb7ded624d59`  
		Last Modified: Thu, 23 Jun 2022 00:46:09 GMT  
		Size: 52.1 MB (52074605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d844fe46570aeb3a40b42c67a4714c432ac2d6ccc31125f7eeb076c05e919ff`  
		Last Modified: Thu, 23 Jun 2022 01:20:40 GMT  
		Size: 9.1 MB (9126954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39d92840e0fe1b4aa70af7e37d1e6c48b3c61da85b2b3d9e13efb83c990d2d`  
		Last Modified: Thu, 23 Jun 2022 01:20:40 GMT  
		Size: 11.0 MB (11041433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbe8b6171db521e3284e73fee8669036467cffe10b2030372d262cb498caaf1`  
		Last Modified: Thu, 23 Jun 2022 01:21:01 GMT  
		Size: 57.7 MB (57713059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304a54a06ddf5360088c970ab81c345cb257f2c4fb82f6e9c48f7e7671864610`  
		Last Modified: Thu, 23 Jun 2022 01:21:38 GMT  
		Size: 201.6 MB (201589767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:24ce11a00391b071a67ed11662e55dc14db3fb6473b4729d64e34ed282a3173c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342084069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54baeb2366e78baa032405ff8dbb9557cfff15249944d2ba36e2a88af853468a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:38:52 GMT
ADD file:d8108af9af2f3fb7f3dd905a9b4dd8391d568ba8dd590a9ca2bbeecd44354e03 in / 
# Thu, 23 Jun 2022 00:38:54 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:08:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:08:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0120d80f9ec3d96114e34087bd467cf9989c9c723cf7622bb16fb3675443565c`  
		Last Modified: Thu, 23 Jun 2022 00:45:18 GMT  
		Size: 54.0 MB (53963635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a0c1f242a443b42292f09b23bf00a038a40230b125f2d832ff706e0b0fd009`  
		Last Modified: Thu, 23 Jun 2022 01:21:05 GMT  
		Size: 9.5 MB (9464738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2c7e9a858ffdd4f52faf3fc1e4e080485c9024f299858237d4b3961f4e27d`  
		Last Modified: Thu, 23 Jun 2022 01:21:05 GMT  
		Size: 11.5 MB (11464163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000d7279af4a42e39fe0892505db82f28dc4127c5b4ff59701217c5f3921c339`  
		Last Modified: Thu, 23 Jun 2022 01:21:26 GMT  
		Size: 59.2 MB (59192570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e247eb958bba36f25d3fbec4ead564df58e2dc5cc7e06e7b32f7e73f839a3d`  
		Last Modified: Thu, 23 Jun 2022 01:22:02 GMT  
		Size: 208.0 MB (207998963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2c91247c20f714f3c89d04f44f5b80fe8b3fd881b9d0eac592b2dc180bd2eb53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316189195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af2fea3853f194e9c9415d0e55650974196d12121b3fcc9d3e0d4f3daf66d48`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:09:18 GMT
ADD file:0db9365eff38bea353e789709159951d557685e098127d950e467c83468aadd7 in / 
# Sat, 28 May 2022 01:09:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:45:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:47:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:53:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:409912beaa99ac80f6ec57bce7ac6621f4659f5f43cdaf3152de94639a634798`  
		Last Modified: Sat, 28 May 2022 01:19:34 GMT  
		Size: 52.1 MB (52061634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6976dd6800a501b4f86f988f732f79809a62582465ed0c2a06afe5c24d753b1`  
		Last Modified: Sat, 28 May 2022 02:21:04 GMT  
		Size: 7.5 MB (7506250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c469859fffca391e2318192162949a194958f00b7d4d3e4aaf787a8d79865cde`  
		Last Modified: Sat, 28 May 2022 02:21:05 GMT  
		Size: 11.0 MB (11019527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5addbbcd3adf2891ddf68850f2a8a25112410557e4531d8e3918d9c5ea011ff1`  
		Last Modified: Sat, 28 May 2022 02:21:54 GMT  
		Size: 56.3 MB (56313089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716aef1344fbb6eae0c40aacc7b5610b9c053301faec0b6d0627d377aa4156a`  
		Last Modified: Sat, 28 May 2022 02:24:03 GMT  
		Size: 189.3 MB (189288695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ae1f638d4dca6ad1c83acdc26afdf7c0189799de730a77c710278a7c560def3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346129292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e90d569d0974552364b9c08249e1a46700e211743b9fd897c6d9491713c95b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:20 GMT
ADD file:af4ab80f98b1cc5089a94e2932d676aad92fb52c2f59476cc64955602ea3d330 in / 
# Sat, 28 May 2022 01:21:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:56:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:06:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b80d749a1cbc85d39c24118acb8615cd7c0ba93c2cb7561974f0473b9863a264`  
		Last Modified: Sat, 28 May 2022 01:30:55 GMT  
		Size: 57.2 MB (57161586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2dd070dcaaf036f25496b09532c660455f3a5920ee198f04d6d52e2a7b95ea`  
		Last Modified: Sat, 28 May 2022 03:34:04 GMT  
		Size: 8.5 MB (8492248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898ca31e1ca70ebebfed2a003df2baad8dd1bf696095a848f745e93a3706aa7`  
		Last Modified: Sat, 28 May 2022 03:34:04 GMT  
		Size: 12.1 MB (12065270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc921ec2a90bafbecfdbc02278b617a2c8851e6e9596febb515ab7f43e0860f`  
		Last Modified: Sat, 28 May 2022 03:34:27 GMT  
		Size: 62.3 MB (62313539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940bc01c3348b9f65b16d0d9e33dfa4a37443258da75c2b59b58beb560bc0658`  
		Last Modified: Sat, 28 May 2022 03:35:14 GMT  
		Size: 206.1 MB (206096649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af353d1a3a4a5a9d4d12c7c94b1a996de3ff20bd9f0ff494c2985bc36f5f6d13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307821808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4089f3b364e01fe523c3b639f62b66da2d9a94d8a58fa937ab02e9d87e8078e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:57 GMT
ADD file:4a6691f8332d56b3f631afa5579acf89d2271614f4a4f77baa24e59c0b2b3016 in / 
# Sat, 28 May 2022 00:42:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:22:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5c219aa5bd4928fd8e410d747805f6d8a6cede332d701af0c9e39dca3b50c70d`  
		Last Modified: Sat, 28 May 2022 00:48:58 GMT  
		Size: 51.5 MB (51490385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b51eb782be06235f2446e523178fdce20039860905eeef1a177ee2ab9b7b259`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 7.7 MB (7662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077ec432669cf9233ec7c2120b3f33664a5d8ac0f8d2a61de67643c292801208`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 11.2 MB (11157636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7881263aae598e496a174ca6809ac1657096989286b9533de93d9151065f0e`  
		Last Modified: Sat, 28 May 2022 02:34:28 GMT  
		Size: 56.9 MB (56890824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eeb6e30d970435be02d5716fc8dcc5c5324f9bf45618a7f1bf4ebad716403d`  
		Last Modified: Sat, 28 May 2022 02:34:56 GMT  
		Size: 180.6 MB (180620614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
