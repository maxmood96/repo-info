## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:8cc582d8a0527423169a6548cddf2e40b06355c5e6960261d179fccb152f3d13
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
$ docker pull buildpack-deps@sha256:b72765c7323b0f170d9c96bc1e70f7d6431fd4a9a34fdc39231bf20e9e415795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.7 MB (370728234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4d2203e3e378182a2cd4ed6da27fae4f86225871e747cb07a4e6c4f7a63c2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 22:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:09:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f402971e72fa142c9d15dd5eaca638787cb5c2e5a412bb3f2a7c4f896ed18ae`  
		Last Modified: Fri, 08 May 2026 19:45:34 GMT  
		Size: 54.0 MB (54028078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14bf1fa31e28d06ce5dc3e4b127ed62c78c28290930f8041edab4719b7e2e73`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 29.3 MB (29286747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc335114670a5a7b57fda466c409652b52365286d8f06c4929c70e5424f0edc`  
		Last Modified: Sat, 09 May 2026 03:28:39 GMT  
		Size: 83.4 MB (83443817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d34c20fef8c413b3462ba7d5af8115bb6c24d7b7d480f26c4e43409c546a50`  
		Last Modified: Sat, 09 May 2026 06:11:13 GMT  
		Size: 204.0 MB (203969592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2639d61ce3b7877b9ad8086b7b96cb30d8a22e5651fe1b161a8d010b0cd1d4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16852069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d414e4645facf326141f805eba403a253f1833f2490f6652dbb6ce8c21110a10`

```dockerfile
```

-	Layers:
	-	`sha256:109aac27d918a8ff8521f172b26ae33a6c24e6c82a42accba132f9a5563236d5`  
		Last Modified: Sat, 09 May 2026 06:11:09 GMT  
		Size: 16.8 MB (16841904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb65a6fe71a53bee9d359618bed1c1d8094e01a19b622818f7befeb9d5f307e`  
		Last Modified: Sat, 09 May 2026 06:11:08 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fcbe13f6fc92288f7840e0c5b1acd25c9637b79c406e766549fa468a2d2c85db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (475953625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d415ef737fc7e1d2057c7f7c14f99dfa50bac6638fabe35fb6057a6db371cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1777939200'
# Mon, 11 May 2026 00:52:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:41:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 13 May 2026 13:03:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:291921d355da34dfbce324263312328392c6a6c78ee971f9b4d7d37f1527cd2e`  
		Last Modified: Fri, 08 May 2026 20:26:01 GMT  
		Size: 46.8 MB (46838649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340855859b1344ded89a6e027caa6be811a60e26a4f08013b27235c463879b0e`  
		Last Modified: Mon, 11 May 2026 00:53:36 GMT  
		Size: 26.5 MB (26453358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edc8a79553eb62a40d99b38aaa32211fc341a1f9cbd23a6cfe2581ef0fd704`  
		Last Modified: Tue, 12 May 2026 00:45:17 GMT  
		Size: 75.3 MB (75313263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731f70c3ecae0b7372580d19e0ad04d33c4079dcc9da9ffe21d063259470b82`  
		Last Modified: Wed, 13 May 2026 13:19:15 GMT  
		Size: 327.3 MB (327348355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:928a3ba1950fa5d74ba8f5d4458b63b4c320e858fe07df8c637aa0b4d5f27082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16942304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fc3e3a10ff39f38e574dfcf00e11812f7a4082a3724045665edee9ad6f00e4`

```dockerfile
```

-	Layers:
	-	`sha256:c7bacdd864cae52f5d01f6142d0e2338d1bb269153b0dbba34f1fa198dc30f78`  
		Last Modified: Wed, 13 May 2026 13:18:31 GMT  
		Size: 16.9 MB (16932140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0164e0bba938ef3d1f65916230099211b3b2b93e73d296489bcf3c1ccf687e1`  
		Last Modified: Wed, 13 May 2026 13:18:25 GMT  
		Size: 10.2 KB (10164 bytes)  
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
