## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:a3c0605ff8ad45698ccf167699de5b7f07be3a2426ac342c7b2274259ac53965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7982e24731ff77cf276e0e3107fc0167e1a4a94c77447a781f16012f9e89b0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283168581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696062cec73d0b4cc2f7afeb8483d0c5f247b4848bac3bfad4d4100c9f326e07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:56:19 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4403.tar --tag 26.04
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4403.tar
# Tue, 17 Mar 2026 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:32:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:19:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:353172d2243ba412db836ee33433b5bf98b7b5e712d6a842def962f77707b920`  
		Last Modified: Thu, 12 Mar 2026 21:05:56 GMT  
		Size: 41.9 MB (41855369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b2f35783e4f17e635643c3b9a28f61d865c4853bbcc849e003c0ec3fe5f4a`  
		Last Modified: Thu, 12 Mar 2026 21:05:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475b6067e1c976b66998cdfd56bc20f210af1c6cbd552f2dd21127fa13f29a24`  
		Last Modified: Tue, 17 Mar 2026 01:15:36 GMT  
		Size: 19.5 MB (19524392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea5ea9e1677e25f72e17f23b3742d51b399b02ec77158e93f5817df2e1af9e`  
		Last Modified: Tue, 17 Mar 2026 02:33:17 GMT  
		Size: 49.8 MB (49815129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b8b2ef0e4bfe61f315ae498e69ac5b27979317a8f1192962c0fb4dac64e5a8`  
		Last Modified: Tue, 17 Mar 2026 03:20:21 GMT  
		Size: 172.0 MB (171973284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fc7656bdc9182a1b16121284624cad39cc1861b8a8a8ef3173cb0a436283581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13005937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d47ed31e1c4d7407c5d1bbf14d3f2cd2c7aae19727189ea7bdba1b61cac6ae`

```dockerfile
```

-	Layers:
	-	`sha256:b38267b65c04dd7a22c59c6149af712f31d6eee650397e3d10d4ceb1bd7313f3`  
		Last Modified: Tue, 17 Mar 2026 03:20:17 GMT  
		Size: 13.0 MB (12995469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d26dd1f9c15ce5f719d53bb227be40b6beb73c56b2765f9dce1c4d853d1a818`  
		Last Modified: Tue, 17 Mar 2026 03:20:17 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:beae59f727a1935049536fa5b12c1ba97d51665ed5ab458c3358bce60e66b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237253848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a446bcd0c9c71265a6495a6a263f993ea5162787b6db0d530337936693ec154b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4503.tar --tag 26.04
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4503.tar
# Tue, 17 Mar 2026 01:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:17:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f698dda2de4e496f317e4914f05ad776006c478a9d69939a895f32c14ceb6526`  
		Last Modified: Thu, 12 Mar 2026 21:06:26 GMT  
		Size: 38.9 MB (38857394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9654d2d19664354ab705e627dc9112e60cb09f957b1d848eaf15ccaf2cbca838`  
		Last Modified: Thu, 12 Mar 2026 21:06:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b4821ddba9f62cd63e431042544efbaa19e2d5fd5f747ec179f809c5d2b2a`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 17.8 MB (17815757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2221f0541d0205e31ad9ab60b2a6ac6aa1f3da89bb4e37272bb559417fe200`  
		Last Modified: Tue, 17 Mar 2026 02:18:20 GMT  
		Size: 52.7 MB (52667351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0e094fdfa5ed72d814bbc610c8063a12e2b715cb3d936de097aa3bc64a14e6`  
		Last Modified: Tue, 17 Mar 2026 03:18:32 GMT  
		Size: 127.9 MB (127912954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de786667b97ce947b32820b75a1efc35c85b4408562a7eb52aa2825fcb342284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12746910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edac6a7c5df4140d174cc9ecd0143a3b0167f3af7db73d70b79ac2df13dd57fe`

```dockerfile
```

-	Layers:
	-	`sha256:bfb6ef9ce0a65036fd3fea8881812c0cd320a5ae9e3ea8f3fd4590b5ec572c8f`  
		Last Modified: Tue, 17 Mar 2026 03:18:29 GMT  
		Size: 12.7 MB (12736379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe74622a063100c5117dac561458aee5585a7f27f199b0d14dad9ea549f7a94a`  
		Last Modified: Tue, 17 Mar 2026 03:18:28 GMT  
		Size: 10.5 KB (10531 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24133b2a0fa71b2a3eb318bf7c0318698076d7952cc562e83914ae4d5edb37da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271733179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633afa535427d81ab361cbd779d4a5f8ed7d27b0aab12821b09d92761a4f9000`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 20:00:12 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4694.tar --tag 26.04
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4694.tar
# Tue, 17 Mar 2026 01:15:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:22:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deb605ffd5670438453f8cd18a0a75ac48b6f24bca27ba1a64802534315973b1`  
		Last Modified: Thu, 12 Mar 2026 21:06:05 GMT  
		Size: 41.1 MB (41064498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41816bff5f93f99104877eec3ccaca96ca2567a60b68cf2911937f97162d4a5`  
		Last Modified: Thu, 12 Mar 2026 21:06:08 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827eee8a5d03fb1b3cfadfdc7c60123e44bbefdea49f5e8ce8acad24e20454f7`  
		Last Modified: Tue, 17 Mar 2026 01:15:42 GMT  
		Size: 19.1 MB (19061953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e1c90ba0c3c664a710cc7747df3a96a7104aa5b4813f95fe43c425108431bb`  
		Last Modified: Tue, 17 Mar 2026 02:37:30 GMT  
		Size: 49.4 MB (49419901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498ca39b6409e3a11e24b57a771cd067f789e7731ffefab8668b3600255ea514`  
		Last Modified: Tue, 17 Mar 2026 03:23:26 GMT  
		Size: 162.2 MB (162186438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9945070c43d30366cc541b1cf51f3d47e2e62bf151649e24b166cddfa6e23483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13060193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d459b34319d7468c21ba0d9662f26e51f820d6641d16353d9dcbd74d4415fdb`

```dockerfile
```

-	Layers:
	-	`sha256:0c41285cb7060bb63da1a0e904557d7297aba1398b9fccdc10fec1c09ed4fc5e`  
		Last Modified: Tue, 17 Mar 2026 03:23:22 GMT  
		Size: 13.0 MB (13049645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff4ad51fbde4f0e6eedaea54b7a43361743e4118930aa88430d8a69f7d21868`  
		Last Modified: Tue, 17 Mar 2026 03:23:21 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1572597e98cfc0a807bae528db97bd2b4cff1f6b4587cb39914518d934c0298f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294812424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0295c92391f4b79a5573250929f08e881efcca4f26efd7a7120663ed9ff152`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4386.tar --tag 26.04
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:28 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4386.tar
# Tue, 17 Mar 2026 08:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 10:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 19:13:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:156c83341267c02582e0e71a15211bb9aba279b6aac901dda9314275f1697d38`  
		Last Modified: Thu, 12 Mar 2026 21:06:15 GMT  
		Size: 47.1 MB (47086183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5631416101e6b03a4223b5a46f1ee4455ad18cc314cb342ccd1664177bd4d7c0`  
		Last Modified: Thu, 12 Mar 2026 21:06:18 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96e7028ebfcf7af4af7dd7e82fb30c2a8a898cd2b0959b5d749640c63f3f93`  
		Last Modified: Tue, 17 Mar 2026 08:28:55 GMT  
		Size: 22.0 MB (21996205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8c82b8867101b4e31919249b2159e7b9cdd7cf8a715e4ba9276463f5009230`  
		Last Modified: Tue, 17 Mar 2026 10:25:11 GMT  
		Size: 56.1 MB (56078301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589b107468e2672a9b64099cfc246829a2933a9404f573f84e117a12aef6f218`  
		Last Modified: Tue, 17 Mar 2026 19:15:11 GMT  
		Size: 169.7 MB (169651346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:706b5afe9f7d4e1151fba4803904d91596ffc838ded745dea76478ec158161c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12978590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed6a1cb250b9667a2233a9e84a713b726b42281d4044601f42f3cbc3a28e910`

```dockerfile
```

-	Layers:
	-	`sha256:60e323f0b8a7141e8e80b2f2db0aa66fbebc8e2e89511d35277c6e0ae1e55fbb`  
		Last Modified: Tue, 17 Mar 2026 19:15:07 GMT  
		Size: 13.0 MB (12968090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61766055992249869d8c56ded78427d51c5cb17b819c7a7024278834fd84041f`  
		Last Modified: Tue, 17 Mar 2026 19:15:06 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4641dabcf2fe35e8cc07024008ec1446fcebea8006349fc56888c370c187466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259586294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd23a41db3c7910e695c7ed15a85346950e284d8d1683c20b0baa1440815a91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:59:05 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4449.tar --tag 26.04
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4449.tar
# Tue, 17 Mar 2026 02:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 11:59:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdefaca172ef708c1d64fdd846fca9c7c20ba96b3ea558c846a6e034985975be`  
		Last Modified: Thu, 12 Mar 2026 21:06:45 GMT  
		Size: 41.5 MB (41489128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99e8c75de62bbc8eb709650e730f26447a7ec4a999f02969cba49315e474a97`  
		Last Modified: Thu, 12 Mar 2026 21:06:48 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91370cb2ea39bc50fdd0bcb30ce054d63afb19753b5a1e066f3a7328b088066c`  
		Last Modified: Tue, 17 Mar 2026 02:20:19 GMT  
		Size: 20.0 MB (20002693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d102bb2d97db4e0299f1265fe08feab0c7fe7f373e1d4106b25caeb53b38c037`  
		Last Modified: Tue, 17 Mar 2026 03:22:58 GMT  
		Size: 51.0 MB (51032278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a4c34a772ef90991a30a0564b52b6483c29099620785d4469bde64957ee656`  
		Last Modified: Tue, 17 Mar 2026 12:01:05 GMT  
		Size: 147.1 MB (147061806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:68429ab53f137f6af862a9bb3771de24c25645414ec220a306f9071ca8fd95fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12791877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81e144b2c9cfe38fc552780cc008e182b54436493f9935a843b02441ba2009b`

```dockerfile
```

-	Layers:
	-	`sha256:939bb5d3c98bdf983dabdfea988cd3b4e54e879d85d747c74d32aed0ebb80ca0`  
		Last Modified: Tue, 17 Mar 2026 12:01:03 GMT  
		Size: 12.8 MB (12781409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83518ff4183227ca24fb25e08dc4aaf75512eaca7d1bd75bbf65faff353df22e`  
		Last Modified: Tue, 17 Mar 2026 12:01:02 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json
