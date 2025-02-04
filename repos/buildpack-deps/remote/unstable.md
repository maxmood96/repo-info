## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:ca5c70c080cd675536af1238e0aad23092ce4ef4d5579521e73da7d5a415c44d
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a89441871a4e4261cfd8f3db1076ca49748dc17d638a043d1c23c6a10c831e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378286862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec553f6acd4da30811d4a22121cf15fce8f4361e3e5bbe4ff4aae0487f625fa1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79a80f133f68fe6301288293c6c55d0abe1750139940f392c2541c7856dc954`  
		Last Modified: Tue, 04 Feb 2025 06:14:31 GMT  
		Size: 236.3 MB (236303634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef63815fc34fca45ace31b1a537fc01d787def667cd47e3f20bc2902cd988a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16918509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d95b29521e7e9a9cbfad7bd2bf2f0c60feb61981efab1c979b548d099c1d258`

```dockerfile
```

-	Layers:
	-	`sha256:abbd56d590bdbd61585fbf3c94dc21f612324f29bfcd68e78cdca9969520472f`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 16.9 MB (16908333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642f9f638d888a947630031a8911443c6dfc2339e5c8eee02b7f95a6e283e06e`  
		Last Modified: Tue, 04 Feb 2025 06:14:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

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

### `buildpack-deps:unstable` - unknown; unknown

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

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe578c1e871363d504bb8bab30736288c85647392e992202c6258e71e2f02462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327929744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c46e692bb0a4dcb234fa5110bc74dbf398d106e8bf1908c30f71f200c22f98`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795004ef2c293073508c69f28eb42c2d7b2f33f65dae4735b067629f5120204`  
		Last Modified: Tue, 14 Jan 2025 21:59:24 GMT  
		Size: 196.9 MB (196917118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e83811cfe7c760f9da87d6f1c5a150ea9a0dd21ade505b732fcdc8e7f0fc842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16669569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e59fd63dd1941542b79def3463a82f3d0501a82065c295a5f9fdcb14c59198`

```dockerfile
```

-	Layers:
	-	`sha256:73f47150d048eba6124064fe6305a459362e7b0775142ef28c837992ad3c09b0`  
		Last Modified: Tue, 14 Jan 2025 21:59:19 GMT  
		Size: 16.7 MB (16659333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eaa593dc99f801f19eba455556f9adb976b1822e75bc2877fe1dc8719fa838`  
		Last Modified: Tue, 14 Jan 2025 21:59:18 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
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

### `buildpack-deps:unstable` - unknown; unknown

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

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a346c8030f310001211274abb71e5c9c2279d293b63c22819e742b69a6c8532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 MB (386542332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877c96aa12281c5fd8180613fe153cb1b495b5ec73f62325e544bec45ba0ca20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e8429ab45660ec1d3a19982bbd0af3a786637fa24a29bbd4fe03f5d823ef2b`  
		Last Modified: Tue, 04 Feb 2025 06:15:15 GMT  
		Size: 240.1 MB (240070662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a856d0d673b5070a08ba0ef1a694cbcefafc2e847fe62a0db8908c9a890af238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc2715ad9648f547ef50c6f946121d126d9bb8ea48f75afe0d30f539576721`

```dockerfile
```

-	Layers:
	-	`sha256:7228efcf52a85711aae46c80cce5e57101b9b21148249ea6e908d113190a5814`  
		Last Modified: Tue, 04 Feb 2025 06:15:10 GMT  
		Size: 16.9 MB (16877179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4bb2dea9acf4e5f3939bebdc437405c35beb7e0d1876c48b51faed87418e36`  
		Last Modified: Tue, 04 Feb 2025 06:15:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c3af075a6bb84a32799c35580e83b5601f890c8d940db050505b4dc6c8a93321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360106862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969cf85422af15790fa0a4564ead6c8e64cd05059f896b02da84563dda047911`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de884e734576434f49639f4eac10e8ea4a8319859bf9f4ddab2b2535f94676`  
		Last Modified: Wed, 15 Jan 2025 18:07:13 GMT  
		Size: 219.4 MB (219401117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98d12704efad8167ae328c80f2b65f7537104b8eb6d65dcb91e8169be51a56ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f78aef405075ee21b5576e2cd9614944b32c443a23c800108a83b0b40e8263`

```dockerfile
```

-	Layers:
	-	`sha256:be2f46aad2ab5b0965a4dcc567ad80fe2f0180465992cbaf83183ad959cc15fe`  
		Last Modified: Wed, 15 Jan 2025 18:06:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

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
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
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

### `buildpack-deps:unstable` - unknown; unknown

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

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:37883c273ffcc4973cc52a84c4d91de0ba98e0e20fcccc5b4252f0370c772a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.3 MB (461345047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fc19dfc28296f054db85a666137c640afc4b33830762a41a845a6d6537fa56`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8fd872592cd59f544fed4df0eb73d6e2bcb134c250417be481a247576f572a63`  
		Last Modified: Tue, 14 Jan 2025 01:36:16 GMT  
		Size: 46.9 MB (46920939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f27f58bcdcb67681cc1a3f5317eea016beaa7c816e5c8b7d9d6410796b02d1`  
		Last Modified: Tue, 14 Jan 2025 14:29:46 GMT  
		Size: 25.4 MB (25411216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f15fff232ce9f2af98fb869b50c765042c46743ad5b2b938ac709c0c4a741`  
		Last Modified: Tue, 14 Jan 2025 20:39:05 GMT  
		Size: 66.5 MB (66538901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb496ce6b35c9b8049f042066fecf7bcc9dce24b556abeb71403e67dc7dacf3d`  
		Last Modified: Wed, 15 Jan 2025 02:40:21 GMT  
		Size: 322.5 MB (322473991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87f382daf5c81aaa7170faf47a769edba023e073cda25b34edee13a36ff07d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16943460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b80f95bd2e955310a7cab1afe139310fa13e7af43dea9601b195ea8374604f`

```dockerfile
```

-	Layers:
	-	`sha256:30a9f42b2b53a816ec8cc31ec13510aa5c042e48efbb2921bf89d32a05ddeac6`  
		Last Modified: Wed, 15 Jan 2025 02:39:36 GMT  
		Size: 16.9 MB (16933252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eda4e14c456fe38754a22519fdadfab2af03eae0d659d1ca1322321ea4364c4`  
		Last Modified: Wed, 15 Jan 2025 02:39:33 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

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

### `buildpack-deps:unstable` - unknown; unknown

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
