## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:b6112899295bc4ee493ef3e21ee6ef732d267ed29af52121df1810f1838d1093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9af39729d3d63f5797c785605e9c26effbfb09444ef91f5bd0099e5827edd880
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.9 MB (406868171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7f2e7a9355bb02a5478b27f15892dda84f9277790d6bf142f99d5982080d53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:12 GMT
ADD file:355a5f56bf0136597bcd90b01ff73fc517b6bf7e76f45b65bf1af1136f434462 in / 
# Tue, 31 Aug 2021 01:21:12 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:03:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 03:03:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:05:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25907b3add375d4f44a3bf4bfc3544b51ff9f4a23fe8c186f3b20e54b37d19ae`  
		Last Modified: Tue, 31 Aug 2021 01:22:53 GMT  
		Size: 30.6 MB (30602781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ef40c83a42d65ce37ce8bc08e06a0c4b994512527cad13196aca51586d9bd7`  
		Last Modified: Tue, 31 Aug 2021 03:14:51 GMT  
		Size: 3.7 MB (3692694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a871edcbb988433606f5a8d03efc8f0d9d49a4cd78a5d506401ec3b7854a2162`  
		Last Modified: Tue, 31 Aug 2021 03:14:51 GMT  
		Size: 3.6 MB (3552016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59778cb761facf0aaa7ff7cab370d47bdee8a1c0764186ec8286f50fb911a78b`  
		Last Modified: Tue, 31 Aug 2021 03:15:08 GMT  
		Size: 38.1 MB (38114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffa26f12ed647c5e1c9898915298f9e7389c733e2825bad35dac65a6b529755`  
		Last Modified: Tue, 31 Aug 2021 03:16:00 GMT  
		Size: 330.9 MB (330905785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b4cd810e63cec40720081b46d9f7d51f6879f979f24a21782c183d6cdf2533d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.3 MB (371327940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea1b0d70c3fe313e6e52e4f870b7ec6ddf510caa3a0accad930efba05e6b01b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:42 GMT
ADD file:0abcd0c1c6aecb3d5af2aa5d9c631949d716076e338faccdd7802906b4979bd6 in / 
# Tue, 31 Aug 2021 01:41:43 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:21:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:22:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 03:22:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:24:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be5e7fb59932c05a5acf0221847ae12179d4f81037fdeb44f8c408bc27ec1511`  
		Last Modified: Tue, 31 Aug 2021 01:46:11 GMT  
		Size: 27.3 MB (27313903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558c8f5e7395b48e26211a363f2c66ea0e729fa5f4ce1e980a22a70c47eacbf1`  
		Last Modified: Tue, 31 Aug 2021 03:40:47 GMT  
		Size: 3.4 MB (3438915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30125ee4f15b1f56a8279e5c1f488ef77c51231b62f4da3cb1a03b8a32fdae7`  
		Last Modified: Tue, 31 Aug 2021 03:40:46 GMT  
		Size: 3.7 MB (3742231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01de5d75b44b35b6f46117f4d1484f24b516edeed132dc1815d6a78fb0cbbd6`  
		Last Modified: Tue, 31 Aug 2021 03:41:28 GMT  
		Size: 40.3 MB (40317890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c3e4e41e25d781afd762c7e0519095f1075b1d9504f209328e2b477700b75`  
		Last Modified: Tue, 31 Aug 2021 03:44:30 GMT  
		Size: 296.5 MB (296515001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9fba45e42da203add658a83d947b8063b6e3e8821e9d87f2735a0e7c94861c62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399490006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d91834fc28eab00910a8bc6ab02bf69640dc79fd4c237189ec0b270e505a452`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:02 GMT
ADD file:ed3a8c55fbedc627dd5d33aecf52df10becbd9bd492f7c3f4f0a710b15629618 in / 
# Tue, 31 Aug 2021 01:41:03 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:13:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:13:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:14:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:835dcfefc46e2b5551a40002ffed802b6b70970071e61e3f9dce0dd0404c2a12`  
		Last Modified: Tue, 31 Aug 2021 01:43:19 GMT  
		Size: 29.0 MB (29033527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff76d237fe2a405ec5c0175da7117764a3725e495a5280fa68824281d0209f48`  
		Last Modified: Tue, 31 Aug 2021 02:21:58 GMT  
		Size: 3.7 MB (3677477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cd7eb9f3f8f76c354e0777c1e299b4979c519af36ee25c5a4b5176d14c93b`  
		Last Modified: Tue, 31 Aug 2021 02:21:58 GMT  
		Size: 3.5 MB (3533509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f0c095fc735f206fea57d94ba168122a4d321e4718f54f2db7b3f7c503ed6`  
		Last Modified: Tue, 31 Aug 2021 02:22:17 GMT  
		Size: 38.1 MB (38076803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feef883879fbaff65f9ee52b7386798fbbe6f94a0b6031c782a0345fbb93d11`  
		Last Modified: Tue, 31 Aug 2021 02:23:17 GMT  
		Size: 325.2 MB (325168690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2be72be9ca82b6475c433d3069b67ee4c9d76f0bf162b5d92392859509e87877
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.1 MB (413058139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef497b78fbb6c17ea0698512be7ab72912b9c4103be39f07db90a3ade98dd07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:11:28 GMT
ADD file:776487dfd6a31c5a5d57d6924dd11136cb94d2e661eb085c76b14213c2220e3f in / 
# Tue, 31 Aug 2021 02:11:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 04:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 04:21:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 04:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 04:42:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f23233eca55841e558566a0a689d1261b17a023a5d0ed1e0ee267da33ff84a9`  
		Last Modified: Tue, 31 Aug 2021 02:15:11 GMT  
		Size: 36.1 MB (36055099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10a1f2d8a9c3bf4f6060f088986f3f74fbf50acda4d6016dfd6d1115fbf3a9d`  
		Last Modified: Tue, 31 Aug 2021 05:27:38 GMT  
		Size: 4.1 MB (4096829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd26809db5804495bc5bf81be1fbeae7b7a82215d30ff3e0c59d3353cc857206`  
		Last Modified: Tue, 31 Aug 2021 05:27:21 GMT  
		Size: 4.2 MB (4241626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671fe0a2b7c06f1e3c899f5ad9e8b89dbbef68ba1f5bc446f05beaeca064dd31`  
		Last Modified: Tue, 31 Aug 2021 05:29:18 GMT  
		Size: 42.6 MB (42605912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9257fa229b5f286c331fe7b926deef3aee7709c3b87ae22f5cd31d4efc1765`  
		Last Modified: Tue, 31 Aug 2021 05:33:16 GMT  
		Size: 326.1 MB (326058673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e8938656e5921a5d321c930f895539216d4881311214c803e2643503210f917c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267418888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccfa4b5ab59d8bd311ab4a7f824737ab812260d9622df726a8bf3f0eecd481`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:19:36 GMT
ADD file:84d3daa77b3c4590ccb1b2c1bdfa7b2ea2629a8e289c7e0df33678a72ef40f4c in / 
# Tue, 31 Aug 2021 01:19:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:16:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:20:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:26:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2027d80189558886be09b6f8194607cd27258802c79f3c3f228e92404c40c304`  
		Last Modified: Tue, 31 Aug 2021 01:35:47 GMT  
		Size: 27.2 MB (27192169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccb43db8246e726e33f90f4887b26c5c6e5c0eb9b7c4fd223c18539a9963369`  
		Last Modified: Tue, 31 Aug 2021 02:53:01 GMT  
		Size: 3.5 MB (3483280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a66489e611edd2a918d67c7aa380888b297b1b1170487f8cf4d412010e9da74`  
		Last Modified: Tue, 31 Aug 2021 02:53:00 GMT  
		Size: 3.8 MB (3803155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a8d532c190bc5429a7b1a5b15e55c1c120cd8fd520ce5adcdeacadde8c6cb`  
		Last Modified: Tue, 31 Aug 2021 02:55:01 GMT  
		Size: 40.7 MB (40741042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fcfc294837d6a343623ab80428c480526c29b2bb2550c72deb28922f97489f`  
		Last Modified: Tue, 31 Aug 2021 03:00:51 GMT  
		Size: 192.2 MB (192199242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2813c9e36e8aa79b52e8baaa49202e6b8118da28adf2c05c0474ee676685cc4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370398338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c30fa68204d8cf8bba78b5f70b8a1b3fe9b5adefe038d919dc178471b101048`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:54 GMT
ADD file:4748ab039bb7c33cbda2bba944346ecf2e0e6238971d842acc53ec7e8c77df92 in / 
# Tue, 31 Aug 2021 01:42:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:39:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2abd65908848180c8f2b1a3f2a6493d9c7c22253fc30bc557fce0bbf12327e7`  
		Last Modified: Tue, 31 Aug 2021 01:44:45 GMT  
		Size: 31.3 MB (31308069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f61cb11476011700fc2feeb76881a7eeceb9638e97fa4c33603d64dab544155`  
		Last Modified: Tue, 31 Aug 2021 02:47:40 GMT  
		Size: 4.0 MB (3950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7802bd74770db74806622bc0f14aa9cc4666241c5b47c5aee05c1b85aa17ebe5`  
		Last Modified: Tue, 31 Aug 2021 02:47:40 GMT  
		Size: 4.0 MB (3962603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7e8b1ada6b39a4ab9001051926a2b823d061ce3d31ae907a24efa8fa9961ec`  
		Last Modified: Tue, 31 Aug 2021 02:47:54 GMT  
		Size: 38.9 MB (38858118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62018211b9b26fc8460e4b465948a6eecc369f5b26a1014a1453ed9a8ac2ed7c`  
		Last Modified: Tue, 31 Aug 2021 02:48:36 GMT  
		Size: 292.3 MB (292319458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
