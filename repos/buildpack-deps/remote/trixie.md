## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:f7fb20b09a5aaa4cb532be6e4b9d2c221c7cbe50fa40860cf837fde4d4ef3fee
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a401721455f7cd3d304c82125885a0365f806debe4f5c4e20b29ebd2ce4aaa71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389791406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a2b5eb137453ffece174060255969de79c2dcd483596381d3dee274173e5a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:02:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9875430b07abbca2f54b7947832f4fbb3cd6cfb30ed102b17e5c02219d905d`  
		Last Modified: Tue, 14 May 2024 03:09:19 GMT  
		Size: 246.6 MB (246638653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:691ee229ebdd7db704cf488c4c65b015fd3f148f57764064ed7606b957a5ebce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346012868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebb0b0a27c1ed169e50e11db9ea570a2455ab53a86840c80a761b5b602d6c78`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:23:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f566f5647f549844c3114f30c34180fdc2fbf60373db5f8568cf8640c08acfb`  
		Last Modified: Thu, 13 Jun 2024 01:28:43 GMT  
		Size: 214.8 MB (214818434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0e51af4938da7eae5a2731db67595e3a367250b460005520a5c6df3d91d6ad39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326769508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fba11ee4bacb01188d3fea61bdadf22c6249a1d10a60811df98d68e5f964e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:32:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a697d87d479ec6a0381ba0f5d19e355f93bc124e534f26d5e4a3258b33765`  
		Last Modified: Thu, 13 Jun 2024 01:38:35 GMT  
		Size: 201.3 MB (201277101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:74e90493e4b88de1d5f4bdab997cf68cff1a4a90235f148c421d9bd75ef85c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369961938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e7bbe62b186251ff6708bbd2dcc44927924de7a0dafbe9acc2dc7efd9d7cc9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:29:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb32f6cc55be585ddde214c0068112a7e2fe0d22795409319c853d4d70757db7`  
		Last Modified: Thu, 13 Jun 2024 01:34:32 GMT  
		Size: 232.3 MB (232319137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7c0e45319c38b72c46ba31ce9e0bbeefdbd528f76e5f7e4f552f1883669ae8ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383055527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf25b60e38dd88e48e389387f8596930523a213ba06cd0eed4ae16ab1cc782`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda544af678f150077336bae7b440115c498098fd52f36e0c9aef598688e21d3`  
		Last Modified: Thu, 13 Jun 2024 01:25:17 GMT  
		Size: 242.0 MB (241966732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:57378db7f4c23f08e44ed387abce25dc157946c5d278e939c617d90a81d6399a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359235322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfd1ac2444346fa5faa73fee8ec7880ec8123e80e7fbb5a18cada43e1446190`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:36:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd0490f57954354409d6530a9cee8fa6f67d1c87e7ad6f04857679d8210c2b`  
		Last Modified: Tue, 14 May 2024 11:50:30 GMT  
		Size: 217.7 MB (217662279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8a9fc4b0ddfa36db425e8b852ee1216cdcf85577a1b51f4cf6b073e9803d6b78
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403613644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b39bde83adcd03e2f6d7985f58e26d1b8dd832081a837d307ae4dcee6e70b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:09:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c804c1ff4e3c7dbd1fc56deb5f124b3b0c0ee135fad48f5777b22b5978eba636`  
		Last Modified: Tue, 14 May 2024 07:15:11 GMT  
		Size: 248.9 MB (248868485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f86256bb0174dc0a1bdb72c6c90ea174b8e42ca2656bf0a6327a79eb785cab83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371533960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbcab6a49e6679246b499f10a4946a4fc412b0bc67f4ceb3a5a6cbe6fe61599`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:26:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9cbe67e7bccd1433cf8a3d17879030af7f30729ba9616f025c0af6408214b7`  
		Last Modified: Tue, 14 May 2024 01:32:53 GMT  
		Size: 226.2 MB (226241254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
