## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:d8703b8d3c43c1b9054327866e567075b19a51b553314c8e43ab592bbdeed7ed
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
$ docker pull buildpack-deps@sha256:34250361750a4b061f5fa55d49dfa475fcbb59f38462ad6c1a5ddf2c2198257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351176978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725364ce75b3d808d6d062b46b3cf31a3515a7dae2d0cd549252cb4502ad43c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab406cee21a5226773a482e38ac91869a010b6b5a398856bb12cca4e8f5c66`  
		Last Modified: Tue, 19 May 2026 23:23:35 GMT  
		Size: 26.9 MB (26893097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e3a290aac34d6c988f9b5828c1d5f042f85c5e0d94ffdd846e594866d4adb`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 76.9 MB (76899603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd5d76d078aeb8bbaf49bf464fa7bd20e32994d4947f7b5e2792c1b5b880cda`  
		Last Modified: Wed, 20 May 2026 01:16:27 GMT  
		Size: 198.7 MB (198672266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf0404b73c2e74a9430bc4d819d0b82d926cb553de0dfe771159ab9b2c352d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16894604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9d0c9f25547df3e33d1e5fdb1fe550a765918dbf2d442c091e80bc261ded6d`

```dockerfile
```

-	Layers:
	-	`sha256:d7523445811e8ad18b8b104dc01408d7b0d986461896175e7cdaa9bafbd1f8fc`  
		Last Modified: Wed, 20 May 2026 01:16:23 GMT  
		Size: 16.9 MB (16884472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cb2626067e82f2a3cf61bf2c5acc22ca16e06d48d1607f01bc642708d9bd05`  
		Last Modified: Wed, 20 May 2026 01:16:22 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9042e632477a615492a648c176169448ca42fd5c34f2ced191a46a55be82f2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296381755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7da9d35864517f5a657e06e1186e8edce67a8cb4134e284007ebb047c4f3097`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:15:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c98d9ac4796e25c1d81c99407f882de7bda76effb4d3c6a5d937bf755cc2313`  
		Last Modified: Tue, 19 May 2026 22:36:23 GMT  
		Size: 45.6 MB (45618956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1515c975babc2c0d71d5cf9a3ec0808ae1a576e22e50913d437d07a60ef65f`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 24.6 MB (24603114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5553a007241b1597e7b47e09586bcab8915ab176f1b18c717170ca0fcf73910`  
		Last Modified: Wed, 20 May 2026 01:34:41 GMT  
		Size: 71.4 MB (71419330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311c064b17e08475b9d99a1518e66f824943c84745f7fabd779c536b5b32e97d`  
		Last Modified: Wed, 20 May 2026 02:15:35 GMT  
		Size: 154.7 MB (154740355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:685b947b8915454056908739247b1b4ecfcc526cc4c31ba4cff6bc089f53a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16649814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d52ef3f8ba07d14f68cd22e25aa387f8043787a81bf71656042580e0958da6`

```dockerfile
```

-	Layers:
	-	`sha256:d7cfe08aaf91a19d15e17d40ac9d2bcfec5ca66cd4cd5287ad7ad749a42f288c`  
		Last Modified: Wed, 20 May 2026 02:15:32 GMT  
		Size: 16.6 MB (16639617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4eb966490a018f1852cd4d661fb9de2b56d8219fe5724da0bdd24ae4183780`  
		Last Modified: Wed, 20 May 2026 02:15:31 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:66bfaa7558a5d2eac1fed87fba8b17cdf0eb7fcc34ba7789823f7099ff6c6539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339622944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a63bf27520064516c4785ea7260a006bcac4c5f276d8239552419c71a71f2d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab26ead8a9a9779bd1e4fbb72a954ed83ffbb2d9d0e5d585eb545c5b6270c442`  
		Last Modified: Tue, 19 May 2026 23:27:06 GMT  
		Size: 26.2 MB (26170738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4f42b49afc591850a47b31466ec9e30deb1aa59f61962edaa6feaffb6924ef`  
		Last Modified: Wed, 20 May 2026 00:27:51 GMT  
		Size: 76.1 MB (76066265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7988827799b15b356a83fd4a2af1cd614f1f7e7046e794849265fd96e8e1f4ef`  
		Last Modified: Wed, 20 May 2026 01:16:38 GMT  
		Size: 188.6 MB (188648332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be11c8170301ec9162fa446ef55d9b81bb0e19dc4b77440efecbfb16cee110f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16975804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd07ba94f4bbcf1fecd24205188ef5c454df5d9b55251236517bb1c70d1c2b22`

```dockerfile
```

-	Layers:
	-	`sha256:6f2660e5ee69611716f275afbde3151f29bedfe39649caa041de184de87a030c`  
		Last Modified: Wed, 20 May 2026 01:16:29 GMT  
		Size: 17.0 MB (16965591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88898097f7317442238a0c45567bc958841f64dc385b263b67744410945c7430`  
		Last Modified: Wed, 20 May 2026 01:16:28 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e01f1e8b0a8a415661426fa0ae2e62fa28b61f3f705e101544ec8af9d95f7f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358974480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416860c111dc26c4e82a7c3695e893340d777ad9278b49e09ab6f0f7ce5af2df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:03:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f3d5431169cdd29adb39f5cf26f13e071f7217f28223b49e250857b02be6d`  
		Last Modified: Tue, 19 May 2026 23:25:28 GMT  
		Size: 28.2 MB (28209479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62d0bd46ff0533780d2f77ff103a5c122ca383e8dd50cef1106912fc2d9dea7`  
		Last Modified: Wed, 20 May 2026 02:45:54 GMT  
		Size: 79.1 MB (79128130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816452ebab1a64920e780eecd17c17935455ff0efed61254aff451c146ecbe76`  
		Last Modified: Wed, 20 May 2026 06:04:33 GMT  
		Size: 201.6 MB (201620867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b891e55cf91705932e2ce63ed8ee8e88b171823d9147410c24cec593fb71e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16863638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6f0720b50bb3ef37392f6b0829b329094b21e06c0ffaa26e9e92c105be910c`

```dockerfile
```

-	Layers:
	-	`sha256:6593d494aa7993e0c997379f04f71ec515fd00036306c54aadc40baf8512e0b4`  
		Last Modified: Wed, 20 May 2026 06:04:29 GMT  
		Size: 16.9 MB (16853527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22a1d63576d73dd46369521287197ba872f73ff94d82f2b38b70e76554ffe9b`  
		Last Modified: Wed, 20 May 2026 06:04:28 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e83774a6df02caee864e5c45a60f6af70610e0f147c708ff86dffb778558fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359227814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf34a6ba86a1abf40fe8293f0cac1d4230508d3fdba8d965e6c096107b478db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:10:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac92e3c123ea205d76f5d82b79747aea7ae5197399f942393a1c3ea0ec0034`  
		Last Modified: Wed, 20 May 2026 01:14:34 GMT  
		Size: 29.3 MB (29285530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f4090d3ef4e4805f871375fca40276f6e550a6f99e7794ca38dfdacbc423a`  
		Last Modified: Wed, 20 May 2026 06:52:52 GMT  
		Size: 83.4 MB (83440421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d397edb24d4359e86a586e5e4985d55346139e6558d333200cd6e8a51fc45`  
		Last Modified: Wed, 20 May 2026 09:11:21 GMT  
		Size: 192.5 MB (192455741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3c21e30b7e92bc4ac0063b64aedb9927322d154613e627800f72bd1ac2c9a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16844727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e13e04e672c9118a6dde4d06ccdbbc652f4b8232f1aac11fe165ee5c18b0b8f`

```dockerfile
```

-	Layers:
	-	`sha256:402fc4058af2bc9c8c2820ce24dbadc80bff503f95fa3354c22b78d1eff184ac`  
		Last Modified: Wed, 20 May 2026 09:11:17 GMT  
		Size: 16.8 MB (16834563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab71b3ccb37c792310350ccc1cd69031efb9232a5fafb09d5c5025fe107a52d4`  
		Last Modified: Wed, 20 May 2026 09:11:16 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b63bf0139569234abbbb5d2cf56b70624f0ca13a61db27381c38ff43292e1ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.7 MB (466742927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f328f061746a7fc5d7ff3c6a841bfabb480dd03b471525480ed2e652595c6c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1779062400'
# Thu, 21 May 2026 13:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 24 May 2026 15:49:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d609dbe8a64103ca9a52594c54358bca867134ca11c5bdbab5024849e5765438`  
		Last Modified: Tue, 19 May 2026 23:39:28 GMT  
		Size: 46.8 MB (46808398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9071891294e630f1468302f4618eeabbee9f63f74797f1ce63bdd2a40a26945`  
		Last Modified: Thu, 21 May 2026 13:59:23 GMT  
		Size: 26.5 MB (26450836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb760ccbad4b8704448bd41cf7b9ae923800147ba7dbe24d29cd36600d159a`  
		Last Modified: Sat, 23 May 2026 06:45:23 GMT  
		Size: 75.3 MB (75313420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0c7be345104387d8f327f70dfbb38b285cca3d4637db1db86e35dc81c24fa`  
		Last Modified: Sun, 24 May 2026 16:04:49 GMT  
		Size: 318.2 MB (318170273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a780c5e9cfc5b44d3bf4233b8f73379c266a6229df83577b068b90a0f26cd24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16931200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a028c68bc53503162ab084bdbbfd225cfc1dc5a346fa7049ed4ec13a7ac9700b`

```dockerfile
```

-	Layers:
	-	`sha256:6ec0d8d40bea8ab86f2c2db90228fb24ec1e7ba332ed3601a8480a2e3a8429e7`  
		Last Modified: Sun, 24 May 2026 16:04:05 GMT  
		Size: 16.9 MB (16921035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7f29841bb119dd3041e2b39d795bdd0023defd5c112f6fd1a37255b75987a`  
		Last Modified: Sun, 24 May 2026 16:04:00 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21bbd71f994f09934a2322324946038b4d021f8a24a6e9d91ab73a719e29ed35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323942682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84abdac20dd0c92fa19d2d82263e4d9058f1435e7aff6d3b6e6b6ca9f871012`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2de0004fb71a1e4abdd27d0619b3567a865a43b4039f4f3ca7e11b6e7bf8ca5`  
		Last Modified: Tue, 19 May 2026 22:36:09 GMT  
		Size: 48.5 MB (48454253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e98e58fdd0e7e9d312d1df7e45d14fcbde914744efb8b87cc091a75f459ef`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 26.7 MB (26690815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb487184dd43970e32613d936ce72502fa8f8c5f662aad3fc0ef56ac0b146e`  
		Last Modified: Wed, 20 May 2026 02:06:15 GMT  
		Size: 77.4 MB (77425565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2048f6eb098d84704cc916dcd451871c41e35c04a0e376178e78d22e39b623`  
		Last Modified: Wed, 20 May 2026 02:46:11 GMT  
		Size: 171.4 MB (171372049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf0a17eb655910d733e43bf1dfb4e9200d99973f4c0d934099523e97b32c9c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f271c9149b1fc5194553db227ea7ca1bd58b7051fb5e25b4ed63a84c3ec612c6`

```dockerfile
```

-	Layers:
	-	`sha256:4b0e7a83923db59edfab50cd9219eb80dc205e06e8ff338e7b043240cff162b3`  
		Last Modified: Wed, 20 May 2026 02:46:07 GMT  
		Size: 16.6 MB (16638606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566961d8ba2e57acb864817bdba3b657ff4cb1e2118c52f5dcbb4d82f434d429`  
		Last Modified: Wed, 20 May 2026 02:46:07 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
