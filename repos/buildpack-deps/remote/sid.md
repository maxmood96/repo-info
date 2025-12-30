## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:f619c3aec4f8a8460526ee13ef4d5c60eb5dbdac7983f31a3a7652583cb8a878
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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; arm variant v7

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; arm64 variant v8

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

### `buildpack-deps:sid` - unknown; unknown

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

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b024f273adc76cdeb3af5320c64428857e61fb5fb60654d31fe3b7a54ad7082e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351554181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6dd70112f981795353bbf3706967f9863b9b5bda571c126123b0534cbe3cab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:52:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217ad4932c84f70ed9491cf091cd8265fbcd5562d33475dc1380251ed82c8c60`  
		Last Modified: Mon, 29 Dec 2025 23:47:38 GMT  
		Size: 28.4 MB (28407813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4886d5c61711ec5b4b405d5f907882fc1f09575f0c9a0648a6cd1812bdd985f1`  
		Last Modified: Tue, 30 Dec 2025 00:34:24 GMT  
		Size: 70.4 MB (70408066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859bad38c10533ba14080390db16c023b16b0155f3869f0f291efb9369bead40`  
		Last Modified: Tue, 30 Dec 2025 02:04:47 GMT  
		Size: 202.8 MB (202799156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:67c844bb936791f8d7530d8c58528616536de5ad7c4f279fac271b47d06a12ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16248923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5d04e63be5c4581be1b25357c920b241cb0affb1f32073822545e166c899f4`

```dockerfile
```

-	Layers:
	-	`sha256:61fcd4b70a8321f74e84f20fd0f850c3ef0d8e76588339b628c1847f1de02af0`  
		Last Modified: Tue, 30 Dec 2025 05:23:43 GMT  
		Size: 16.2 MB (16238812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8df5ea87e6bbaeac880524c9bfa1364399efa594bcebd371884cf0aa4d92908`  
		Last Modified: Tue, 30 Dec 2025 05:23:44 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6f26e4453e1f3cf280d8636105407e8e0f2dee976fa89d1cd58b96ed42b1838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348290913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bd8e4883c6c4448654ca0c7d60c16ba82c83326c29a90219afc13645bbb6e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:31:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91f19749139bb2193587558635e0a320b0f29835fa1325bcb8c73b48ad8b72df`  
		Last Modified: Mon, 08 Dec 2025 22:50:49 GMT  
		Size: 53.5 MB (53494424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a82bf53318ee9ff50934cd5a455b97b8549b92db55df72cf410249ca6112c7`  
		Last Modified: Mon, 08 Dec 2025 23:23:07 GMT  
		Size: 28.9 MB (28884607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e0f90ac822b83290c4938a8d44e3bfd579a2891eac5e11b8dec4f3a80cf68`  
		Last Modified: Tue, 09 Dec 2025 02:11:35 GMT  
		Size: 73.9 MB (73921341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eeaa3713eb2b2168c3281b5659dc1e0be47bbb9fd7a59a257ce2c86ac33053`  
		Last Modified: Tue, 09 Dec 2025 10:03:52 GMT  
		Size: 192.0 MB (191990541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf1c5b72ce2943b9556f92e3eb46be917dc56eac79ea63cc063b258f445d951c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16261852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad855282ea4285ec2d611793f9c8d51ebbc5a2de1a6028bee1c3fcac3dce3f0c`

```dockerfile
```

-	Layers:
	-	`sha256:2328c630cfbb172e749f794e3d43dbb900617fec570b3dd8e0ec5f1737f6507e`  
		Last Modified: Tue, 09 Dec 2025 05:23:02 GMT  
		Size: 16.3 MB (16251687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b5a9b131b2a9ecd8f2449ca93b8caa06bdfea369a2553bbc8f44c43a66a97a9`  
		Last Modified: Tue, 09 Dec 2025 05:23:03 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0fd2ec2f13ddee70f856dd4c2fcb9dba2e9df4384bda5ab95bcbf6a5aa127c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.1 MB (456101164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7d72871e5a0c5bf5acf72f3218ca9be806c75d395a479565c059ed6391e7c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1765152000'
# Thu, 11 Dec 2025 08:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:21:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:109a9388fb2c93203e12f30aeaef237cc88f26bdfe719e6c75ba4b856571d621`  
		Last Modified: Tue, 09 Dec 2025 01:53:48 GMT  
		Size: 46.9 MB (46917024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6713d289f87fadfcb1cc49dc5c1255a2e68dec8f35d177d80c213c8c3d375`  
		Last Modified: Thu, 11 Dec 2025 08:37:29 GMT  
		Size: 26.4 MB (26413809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a6f1c36dc6239a02beb52306b77dfb11edb7a5a71763ffc22541d84875bb0`  
		Last Modified: Sun, 14 Dec 2025 08:44:39 GMT  
		Size: 67.2 MB (67233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51718b5dcabf7be1aa6c2ccbd7b32debce4d8f3ea0075d9828fa3ee5810df9e`  
		Last Modified: Mon, 15 Dec 2025 06:41:29 GMT  
		Size: 315.5 MB (315536715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bba480685c44128dd895f36697ac1d7112322fd14ea0c873093c3bbbbe4ee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16330606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d110314613cb97c7236f4ad6cf24ae5be531186e95747efab9c6bb56ee3059ca`

```dockerfile
```

-	Layers:
	-	`sha256:19f59e41cee61c7b91ccdf085c0f63f2f710a9cfd3612a9a352174c3d6fa2868`  
		Last Modified: Mon, 15 Dec 2025 08:21:28 GMT  
		Size: 16.3 MB (16320442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b329f6f1d058e35473695b4daea2bc5d92f94f1fbd8e5cfa346085239cb076`  
		Last Modified: Mon, 15 Dec 2025 08:21:29 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1ec80dc70d746ae898003f26d448a1a2c3275ce15fc96090a8b0bd8f609ef94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317810442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c60ec694d2ba22f9527bdf13dd7d592bcd045f8c589bd7cfb7ad98aed6899c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 04:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:12:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d1672feb37bf4d7307a6feb7cf62c56febe8495830b9f965806ad0a97fe6efac`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 48.4 MB (48375355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244417eb312e7e292025b53816a5625d309f746b46cf7d1aa0e277e78d585a2`  
		Last Modified: Tue, 30 Dec 2025 04:13:56 GMT  
		Size: 28.3 MB (28256642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc743120394a36380f161c5b1434a6f1f501cd116c70ceb8fac78a9c4aa0051`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 69.2 MB (69164822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ff4e7a3fa99c046317ea226630a50a99e65f0cbc21e778aa031a23f53177f`  
		Last Modified: Tue, 30 Dec 2025 06:15:26 GMT  
		Size: 172.0 MB (172013623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6be5eae0dd910abb578bf22be11c8443c0cd6d7a25b6b4d4e14197c8a19e108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16056360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d5e6fea717676edb83ef78db449b4217708562eefd8fde6993dd5432c17151`

```dockerfile
```

-	Layers:
	-	`sha256:101d1f1faaa660b251acad5df98aa6bed3719239a8c7e7e3a1fa2d75f917e631`  
		Last Modified: Tue, 30 Dec 2025 08:21:30 GMT  
		Size: 16.0 MB (16046227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d58f4ba0e461034e914d4fae687cad44373debd5a7c87d1c4e86eccd02daea`  
		Last Modified: Tue, 30 Dec 2025 08:21:31 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
