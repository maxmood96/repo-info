## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:e1d224d4a93ed782078dd8470aab56def4ccf4deb5864edb64e9939af3df655d
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
$ docker pull buildpack-deps@sha256:4cf68c882cee9b417142c8f85e20e26fcdb0fa83cc0f991801de65462df2f4cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344815719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f756652badfd81aa904ebea98fc74ac8af051853f59e0e07e17c01a6fe5fd60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:46:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:46:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 04:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:47:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a406365e2c651e77ea1d2dedd2c2fe7317552757dfc2701d2cdf6a578a51e`  
		Last Modified: Wed, 01 Mar 2023 04:52:19 GMT  
		Size: 9.1 MB (9063535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515af3674ccc4fa7b84288322c2d1250d4de5952aafb54a33baeaf74fb694632`  
		Last Modified: Wed, 01 Mar 2023 04:52:19 GMT  
		Size: 11.4 MB (11405848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4328fcba3826a509a956e5614c022c05ed89b4e718a69b607176d4a8f97f0e86`  
		Last Modified: Wed, 01 Mar 2023 04:52:36 GMT  
		Size: 64.2 MB (64156733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf5761bef1786d1a3043cfdd4502ded7b68eb76cddebebdfd5e61420f1ab445`  
		Last Modified: Wed, 01 Mar 2023 04:53:10 GMT  
		Size: 210.9 MB (210928317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cfab3ca8a8f26671e80ccdb59dd4ba9f96d324240fab5eca7fda5b7282e680d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313512864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98658392247eaba632e8d135986bbf3cb581ed4c064c7c09cc42508038e13052`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:01 GMT
ADD file:4fadb88d3ead8d91349c79d7e903bbb8f6130b292bda6cb8099131210a815bc1 in / 
# Wed, 01 Mar 2023 01:49:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:21:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:21:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03e1abdb2ebe924d64faf35eb6563891039999ec54a62f65419caf539ba6a88`  
		Last Modified: Wed, 01 Mar 2023 01:53:21 GMT  
		Size: 48.1 MB (48107781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d446d9cfc1201a906803d21a6e36423e22e9bebf24cf64bd16a4a3a73af61a2`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 8.5 MB (8514426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc22595c5f06cd6d232ff8a3594b9aadef31095cb355dffad2b48a861717bf`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 11.1 MB (11051502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0760e34b5fee30fa55ba71775caf6a3b2e755775ea03be4db0c03e5d83ff0a3`  
		Last Modified: Wed, 01 Mar 2023 02:26:32 GMT  
		Size: 61.6 MB (61563988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0bee41572d3fd2c79c2cec17ba9f302c4197090c7cd926637454ea269c1fcf`  
		Last Modified: Wed, 01 Mar 2023 02:27:08 GMT  
		Size: 184.3 MB (184275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4fd065ebb7280f186e201ef931745f11b0ed5709bb74ebfce845fa07383b77de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298924502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb866bf86688fd657c0d0bbb77f601dc7b5b740627aacc2b35cdb24985d07cd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:39 GMT
ADD file:2cc322ac43103c8e367e39beaccf285da593ce4935ec4b1c90ae321a43b7123b in / 
# Wed, 01 Mar 2023 01:58:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:37:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:37:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:38:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e5967747d4d88696bd5d5f37c0b5b8bcf8b29f3b448f6d1dd9623bdcc655965`  
		Last Modified: Wed, 01 Mar 2023 02:04:52 GMT  
		Size: 45.9 MB (45878967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00c059161524278c4c36c19bc9e15f881a76d35dfa7907d64e5368fa08cfabe`  
		Last Modified: Wed, 01 Mar 2023 03:11:27 GMT  
		Size: 8.2 MB (8158629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2cef807b62672343d701b6833953bd521a7ce41702624f45d2d796b0748e2`  
		Last Modified: Wed, 01 Mar 2023 03:11:27 GMT  
		Size: 10.7 MB (10687679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aec6c2a63ff15795fd7235464c074e62a01aab27b66c75e51aca4b22d1ec07`  
		Last Modified: Wed, 01 Mar 2023 03:11:48 GMT  
		Size: 59.3 MB (59272951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47368484dc827d2541150d970d099cbc827331cba4014efcecf477781757c153`  
		Last Modified: Wed, 01 Mar 2023 03:12:21 GMT  
		Size: 174.9 MB (174926276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:844c8028a9815c68e30fdb0e3c1284cdd82ca2e3b6d6c93da5ddd5c6fc929502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335903373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932509bb66171d164ed37159485c8587937293e2a8149266b757ba8858fe5483`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:52:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:53:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110847b2a04ab78caa763031ad2defabdaf9d626dbfcec71b215d35f0b70f09`  
		Last Modified: Wed, 01 Mar 2023 02:58:08 GMT  
		Size: 8.9 MB (8900926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd381966a1347f9482594ca89251700a2fc3c4cfc23300a89d68207091e90084`  
		Last Modified: Wed, 01 Mar 2023 02:58:08 GMT  
		Size: 11.4 MB (11371514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dade03fa0cf349d2c4310e97b9776862ea961b32865410ca43789d56b255550f`  
		Last Modified: Wed, 01 Mar 2023 02:58:24 GMT  
		Size: 64.0 MB (64013118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd468c1139187176cb306ea33f3fa3f4b68fed6a00e7d0835793454ce00e1b`  
		Last Modified: Wed, 01 Mar 2023 02:58:52 GMT  
		Size: 202.3 MB (202322476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:631c6b61580c0129c1a56f05b9a93618a0a1afdabbcf59f3a128367f86d855d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.2 MB (347248309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c7b891ef4ccee961ced21d3fe4461e8ea27d47b2529539f9c33b23fdbb62b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:14:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:14:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:15:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65b68a1e6101c58260f889183e2e061e123bbc07a479a4ee59fff5649daa51d`  
		Last Modified: Wed, 01 Mar 2023 02:26:18 GMT  
		Size: 9.3 MB (9251109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63437f1cf3bc2a6cddc930ecd9a659ccfbcce779ac90a9c50efc7e8c1f56b42`  
		Last Modified: Wed, 01 Mar 2023 02:26:17 GMT  
		Size: 11.8 MB (11808756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd353cc8e971b20a47938912dda14d6fec9624aa9880053413a451cb3bc0f60`  
		Last Modified: Wed, 01 Mar 2023 02:26:41 GMT  
		Size: 66.0 MB (66012422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b99a677370160cefe862644ca09270260b636f9de7ee445839ef305d8857f6`  
		Last Modified: Wed, 01 Mar 2023 02:27:28 GMT  
		Size: 209.9 MB (209861751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:47dc0fbb2a082ab8902bdd131ee988a5f0e00dcefd372fb7bfeea467c0c1ace6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321371150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb9a05e6abe2c06e4797caa146e7499b646b00ed39cde466eff314a31d0ee7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:11:29 GMT
ADD file:0cba93ebf4cf24adc0d2ab76ca2285ed3e4c1d07e2498a55a964f61a47d0f560 in / 
# Wed, 01 Mar 2023 02:11:34 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:25:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 14:27:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:32:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6fa2f96bfa02eb0ced41b1f356f7b6aa1c6dcd2de446f0e6931fb513751316f`  
		Last Modified: Wed, 01 Mar 2023 02:19:32 GMT  
		Size: 49.3 MB (49270629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d065d7ea1126da8c947e70a82de46ea4f5654122ed4491abeca140ff6e5c5865`  
		Last Modified: Wed, 01 Mar 2023 14:38:52 GMT  
		Size: 8.4 MB (8431807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9fdc617c60ef3cb7ebd08a285a7f5620969f1115a7d36b712df4a1d6a5a21`  
		Last Modified: Wed, 01 Mar 2023 14:38:52 GMT  
		Size: 11.2 MB (11153650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aa7dc7af7fb2bbb1d9ee43b715bd2063af972d33a79974539ff4b29aa3ad89`  
		Last Modified: Wed, 01 Mar 2023 14:39:42 GMT  
		Size: 63.0 MB (62993873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96576f9b714a0a396d90707c7026ab68f17a79237d0fca82751b6c6ff8f9c9ae`  
		Last Modified: Wed, 01 Mar 2023 14:41:44 GMT  
		Size: 189.5 MB (189521191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:270e720c1a0ba1d7fadc6591991b8d7f9984f5aea254d2191222f1caae76c910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358677337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4b45352ad5e080d3923b7fec61af29c23f2d69f6a6616fd50b10fd0c9e8385`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:54 GMT
ADD file:2c1195fd765d1da7082bf383b9c5ef0b244e5398006d53897d5ea40e919399f1 in / 
# Wed, 01 Mar 2023 04:47:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:31:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 05:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:34:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6800c47237e7f7a1e5340856e56ba98e2b69a475b2458bb2416fdb0582d8c28`  
		Last Modified: Wed, 01 Mar 2023 04:54:24 GMT  
		Size: 53.3 MB (53273011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff0fff502cf707b8386c45c579606a759f85d3b49c007814826ad27212fdf5`  
		Last Modified: Wed, 01 Mar 2023 05:41:08 GMT  
		Size: 9.7 MB (9652015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ef4d32b9b5d605909945396d9e13b86c238ff2ea6c800b63cef6d06dc2d6a3`  
		Last Modified: Wed, 01 Mar 2023 05:41:08 GMT  
		Size: 12.2 MB (12168382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf54311632074a960030227c6fca18a718af9b2631164c5c93529e814a5f50`  
		Last Modified: Wed, 01 Mar 2023 05:41:38 GMT  
		Size: 69.6 MB (69617831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48046f9759059f8abfcf3bf8b3ff28b67f3df1bd9cc3a2d31dcbee40947822d6`  
		Last Modified: Wed, 01 Mar 2023 05:42:40 GMT  
		Size: 214.0 MB (213966098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3a887968fe43226ca614e3bdfba591197b3593e08bde65a9a38a179bf5715812
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359929860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0617997a465ac3f99d967a05d654c18e959edee32e325b2b1dc07db26768495`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:40:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e7099a4ad88bc20a780df4c500b9445dc2cb39e8ac84d70a11e8903e5b6448`  
		Last Modified: Wed, 05 Oct 2022 03:40:39 GMT  
		Size: 237.9 MB (237914651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f36f7686751e847a8c69af8eba89a80c31e16ec89434ba40ebccec03984464e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313760190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22a70710ffc9aeb0b1ef9ecfdbb6a892cec5ccdd05e291bf44c01c504fb8cfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:50:42 GMT
ADD file:a35d410eeff51ff3b7d9c823bc5ba421ef11373fb29ee93e8256efcbcdcee908 in / 
# Wed, 01 Mar 2023 02:50:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:16:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 03:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:17:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e87143a56f85b3245b752ff94d616ef62e6372c0bcd9338b791267ea20f326`  
		Last Modified: Wed, 01 Mar 2023 02:55:04 GMT  
		Size: 47.6 MB (47629137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07cda735865838550e6455f8a76e842211afddfe8503e32aa744121e3435ae0`  
		Last Modified: Wed, 01 Mar 2023 03:23:06 GMT  
		Size: 8.7 MB (8700269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c406447e84cbeb09410da5fd14cb6601c6f124b564b303a89c89e53406f68863`  
		Last Modified: Wed, 01 Mar 2023 03:23:06 GMT  
		Size: 11.3 MB (11268803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b0879a47bff8d8b52a41d4dd0ceb2fa4313863026dfe04be33a743663128f8`  
		Last Modified: Wed, 01 Mar 2023 03:23:22 GMT  
		Size: 63.2 MB (63158949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a52b22ad7915c526a6a5a76890d098c9218f26db48004203de3a4630e03a54`  
		Last Modified: Wed, 01 Mar 2023 03:23:50 GMT  
		Size: 183.0 MB (183003032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
