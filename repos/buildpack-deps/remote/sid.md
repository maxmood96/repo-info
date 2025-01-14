## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:8dd6ae245603735d85493dc5b3c4e9b7dbe13dc0ef1bb0b39f910e9ac1fb2a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6674aff63cd83913768abd5426e40cb70b3c5172c84504ee8f8d3bf835b7b258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377612953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a696400049506209a4140e5a7b3cab9494580f72a7272c1ef1986e5a3c8be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76be34fccf5c64699db16068e9e561c466873ad6fc8da852c8c21801ed35861d`  
		Last Modified: Tue, 14 Jan 2025 01:33:25 GMT  
		Size: 48.4 MB (48375138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81659ab3e6cea3ecbc9d772f851c94ca5f88bde45b2b1d558924da5b4ef5f256`  
		Last Modified: Tue, 14 Jan 2025 21:00:09 GMT  
		Size: 26.0 MB (26032098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3ae95ad3a1621d0b6af5d5c8679891f7f4cbcca866d15b1c931112693f34f4`  
		Last Modified: Tue, 14 Jan 2025 03:18:18 GMT  
		Size: 67.5 MB (67502458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ad06a04e7c3f8633bc27b18748cb78c992d2b5d0a7cf0e3ea1f4eadaf6f239`  
		Last Modified: Tue, 14 Jan 2025 04:17:33 GMT  
		Size: 235.7 MB (235703259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:caf6c9c91d3f513516f0393e04a321613aa3ae8164b67beb5eef50922b24c666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16900785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765982bd1f7ad833d745e6240902d6f10c9211aac356364245a3ddf9439ffa27`

```dockerfile
```

-	Layers:
	-	`sha256:f2cc20e84ee77dcdbb62c5b30f2da2e026dacda4187b5a0bddba3fab08f676ee`  
		Last Modified: Tue, 14 Jan 2025 04:17:28 GMT  
		Size: 16.9 MB (16890609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080deff27442fe303528bbf4f5445cc496b6283acc3dd3bf76db329f2f205bf4`  
		Last Modified: Tue, 14 Jan 2025 04:17:28 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:699b99eabae12edb11c54cb0905cfb629084da59050e2df55e88835ff6c1bca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342823897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f7864307f3823165162299134b9b48e91759c438db2ec1f2dfffd19d424c69`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d52a976a3fd7f28c8f846fa169d38eb4f52aab56f9ee1cb5fbdf7c3d31fa88d`  
		Last Modified: Tue, 14 Jan 2025 01:33:50 GMT  
		Size: 46.5 MB (46532542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f95931378232e134e2433bb5ceaf5ca525339c23b43efde26fa179c793eec5`  
		Last Modified: Tue, 14 Jan 2025 06:09:14 GMT  
		Size: 24.7 MB (24730945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7964c97d01715538ed3e44479e82eb334202df2c205477a9386994f1307ee2`  
		Last Modified: Tue, 14 Jan 2025 09:33:19 GMT  
		Size: 65.1 MB (65059813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ff809d7bd4efa5fcd6aba8a237a7e280cd368e5767f0ba332741cf9c73f312`  
		Last Modified: Tue, 14 Jan 2025 11:01:13 GMT  
		Size: 206.5 MB (206500597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:724932cdfc958089a4e8658e98216fe95165a7268770d53f4ce339c40c6d7677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16667825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cba05f05509bf9f78385bca2ce27fd3c9f77634a1b42b16e1f6b7ad13a9646`

```dockerfile
```

-	Layers:
	-	`sha256:680904d52e7c60d083f9b5d92818acfeb54ba518a424d6cf023933c792d193c8`  
		Last Modified: Tue, 14 Jan 2025 11:01:09 GMT  
		Size: 16.7 MB (16657590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c69f512f44f0dfc7324a646cb561008647579b4ac3c62a510275c1c2a032c39`  
		Last Modified: Tue, 14 Jan 2025 11:01:08 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f25d04dde3a062259417b55543826698a46ae0abf2196db469ba065c0b3baa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323228858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa9de5b107250b490e04108ed25422f7e1d02916e33f39f1cc1bc4c42153a2b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd381bc5446358c906dd1f7ac3878d03bb1e1267963891069c3e6e2c97919218`  
		Last Modified: Tue, 24 Dec 2024 21:35:32 GMT  
		Size: 46.8 MB (46763305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419ccba1fe0df7cd0c879e1f8261dab91d1fe412b8df835212e60f95b90dbb7`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 19.6 MB (19608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367601bc4f065e38e007f59c54dfa0b3ad1eb3805f4c77d1ffe0c358844eeb5f`  
		Last Modified: Thu, 26 Dec 2024 10:53:24 GMT  
		Size: 62.3 MB (62298046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669825bab5af4aefbb346694300a3ae158cc74fa3a2a5fe1bdc47d76463dd57c`  
		Last Modified: Wed, 25 Dec 2024 15:50:30 GMT  
		Size: 194.6 MB (194558558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e00ea1c3b619def4a5af35a9a0191d4a4cbc2a5d1bdcf9e19ff8fd51449e348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e5c1c2ba1bb2c159bc65bb44ebc4aa59ffd49a43cb4dcb978d07230f02a4cb`

```dockerfile
```

-	Layers:
	-	`sha256:61cb8fcbea9962f7b30637d4f2a09eed0898e7b8f48e852dc5b0114a637d4703`  
		Last Modified: Wed, 25 Dec 2024 15:50:26 GMT  
		Size: 16.7 MB (16674208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e6d5446d5759f8441354a28e02b1e9f28f692645afb5601d32181688d523388`  
		Last Modified: Thu, 26 Dec 2024 10:53:43 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:789f10d38342832bf75ef3e2b9ee9f29c017fac09a6f868925fe21d87a81f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372546196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e83d3f56d50bf5b5f068663d981200a5154d5a23a3d0c7bb6402edad1f5f64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 20:57:23 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68415822cccaa14224085f576cbd5da670da2f1a5ddec7d638f697742f5d0fdd`  
		Last Modified: Tue, 14 Jan 2025 17:12:06 GMT  
		Size: 230.8 MB (230824036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d60646ee171c4bba05f9cc204056ad1c63baeeab442bfdb1f4eab411b29c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc196fdb5c8549d2f62aff178e0847779860dbadc42b2b180f89b418ce37f93e`

```dockerfile
```

-	Layers:
	-	`sha256:6d0948f13d2062aca9845321a479880fb218c0b6ff7f1b94ac1794b6ff823c72`  
		Last Modified: Tue, 14 Jan 2025 17:12:02 GMT  
		Size: 17.0 MB (16977645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d591e35d33d3cfcf7cf730fcc9b68431bce541892eea719c801528f64c8f264`  
		Last Modified: Tue, 14 Jan 2025 17:12:01 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d6376761d504a15f057f4c5638b100adeb8c05e0afae3fcfb0dc61a92605f851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386384329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe2673dac7427064fd939310e30562be3d24b9fe3ae03cbb4a1de3706adb1c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1e4243a6e921bf817bc744dbf559de39acec531c69436c119d566f9645bf931`  
		Last Modified: Tue, 14 Jan 2025 20:38:41 GMT  
		Size: 49.8 MB (49778367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499f1145672c6dc66a0a48bab855b0052609dea7a87335a024adaf65cda0b10`  
		Last Modified: Tue, 14 Jan 2025 02:17:21 GMT  
		Size: 27.2 MB (27178007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8346a14ac4c6ebb8fcd6102079a994f8803f83fade3d0db9f898c6c81c8d66e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:13 GMT  
		Size: 69.5 MB (69467971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5af8110f7bdc4503fa2a7dc7e0e4eab9c3735d921567fc32f913ffd1b1b410`  
		Last Modified: Tue, 14 Jan 2025 04:17:12 GMT  
		Size: 240.0 MB (239959984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7234546c0c15b0045a073e59ac992bfee54dc7dd95a0d8b2c712f77a6b6c01c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16869609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675dfa257d99462b53ad5df040ecc293a4844ffa31546a51e733dca82299338b`

```dockerfile
```

-	Layers:
	-	`sha256:c5433c17fe81c2e0bbcdf68fd9d2c5357e0c307ec482e6265dba86e6f2d56b6a`  
		Last Modified: Tue, 14 Jan 2025 04:17:07 GMT  
		Size: 16.9 MB (16859456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a405bc5694346e5da06a3d2913538867b7b111d93009923dbe3a1de50581433`  
		Last Modified: Tue, 14 Jan 2025 04:17:07 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:963d82c26c47eb528c1d100ce465f84073f1a12f5502b284ab46a6063656f7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353770738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cf8f4b54574bd22ddcf6857f562bfc0762f7e6d875ee75e7ebb3415b081349`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2225e4bf9a501ecd52da3f4301136a4a3ac3273d704acaffdf95ff67153847e7`  
		Last Modified: Tue, 24 Dec 2024 21:33:59 GMT  
		Size: 51.8 MB (51771333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315cddf1f38d3ec912dd995fc72b7c70105918274b7bd71b5f66a9e8789a52c`  
		Last Modified: Mon, 06 Jan 2025 21:30:30 GMT  
		Size: 21.7 MB (21740832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bff240cec674232066373df9095fc00a6e03c4199156cd01f197c25fb6340c`  
		Last Modified: Wed, 25 Dec 2024 19:18:25 GMT  
		Size: 66.1 MB (66117357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd17b1049dc80f74a754eadd3746cfb9350b54724e825429e89ad275a1e9eb0`  
		Last Modified: Mon, 06 Jan 2025 18:31:31 GMT  
		Size: 214.1 MB (214141216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfbf4256549514c3ee821f5b48e02c78870f14d5456c13711c2511f0656efb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6fbd77d9a581bb4ce48719a867bd1ff2f46f92f9d713ca9cfb4878e3f377e0`

```dockerfile
```

-	Layers:
	-	`sha256:1799c7a181805f40cd208eee3f299fb55da335b23077338fda96742d9f4198f1`  
		Last Modified: Thu, 26 Dec 2024 10:53:41 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f945636514ae3362ca71164884853f2f404b1119ca45926602f12d477155a9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0546df0594a9cf5437bf0c515631731c6d736876e68e9daaf7b025bc56efdd46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 22:21:56 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943e22d3036deb30248e5634a993ff72c73507d02437a5bb09280b60bf18d6a`  
		Last Modified: Tue, 14 Jan 2025 13:04:19 GMT  
		Size: 231.8 MB (231751317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f65afdda5fbd62f678db83abfa2fe8e77dda067ff81471cd5b968084e06b0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16889169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ee6c8a1fa836d956d9ca48a65ac8f826a5d616d3bd16b7c2e016175f840e92`

```dockerfile
```

-	Layers:
	-	`sha256:2fce16de76b13f416770a657209c2106c50c3ec4ed409e55241d96278276993d`  
		Last Modified: Tue, 14 Jan 2025 13:04:14 GMT  
		Size: 16.9 MB (16878961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b4b42020474e39ceb70591d326ad42b7fd3699657c3881062386d87d8f34a3`  
		Last Modified: Tue, 14 Jan 2025 13:04:13 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b62037a1072a5493b0806b2a40083efab88c113730b7224737967891488d4838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.5 MB (456452555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142a3b0445696930eb25b8c778bb03541260e32c1e43e395347b63316ec8736e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9bbab72f01dce27644d4f039f493ac5e6e54ff93d5cddb115f95af7c7ff7d`  
		Last Modified: Mon, 06 Jan 2025 20:30:32 GMT  
		Size: 66.2 MB (66171360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54187c1e7b21de5b4cd18d27400647f4fdf2cb2ef2acc86a335258b7e6a877c1`  
		Last Modified: Wed, 25 Dec 2024 10:49:18 GMT  
		Size: 318.7 MB (318739937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:68dc09db9129d24f164526c9c74706cac222ede2349ca25f774adece6924fd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16960145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a0b8f28ea33804fa8dff20e345656aefcfc11e14b7e86bbf09bf0e5270cb39`

```dockerfile
```

-	Layers:
	-	`sha256:9089f3524de6e9c5ee01095eb8f7378fa6116de0039f2caf84500f7a3c66c04f`  
		Last Modified: Wed, 25 Dec 2024 00:34:10 GMT  
		Size: 16.9 MB (16949938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59c94f65a1124b3f9e715104ff580b87fe615fa7c8bbe79add536cc5e45d607`  
		Last Modified: Wed, 25 Dec 2024 00:34:07 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93ead5df32df5fda7821d7eea3245b3ad1fecf33ab58a7fbe75672128d2a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350769776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bf6ddec63e07aaf55bebcf801af659826e992e4b6344ef4f3fb7b0f56001f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98a334b3a419c858b25979b9c4fcf97a87431d5b5cddfa6c4c566454b23fcf62`  
		Last Modified: Tue, 14 Jan 2025 01:35:18 GMT  
		Size: 48.4 MB (48434824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c90ca5b141c789480c7eea03644a6f254edf6c95ed1e124a245a18b8c3cf`  
		Last Modified: Tue, 14 Jan 2025 05:00:30 GMT  
		Size: 27.2 MB (27196670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c226835589caa484a321d0762131f155a336675c8b326b2fb32917038d1fe871`  
		Last Modified: Tue, 14 Jan 2025 09:11:02 GMT  
		Size: 68.5 MB (68532734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ee3ebe99142809d95638070bf937a25f6487ab59250faa71ded6bbcd0dcf6`  
		Last Modified: Tue, 14 Jan 2025 11:17:51 GMT  
		Size: 206.6 MB (206605548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd84808ef735ca84f852e884ede3f5d30f494c30ebdfcfac6d4acb304edcaefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16682803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcba902ca02bdbd2fa325c971ad0d962569c31f8134d6bf80819cdd45ec97c3c`

```dockerfile
```

-	Layers:
	-	`sha256:33660ad64d7fe7f55455954a254a4ba36f59ffc22e0fc691fa83f9ce752069e9`  
		Last Modified: Tue, 14 Jan 2025 11:17:50 GMT  
		Size: 16.7 MB (16672627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c6b274d24546c7f80941c17f12b7dc21cf3a4af00aa222a43f2173c9504ed9`  
		Last Modified: Tue, 14 Jan 2025 11:17:48 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
