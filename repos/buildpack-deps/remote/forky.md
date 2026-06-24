## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:8b4d9077a3016d90258a2f68582c86f27417cda990e1ebe7f9565488868f1d5e
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:adcae8030b0aa64e7bb07e6f0b4255484b7afa6f9d29e4b3ceb10596f39458a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351968273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7ac63da9e7de76076d6e1cd275dbe8d3cf949231e4d11aa0b7032be545b8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:447e2db1403dde86cfbb4e736a0555036d98321ddc327da9305db2a007cde1f2`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 48.8 MB (48757790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fbe9d185e99fa84c122139e8f5eb118264f12c2739d72b125a4024012aa961`  
		Last Modified: Wed, 24 Jun 2026 01:41:37 GMT  
		Size: 27.9 MB (27906956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46dfc6d731baee823ba1e8a0ef9ac7372d172c399b7f8df359b41cefe80fb1d`  
		Last Modified: Wed, 24 Jun 2026 02:29:04 GMT  
		Size: 76.9 MB (76935076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3545d83483dcf3e9eaf76f7e5108943250b442d163860a5e1c02fb89f04d2b8e`  
		Last Modified: Wed, 24 Jun 2026 03:18:08 GMT  
		Size: 198.4 MB (198368451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48057e3792c2281b7e9bfc65e1aadf74d1f75f724bf7d7d22dca984410cd25db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16837910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbed35ab657df56f9153082c4c8d50eb2297eea45d223751a0f32c033e9140c`

```dockerfile
```

-	Layers:
	-	`sha256:3201dfbd208c4df64454f59a2559006b963558350158791bf3ceb8f4c25f2851`  
		Last Modified: Wed, 24 Jun 2026 03:18:04 GMT  
		Size: 16.8 MB (16827766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42024a85800bc31b89ae7572cb0a7e965b5d70ea0a15deecd4f12983e96c09d`  
		Last Modified: Wed, 24 Jun 2026 03:18:03 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d82630c03d4e454161c746da0f7f6f8560e8c8c4ada29e914b2227f47e151d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299238567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457a90dbc2742c09774b16b17c8ae41df5c4dea9378e526f78ad724a442f4cfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:44:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:20:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd14977d91415ae0c2f3a09dcc1dbfa071bbc9d1eaf7ceed6655fe0e671e8d27`  
		Last Modified: Wed, 10 Jun 2026 23:41:34 GMT  
		Size: 45.7 MB (45676562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f62967a713e6868315df8fff6281864c11e6f1bf85c4ff4746f06a1c2c7935c`  
		Last Modified: Thu, 11 Jun 2026 01:25:13 GMT  
		Size: 24.6 MB (24579632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ed9ff89ddc0e8e4bde82bcf767d8515b2d3abebc9c2125ed74145f8b0678e`  
		Last Modified: Thu, 11 Jun 2026 02:44:42 GMT  
		Size: 71.4 MB (71434017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94b5125968b952616c149b4566ad931d071e1fe8a5e08f246dc9d2d950eb28`  
		Last Modified: Thu, 11 Jun 2026 03:21:15 GMT  
		Size: 157.5 MB (157548356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c11d50228fb50ee7e19ac9556306e6a0bbb4986c00e4bbe53c5aa29f8e5c293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89f83ac0077e9a6b21d41641efea3db9785d66370bfe16c3eba95f2a63ef183`

```dockerfile
```

-	Layers:
	-	`sha256:72fbcb14cfb9338ec70582c3e5abe0ce1dd002dbe4a5224f6341e7c051727c6e`  
		Last Modified: Thu, 11 Jun 2026 03:21:12 GMT  
		Size: 16.6 MB (16621745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57745a417b0b48c4d6375049415ae439ab2c036cd5eac2127f4c3fe6ddddf53`  
		Last Modified: Thu, 11 Jun 2026 03:21:11 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bdd5579e884d3dcbc50f5b81bd2372dd6bc1b318d8d351f38eb9ee63878f1a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340467816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868aae4b2dd8768cee89a3aa40b6b323186a51ba093a3907e0633703c4b0de9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5991d5bb2fa21186c9152bf0a9fa1c9c73892f68235c440c9967628fa5ecac9`  
		Last Modified: Wed, 24 Jun 2026 00:27:35 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6ca5e706504383a18ce6cb67cbeb352fc200523287b4db4c777b56d674314f`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 27.1 MB (27111423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e562ebc808640f266dfa12e53d32bf4287ffa8b4390ee319de6e6435fd2fb`  
		Last Modified: Wed, 24 Jun 2026 02:35:38 GMT  
		Size: 76.1 MB (76103880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e0533929b76db64145777ec5a876bfb5e027a3f6e076dbcd8fd4e15f4b8ead`  
		Last Modified: Wed, 24 Jun 2026 03:17:50 GMT  
		Size: 188.5 MB (188483801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea71dfc90e57fe185a430142f34b140d6ea97c9f8faf15ef10d473860f024902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878bfed4d177c0b3d036a0a498483008c28ec2bd5dcdf67375828ecfa1099753`

```dockerfile
```

-	Layers:
	-	`sha256:931fdd14bd7ead53f1d53ffa14c0d4e7e2a6f4f3bdbcf41b9808e38c373a10ac`  
		Last Modified: Wed, 24 Jun 2026 03:17:46 GMT  
		Size: 16.9 MB (16933922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03264676e671cd270e452dfb91031373b7dfaec3f320f9f90f6ee358a7ff1fa3`  
		Last Modified: Wed, 24 Jun 2026 03:17:45 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af48de16d2d5f8ec51e0c4e9b84eb9ce78294ee65e8343dfa6cfb295161d40fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362342292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baaf504ac7463746f41805ba84fe993c1f9ad62fa72a3dc89869e122ab58287`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efb4928ebe54ee107e6463403a2a4853abe521d8dabe3603a0df92499fa85ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 28.2 MB (28164931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d199197c3ac4542d3e5be264b601c0923a198de45a4b527c9ba6b3bd662bd12f`  
		Last Modified: Thu, 11 Jun 2026 02:25:02 GMT  
		Size: 79.1 MB (79074755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273f3607257ab36510131316d2146584bb49f4f8013a1a1b105bf5404acc781f`  
		Last Modified: Thu, 11 Jun 2026 03:17:18 GMT  
		Size: 205.0 MB (205025796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7329d7f40a1012a58831672ce26dd5b1b3141e70ed8b4e204508f6fbd1789400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16845789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9bbb76e7031715b489ad19fe1a8a91f5c37020fdfc61a6108fc01a55a3bd70`

```dockerfile
```

-	Layers:
	-	`sha256:ef9a728d1b6d419b133d9859cfd1fe36583fc0b961bef6f7377cc95902f36829`  
		Last Modified: Thu, 11 Jun 2026 03:17:15 GMT  
		Size: 16.8 MB (16835666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3caee39e43846e89f828bfcd49f757f5ed970af9fae778ed7ff1f189804de1d2`  
		Last Modified: Thu, 11 Jun 2026 03:17:13 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b9fb4967940c89682f3afba55dfedc361a657ca39314e8f05ae276295a52458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364027871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a4f62c5368f04934a557dc9a6f6e725e42a26bfa4059f44aca1d07816f145`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:45:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a6e9fc5fff5ecef539442636839ebbab04ed9b3cd7caa39a93b1023297047494`  
		Last Modified: Thu, 11 Jun 2026 00:22:03 GMT  
		Size: 54.1 MB (54103105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ae67043641e8afbaed6931d7c5b7fbf2860dd1ffd02c08f3ccdcf4f71c0dc8`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 29.3 MB (29286641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2adee366a695e860bba6b9b864396a612d4bad8c56699d51febd6115cfbf5f`  
		Last Modified: Thu, 11 Jun 2026 10:27:41 GMT  
		Size: 83.5 MB (83454656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dc25232a11567acb43059c509a72ae012e0c9b18ffe28586086475b14dd1d1`  
		Last Modified: Thu, 11 Jun 2026 12:46:42 GMT  
		Size: 197.2 MB (197183469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b569748e7363427af9e35e9d78f326f4bb80088f3d552e5a697d69109a1626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16826849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12d57cacdcfcd9cff31d56ccf96d26f2a32008c26d201ac838b879a1d5e5df`

```dockerfile
```

-	Layers:
	-	`sha256:44c584be55d8044c6227aab42b49b4de5966c55f2a1886fa747f76888e9f6412`  
		Last Modified: Thu, 11 Jun 2026 12:46:37 GMT  
		Size: 16.8 MB (16816673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31fcc86ec9f97062395db47ae5dff21655b82ceb0eb8446d689bf18d0b93d9fa`  
		Last Modified: Thu, 11 Jun 2026 12:46:36 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:86e2bc741d45d221cad453e46b175df8bb073c54fb1d5ea279ede612c1220799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483605041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebca1ee6e62d36b3f056bdd724eb147628d63f9757b8980724387a0c86c3b7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1781049600'
# Sat, 13 Jun 2026 04:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 16:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 18:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ed3cb07ce8ad88fd9ce6ed049f21f5d3412d5a91293105a260fd0d8e0631f44`  
		Last Modified: Thu, 11 Jun 2026 02:45:18 GMT  
		Size: 46.9 MB (46868403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb714707e363663ab0edd89dc96807f795de4da64598f885f54d7c7c44ada6`  
		Last Modified: Sat, 13 Jun 2026 04:39:40 GMT  
		Size: 26.5 MB (26471353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3c19fe899b06864910dfe2969dca7d63f75a9c740280bf6017b248680b7d6`  
		Last Modified: Sun, 14 Jun 2026 16:56:08 GMT  
		Size: 77.7 MB (77667866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c213baeea96014b6cdcdf5f218c2b77e14567b8ec30c51af6812231ce35bd2`  
		Last Modified: Mon, 15 Jun 2026 19:01:57 GMT  
		Size: 332.6 MB (332597419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d9c553aba6be5f653166139f5b5621b146e4ba5c51fd8853366fabc9bc9b142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16910772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6e790504ba681eddc56190c364f7ea3c6f256b3452ef24b5c8542c36b9ccd3`

```dockerfile
```

-	Layers:
	-	`sha256:658ad52bfcb40042074c273d9d51fd4779a186d232d71d741dfa60064a428ad4`  
		Last Modified: Mon, 15 Jun 2026 19:01:12 GMT  
		Size: 16.9 MB (16900595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f1f806847fc60bfce64a7e01ba794675627f606b838b5235936eec8d4834d4`  
		Last Modified: Mon, 15 Jun 2026 19:01:07 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a05989d6613d5e9885c73f9547e5bb7feedb561c43f67a84babe229391d7dc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327118071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74a3d6190de0d63161d9609583ece1b6f63182a142515625eb4cbce02a77ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5198203a924daa24fe6af49f715c31ab29dfca39eea778fa09abc744d2bad231`  
		Last Modified: Wed, 10 Jun 2026 23:41:11 GMT  
		Size: 48.5 MB (48513108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede4a9f8d2cf16954d7483762c1a757bd649ba11bd48dc0e08d51861877f2e58`  
		Last Modified: Thu, 11 Jun 2026 01:44:12 GMT  
		Size: 26.7 MB (26680114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccda3e4041c62fdf0380dbc6e327f0ed32531c1d9a4fb592c7a1580acb6a13d0`  
		Last Modified: Thu, 11 Jun 2026 03:26:59 GMT  
		Size: 77.5 MB (77475379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a54d70a86ec298967b1e89de8055bb4b1c4cdf853111adfb0446be71ecea443`  
		Last Modified: Thu, 11 Jun 2026 04:16:46 GMT  
		Size: 174.4 MB (174449470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b0c24a44cd98d3c5832450aa5450da45756e78a83065f42fdbcd8ba7d6e2c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821528567aad1b3ae19595e65c7ae678c8524f762f57432ce97998de7cb809a3`

```dockerfile
```

-	Layers:
	-	`sha256:e740204952c2b168332527ed8325f2662564c9e35865d9dfc826c2b5f026a26d`  
		Last Modified: Thu, 11 Jun 2026 04:16:43 GMT  
		Size: 16.6 MB (16620734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeee73bee314745bb304642938214daeb82af602971be651111e332335d5912`  
		Last Modified: Thu, 11 Jun 2026 04:16:41 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
