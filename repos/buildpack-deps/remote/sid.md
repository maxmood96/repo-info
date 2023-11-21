## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:58b74bc526cd9f6f23f82e61c8004905d6b8c04fb19b325eb2db721554379555
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
$ docker pull buildpack-deps@sha256:1bb57291cb27861203bc17e4848783362fb10ade1824898cedd562fe66191d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (380043568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca56d88a95176f72a814f1022fd7f67d6fbb49ed503b8db572dfe63c9647c6c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:58:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3978af1e166e57bdb05260799a7b1770bd65f02601552db72ffbe944a422d`  
		Last Modified: Tue, 21 Nov 2023 10:04:34 GMT  
		Size: 24.8 MB (24793981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae081620ae95b09fd1b9617c1f676d0d998479bc08e6bebee281d0bea30f3f7`  
		Last Modified: Tue, 21 Nov 2023 10:04:51 GMT  
		Size: 65.5 MB (65507860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97328c59445824f5934c3e7d34a23a0879a5318cdb254df42906aa0522cfef9d`  
		Last Modified: Tue, 21 Nov 2023 10:05:27 GMT  
		Size: 237.6 MB (237619459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fcf7edb8ce652541065efcbc0f507104b809f1e99b8353836e0713ff4525e41d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348901354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89ade2f919c3a4ff65a0eb3b9f73bc2ae64a6ba48b4f89ea808f2dfdaab921a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:01:33 GMT
ADD file:b1618939ac80f9d3256d12ed22ac3e37f61dc396e5370e7a4013561a073af181 in / 
# Tue, 21 Nov 2023 05:01:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:19:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:21:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:228b88d8d39e27fa3bddca63f14715a5dec3e5c3de7b5b5a892c00385ea38d2b`  
		Last Modified: Tue, 21 Nov 2023 05:05:36 GMT  
		Size: 47.2 MB (47196697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df76a43e2f790a0c0d3fd4795cae7a8d79b43803710d103b38936a70bbe216`  
		Last Modified: Tue, 21 Nov 2023 06:26:42 GMT  
		Size: 25.9 MB (25892928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8da3dad66ffd081a2a6a2a79c62c577b4c8f5b7751d2718f24e60791eae1e`  
		Last Modified: Tue, 21 Nov 2023 06:27:02 GMT  
		Size: 63.0 MB (63027803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4fcce692f91cb6588fc68ccf3c8e63e6e26a568c586b8fd8af47793481bd9`  
		Last Modified: Tue, 21 Nov 2023 06:27:42 GMT  
		Size: 212.8 MB (212783926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e988e2b761b7907248c3baec9d8b049bc00d14cf504d536fa5bd326741b3c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329762097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bf22b48f37312328eb7e982bbc9d1e2c935a9405231e9ac750dcc1fe1d4b3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b893a98c470e054f25c3d481469624db1f3da7ac9daea450c53b2a2143f696a`  
		Last Modified: Tue, 21 Nov 2023 14:18:01 GMT  
		Size: 199.2 MB (199248157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f225bbcadae8e6551be733c86ec70bdfbf01b19f0e7e455fa62e0abf26aa53b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.3 MB (371250495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd8802d413e16d8959c5b5ff9372558d845c6e8e17362f75316d30ceaeb7eb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:03:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19182edeea8364f6c86849824848525bb23ffaa624f5316c079717a211be36da`  
		Last Modified: Tue, 21 Nov 2023 08:09:28 GMT  
		Size: 229.0 MB (229024712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae76f8ad80b82b6fdffaa4931dc6daa3ca2c972c3b5b05f2cb4991fb4720e31c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 MB (388669349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96527636c4addf379e53b4ec348c7fe3db44767d72e6489bb2c45db3f96f34b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 13:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:53:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7af088639fa61079db294f16f91145938a488365f2aec8cef7a85da80c4b13b`  
		Last Modified: Wed, 01 Nov 2023 13:59:54 GMT  
		Size: 25.2 MB (25185750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34a1138df818473932216f10a656452bbeead89efc81870811003208908e138`  
		Last Modified: Wed, 01 Nov 2023 14:00:17 GMT  
		Size: 67.3 MB (67267247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4105a9010ad6b6eb2295fe9bd43b392d6a4b2314d5c52c4020f7645fcd5b3c26`  
		Last Modified: Wed, 01 Nov 2023 14:01:10 GMT  
		Size: 245.7 MB (245699866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b0323413cf5df00b4a8ccf599bb7c124213661346eb6d16ba91745f4dd5415a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356033125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b70ea1b2e9877847febdcc801fd42193ac425e09832ddb328ebe3cae140f4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:12:53 GMT
ADD file:9030cb9b65f8be61ec19318a90c95afaaac8943c61f5ee6b30b90d758a8b0964 in / 
# Tue, 21 Nov 2023 04:12:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:41:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f090d405a1df972a813ac2207398b0e5b36cca91650c17a34fb17616a3e7fe19`  
		Last Modified: Tue, 21 Nov 2023 04:23:59 GMT  
		Size: 49.3 MB (49341847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e9e1c518f951e1dc2742e209f1d1b2ba924d2068f93c7d8e386603f98f04d2`  
		Last Modified: Tue, 21 Nov 2023 13:04:52 GMT  
		Size: 26.1 MB (26077539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ae92ee0eea266534adac9439fab060820cf91e6c7180edcf62427764b9201d`  
		Last Modified: Tue, 21 Nov 2023 13:05:44 GMT  
		Size: 64.3 MB (64313449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997cc05cab3ea3168186a6de670c6ea265373255594781d5cd74941a10857db`  
		Last Modified: Tue, 21 Nov 2023 13:08:07 GMT  
		Size: 216.3 MB (216300290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1766ed0c020a64b0c0245a19f9ba7a951551f98147642a9acf6ede2115229dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393372396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e24823afdd39ee710bbbc971c39d0aa4ff7fb43aebaf6a79c893b045539c7d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:02:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b31909696ac928d37c89a4769a0d196f1f4641efdd73d46c6a365e9c76eea9b`  
		Last Modified: Tue, 21 Nov 2023 07:10:21 GMT  
		Size: 239.0 MB (239016768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cd9775eccbc9ffcd297a1818f606c97ed2ad5ca30801aac383fd3ff85ac44fab
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415648463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ff0980fc3f2e38808c31811962bbb2b3158891d22903ae44c81b2c9ab8eb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:02 GMT
ADD file:6edb177cc4c3fc7c02043410bba7fabbbaa23493a2e0444ac13e281f6fd7d209 in / 
# Tue, 21 Nov 2023 04:09:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:33:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:35:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:42:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9197643899c29fb1e411101ee2f4e677b44704d5c2c8ce98f7567cb7f7a6cf58`  
		Last Modified: Tue, 21 Nov 2023 04:12:00 GMT  
		Size: 48.2 MB (48206696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0617cf6ad3eec888f08f7b773880b515adb1cae0586b8aa6f4b5f40076079dd`  
		Last Modified: Tue, 21 Nov 2023 04:43:06 GMT  
		Size: 26.8 MB (26784568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e112439f28d2102590bea4e42209332ea3595b8c9789016a1e8b479e123bee`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 64.7 MB (64702623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b281221811c330e1fa4440fa0722c3b2f9601f5f9016ab7e7d8f32cdda28633`  
		Last Modified: Tue, 21 Nov 2023 04:49:49 GMT  
		Size: 276.0 MB (275954576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93fc2e94d1d3a26456ef129ab582ef7d63a767ab8762db8940202c77f1388df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355072174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc793a1658b88281067a4063d6ed988d648fdb13eb5611f6e42534971d82b3da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d423dea4ea04d9998b72e9dca146ee1f13e78ec50b02fa0de85998fc82032b`  
		Last Modified: Tue, 21 Nov 2023 06:18:48 GMT  
		Size: 211.3 MB (211321007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
