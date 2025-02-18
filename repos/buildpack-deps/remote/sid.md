## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:f07cd52eeec40d81742aef51b44ba453fdb97d7c0248a48b94470b716610f32a
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
		Last Modified: Tue, 04 Feb 2025 07:09:27 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 12:01:09 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Wed, 05 Feb 2025 03:36:54 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79a80f133f68fe6301288293c6c55d0abe1750139940f392c2541c7856dc954`  
		Last Modified: Mon, 10 Feb 2025 09:02:19 GMT  
		Size: 236.3 MB (236303634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bc797efcc1bfb1580fc82fef2235b5ae298f3c1a39da7bc1e3284a089c152205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342450921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4454bda53f727cd002c420b50b5434bb0a09863c78197e6fa36bd5dd1665a040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 21:20:32 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8315467ee71a8ad5b2dec12ccab0e7fceaaf53e524d175daa1d5cf08d233072`  
		Last Modified: Tue, 04 Feb 2025 11:45:34 GMT  
		Size: 205.8 MB (205830615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16dad910d55c70dfeba9c305910e8bbae19182f85b9380b16fddc7878158d74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ed49a8170d29bc351d2875938957f1037cdc6ff9d7545fa23f2fe1b181fe47`

```dockerfile
```

-	Layers:
	-	`sha256:19357ca9bf0b78bf8c5485b1935cb1fb4a1b0648d36bec0ee73d5b6072b898ee`  
		Last Modified: Tue, 04 Feb 2025 11:45:29 GMT  
		Size: 16.7 MB (16677723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c95894fead5209f44c8c99d0fd361dc9405cec026e929f9bf97f45e260a7640`  
		Last Modified: Tue, 04 Feb 2025 11:45:28 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bcd1f561efcfc768c9956f25915c1953a59945173dff19895b70398b7f92f6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324730450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61ca2d130998ce89b1b278a75717c82c41227a2056f926a433a2c33533a1b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Wed, 05 Feb 2025 06:15:39 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Wed, 05 Feb 2025 08:49:48 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f786aba56916535ebc6b771a35d47d2175891c3c573a3fe39933177009842ff`  
		Last Modified: Tue, 04 Feb 2025 16:22:53 GMT  
		Size: 62.6 MB (62564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ec567b6fa22351018590d615d7285dceefc62f5cb3f6240b4c36b8ff2bae93`  
		Last Modified: Wed, 05 Feb 2025 00:22:29 GMT  
		Size: 193.4 MB (193434739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:148cf3fc48d9400141c5dbd727d88bc65750257bd65df8dad9fd781fe7f873e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72234952bf04daa7f191c68505603b02f16022b91bcb210be6fd814d4c67321`

```dockerfile
```

-	Layers:
	-	`sha256:d6695666774b275ce288eebcf6c9ff4e699cb0277a54cd2b7c2e0d1fae1ba416`  
		Last Modified: Wed, 05 Feb 2025 00:22:25 GMT  
		Size: 16.7 MB (16677310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223486d1208cfae26b8101f2b31c7d4d4871f08862003f791c41451f1810bd59`  
		Last Modified: Wed, 05 Feb 2025 00:22:25 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:484771716a56f37087dfe4f3aec471cacc8cdd3e7a165ac894b95ea2ae817203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368631771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fbcc5dc8bdf83e5923dab75b6dbb3102a77d6b23592f44fe5fd820efc4ccc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 21:15:40 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Wed, 05 Feb 2025 03:23:16 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736977a6a976908d4675041b7224f0f03bcf47bf47293685f8218698d9a2d23`  
		Last Modified: Tue, 18 Feb 2025 12:29:23 GMT  
		Size: 67.5 MB (67513524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3afe787af6d04bcd7a7110752b65373b2683e89c3d2ae87036b31a33b54b92e`  
		Last Modified: Tue, 18 Feb 2025 12:29:20 GMT  
		Size: 226.7 MB (226740893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:21cc816b26cd8ba4cedd4705c36996851df5ee16b693c1126dc4a3055b7413da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17003461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bab27edcf521979ec7d0d94c0db277d211c8e2a938181847f76396295f0ae0b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f40b48206145213439f63e923076e06ab23c0dd8a3ac7a2f580f43c2038233`  
		Last Modified: Wed, 05 Feb 2025 01:41:46 GMT  
		Size: 17.0 MB (16993205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4c074af86e19f7a830e7425a78b264b1b661d20385df1f117963e6f6d23b09`  
		Last Modified: Wed, 05 Feb 2025 01:41:45 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

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
		Last Modified: Wed, 05 Feb 2025 12:01:47 GMT  
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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cb055b54c506e0bb61919a1ec3fa33ac81d9b11f9a4f8d579057d0c690100fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358580680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822f6c8aa328b153d5fee392c6d2640f16c85704bf359da7f3a44425b7f685e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ba41641f188bb1d74522008f197d258fe218bbf039fa1f236165286ebcda75a`  
		Last Modified: Tue, 04 Feb 2025 01:39:07 GMT  
		Size: 48.7 MB (48680970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214950258d5885930b9bdcaedc26eedd6794e5ab349aac8800d95c05105fa89`  
		Last Modified: Tue, 04 Feb 2025 19:27:31 GMT  
		Size: 26.1 MB (26068631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46162e9940e0d980c469abb7969964a7334e5e0da594584952af4acfefef17d1`  
		Last Modified: Wed, 05 Feb 2025 02:57:00 GMT  
		Size: 66.6 MB (66630216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b0bcecb6cd78ad82b4eb9c7fc93ecf95d69e341e3b45ea9d1660fbfc9e8b47`  
		Last Modified: Wed, 05 Feb 2025 07:59:11 GMT  
		Size: 217.2 MB (217200863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c00432682cf51313e0182559af347d540ce8781bbe5f8af066e3f5b1133e947b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7400834c7dc1d0bd961858da8a3e4d286c7ba710bfc5880613041409cd768fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b0c24c52ff3088be14b9cf47fa8bb00342de08e075d6a7d42dd6aae35707c518`  
		Last Modified: Wed, 05 Feb 2025 07:58:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:19aba767d51f2978a1149814c39fb58ab631b9e4d1c8b56091ec87330c1a9f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384472654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e988a3adcfc23acb899d19e70bc53d7935b4b9ea64534fbdac848fb4b5d1a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20ee406f6988f44113bcc71bae5adfb439e360c88b767260000751228a498e00`  
		Last Modified: Tue, 04 Feb 2025 22:22:01 GMT  
		Size: 52.3 MB (52287301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8eaf628cc7675b29225b3b455c5d86d2c6a1f5fa29d78dfb7f3bfa69b3ec`  
		Last Modified: Tue, 04 Feb 2025 07:25:22 GMT  
		Size: 27.6 MB (27594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e93e140d3d694402e568de11fc711950a112421628cf6102d07cd3e104fdd3a`  
		Last Modified: Tue, 04 Feb 2025 15:48:07 GMT  
		Size: 72.9 MB (72896768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359ff4fecd164e54eed8dc426733d2c77dfd29610093c427df1db3a3f0794f56`  
		Last Modified: Tue, 04 Feb 2025 21:59:47 GMT  
		Size: 231.7 MB (231694043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfe39a120090e71bb12062da308cb7bbf518e09424e3544740a280182d3d0d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16909329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e133cdee6fe7e0e8f0d94e8b0ec58d5754a39cb06785ab94e018b30735c4a376`

```dockerfile
```

-	Layers:
	-	`sha256:a2ba07c1c7a1bae8871fefbd69f40ff75c1d1549ba3875a898fd9c6e7b6abc7f`  
		Last Modified: Tue, 04 Feb 2025 21:59:41 GMT  
		Size: 16.9 MB (16899122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44961c313249edf7825387f87ed2dc5dc3eba21b0a020ced818f6ad6b157bc2e`  
		Last Modified: Tue, 04 Feb 2025 21:59:41 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3639f13190096719aac7a54bedfd4e09b26fc0dd2a909639e7cf0a3fd33ba631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460506022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e888d6f05533ef4be30c9b22e055cac880d4bb0df839b638fd86c8a2bc90772c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0674f07b14526b99d8a1ad6e260fa13f5923299979b4990047db0a18f0e7754f`  
		Last Modified: Tue, 04 Feb 2025 09:50:26 GMT  
		Size: 321.6 MB (321559378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b8df108a10b1e88d6b87824249ab1fb77f1b9afd698bc50f1911e8450899dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca31fb4b8ab775c0c89f10c2d00db316af5da9f635cec87da6421dcb44f602e`

```dockerfile
```

-	Layers:
	-	`sha256:844d407e0f895e351a3eb25d6945314331d6d457cefa01ea0b3de0ce8c11ee63`  
		Last Modified: Tue, 04 Feb 2025 09:49:44 GMT  
		Size: 17.0 MB (16964438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8f8a3c148cbeea3b0e96dd11781e968a527ea4b64c2fd01544e28ce3ff8eba`  
		Last Modified: Tue, 04 Feb 2025 09:49:41 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f45d09370ae47b45bd2fc6a1db07e92d76034b4dee8272814e7eadcdb5be7a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351238963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939fc2a705ad1f83b8cfd957e9962788b1cfb40bc1d137f60773439faa2e4f3a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Wed, 05 Feb 2025 08:49:47 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8e9f79a90256c65272d5e3f7412b708597a6f16ea9693af76e4d17ce51d21`  
		Last Modified: Tue, 04 Feb 2025 11:36:07 GMT  
		Size: 68.6 MB (68555496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1715c9c9e70a673d679b5b2d1d80c3ef8e6b10e9dd5431d6684973bf0aadfc4`  
		Last Modified: Tue, 04 Feb 2025 17:58:05 GMT  
		Size: 206.9 MB (206908221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27ad1d387f1d09ffdf35015da6c60dbd832b71ac8c583d95fe02c5a61cb87f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16702932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad5872bb0320e1010c826f48c8fe488e01b0c4f9d61493817b39cbd7cf6f559`

```dockerfile
```

-	Layers:
	-	`sha256:7a4214e24e3828e1f3125b3293795461ec038fedf3f1101fea0d98e9e317fdc4`  
		Last Modified: Tue, 04 Feb 2025 17:58:02 GMT  
		Size: 16.7 MB (16692756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e85488ed9c1eaaddfb7a4d98b9d1359d229993a1323216d289ef480c121fa04`  
		Last Modified: Tue, 04 Feb 2025 17:58:02 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
