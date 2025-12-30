## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:b1be8d5ff5875d23b7cdb7d43feb820ef60f291d39b1b46591a1b829a7c13c15
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:89f23a128637039e9590189e920d318065a0592eaf9d4f653e501243a9696bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378660455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b943db9d1c87a4772d9fabfcc812ef2c2ab1d3b2d149a8a45baf113e61b1700`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:40:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e37abc533a09f86edcf3602251a61a6208ddaa131e1a1d5757e5f94a54d645`  
		Last Modified: Tue, 30 Dec 2025 02:41:24 GMT  
		Size: 236.0 MB (235979646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9369c3a26b826a49efd42e6e0df6697c34a5a53dfc3a04fa8c60ebd2799c3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c689d816d3b1ecbf2c957a9d6a40fc72abaa576efbe166ae56f3bd9c52a34aa3`

```dockerfile
```

-	Layers:
	-	`sha256:24cb5c676a45d2f29f933468c35d3dec747d3de67a95ce8baf5d961dd89b9a7e`  
		Last Modified: Tue, 30 Dec 2025 04:25:01 GMT  
		Size: 17.2 MB (17207381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb08dbd3703eb02a242085956ecb75c9033bc1a5286d6bc345e5b50978956d2`  
		Last Modified: Tue, 30 Dec 2025 04:25:02 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1ab8dabe087fcd38a7ef10dc3a85ee306d43b09678e3321b4186a1df1b35114b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342820521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ba9a3f90eac4423240e1ab76b74a80778cd8d7ec03a12bab75b0313806709b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:32:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a515687a5a3da2827aa6a3b8071d1f515ed0d5cba1dbfad9af02797c060c18`  
		Last Modified: Tue, 30 Dec 2025 01:51:10 GMT  
		Size: 65.3 MB (65317909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68072cf099e255739c5dbed1ad6775d11fb11c6212d9e07f276471ca4f471e33`  
		Last Modified: Tue, 30 Dec 2025 03:14:24 GMT  
		Size: 205.7 MB (205708113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6e87887173047386e4093b742b5c61ec32c2e7d60ae92fc8447920c9e7cc56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16980113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774abe92b15fa9798ab21433b08fe7662265f19edcdd0a51ac5a3f29a6785ed9`

```dockerfile
```

-	Layers:
	-	`sha256:84521c46d9a71bfd94a73a06fc06c0261aa64f3464f7f804a791e280eb299f6c`  
		Last Modified: Tue, 30 Dec 2025 05:22:11 GMT  
		Size: 17.0 MB (16969579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cfb1860a388eb0aa83f043e7348fc4108b748a9d050856a807e9a9eb40fced7`  
		Last Modified: Tue, 30 Dec 2025 05:22:12 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d4206b2733f9a3f8c091ff596c3709c7bc09dea4d91e974b73d84daabc567ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325311683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a547185bbc91be5f817bd96f44f2207147bee70d444534fc185278d5a9c15a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:35:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed5488c5068f5c77a6b4b6f6b02bab38e7073441d08f85d6bab0a94c1cae889`  
		Last Modified: Tue, 30 Dec 2025 02:36:47 GMT  
		Size: 193.3 MB (193259793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47d6a2d99cbcfb47289450d3495b029aed66c488c251f9fb3c74b0b30af18825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0547d033f828be31592080f97aad74c46de6e3cf7e715c939e9498057f2a7f42`

```dockerfile
```

-	Layers:
	-	`sha256:3b6046108e1a147be4bfe9f32cc010b36a986f51ed019ca5245825663c3fe61b`  
		Last Modified: Tue, 30 Dec 2025 05:22:25 GMT  
		Size: 17.0 MB (16975369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e65d0e3fb6a11839a396cb2a9028c0d60f513a988db812221dff258b58775d`  
		Last Modified: Tue, 30 Dec 2025 05:22:27 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ec36d1f055d3d797565009dc9ef0124c6a854bca9e59da6f3ad0ed87760ffbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368360928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abae91d8b345300a0013ebadc909c4e497f9729b24d0b420ffc53f1253d344b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:38:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba313b9abd0e83099c56d61a9c6454295140adbe52f5e05df85e9dc33574fe4`  
		Last Modified: Tue, 30 Dec 2025 02:39:58 GMT  
		Size: 226.1 MB (226105906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed9cd4c6a91931d7925f49d6a35baf2890bfbdcd10f50c192014d3c1243597b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17302229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1496dcd121093d3e32e0b363d5d57ce2181e612d5b2a18b296245035041c196`

```dockerfile
```

-	Layers:
	-	`sha256:794d84949c041fd364c9eb5e90497bd00061976ad16eca11e6f90e6dbf02b91f`  
		Last Modified: Tue, 30 Dec 2025 05:22:41 GMT  
		Size: 17.3 MB (17291675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd09c4b3cb04596e0b3b71c3aad2f99cd865e280b20a04da60e61af2d6cd808a`  
		Last Modified: Tue, 30 Dec 2025 05:22:42 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d7b98ae5f1c813c67a3354f11585933ff3e8bd2e0c21933762dfac0e6b691bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387448148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d3a87f21be6f8bab795d1233a0ec64fa2061966b87a5cdfe2035141b95b665`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b502d5bfabc8613c27931d0c9c661d4d6c91e79ad218bc5c52c7134f82acd5`  
		Last Modified: Tue, 30 Dec 2025 01:53:41 GMT  
		Size: 240.1 MB (240075297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a6e4b63984d05555f914d701b4853824f8e1293c5498c0f559310a44943b613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d40064861323d56ede424538ed4f0d710ced36c192b4a50dcac8117bbd1ddf`

```dockerfile
```

-	Layers:
	-	`sha256:4e8114cb27aa9a7579dcaa048a5cc774080541203d955eedb38d82d9c6f9f84c`  
		Last Modified: Tue, 30 Dec 2025 05:22:55 GMT  
		Size: 17.2 MB (17176974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d09946ea79477bead55887543c6d9b2d1343f0e00aff46020fe463744ea9ef`  
		Last Modified: Tue, 30 Dec 2025 05:22:56 GMT  
		Size: 10.4 KB (10434 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9760d28fcdc9d5d5dfcea1e4b56b9f58832068df53a41631c110ec2e1bca739a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384234327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3692082d0ad494b5f82f9571c5f3671923486981670c1bd50ab467f82ea7fff2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc59b593a33ee8746f94dd61c3d4d2abec3c25d3c7e93e36a9043ee716aacde`  
		Last Modified: Tue, 09 Dec 2025 04:45:03 GMT  
		Size: 231.1 MB (231106988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c7386ce4884d1c8ee2d50f3dc2135f5a1bc5e1c81eb41eecef5d917cc7b044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f777ed4bc136b478234f9cccf6d43062fdab518d9d3e58e434a3bc95bc37aa7a`

```dockerfile
```

-	Layers:
	-	`sha256:0d6018f0ceb675ae9ec899d7adbf518d8875dfd91f9144b749a2173fd2fe4fe5`  
		Last Modified: Tue, 09 Dec 2025 05:22:01 GMT  
		Size: 17.2 MB (17192876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c3d1f1f6563dd81284d09c3b0e5dc400a83ee2c524919364c75c8f13701309`  
		Last Modified: Tue, 09 Dec 2025 05:22:02 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9a7bcfae3fd3f72b87c3bc94c33bc9102742ada99be131ce850d6b1d88f45868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462271510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af1f66294eb9c47b90134432e5292ab8717e5aa7cc6a8630efbc218e30a5500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89b1e152c7f5b34657f3a6e97a87170ecf850bc400696de74b3929bc238f0d3`  
		Last Modified: Mon, 15 Dec 2025 06:59:37 GMT  
		Size: 322.9 MB (322886042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9aa3de166fbcbb589ecf72a66426401f5ac2f1042220bc51ca7aa820f8c525cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17274019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f691a547262e11fa430d939d9ac0809bfe74a794c6a2a9daddb4d97a18f9f3`

```dockerfile
```

-	Layers:
	-	`sha256:2f2acf4ee4ef18af5b0162cff20339e454b2227ca89334e606bcd55be3490782`  
		Last Modified: Mon, 15 Dec 2025 08:21:19 GMT  
		Size: 17.3 MB (17263519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645ecbfa721f66d25047f554dd420a505b9334c0ff031c5fb29796dedd03228e`  
		Last Modified: Mon, 15 Dec 2025 08:21:20 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bc892098ce5b4371117778ac77b7626f83fe5012856d0e9b3876ce30a9710c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351235259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb3a404601fb419b23d313052461aec7b97b472fb844ef6da6eb2d7fc2a2a0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d6b6af65161fdf6adbca5b49fba0d0a414708fb199521ee78075952e4ba4ca`  
		Last Modified: Tue, 09 Dec 2025 02:59:04 GMT  
		Size: 206.5 MB (206478489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2de6eea32a4c931484689a077fd95179d1f2b556517cf8cc9b1f9bb21a558f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16995022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a531de00f6f2c14b865cce0d537ee7029f3ab71b3629b6f80efe246a029b7f5`

```dockerfile
```

-	Layers:
	-	`sha256:79012e8d3bb3447b32400ddc872c2fd958488f430efda167ada4a57c67d4f592`  
		Last Modified: Tue, 09 Dec 2025 05:22:23 GMT  
		Size: 17.0 MB (16984560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a902a384375eef2994ccccbd218cdd9176a7eeb46fa3e38e7140e46963f1001f`  
		Last Modified: Tue, 09 Dec 2025 05:22:24 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
