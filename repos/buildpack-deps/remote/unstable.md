## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:1b1fbb2b74e1c032d126beba474f18825ff4eaa165543f94c2933068762f272a
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
$ docker pull buildpack-deps@sha256:905a055ca08da61e3e26eaa6ef1b7c17a51730439c2ba222e813cb5ba47a4441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344017771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300757072f4a4d31e6c8115972932be059fee287c028e4053cee89dd9ec7216c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:46:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:38:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff00e9a4f0fade15b203525aaff92a3d5f8f8fc08fd83188ea3896aee735cf9`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 27.2 MB (27163941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cc8637f491021b1a5b654de24c9952c1a34d6f439d5276b217858ffb0cbedd`  
		Last Modified: Tue, 30 Dec 2025 01:24:03 GMT  
		Size: 68.4 MB (68434183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb658254d814dc915114b8cc09a7ef261ed328dcea0bd05f9bab1ce5865abe27`  
		Last Modified: Tue, 30 Dec 2025 02:39:30 GMT  
		Size: 199.6 MB (199598529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5376b852d8102368f4a3aaf1bda38caeeaded3f6aba25cff840cff9f7c5f9268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16279189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d5dcaf52097bf954830c04a3566eea0683907bea37b1543c325fefc4018ecf`

```dockerfile
```

-	Layers:
	-	`sha256:4c98d49feffbb461fddde45e8355576caca0e3a5737a90ee6c68969ae476a0fb`  
		Last Modified: Tue, 30 Dec 2025 05:22:56 GMT  
		Size: 16.3 MB (16269056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d60fb0c3879d67da5b1e3755cfc69be8e8fd9605e37eae1af9950a0c392f1c6`  
		Last Modified: Tue, 30 Dec 2025 05:22:56 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c99690ffc05338c32dfb5cd7abbf23bcffb1835d0587d70c1bb389f1a1ce513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291862782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f7a148631b2a0c0a1ef30e5983e7908689e6d319237a7b80b633fc69d53ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:35:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fa37dcda97874915e8cdcc90ad670632c868d75ea88f3d100f667fda60d8b657`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 45.1 MB (45112498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4476f3007fecd22f80f4b20b480cc2969ce90429f8c85967f8e864a1ea4ea7`  
		Last Modified: Tue, 30 Dec 2025 00:35:29 GMT  
		Size: 24.9 MB (24876058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e43ff0df27ddbb7e584554f19ccd47c0d42c490cd66902adb1e4ef8c438b50`  
		Last Modified: Tue, 30 Dec 2025 02:07:49 GMT  
		Size: 63.3 MB (63335919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d450b59028a9d6de3b38244e49dae256aa402b99208d9d9595e16d92fcb6792`  
		Last Modified: Tue, 30 Dec 2025 02:36:36 GMT  
		Size: 158.5 MB (158538307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:abeabe9c98415a31a1c3d74b66df9ee6afca2d1e1cb2a295f6ab99c48cd3d725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16034940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f7310b0f7fac2fe004e4f68edb694b8f91319d6fdc36b4372692425181f08e`

```dockerfile
```

-	Layers:
	-	`sha256:6dbc5cde98d506e54ebd964fa5d763dacae1ae9f2e441d7a6d07aef9b6b6d361`  
		Last Modified: Tue, 30 Dec 2025 05:23:13 GMT  
		Size: 16.0 MB (16024743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd1e9cd35612638d3741c1d146070bf374a6fb5819a2fa563bcd433345434c9`  
		Last Modified: Tue, 30 Dec 2025 05:23:13 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3005a3a5191ba64778e6e72c837db16133e5f8754b3919a97292aee92b5d9ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (332957934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d786e490c369c48ae1377e94c78a91f199c3c615e0dee21e77f264bf5eecf92b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:37:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ee77a5614dc66e1139efb80cfe733dbde2b288b1202ba35c49e9a008fab1f1`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 26.5 MB (26450657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fd72cff7703be5b505c0f450c68a28d0e97b7ea4b0af0d5b1b9aa834492080`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 68.1 MB (68145507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce2bf0f699054a8d096dcf37c8282a5bf3b7f9778cc38f0bc7f4d7a9c4102f`  
		Last Modified: Tue, 30 Dec 2025 02:38:39 GMT  
		Size: 189.6 MB (189560741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4cb0a3857bc679a4d0143a57843202a4e28af371673163d4bc0f3e5a3d791ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16353819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f871216af75ff0c00d052e5bad3eb8ab6c34a418586913bd1b476e7ce7a6084`

```dockerfile
```

-	Layers:
	-	`sha256:abdceec8c7046eaa567c657acf8c2f18a0cafa9091e3775404b97b89bc266bed`  
		Last Modified: Tue, 30 Dec 2025 05:23:27 GMT  
		Size: 16.3 MB (16343606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92f59bfb7d3a61da72432d492515eee3b28f4a26ac891ef3c38c2a69fda1a84`  
		Last Modified: Tue, 30 Dec 2025 05:23:28 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e63237663b0943db535d4b300d62337713697697ec4a1262b4a2b381688d3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350331499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45622a3f20b9020dd6f0fa1d590128c09e147623903113f3e767da81a7ac5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ebc798fc10f8015cd27d3c8885c010f05e57b86cddfc6e327bc7f746362b1e`  
		Last Modified: Tue, 13 Jan 2026 02:03:10 GMT  
		Size: 28.5 MB (28474654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7a9609654b5ff3001c4a4b23c058f78703d8972ed2b4f3df257bb6cb1e211`  
		Last Modified: Tue, 13 Jan 2026 03:04:37 GMT  
		Size: 70.5 MB (70466208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d16d814db068f5b5ca803d4a81c723bf3721b606414e5dda8deaa9e7f3b0d0`  
		Last Modified: Tue, 13 Jan 2026 03:55:27 GMT  
		Size: 201.4 MB (201446821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65a9b8bfd3eadb1153f49faacd0fe18eb467cfc0941b6d3533e6f34ce590b79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16272757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5d5a84f66eb9df4607bceeb98882788b2e707f4034e9628f0df25f61bbcfc`

```dockerfile
```

-	Layers:
	-	`sha256:3e47b09eb66d440212b36fe03170cd0372343d9493a5d605a50af247c91f977c`  
		Last Modified: Tue, 13 Jan 2026 05:24:57 GMT  
		Size: 16.3 MB (16262647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41b8b2b2c44c81ea32b5eb8f0b337ddd65891f834abb282a925e3aeaca6fd3f`  
		Last Modified: Tue, 13 Jan 2026 05:24:58 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:16781a5401ed7468decbce5e26facf5d1c50ace7c2588516190c473c0cb3b449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348539679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546608adf848545963b396b72e532d7f202802405a8316392fdf57fee2d919c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 17:38:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 19:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 21:39:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4751b9b2bc723252279cfc4495d1386aada5bcd65548da744f319db317b21560`  
		Last Modified: Tue, 30 Dec 2025 15:09:27 GMT  
		Size: 53.5 MB (53504917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2461812a9f73d501a89daf3b185dd9b6d6fb2e0eebe88b30b17f3f49a5419e7a`  
		Last Modified: Tue, 30 Dec 2025 17:38:54 GMT  
		Size: 28.9 MB (28865214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40a53e9257439f313fdb9e67c9aa13cd05b018790aaefaa0af5eba267630a6`  
		Last Modified: Tue, 30 Dec 2025 19:53:54 GMT  
		Size: 73.9 MB (73934484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0a8343dad16db44ca55aeb85c946162ec53b4e4be9697a1d5a62c071aa9715`  
		Last Modified: Tue, 30 Dec 2025 21:41:24 GMT  
		Size: 192.2 MB (192235064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d46bf184e81b2ac4bbe4fc446169b42b6ccebc3eda51482c4b2b38e368a9ae4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16252148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99c6d213f61ec33f429adecbfccc4084e814d43a682a74ddec4eb0ee981e440`

```dockerfile
```

-	Layers:
	-	`sha256:25c63a1e4e20e5bd0010ace58c744e709e5f289a393e13a75f3d33cae8d03d6a`  
		Last Modified: Tue, 30 Dec 2025 23:21:14 GMT  
		Size: 16.2 MB (16241983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5eae9e2163406e15bcd77c9c58a8e18bee818bf96d71ca37db3887bebd362e9`  
		Last Modified: Tue, 30 Dec 2025 23:21:14 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:39134a8719af5b4377a0fe47a226ce72bd94cdcb94ba7a6d98bf7d6e9eb85a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.7 MB (454699138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda8160f1621684f1dff8423f293e78b5e8c1a9022132540b4dbb6c40fe741b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1766966400'
# Wed, 31 Dec 2025 10:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:37:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 19:42:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:992d8af34d90a1736cf1953fc1b6a42478d3f56705880d255aceac14902fb105`  
		Last Modified: Tue, 30 Dec 2025 00:37:42 GMT  
		Size: 46.8 MB (46842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59f77af8fac6fe633c43cf8effbdd88f2374763db6aea46bfef4f1a063d920`  
		Last Modified: Wed, 31 Dec 2025 10:14:20 GMT  
		Size: 26.4 MB (26352545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfcf1a86a02992f6a6c9bf0cf2dd17b8a12c73c26f7604edf6b0a50cdda329c`  
		Last Modified: Thu, 01 Jan 2026 12:41:00 GMT  
		Size: 67.3 MB (67256815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d59080f72110044ef44e6be7ad52b3cfcb4e2e1c9f2de941b675556a6adb7d`  
		Last Modified: Fri, 02 Jan 2026 19:58:16 GMT  
		Size: 314.2 MB (314246938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29743d3b75f9533084becafbe278ef486808307caca1500207a285b9ea3beb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16327039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a391462719e6ed9b991c7839751c47f797ed6695a8e1a8426ed86fcfa251617`

```dockerfile
```

-	Layers:
	-	`sha256:03791360f3919c381923923ed5babca6587f10fab0e29eb963c45b023b21c66b`  
		Last Modified: Fri, 02 Jan 2026 20:21:30 GMT  
		Size: 16.3 MB (16316874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8426a6a8f2b84e0e334b443b047cdeb0c63e98bb22260e902b4fc823b9c793ab`  
		Last Modified: Fri, 02 Jan 2026 20:21:31 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e7b368109d15f0554329456a363187dc202ad791a661ffa179ebe5228fa60a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315668916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a817d2e387c7c0c20f349c397590628d296e39d00b69f92a8d29319e1607bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9a1f6e22461ab2a7c3b148cd7fd0131848ded4c904183b11402001b4c02c1f`  
		Last Modified: Tue, 13 Jan 2026 00:40:59 GMT  
		Size: 48.4 MB (48388631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023c3faac75568557121b3e0aa2c658af780e8a1a9143b42405a60dbbef8a126`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 27.0 MB (26996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8af6004b3a4bb44f014415532f591a277692d1804c8d47f715e1ffb386211`  
		Last Modified: Tue, 13 Jan 2026 03:16:06 GMT  
		Size: 69.2 MB (69226189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56476b5ea5eb457690e45ab37a809bf433dfdfd9590f390c524588409a87f0c`  
		Last Modified: Tue, 13 Jan 2026 04:19:12 GMT  
		Size: 171.1 MB (171058080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df98fe9dedf6d27fbe181915a83f5be5ad96cb34c51dba6144bf495529eda08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16080190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8af1f062d7768df3b401e4b70af3f53b117e29390eee8f0f0833e7eb535cfa9`

```dockerfile
```

-	Layers:
	-	`sha256:25724e792905f6c0bb6122f56cebe733b712b986b721aa5684a5b98e1ed952d4`  
		Last Modified: Tue, 13 Jan 2026 05:25:35 GMT  
		Size: 16.1 MB (16070057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befd65dd2273ff594308eeab92646c914e6ec0db82fa2b9c97d1fe9176631512`  
		Last Modified: Tue, 13 Jan 2026 05:25:36 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
