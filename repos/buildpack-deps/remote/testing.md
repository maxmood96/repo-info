## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:c2646e35c82f2c8cc0cecdcd615ce9365037ddc356b9689fc08fe83a946052c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:824a3da69c8e6b6bb58e4f3bed9e23c914be1192d120b4b352ae23b5c0ce0589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376856336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f079e0d86424b0ca6e74ce776aea8481e0d7bfd6bde18d61ae8ecac722bbb787`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9146d6057920f25892ed3e631287d1e0e740bd11f7e3dd39c76c478675de8456`  
		Last Modified: Tue, 14 Jan 2025 01:33:33 GMT  
		Size: 48.3 MB (48276092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b2bf2fe5435a7871b88dbb724a93352983bdb5ad01681e2165e7056a7fbf25`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 26.0 MB (25972171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032bdd1daea694fee79d797bd4ea26270b8efc19783b84bfdd169027d675bdec`  
		Last Modified: Tue, 14 Jan 2025 03:20:11 GMT  
		Size: 67.1 MB (67065294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31434e237fbd9b481cc25e850098140ec1c62da7828d968de14da49dbc25b378`  
		Last Modified: Tue, 14 Jan 2025 04:16:56 GMT  
		Size: 235.5 MB (235542779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1db41c33a3767417e93d173bf2618a84bc30e2854b9df165c1e63bfbe83cec07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16904281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a5815aa7b63448da6ab772c561f4c7be632d8d4f3ef1ed1d869a0a621aff0b`

```dockerfile
```

-	Layers:
	-	`sha256:c3e34458ca0ce99574e0f1bacf78adeff7d83acc9e9a62c9aebbfe60e42ec7a1`  
		Last Modified: Tue, 14 Jan 2025 04:16:52 GMT  
		Size: 16.9 MB (16894088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bae787a117f91ec2c5b71f59f2126bf5521f3c77f75842ffcbaa091ce9dc311`  
		Last Modified: Tue, 14 Jan 2025 04:16:52 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:42acbddd88b8c2f9e42f0a46d8e2eaec20aeafb4b636d2fcb07560c15aa38c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341916089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4234ab059a6b0b97bcc14cb3c44b859d4b38c5b40adc54c05f45e268df22a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76cad3cf5a6ccb480f47b45bb1e37068b6554531620fd6fa1a71d8bd07d07d73`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 46.4 MB (46441720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8fffcdf3a616be17dc58906cdefa8833c6afb82ce71878155d250e95d14d5`  
		Last Modified: Tue, 14 Jan 2025 06:09:57 GMT  
		Size: 24.7 MB (24664103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f91cfbf6c5d0b11eb36fffec7e0d991a9d0c8dc91887a15d7aada2df4fab3ec`  
		Last Modified: Tue, 14 Jan 2025 09:34:29 GMT  
		Size: 64.5 MB (64487465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add04e7c3bf8460d866d5a8a6a4ab5b87878a8ac04a971d99b0190cecacf7e91`  
		Last Modified: Tue, 14 Jan 2025 11:03:56 GMT  
		Size: 206.3 MB (206322801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd93778a7d02c449822c06dc60e5211a5d56ef79911c4d8d890c5f6a9f846250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16672124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fb63f2ab516bf2b54bec660ad1bb7d29f3446035c4b8a5487088546a1fe64f`

```dockerfile
```

-	Layers:
	-	`sha256:85109dcb5789b576cb2bc4f5884501150cece09e245a825023b6fcc011b41e5f`  
		Last Modified: Tue, 14 Jan 2025 11:03:51 GMT  
		Size: 16.7 MB (16661872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9bef0f103e880a32446fa921dd59f4f2af69bdc2a7fcde166f88a4dd94371cd`  
		Last Modified: Tue, 14 Jan 2025 11:03:50 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6d5652822bbc0c3bcd4b1eff1dca2f76d1b48d397e547616f82d9638477e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323923481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b323295859897e21b08b6202c32b50b7dd25c1b6061ba4a47ba1a4430b263824`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9300ff4f70721ff1e9737e80c1a1eaa49b83fa08a552177c95c775ed44606a84`  
		Last Modified: Tue, 14 Jan 2025 22:01:42 GMT  
		Size: 193.6 MB (193641875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef0530b783e5de869f817fd642dfb1caef42ac28d62ce6e28fdb91a456ea0c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16671715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a75c8344b5fafc11d176ae43785d83e5059676edb9609011e2396efdb61abdb`

```dockerfile
```

-	Layers:
	-	`sha256:d25c91edb4beddef9af8441097837eeb335ad8933a5e6625886cf33db46cfcfc`  
		Last Modified: Tue, 14 Jan 2025 22:01:38 GMT  
		Size: 16.7 MB (16661463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad274817363339e07ad186527b366b93e96d7c027a00944b37f01ea200af71ff`  
		Last Modified: Tue, 14 Jan 2025 22:01:37 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a64b528a91b982ca51b72ba47a808f07b867469d5da3954dc0a664f09f5b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368167662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41f5d3261ad99085f5e16f4d0a6ea0ee11050b3a28df955008125a52b7e3761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f57a614701f3245516a9cf7adb78fd0830fd5bea39e42e511c29cd73c44a41`  
		Last Modified: Tue, 14 Jan 2025 17:14:04 GMT  
		Size: 227.0 MB (226977944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3c7d09cfe30fefb345323728b6556604e927d8c2a7201ccb407f5e42cad7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16990040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb21a81412050be940a80a673b2d3dcb80be439fa563479e47b233929afbed70`

```dockerfile
```

-	Layers:
	-	`sha256:02eb0397b03f384d9a6d137f8060b59de6798f4277e6b7155091f20d26610ac0`  
		Last Modified: Tue, 14 Jan 2025 17:13:59 GMT  
		Size: 17.0 MB (16979767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc21006030d24c01acbe412539fa49a96ffd74930fd6fc2d23963e3bbc70eb9c`  
		Last Modified: Tue, 14 Jan 2025 17:13:58 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7f98f35579e0cd6463e5b9e579980dd21c8d1977b1b554af623128e212ab6ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385453738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abcaa87aa517ce4139d1e1dac6cab82d9047ffad276c3f30e5ad0ef2f9cac50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b7bebb3fb62b18c851bbf703cf6a1caa57f7ffda09b0b23b4e4cf1051c666c9`  
		Last Modified: Tue, 14 Jan 2025 01:33:38 GMT  
		Size: 49.7 MB (49675708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628707934f13167c16796e4cf79505bf1ee994868dc399d6e208f3c459420999`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 27.1 MB (27114070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f322000966464f5b86dbc320a5e9d43083269c9387f23cf70a903c8da719c`  
		Last Modified: Tue, 14 Jan 2025 03:18:19 GMT  
		Size: 68.9 MB (68866928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c01ded280d151f27a6ab6885cd56876748451d6bf705e4598086945a4def5f`  
		Last Modified: Tue, 14 Jan 2025 04:17:16 GMT  
		Size: 239.8 MB (239797032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:494a17dfef5ff44db3d36bd99057992250ea553d545836cd024535a5a2e8a3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16873091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c03b09d0dcf270009d7470b208fbc6998cfc5872c5b1be4688dbdae3c58460`

```dockerfile
```

-	Layers:
	-	`sha256:1cb306e7067a494e3096cabcc4ae7ca0a90878b89adde0579bad8b0832f52cae`  
		Last Modified: Tue, 14 Jan 2025 04:17:11 GMT  
		Size: 16.9 MB (16862920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de746c714c14d4dff5bf643f073a23a90e66caee350640e7fc8eca6834f8258`  
		Last Modified: Tue, 14 Jan 2025 04:17:11 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:aa5fa8fee1a908124ae3adc565543dfbc931cd430a4c68f7ad938fbcee2333fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354487822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af426ea9e9fe6cb17eb21147c060df9727d22c4a02f6d69ce356aad9242482b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dad556c93c7fbd44bd1df34a958ab27627b99c3df6076447109ea0903c46714`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 214.2 MB (214193873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6353c960241b82e055e52d6a26b7606c8831cf880e464ed1d6255d758d19c3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5a82460cab0b82fc4e9188547d910028f8cab28c7d7bbee19dc3cd407f793`

```dockerfile
```

-	Layers:
	-	`sha256:4569235f2213d7cddb66a73d7068690a1abbeb777a4852b2697d7d207f52d8fe`  
		Last Modified: Wed, 15 Jan 2025 18:16:07 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e7ad1938d3920ab76b97cdb0269dc3e146e5e6df9228703a73d312deea2b970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384517027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fe2d0729ff9734c1cfabfd95b52648072a577e4cb67905bada67aaa788152f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c13c3f363d5cb80dd126d46dc749469f09c6bcf87873368d4910edf4c8fab0`  
		Last Modified: Tue, 14 Jan 2025 13:08:14 GMT  
		Size: 232.4 MB (232418269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b272982f72f68b67efc7c6a61a563586c1ca471dac11804f4ebea07fa02c30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16893502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9551896361669f19dca1b2f2bfc5f14df31a73639e98be441623b4ab72783`

```dockerfile
```

-	Layers:
	-	`sha256:d0cebc80f7ba1e831ad0fd69b4cdb1a684550f85676baa46a01a0369228a2278`  
		Last Modified: Tue, 14 Jan 2025 13:08:11 GMT  
		Size: 16.9 MB (16883277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8973654c9bf96e1c45cbe69e6de6aac1822ccbd7a68456b5b54d6b1a3e3b206`  
		Last Modified: Tue, 14 Jan 2025 13:08:08 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c269b72c35b95814f21ceffb69ec1624b4531d8b4e87ab81af3ebfe16b455a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350086446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd137b601fa29b6959f2bf38bf9a5799d3bb6d994f910d052acbb470373194d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a96882092e58b6b0f460c25e0b3fa57215487e6282387621e5c4dd2314637493`  
		Last Modified: Tue, 14 Jan 2025 01:38:54 GMT  
		Size: 48.3 MB (48329740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c639414a48a5e91286e442a3c2a376c94650966c4fede85d34f85e98bf430e8`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 27.1 MB (27131328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a0617227e41b6c45ea475d62d65ee6e02048cb238dcbfd9f884635a3d44568`  
		Last Modified: Tue, 14 Jan 2025 09:12:11 GMT  
		Size: 68.2 MB (68150739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10418c2ff73fdb0d646523d4f04c8033e632051fd913baf1a7613485f088ba63`  
		Last Modified: Tue, 14 Jan 2025 11:20:04 GMT  
		Size: 206.5 MB (206474639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80aae46b3af426dfe933e73c3da2bbc571f3155ad4fe717d4b07aa2dd9e41901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c455383ad764fc23d63f45994189401ea53025b6068ce94683f5defbe2125b`

```dockerfile
```

-	Layers:
	-	`sha256:dd52e57c85451a22dead751eaa430c4c6b1931235c8b39a3e7252e0700730938`  
		Last Modified: Tue, 14 Jan 2025 11:20:00 GMT  
		Size: 16.7 MB (16676901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01ba2d6246ad25bd5819324375382448632dfb6c3c500a62dd94402529f9ffa`  
		Last Modified: Tue, 14 Jan 2025 11:19:59 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
