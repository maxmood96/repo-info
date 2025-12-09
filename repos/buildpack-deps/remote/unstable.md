## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:3983852e94fbfbf3192eff72a260f8619490912f5ba92837b6899d0a60ed75f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6dcafd72a00cd7683c828e6035caa39babfd4fc781cbc1e9ceef3dfd94144c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343824885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529953b46f42ba003c545317787c68a158c20cfdda99b1387b8af40541b0658c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:45:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8ebe9a9fefe126b5d099857127577acadfabc1b7d98ce416ca0faff37c513`  
		Last Modified: Mon, 08 Dec 2025 23:07:36 GMT  
		Size: 27.2 MB (27197450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefa9b0831ef76f3b6f478e168c5a2d244535ebb9ede263a69d319a2cdf5e22b`  
		Last Modified: Tue, 09 Dec 2025 00:06:54 GMT  
		Size: 68.4 MB (68427481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df42d636bcd80dc7d9ab4d2be6574fe99db41a50f60b4b417fe39ea88e6a82`  
		Last Modified: Tue, 09 Dec 2025 00:46:06 GMT  
		Size: 199.4 MB (199382431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c38d4411ecda5b97186b1c43da600bf7084e809e7e530e6e80daad00d554659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16288880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70698cc0b1ea781283bd14fb7759319ede3317d0b36dcdec5830c1790079278b`

```dockerfile
```

-	Layers:
	-	`sha256:2be87dbca03acced547e7f314617d15b73dd94c43c4654efba8c51fa82c35e83`  
		Last Modified: Tue, 09 Dec 2025 02:23:11 GMT  
		Size: 16.3 MB (16278748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82379c4beb786d157b8736f0a32bc4f9e6ed879812a016c10c317db6bebacb2b`  
		Last Modified: Tue, 09 Dec 2025 02:23:12 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a1b1f72af6f6338079f7148e1414e729883132f423295d996e124fd0d7676ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293756718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879640722112188115c407ba72ffe504e9f1cb55ab495f4c1368a6f718c1861`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:22:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:249f143dbba2558bd4f87316a884ba0d2b99358af5b3c63e9ac2b9640e6f9846`  
		Last Modified: Tue, 18 Nov 2025 01:12:47 GMT  
		Size: 45.0 MB (45003691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd7e51b270e55f3a7a9a2d43268061869ee4c4d0b6076dffdec9ff8ef06009`  
		Last Modified: Tue, 18 Nov 2025 03:59:26 GMT  
		Size: 24.9 MB (24946289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b78319f4c6f1757d125d21ba9e88a135787bf828fe59c5234a165914a13aa00`  
		Last Modified: Tue, 18 Nov 2025 05:29:13 GMT  
		Size: 65.5 MB (65528313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df725a769d8719e32d3cc09c4683ab2b9cb9a8b0d734fcdd3bc1d185e839ed`  
		Last Modified: Tue, 18 Nov 2025 14:30:54 GMT  
		Size: 158.3 MB (158278425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:192ef01aed1a92e6dc46f0fdb31977540ae3afdfe0a8ba33dab9bb6f2fb0b1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16021486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6101b8682a5d52af287680d3d83434f568491e741014c15b9c1b7e2a94b9e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe50c8ffd0a9ca0a7166497f210f77086270da4dbf4ebd8838387b5c4cdd0a2a`  
		Last Modified: Tue, 18 Nov 2025 08:22:52 GMT  
		Size: 16.0 MB (16011291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042310df324321e36cd1823df37fff7cb35fbfbfd7c07a0b4d55414c8dd31113`  
		Last Modified: Tue, 18 Nov 2025 08:22:53 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:09b935d1db77f92cfe9ebfe2b68f1cc88b8abf5ecd2a77056eaf00c6370f1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334679300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2d24efbd9fde0f77105660116833e9843f9e3068d3a4827868080ceca52527`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f615e7cb4b13e78f79053e3ff3386cb79b093cd2d91fe819f692264eb1475`  
		Last Modified: Tue, 18 Nov 2025 03:26:37 GMT  
		Size: 26.4 MB (26445334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8961176208fb3c6520aee3a23dd4452025d1885baea507b988ee8fdfe1d8b591`  
		Last Modified: Tue, 18 Nov 2025 05:39:35 GMT  
		Size: 70.5 MB (70473388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf2e288fc97b8ac4d59a1e19623443f9d468782962eb3f4ed050296d55b7f7`  
		Last Modified: Tue, 18 Nov 2025 09:13:47 GMT  
		Size: 189.2 MB (189169189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1256c463e474f81d497ffb124828e27c6f7155e2f867c5654ca97d14180ea27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c945c66cfbe74a5bce3db4dc2ae08c86ed658c548bcc74f8966ffe51a7334ff`

```dockerfile
```

-	Layers:
	-	`sha256:61430c1ddf44684f3fd275b439437107189e4cb49bf8fc75307293ee228a12fe`  
		Last Modified: Tue, 18 Nov 2025 08:23:06 GMT  
		Size: 16.3 MB (16328892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d93e86de7d873bcde12b7b009830dee3e34c46bffd91f11df084712c041a4ce`  
		Last Modified: Tue, 18 Nov 2025 08:23:07 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:170ffba505dcbb85976c5600d4ff4f4d7cac5fc3ccb3aa70f79e31823d15e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351358066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec76b8ea66f8b054884d9319657d9424780d6f5b93d6d3ae80e18689da96ecd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:17:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e94662795a8f26e5463a4bcfcaabfbdeca01c44b799e3fa96524d3ed5ff0a`  
		Last Modified: Mon, 08 Dec 2025 23:14:49 GMT  
		Size: 28.4 MB (28430929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2dcabacda9674c82129e92594c80d843967d7757a07ee38e58f0c8b9e9e24a`  
		Last Modified: Tue, 09 Dec 2025 00:24:37 GMT  
		Size: 70.4 MB (70406743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421f45c263fc9ae77e5e4099fef799734e68d22ac77fe7db9913198736d4980f`  
		Last Modified: Tue, 09 Dec 2025 03:25:09 GMT  
		Size: 202.6 MB (202572428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22c92c018089a0fdf8726dbd8421a80b1d49bb0ce322474336d846d42c7fee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16258608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57968fbf7faaf29036b7c6e4436baa778ebca5db0b5b79bb6eaa062c55ee2a4a`

```dockerfile
```

-	Layers:
	-	`sha256:d276d92e8a72c7e135d4a67ddc104205613b6aea9d3bdb31ad38051bf73f9604`  
		Last Modified: Tue, 09 Dec 2025 02:23:52 GMT  
		Size: 16.2 MB (16248498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43501e64846238fc14bccfca416a118ce821d0f4f8c1c3a70b12db9b84777f7d`  
		Last Modified: Tue, 09 Dec 2025 02:23:53 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a21abb667e2c4ba45580023c8f1bd3592d3397951cdb7fecb4d30501ffe80bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350639598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b291747da511ceec5d0d7a9cea8e5ea4ba65d16e4023c9b8b0fe98b78a887d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:17:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233726152393942e1ef6b4533705d6bb3e4142964e6e486a7902cf456eab5151`  
		Last Modified: Tue, 18 Nov 2025 01:56:30 GMT  
		Size: 53.3 MB (53335631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8247117b12d78345474708e2bcd8a4be4ebcad8965145f6ab351c359ba9869b`  
		Last Modified: Tue, 18 Nov 2025 04:07:17 GMT  
		Size: 28.8 MB (28838475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df21c22b8199e396dd68073d81a213289efbf6a3e913789e13269dae310802c`  
		Last Modified: Tue, 18 Nov 2025 06:53:03 GMT  
		Size: 76.6 MB (76569175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630d1e40b9d0e13098920c6b26b3c2b64fe405597d473ef6e78888037547dd0d`  
		Last Modified: Tue, 18 Nov 2025 14:30:49 GMT  
		Size: 191.9 MB (191896317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e128cfae338f8608d768fdc0f51f80be4979c038aca75cc0a96e60a6c771640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16238654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d1901f3ace143a9ec8cb7a464e37b2c85f2879ccb605eabe4980ed572f0f5e`

```dockerfile
```

-	Layers:
	-	`sha256:03a5babb24490f519e5724f20800e37c2ac5432d7cc5caac255161c8960aac88`  
		Last Modified: Tue, 18 Nov 2025 11:22:40 GMT  
		Size: 16.2 MB (16228489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b98b48612f210716dd5526f4258cf9ea2223f065bc75dee3c89c7f0d3cf379`  
		Last Modified: Tue, 18 Nov 2025 11:22:41 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:560382490893079040e0ff079cfbd4f17fb94c7d743cbb76e636f2755db32f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.1 MB (452138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26071e0c7b6ba26393f5e5fa6eae79e0699d8e431cd5fdc51d66f78916b24d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1763337600'
# Wed, 19 Nov 2025 19:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:31:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed67ff00f4a63ed57f98b299833d8c2bd5b7627bfdca1af20fe366dfb5d9d552`  
		Last Modified: Tue, 18 Nov 2025 01:34:50 GMT  
		Size: 46.8 MB (46807232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12faa2c8d5976c2936626416dbd958b979633ec7e97e5fb377956f757414803`  
		Last Modified: Wed, 19 Nov 2025 19:35:09 GMT  
		Size: 26.4 MB (26394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c856553cdba1b452f2934482676983f9c2dee9a9410ebeeee2db907f70948a`  
		Last Modified: Thu, 20 Nov 2025 22:25:57 GMT  
		Size: 69.6 MB (69597545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf6d06ff1c105ed6a3cf1531c6c52c5a38a0e4bce47bfec4b65cce8f7da031`  
		Last Modified: Sat, 22 Nov 2025 21:55:08 GMT  
		Size: 309.3 MB (309339401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eeab707c587e210436d5cb35faae401130eb0565134bc00462108a2f98436dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16311848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79bcc184d1b5e0bffab3e5364c548db87ff63867971b3ddcbf2584dd1c2f088`

```dockerfile
```

-	Layers:
	-	`sha256:9524882e97e0c9f78e82eded7c97a04d66c93abb3be29254aae9d06ee47133cc`  
		Last Modified: Sat, 22 Nov 2025 23:21:13 GMT  
		Size: 16.3 MB (16301683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e341bcdb3aaa46b4d3f480a30a2055291cd10a05824e42f4a7084bfabe8d212`  
		Last Modified: Sat, 22 Nov 2025 23:21:14 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5069e2df4afe2669fbe2fbe6550d61b125a369656d84b1ee637e5c48b05bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314043589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbcbaf20206284fea4891a4fb83e0fe970ff9fa99f1c639af9adbf5e8a210b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 16:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 17:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 18:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3fac6ecee4cd3dcadd720b65cbc3dc0f3dad0b4ed9c8b5d4ab2833f1e8d9ed22`  
		Last Modified: Tue, 18 Nov 2025 11:50:57 GMT  
		Size: 48.4 MB (48370424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c3b5545bcabb40092d94aecec534cb4b55ae8e70b0d58ae879cce24508532`  
		Last Modified: Tue, 18 Nov 2025 16:21:54 GMT  
		Size: 28.3 MB (28338991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43eaccb5c28ea9f4e8082e22dee4766d2480b9df74579ce01f2f4291398a97a`  
		Last Modified: Tue, 18 Nov 2025 17:13:26 GMT  
		Size: 71.7 MB (71705173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f29225e45d027053fdb28d7ebf9d9afa1f9b40117426f1fa5cad3639e0949c`  
		Last Modified: Tue, 18 Nov 2025 21:15:56 GMT  
		Size: 165.6 MB (165629001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c547e25d559c3bcb2e0278c19fa811e10877066631cd03f2dcf65cbe80e739b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16031140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0c2fa522befbd4c6ea48321ff43de748f56d25295e08093cc713f5a8331745`

```dockerfile
```

-	Layers:
	-	`sha256:721df2f45c9e83395e69fc2653ef95e75a2d9878e59211082f91b51d7535623b`  
		Last Modified: Tue, 18 Nov 2025 20:21:34 GMT  
		Size: 16.0 MB (16021007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa2544ce90ba4443e482511969172933fac8ad7a9ee98313e100bf67b9eb13f`  
		Last Modified: Tue, 18 Nov 2025 20:21:35 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
