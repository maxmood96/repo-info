## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:a4772c86738ece1dadc0a62a8336d9ce7d9d9e1f472ca66f3e97596693f4c4b3
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e93045f462e0b6624a16edc689086d043a00941981aa1add866faa18a297d201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351986667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ba54dc40a9db6b65848210c2351d99c74e8c7391f1ab54930866aa432be9ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:19:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:38:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a3b9aa5dd67fed7efa597566954b806b6c17ff4757052490684a87ba9c100`  
		Last Modified: Tue, 24 Feb 2026 19:20:08 GMT  
		Size: 27.3 MB (27263732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee694f6c4343c44df75d6ec35f4054147fa9bad772a564b5f1de4cfec3c634b`  
		Last Modified: Tue, 24 Feb 2026 20:04:30 GMT  
		Size: 76.7 MB (76661494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f684dc9491aa6e09cfaee0f1f71aae624af4aefac394de5f04568139c80bf4d`  
		Last Modified: Tue, 24 Feb 2026 20:38:59 GMT  
		Size: 199.4 MB (199394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6443a8669f2fbda7423a480a61e83672f29fb947a8198e6879b88308bff389d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16879764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134d42fb7205feaff9b5c26598ced64c9a59d19b72a6bc2c6314949c02eca3d8`

```dockerfile
```

-	Layers:
	-	`sha256:1296c1b36463d9542e023c831d9456d0e81e63366327f5ede3920a261e8efa64`  
		Last Modified: Tue, 24 Feb 2026 20:38:55 GMT  
		Size: 16.9 MB (16869631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8659bea8d63fa9a892b525e7f529d19b20a2b6862d9a603ddfc269a72ff9a7e2`  
		Last Modified: Tue, 24 Feb 2026 20:38:55 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3666d6b9948525fb4f4ff4ed4d123228ca266c698a466e234b168a459e2b34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297054891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5feabf53567bfe4dff7ac0db6846f14b151b11b5322427ef172ff896f06406`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:21:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:659484058ac0aeb678184c63f6d8d114ad6c5b9d6dec2a7ef5b116eede567c38`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 45.6 MB (45617401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe3a9f29c87d719cd363c9ea832a530a5b4b4746470456e3c9b94d23ec5870e`  
		Last Modified: Tue, 03 Feb 2026 03:32:06 GMT  
		Size: 24.9 MB (24914493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426290709456e99fd9663e54c2566f480e6c006819bb369d8169614f425f8cd0`  
		Last Modified: Tue, 03 Feb 2026 05:01:01 GMT  
		Size: 63.3 MB (63348709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d19cda7502ce7d0fd94cec7fcb20dd7a225ccefea8bc300fbe5e2eb243d69d`  
		Last Modified: Tue, 03 Feb 2026 05:22:35 GMT  
		Size: 163.2 MB (163174288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:009f1cc7b6126dd0d575c13ac08dd87160704b5d136cb73b7f8a4273004d8171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16127541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43f526d199147ecf9d491b02ba4da4793abdce6eb6d59dabddd30fd0c12363`

```dockerfile
```

-	Layers:
	-	`sha256:3241060ce0e3c0f48bed5c8469fe102f671afe93c9b930fab25d23a2d9b02b22`  
		Last Modified: Tue, 03 Feb 2026 05:22:32 GMT  
		Size: 16.1 MB (16117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8cad22d8eb05d84e2378c67b0592a1e3528ab3ba28dcfd90c2a69978258fb3`  
		Last Modified: Tue, 03 Feb 2026 05:22:31 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffbb372e2e9174e69afd1da82947276ca6994a8c74ddd88624ddc91a8224e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336942940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e2272b72960426c6ee40c5cbd1d9210ae27f4437d7f5ca7b9d5d906f36b94a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:45:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:21:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:02c386337e70e225c826a0b6295dc937d7a841e7301f60fa7a03adccf75af2ad`  
		Last Modified: Tue, 03 Feb 2026 01:15:52 GMT  
		Size: 48.7 MB (48679232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d5d2801ff6474ef689dcd67964dfaeac9d07e6acea8bddf570dd1be8c55d9`  
		Last Modified: Tue, 03 Feb 2026 02:45:59 GMT  
		Size: 26.5 MB (26523095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30714032e2382907ddbc5aecb4821586709d9c81d8af4a66dbe020f5684a50`  
		Last Modified: Tue, 03 Feb 2026 03:47:29 GMT  
		Size: 68.0 MB (68012476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf55203b5e22078fee7d8bdbb9b04739095289e37291516577680ea1550d92d`  
		Last Modified: Tue, 03 Feb 2026 04:22:11 GMT  
		Size: 193.7 MB (193728137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d57fbb6d43fdc21cd4762643df0ec593a825ea4fa7180f4dbd9dde4066f09ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16460811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265864f1c034eab377c22f3a6dd9b030d6909a17801585c15dba0b1ffee4f289`

```dockerfile
```

-	Layers:
	-	`sha256:3b87a184242cb4c7aa8e396c468515e74ae26b71ed80e532488a9e2fb22d36b7`  
		Last Modified: Tue, 03 Feb 2026 04:22:07 GMT  
		Size: 16.5 MB (16450599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d84c3ea64417ac0ad235cd9cf828737e72056749e93caecbf0ecd717211fbb`  
		Last Modified: Tue, 03 Feb 2026 04:22:07 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c45c85a761e02092eb1146e9c3d84b08c4ceb72ee103e281689f809f84ac9ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359882168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ee60bca2d33175a25dd8ad5ba531b0f0e132eff3ece6f73098852061e0d46f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:19:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3559a7084ebe893d133871358dab0d079615e3eaacd04f900b699ede2f39f35d`  
		Last Modified: Tue, 24 Feb 2026 19:25:03 GMT  
		Size: 28.5 MB (28522446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24f85b42485f9731950f1b8fa7613f52dc2e2ad73698b31dbb6e317dd54b8fe`  
		Last Modified: Tue, 24 Feb 2026 19:57:26 GMT  
		Size: 78.7 MB (78650294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bc3930ab66ad776f10019489a6aa1c6007ff2294c20efe0dd69486b9e08f6e`  
		Last Modified: Tue, 24 Feb 2026 20:19:41 GMT  
		Size: 202.7 MB (202687313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b4e34459401578e7ef5fb3faf905ffc5d3f165f1e6dcb5af728bbe31163a631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16848814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d80ada1cf8cc6c227effd73a144669c462fc150b6a9708a422c4d77d718450`

```dockerfile
```

-	Layers:
	-	`sha256:b797b306a7b828103283952d33cad6c8ea272fcbae4615b959842abf417c382d`  
		Last Modified: Tue, 24 Feb 2026 20:19:37 GMT  
		Size: 16.8 MB (16838703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53d2471c2a462e3ccf6366e8ba829dc52779ee5779d16dff694e005ba4242bf`  
		Last Modified: Tue, 24 Feb 2026 20:19:36 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b9b0c5635832d854ed9036632fea1413a9aedde68c8703a6266dad21cd6884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355180466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934635910964d46e6cfa07db9094202c43291118690adaff293a73a14ab809c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 05:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 12:43:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73480cc26c615330eccab26ce34bdcf83d5889a7e09a86213699bf4e4f64bc74`  
		Last Modified: Tue, 03 Feb 2026 01:14:38 GMT  
		Size: 53.6 MB (53584520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46f8ef4210c5f651d581237fe6e5782b63d5da72519ff94633f59a07cfaed33`  
		Last Modified: Tue, 03 Feb 2026 05:23:30 GMT  
		Size: 29.5 MB (29509264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe352572c54ca60911e991f1d6004a94abce88a3e25f468b3957f438bb769286`  
		Last Modified: Tue, 03 Feb 2026 10:38:09 GMT  
		Size: 74.0 MB (74007895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca3e48e72f3c09f354b55767bd42551242a2ade35bc54f6da5ce7a067209ead`  
		Last Modified: Tue, 03 Feb 2026 12:45:11 GMT  
		Size: 198.1 MB (198078787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d660448515d1378467e6598d2470ab3917b4c1ef57cec347fb36e99498da124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16344887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730d035dc4b67638b400a3a794d09a998ada0b2ccb966db81d445c22fedf20b`

```dockerfile
```

-	Layers:
	-	`sha256:a75316218254885b67fdea6e40742bc527d059ea0011c7b6bf8835861821cecd`  
		Last Modified: Tue, 03 Feb 2026 12:45:07 GMT  
		Size: 16.3 MB (16334722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7156b2f49090b2adfac23b03922bfff25f6fc6cebb7bd83e5dada7e5b96f8eca`  
		Last Modified: Tue, 03 Feb 2026 12:45:06 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:20880887ac662555b4405ffdd286802836b4fd3cfc33843f00d2b613d1b80a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462333400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4886d743725242558ab6174a9b21bbba6fa1a183af4e894e7e4121607f529141`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1769990400'
# Thu, 05 Feb 2026 03:14:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:50:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Feb 2026 23:29:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48f09a2bb3a57a16959e5ae66db8cd1e1c1ed0c93449352dcc6fc0b64e55cbda`  
		Last Modified: Tue, 03 Feb 2026 07:02:16 GMT  
		Size: 46.9 MB (46890143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0416dc273ac7c8750810633c99f22464f2e2bb48f2a6515852ce21ac1a4a7c0`  
		Last Modified: Thu, 05 Feb 2026 03:16:37 GMT  
		Size: 26.8 MB (26767187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40443e0d15d0b1f4d6ccc3b2b45d939f99796b01564ba57c27e672dd399d532d`  
		Last Modified: Fri, 06 Feb 2026 07:54:03 GMT  
		Size: 67.3 MB (67275341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cdc8b06a575176b654014f8c626ecc2dff3faf8ec6c469d72566176d07778`  
		Last Modified: Sat, 07 Feb 2026 23:44:45 GMT  
		Size: 321.4 MB (321400729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0d4579da7f359de22d382693a17dcf77cf96273501fd28bbe3d8f602e387531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a34649c1bbe6b01a98eee444db3243e19fb2cce94e43dea28ad51aae8cfe46c`

```dockerfile
```

-	Layers:
	-	`sha256:ec368744b27916b048f23654ac05dc0f453bc1485f8d2c9832777d8625797caa`  
		Last Modified: Sat, 07 Feb 2026 23:44:00 GMT  
		Size: 16.4 MB (16404187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0119ac7dbb6dca55b1bc23a643aee0d64af276db814c1b0de6a0516d026c0c5`  
		Last Modified: Sat, 07 Feb 2026 23:43:56 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:be162ccf02d71fbbd14582ab3609944f62d4f8695e96c2d7645bf16853dc0ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cf126f747e326f2bff9ae95b68602064ec505b5c210488dff0e889d015914f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 03:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3bfb68c2648b1088debcce6bc605d7ea6709b6f129c9ce647bf0a7c385d8350b`  
		Last Modified: Tue, 03 Feb 2026 01:13:18 GMT  
		Size: 48.4 MB (48421195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd1e07a5a5c7ee531c5adb5cc340d101adfb8e3eab835cd2272f521de25591b`  
		Last Modified: Tue, 03 Feb 2026 03:45:17 GMT  
		Size: 27.0 MB (26999734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903e028f5ff83b35a3c307b4e4b9628f0b8429f5ab23010d2101829884a6eeb`  
		Last Modified: Tue, 03 Feb 2026 05:29:41 GMT  
		Size: 69.2 MB (69166722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa7c665631817fd69fbb1273f3acc4812270df409f2328ff6218de18832430`  
		Last Modified: Tue, 03 Feb 2026 06:15:30 GMT  
		Size: 171.1 MB (171148813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b9e16943bd95fe59a3bba4d1b03b2be0758e22eecb0783f785b40362b771e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16144088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baee110c81065679e12eb3d5cc74ed04848a41c664d0a45fe4046dc694f56a8e`

```dockerfile
```

-	Layers:
	-	`sha256:541cc9c25fb9069341e04cc8862898dd403395c943b03a4f4b3d885db82b4f11`  
		Last Modified: Tue, 03 Feb 2026 06:15:27 GMT  
		Size: 16.1 MB (16133955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0449f3641bb0878155226784c40778b28bd307dc98a6d2b9159085b2f1cc276`  
		Last Modified: Tue, 03 Feb 2026 06:15:25 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
