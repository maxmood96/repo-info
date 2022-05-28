## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:a4896460f22f9af67de77ff84d3891ed48c4bc9e42ff45d7b1e4a4ef4ad95672
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9ab56ff71eb6c525035aec09df8293f7e8777941a92e0c1af14df12ca7464046
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322362474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679938ea7aec809e7186dd5286c5f84a818a8244047f1044b3463a104b499f8f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:41:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c91c4cd86dde23108ab3af91e9eae838d0059a380ee7dfd4f370b6d985523`  
		Last Modified: Sat, 28 May 2022 02:49:31 GMT  
		Size: 54.6 MB (54579133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc8d88542628a7668ee653a4c00f2cfef5f9ea24f407227b6b63508c56eba3e`  
		Last Modified: Sat, 28 May 2022 02:50:08 GMT  
		Size: 196.7 MB (196743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a202d869187c40664b79433b3780a4d29fcb6ddab473be30ecda7c9f99628b96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295202429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940ecd7f22957fcac92be5a14b07e84b3a7da4624d577b72f7512cb5a606346`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:59 GMT
ADD file:b4fea5a360c5cca5abc5866da48126a30eeaf4e976d09c479958fe445dae8021 in / 
# Wed, 11 May 2022 00:49:59 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:06:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0ca4fabca59ca0d617061b776745ff41fdc3968ce90dd2b9198717e0bae91d98`  
		Last Modified: Wed, 11 May 2022 01:05:03 GMT  
		Size: 52.5 MB (52476689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8d2e3c89e648f74d8cba2be942f53fbcdf53c845d8180c2c93199322a0573f`  
		Last Modified: Wed, 11 May 2022 02:30:00 GMT  
		Size: 5.1 MB (5065455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aff9f1fe546a28b9bdb7a85b87eaaa7c9c039d0e60a7372cdcc31f58842e25`  
		Last Modified: Wed, 11 May 2022 02:30:02 GMT  
		Size: 10.6 MB (10573055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bfe50f7f2db6acb117a778b84c53664ce16ba884ae8de0447fbea2a07acea5`  
		Last Modified: Wed, 11 May 2022 02:30:56 GMT  
		Size: 52.3 MB (52315350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05269c666a9b2a1d1fdb5711a7b6010c64b428265414acf3c08eb268ae396ac5`  
		Last Modified: Wed, 11 May 2022 02:32:56 GMT  
		Size: 174.8 MB (174771880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5428a315ecd0c8a70d04d945943553fbc7a7e7fa3d7442f13dcd4904134e3189
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282648739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab65236e4127946d75cb9c12e8d355a4cbf5d630dfae676857305028d4e283f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:21:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:21:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71423015d7b4f718e54ff1561cc06bb4c8357baedc23b49d25fe99cd4b0ae41`  
		Last Modified: Wed, 11 May 2022 03:46:39 GMT  
		Size: 4.9 MB (4924901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f92194faa0a66e5bd160b229941428f0b0387c6e313e4f1f903c678fbb17e`  
		Last Modified: Wed, 11 May 2022 03:46:41 GMT  
		Size: 10.2 MB (10217886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c410c75a05c2df4ed485cda22fd35206e0ea4b9fbc9f096b11ed5adc6f83fa1c`  
		Last Modified: Wed, 11 May 2022 03:47:32 GMT  
		Size: 50.3 MB (50329744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767978ffc99a492ddd06d37b888a093595a05ac353ceefb2cc01a1322f34164a`  
		Last Modified: Wed, 11 May 2022 03:49:16 GMT  
		Size: 167.0 MB (167042139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a0cb6d44c0e2d4852f3b991e467c858268e42e29b8d7f45864ec8845f738be1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313384938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29595d71037a1e217bfa27b64f859ca2dfac3ad4ae4bf11246bb9d78e115c4ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:25:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:25:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:26:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d3345afba43846f3e638752cce2f0d1d47b21cc667ba08b00db10767a4702`  
		Last Modified: Wed, 11 May 2022 01:35:45 GMT  
		Size: 4.9 MB (4938615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e267d6aa58f93a513352a3b46c7addbf9335d7d43bfa4f1df4026d21785181c`  
		Last Modified: Wed, 11 May 2022 01:35:46 GMT  
		Size: 10.7 MB (10656992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f647907d26b879e0d43f6f4f0807f01e4dbdc034edcecbc988f6033cf401becf`  
		Last Modified: Wed, 11 May 2022 01:36:07 GMT  
		Size: 54.7 MB (54672822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0b3e17bdee16cf8bf269a4474bf56713879991bf87ff3bd790aa96a6f00e3c`  
		Last Modified: Wed, 11 May 2022 01:36:46 GMT  
		Size: 189.5 MB (189482172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fa668c3f80c0d46cb4ec95408b63d37e2d9949a6aa47a5e778f2c9f7016b00ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327716434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d37ca9af771dde21e7f6ded4d0d90e4a34694b05c6229eafb4f26a14da93e0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:16 GMT
ADD file:2ecdc28ede565866b7302862c5e2a4b70a3afb165b383a4df315957be6dd754c in / 
# Sat, 28 May 2022 00:39:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:10:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:11:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:12:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9460ac70d7d688bab5f76bf5c30d1d8577c1fe0b74778427b0febf82ec246360`  
		Last Modified: Sat, 28 May 2022 00:46:11 GMT  
		Size: 56.0 MB (56008088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8e3a15723f23c48aaec99a47e8db8febb69c63c6c4fb228e79be0e24f60990`  
		Last Modified: Sat, 28 May 2022 01:21:17 GMT  
		Size: 5.1 MB (5080488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fef8149909e6cd1b5e9ec92e3e9fa99c4f56aa60aeca1fb6d09b707c41357`  
		Last Modified: Sat, 28 May 2022 01:21:19 GMT  
		Size: 11.0 MB (11033704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acada7e0f75318a771bbda23d86cd3ba06d286bbf27e121de75b94b6bebdc1`  
		Last Modified: Sat, 28 May 2022 01:21:41 GMT  
		Size: 55.9 MB (55914738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfbf2a1bfd265f905f70b523b09d7311f1bfc78b44afdd335967bfb8ab0fae7`  
		Last Modified: Sat, 28 May 2022 01:22:22 GMT  
		Size: 199.7 MB (199679416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d48c3cf014b26d82d82cd606159a862a875c681de0bc88009d33d19ce5c52714
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301036510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7185f5f5d23ade47430063a1219fb3effa542d90c27408e4494bb0ad137403`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:10:35 GMT
ADD file:bf0066890c02fe9254ebe22df9f29cfa14ff8023e297cd8ce14c32d423c81099 in / 
# Sat, 28 May 2022 01:10:40 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:54:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:55:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:56:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e3c10d3d838c43f5c37f26af81b379c8e9fd26b58bb2a30e2b137934e2266ef1`  
		Last Modified: Sat, 28 May 2022 01:20:51 GMT  
		Size: 53.3 MB (53272327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0960f5bc3793d07cc0d0910bedc52256987e77a953ca437c6dbc0ad21bbb6b3f`  
		Last Modified: Sat, 28 May 2022 02:24:16 GMT  
		Size: 4.9 MB (4912484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba3dabc5ac5e0b5c503a658e3366ba3e36e5989ca98f5b3c9993bee50d5cbd`  
		Last Modified: Sat, 28 May 2022 02:24:18 GMT  
		Size: 10.7 MB (10660152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca0affb9d083d5f8df62cc8c4cd9f2b3dcbf363568b23e7e693afdd8cf8fd70`  
		Last Modified: Sat, 28 May 2022 02:25:08 GMT  
		Size: 53.3 MB (53298286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74465f3d364c2b4fbb9e2fdab084a7ffa625effa298b4f09bd7c605a079451`  
		Last Modified: Sat, 28 May 2022 02:27:12 GMT  
		Size: 178.9 MB (178893261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ae0b3e8178b9604a167d023923ba65f41a6a74604f3dd0a71c527d1f4c6cbfb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330677702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87740c67a652f7b6440461c47137fff64302b5cceafa80e38a554a8de6c3e01b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:33:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:37:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:52:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab8b0050e0adc77a432c7431bddb52ffd7a7f6133ffec0b7f2766c951614fc6`  
		Last Modified: Wed, 11 May 2022 03:48:01 GMT  
		Size: 5.4 MB (5405221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d47d2b8f433338bdfaa5388d0c010792ba3e0bc820e40cd2d316a1b0b6aab1`  
		Last Modified: Wed, 11 May 2022 03:48:01 GMT  
		Size: 11.6 MB (11627779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093f433f2609e3f4f5695cf59234918a3e0d13ac7eedbe9323cdcd2acfb1ce52`  
		Last Modified: Wed, 11 May 2022 03:48:30 GMT  
		Size: 58.9 MB (58855572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bc4e97f9eb6c89e59961459cedf106242c7fb053a8a926e6d078080df1eae8`  
		Last Modified: Wed, 11 May 2022 03:49:21 GMT  
		Size: 196.0 MB (195952606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a68d5ed07e9d5d4c8acc85652f0426793985d7954c8e161f5b9fa4cf9bdfc4bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e47464ff7c6cc536741536324bf0c463cee2f2a4fd6cd87d9f06a5d2a340c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:39 GMT
ADD file:2aa6033cc58847736587260ccd8559fcc352cb0c91436fe6bc98ff1c0e457cc2 in / 
# Sat, 28 May 2022 00:42:42 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:23:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:23:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:24:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5729889737c79e488091d7133428cefb547531cac87f70671a7a8def5c83b822`  
		Last Modified: Sat, 28 May 2022 00:49:25 GMT  
		Size: 53.3 MB (53276622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8c82464c5aba6b429740f5e491eb99acd73a79a066d32206dece6dddf15135`  
		Last Modified: Sat, 28 May 2022 02:35:04 GMT  
		Size: 5.1 MB (5140603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2def663d7ef6cc773e576712a1ab885d906b1d5fd627ca2bb09120f3366d3140`  
		Last Modified: Sat, 28 May 2022 02:35:05 GMT  
		Size: 10.8 MB (10765425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec40ed3a753730ad01fd413a02ef67b6d923582dbd602a0bf67e6b1d6723c3c`  
		Last Modified: Sat, 28 May 2022 02:35:22 GMT  
		Size: 54.0 MB (54044714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3637100fde81b78ff49f562b690ff1949d3b8bc29335489d16920e60991bf0e`  
		Last Modified: Sat, 28 May 2022 02:35:50 GMT  
		Size: 172.8 MB (172758391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
