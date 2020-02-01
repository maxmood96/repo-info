## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:a3a0ba9083b348ae5d6faae3dc5932b0922e94aa26ecd92d086b18b25bf71c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9740d9e81601d10a3b719673ab1ecec875db92c22cb300725860eb868e32be73
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325431298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adbcf3b6aff7c8fc375ea6c6222ef7650025bcf6d393aeb19dee809091e2878`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705a4c4fd310b96bfb3d7928428e65f0d3f5bad0cd0bda1434aee1d89418468`  
		Last Modified: Sat, 28 Dec 2019 05:04:45 GMT  
		Size: 50.1 MB (50072671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c877b722db6f4d4297c21f07162d21fa6ac6f51d03360f75e24cfa3bcaefe57d`  
		Last Modified: Sat, 28 Dec 2019 05:05:38 GMT  
		Size: 214.8 MB (214840548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:372cdb5e282dedfe94d834079712289c5ed200313896e2f7ae260960f60f2f59
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309419129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffd07848d4b775187aba1e7d9ebe10019611a385e7b8e26bc880108dd584085`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:52:56 GMT
ADD file:003f4ef6ab6701f1cce91c9774e3c1d199cf937ba1641ab43af5ba549c235c21 in / 
# Sat, 28 Dec 2019 04:52:58 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:42:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:43:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:44:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:48:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e58f920d198d7f6350a4f92bed980e92dd883ddad00ee7e4667d621ad90766eb`  
		Last Modified: Sat, 28 Dec 2019 05:00:03 GMT  
		Size: 44.1 MB (44073023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e028558990d3fc06833bbd77b26478420ced119418f35d5c6adf417d49e254`  
		Last Modified: Sat, 28 Dec 2019 05:54:48 GMT  
		Size: 9.9 MB (9866285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3a77129a757a347e5e95b9d58eff15f43b2e070ac78e55de3747284d43fda8`  
		Last Modified: Sat, 28 Dec 2019 05:54:46 GMT  
		Size: 4.2 MB (4159250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83530215564a3e01544a5787501086758b38fb2736ea9531270218844819bb6`  
		Last Modified: Sat, 28 Dec 2019 05:55:11 GMT  
		Size: 48.3 MB (48282687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f23b8f07e8c84c1adf12c46777f410c1edb7cdbc4b029e69ecc02933e2b68b6`  
		Last Modified: Sat, 28 Dec 2019 05:56:15 GMT  
		Size: 203.0 MB (203037884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:92352b0aa66b9958bf7513617d88fb043637217fca576763cb53f7b4da26ffc5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297448257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e89f0e7a95f7d55a37243683fc1fc9830a032fb943158016fc9a37fe27fbe4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:00:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:04:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad0ae2287846b9d91f237a798b6ae550ff58e33efb804be1ca049f9fd7a480f`  
		Last Modified: Sat, 28 Dec 2019 07:11:24 GMT  
		Size: 46.4 MB (46399839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85007ed2d2e692ae9d2693b8e9e7d47b86b28377923b5051a85c235755bfdbe`  
		Last Modified: Sat, 28 Dec 2019 07:12:26 GMT  
		Size: 195.5 MB (195523369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb2dc614effb19c1d1b3d8ea18b782cdce7b3115bec49eb15e35a200079f639e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307267386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391da261309df9fd03435dbd3c3466280b22d59b75097028523e574924edbf8b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:32:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a82fc9ca296b095585ba7f3f6d83566428dbefcbfd284e242039aba97840b2`  
		Last Modified: Sat, 01 Feb 2020 17:39:40 GMT  
		Size: 48.0 MB (48024205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9a981e1269e4bf23132efb6a90365b5d82020f20a2ae5252c2d7c3b9ad7f48`  
		Last Modified: Sat, 01 Feb 2020 17:40:34 GMT  
		Size: 202.2 MB (202233524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fae62235c0dc73a3155c1d8f1234cf91ffd47d7bb0afb715c0f30744fe37b811
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333000320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0806bd3128432438a7469bad389a0904820e1d94b9966be6bb0415e820a664`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:f348ed8c5f7efee9f7e88d9a9bd1d57bca1bf445d486996cb6168da85c0bd43b in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:38:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:38:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:39:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:410821d7ff8b427b8dfb93dcf31b1836a617f5c09be71f83a16ef2c5946ee700`  
		Last Modified: Sat, 28 Dec 2019 04:47:20 GMT  
		Size: 46.1 MB (46100094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeaedfad53e910bdc66ac7862f5f3947575aad9685d5feea1b7c59abce08f95`  
		Last Modified: Sat, 28 Dec 2019 05:47:05 GMT  
		Size: 10.8 MB (10817785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25ac55b31a6a0657f064091eb17ba42f3d06984c79ad2029702e0e6abfcff01`  
		Last Modified: Sat, 28 Dec 2019 05:47:03 GMT  
		Size: 4.6 MB (4561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e73a3cb511b1de4f269d1d6cb6912275c54f471028cbb55c137b8c6497f755`  
		Last Modified: Sat, 28 Dec 2019 05:47:23 GMT  
		Size: 51.6 MB (51595587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6b40aae89aa5be2fd05bc653e286159f74af6500ce653f8920ad8129617ca4`  
		Last Modified: Sat, 28 Dec 2019 05:48:21 GMT  
		Size: 219.9 MB (219925419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2c418446bd0f5485870105b809bdbe2ecbbb645cf91c4b05a882cfd648dac1b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320514862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55c260fec84ca5065c834ddab2bb42f839dbccb8105e447294f8e84d5184e6a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:59 GMT
ADD file:0da9c5c67cad579be1a33f0f66df515de7f3ad992050c39cbaac281a01be41b3 in / 
# Sat, 28 Dec 2019 04:23:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:12:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:12:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:18:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32185d9fc6268c6a6d87060ea324482fa22129c0f06d0f35e1376ca27b5399a0`  
		Last Modified: Sat, 28 Dec 2019 04:32:44 GMT  
		Size: 45.7 MB (45652475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff48b558393a869138bac45b7d540a1536280a8a4a86a3d0ff0dcab238a6418`  
		Last Modified: Sat, 28 Dec 2019 07:25:43 GMT  
		Size: 10.0 MB (10002000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e334b7fa51f55c0f060923f801160877cc313f1e3e40cf76efd21d94691cd565`  
		Last Modified: Sat, 28 Dec 2019 07:25:41 GMT  
		Size: 4.3 MB (4296599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66ad4e8e64de1e6f91344e81581ac6cbc65550f1561a83333f8367c7c8cee56`  
		Last Modified: Sat, 28 Dec 2019 07:26:11 GMT  
		Size: 50.1 MB (50085193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5592ef7c614157f7f318f39c21b6e0f5fe36384bf13f916ee5a99939a08ef307`  
		Last Modified: Sat, 28 Dec 2019 07:27:19 GMT  
		Size: 210.5 MB (210478595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ba22b96865a458b560a8e3c1a63d4ed8fef43c27ab20dee7ec289ce7bf9d05ed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317273755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2a8c08bc8dc9e0fa586453eda76d346b498747caf06d583cc781e6b0a237d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:08 GMT
ADD file:b85ece7344f0ad0749b115e76a51a3b9f322e23bcc8c692cd2edff403ba8840e in / 
# Sat, 28 Dec 2019 04:43:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:49:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:52:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5bf261872a9b22035011c2bf77259c73389d0d5786e4b43bee1df89b5dfada2f`  
		Last Modified: Sat, 28 Dec 2019 04:46:24 GMT  
		Size: 45.2 MB (45241644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc7bfba26bbc482688409940aa0ec283a70804eb1cc6d540e0643c19909078`  
		Last Modified: Sat, 28 Dec 2019 05:54:58 GMT  
		Size: 10.3 MB (10323981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2623665c6d27c8c2e9ab44efeae2139d495077f86d1be219a93c300bef788036`  
		Last Modified: Sat, 28 Dec 2019 05:54:56 GMT  
		Size: 4.4 MB (4372209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61ffbab9b0222931cbb6d98ccd0bccb98581c65656a88a5dcb89c5f5d42872e`  
		Last Modified: Sat, 28 Dec 2019 05:55:10 GMT  
		Size: 50.5 MB (50497131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4749d4a88570d0d1e6a3bd6951a902c80f987da8de750bc91ec46359d75904`  
		Last Modified: Sat, 28 Dec 2019 05:55:40 GMT  
		Size: 206.8 MB (206838790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
