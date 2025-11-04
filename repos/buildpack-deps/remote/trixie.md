## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:ea9412709164f9888bb5dbbf61361b0ec10d281b4ebffb6f7ddd7e4fd06ab026
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:18e95df6e7195087f770e8d98e465a78ea4dadd68ca05dd6b5be5dcac1a73f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.6 MB (378613344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905c8bd319f10ef091416bac35e3597bb79f8b81dd926b015a0d1c8f61dfc363`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5bd8a8d262418bf22e705535ce38c6789dc72e319d76b30aafa5c331b6924`  
		Last Modified: Tue, 21 Oct 2025 10:24:40 GMT  
		Size: 235.9 MB (235927971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4607f2202cd48d4d21539489deb5e92c9c4c2b7f079f51ec334000cc7aeaf4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5faa218ce920ef1d9389315f3b6cc796b5c016d5df9447b61e260b824119f7`

```dockerfile
```

-	Layers:
	-	`sha256:6c132b4c484234aac9e526eb791df3aeb4c0c35696ee7d2685d56b7e2846df9c`  
		Last Modified: Tue, 21 Oct 2025 10:21:25 GMT  
		Size: 17.2 MB (17207191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f8f87d91ef8a53766f0b4fc456dd07cf1b808c03bf80ef8c1a6715ebc7ca2f`  
		Last Modified: Tue, 21 Oct 2025 10:21:26 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:53aed554c6fb3cc08d7304cf6959c8e226baf9a830be3191b2e58159c8f8e719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342777591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90de7df8cb7c180bdf9d3f810b82f53a13f5dd62d338df7ec813463372be555d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:51:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:13:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e91b819b99c2c8690acb5b01465ae84356bc40a50656db0ab817eb28337198`  
		Last Modified: Tue, 04 Nov 2025 02:51:11 GMT  
		Size: 24.3 MB (24343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6dc99f3137f9645c516987d6a868e6cc6233f36d0a984e9553daeb02a012e2`  
		Last Modified: Tue, 04 Nov 2025 02:52:04 GMT  
		Size: 65.3 MB (65324780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badeeffdf7a41911058577c2b4e7fc8a5587bc32f50c3dd26f5f734563205194`  
		Last Modified: Tue, 04 Nov 2025 04:14:36 GMT  
		Size: 205.7 MB (205660256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbd06b09e01d92c88651a2e5aa1a1a6465c846f72c790120acf888ede24e2176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16979923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4ebf68c4cc359d94cb42e9010e5427932fdc824e88d21d4417df6efb477d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6489652404518f275ce1f6cb5b12cc76fb90944928ef99ceb0cc8b577d34471a`  
		Last Modified: Tue, 04 Nov 2025 07:04:53 GMT  
		Size: 17.0 MB (16969389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcd8f1628e86fe04a4e6e2bfd995f37cf7ca20e2e9848502e50270317a2c3b7`  
		Last Modified: Tue, 04 Nov 2025 07:04:54 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ac1e134f0e620ef803700685c6ef798a8d9e073ffbfe911ac6f0c7b0ece7abcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381a3af234d63163123d651594b2094d8632edc2f2a7f37bc6fc3d9ebc332f5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44df842311a95b0b7342e7e98003a42713a82b0548bbc4622c6034066983fd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678f36a1315fca6dc09573043e8f35db273ac271659700a4cdde87772b45f41a`

```dockerfile
```

-	Layers:
	-	`sha256:477c1e763582ce8b38eecc2bade06be440b93830dfe6c8cf63eba101263e36a4`  
		Last Modified: Tue, 21 Oct 2025 07:21:07 GMT  
		Size: 17.0 MB (16975179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1eda9243061e2945b5686c11df40c772d6d8b432e88f54ffd542d7b3cd01c8b`  
		Last Modified: Tue, 21 Oct 2025 07:21:08 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e70e8fca2c99af07667a04870e0b5167a755ae19ae04775b6ad3d245897f4c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368328329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4027aadee511f63ef4bd1f278f7fe4eceec94c9aae0a1d470dc4277b42752a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a562920b68b5bfa0b3f27ea28aff7d335d506bbbf4d887f457e7e2f83f9e8af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17302082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b0a21c5020f6168c0526cef63c0b373f4786783f1f013900484bdd84f5cfe0`

```dockerfile
```

-	Layers:
	-	`sha256:3e305f96e23689f176dcbe2b6855a1fbba9b5ff31f08b9aa5ec8170438faf96c`  
		Last Modified: Tue, 21 Oct 2025 10:04:29 GMT  
		Size: 17.3 MB (17291485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf28d6edfabca67a799a6c77298d15d9fb1b2296799c1a7959f8fd049160b841`  
		Last Modified: Tue, 21 Oct 2025 10:04:30 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6d552f8a441977a702670c5bb0d12a33d899be3a49575705109eab19a1b8fd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387424725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4a05ad2f3fb33616a435cb16c184cb5c8abaa54b9e49a8250ad0f5b809c38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69000afa7c3cb020910048fc97eae943e68e19e9bd15554b79451ba4fe3841a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8917b516f30a8c2764aa6082f4a8be3607c1cb5ee4ba376fbeb146f75d91a9`

```dockerfile
```

-	Layers:
	-	`sha256:8b433b9fc629ed94bfe0d6ea3243c6fe144241c91a8686aecab6789e28584f49`  
		Last Modified: Tue, 21 Oct 2025 10:04:31 GMT  
		Size: 17.2 MB (17176784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a23e7cfe2330eb7eb402cb5b8a0816f86ca63052abdd6058e48a4d310cb2d`  
		Last Modified: Tue, 21 Oct 2025 10:04:32 GMT  
		Size: 10.5 KB (10478 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0a0ab60218a9132c672fd342289bb928f46e35f484f209d50c392e12403ac89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384221891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e0ae1310d79903a088e9cd4d97902a8f060d2b7acc4c703c7b581770307079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1158d6a4aeb5a6fa692be7c882dcb105573cbaf36dc12e9d4dc4ec5a7001509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69317dc0523e97168fc7d979165c4ce1d722490b0a3a69517f7e1aa416288d50`

```dockerfile
```

-	Layers:
	-	`sha256:20ddc7d3b51901a4622ab1ccd669382ec06eb079f55501c0890bbab53b244e5f`  
		Last Modified: Wed, 22 Oct 2025 01:21:23 GMT  
		Size: 17.2 MB (17192740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3128b62937a39e4c3f63212f08921465ff04cfbb78e7c6dd57720bd1c1099287`  
		Last Modified: Wed, 22 Oct 2025 01:21:24 GMT  
		Size: 10.5 KB (10542 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a4c0edc459647aa3ffb166aa1c38ffbda834a7d4af2528a46eb43559a6c94fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.2 MB (462216228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9df24c16690cf2d4201de0b999b3457a1b9b4041093571f6cd6016b61c3d1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:064d65c6ec3226273998a935cc98a9d7f4664440eafebf3b73d39194913d1a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63c00edc28268915e977bb93522173c7d1f9fb4a7c867e978c9887b9bcd0425`

```dockerfile
```

-	Layers:
	-	`sha256:59f23d54b27d2e675e1db0707f00257859e0291e7d982d948db1660a4605a82b`  
		Last Modified: Sun, 26 Oct 2025 13:20:53 GMT  
		Size: 17.3 MB (17263329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bf7de15fbbfccd4b4ea03709a298307b6b2d802f25a8ce0ff12cb86ec1770e`  
		Last Modified: Sun, 26 Oct 2025 13:20:54 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:caa41e3d9b4b228c0b4c37231bef4a469f3a69a4fa9e16a7f04f5db8a63e597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351225832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f1b0b5c344bab415c17442300045a7e67706933ca314f38537be9b63a1f9bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e3e4008a7ebff564ae432e603a03fc184b4d044b132757c28e86ef8284be4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6521efabf955d0ecb7983e48487a7e0c0af90b950d79b33670e71daa1861615`

```dockerfile
```

-	Layers:
	-	`sha256:5d121247b1a2f3284c6fa94290af4fc165bd33bd1a4db73d074a7760a1dc9a54`  
		Last Modified: Wed, 22 Oct 2025 07:21:04 GMT  
		Size: 17.0 MB (16984424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d4a34de4b73392daf6097eea6b3f170c5c972315684108265432fd5b99ff13`  
		Last Modified: Wed, 22 Oct 2025 07:21:05 GMT  
		Size: 10.5 KB (10505 bytes)  
		MIME: application/vnd.in-toto+json
