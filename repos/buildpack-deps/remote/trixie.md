## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:ec46294f477c43267c4027ca9be3ea642dd5e5f712c3d7f9bea8decf81aa6b4c
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:adaaa8f2b162e17331dd9574f39e65744d2050ecc0ee4f9fdcea9f077a688ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.0 MB (376016797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5f5ccab4d7534b313601a130c99d95de1717afc7afec5e63b16a609bbf5b8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5dc28167de372c586b840aa2cdcf07e2afc8e85b392a5dbb5552be77587eff75`  
		Last Modified: Tue, 24 Dec 2024 21:32:36 GMT  
		Size: 52.2 MB (52212351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfcdb7af4643d9e902826381436aafc5ca852c439990983daa707960060dbc0`  
		Last Modified: Tue, 24 Dec 2024 22:15:33 GMT  
		Size: 21.4 MB (21406167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389a305f06858b3033956e0f308da92fdc18e3e15dddb5afd66e1616ffcfefee`  
		Last Modified: Tue, 24 Dec 2024 23:16:10 GMT  
		Size: 67.0 MB (67018604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c2ea474069b99d6b2b055dbd0819660c3cb0372d1b8e4d77e2fd06db7282de`  
		Last Modified: Wed, 25 Dec 2024 00:14:11 GMT  
		Size: 235.4 MB (235379675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb642860809212e93f27fbc700a6f85e8ffbf35e4add872e76ebc5b70efaa72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16915583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816596efc782cddb18d460aa720ec36bdd21844c52d62c8c4c55342be138ea88`

```dockerfile
```

-	Layers:
	-	`sha256:5d02afd54f6acbb4b1de0d3a398a7e1b218594eec2108e28281415b76711701b`  
		Last Modified: Wed, 25 Dec 2024 00:14:08 GMT  
		Size: 16.9 MB (16905390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798589d5ed0a05ab2a00412dce5033f5d2d38bd7c105bcbf972521506818bf4d`  
		Last Modified: Wed, 25 Dec 2024 00:14:07 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:22c1c77575a3a828aa61d40b614beaae803882da68c24e50b9cef9b830c98679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339557430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed01d8967dcfd60f646f101cf8cbbd60a9e20b47e374a7ff6d5afddb4d20226f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5a5271e09aab30795789f051d2425121101b650637f36e772bdb80c62bb4833`  
		Last Modified: Tue, 24 Dec 2024 21:35:34 GMT  
		Size: 48.7 MB (48738917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd230c08c2a8f220f4a7754708d43b365ecaa32d038ae6429f10953c7ef0284c`  
		Last Modified: Wed, 25 Dec 2024 01:32:00 GMT  
		Size: 20.3 MB (20299500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bb5fbe3b18f1821e5711e289a996102173dec864a8442d53c9dfe3b763817`  
		Size: 64.5 MB (64463891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c4113b4c4091593cd24a82366f6dafce9dbd0dff1c42044d08d10817f0a6`  
		Last Modified: Wed, 25 Dec 2024 06:25:09 GMT  
		Size: 206.1 MB (206055122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1601199196e49ff48c6a1ca3d3b22e656850970860ac5a2a537b9fc6a127614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16678034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f601bdd7e680c0b395ce75cb81ca343ab246ef00fcf95c82084bcdf87b2c6417`

```dockerfile
```

-	Layers:
	-	`sha256:f7d35aea7fd68c1c077d8075ace8f75271fdb967769eb58927ff2ac40a7c53a8`  
		Last Modified: Wed, 25 Dec 2024 06:25:04 GMT  
		Size: 16.7 MB (16667781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f815d0e1e66c6f9f28c21a34fe2c5d1b338a2a2716ce55df5374d817167707`  
		Last Modified: Wed, 25 Dec 2024 06:25:03 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a47836e5c508b475db9d9c89b585d58fd0501e6034a00bd50a4acfb803714447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321708500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e196bc949cb19b117310f83bff1f5bf76bbf03c15aba9c7827f511d488e4d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7dbbd0b59e8fd2a826bed9f5cfe195c9cb61ad138accd85ab45d8f8eb5e53a51`  
		Last Modified: Tue, 24 Dec 2024 21:37:24 GMT  
		Size: 46.8 MB (46767965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a49163ae7afb92f788f8101a5f0b57af46d0766372255bb4e15ef002eddc2`  
		Last Modified: Wed, 25 Dec 2024 03:45:38 GMT  
		Size: 19.6 MB (19597771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3bbaffabd773ffb28e659f3ce21da08dd9edecbf06a175c763618e87bc80bf`  
		Last Modified: Wed, 25 Dec 2024 13:03:46 GMT  
		Size: 61.9 MB (61886443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0332ae04a6c07cbeb23c5633750d5f89826697230cf707a3872b4a1f1d6d3d0e`  
		Last Modified: Wed, 25 Dec 2024 15:52:42 GMT  
		Size: 193.5 MB (193456321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb1e088f843538bbe6144d3b05bc6832bad7fee83b6c7f253c6c9aeed809e9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16683832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b49594bd3f67434c1ba84700974bdefecba2fb150336d44690f57934d77bd6`

```dockerfile
```

-	Layers:
	-	`sha256:33c8ebed494fc8253894fa489d9373915306e9e7949c264d4913ef4c3219b98d`  
		Last Modified: Wed, 25 Dec 2024 15:52:37 GMT  
		Size: 16.7 MB (16673579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df733506f13c0adf93cb97b8f46fdc61dadf75176b2c00b6785c805f88509d91`  
		Last Modified: Wed, 25 Dec 2024 15:52:37 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ae230f4566071f6d657ac22ee6ec6d0a1cd06400bd739c482967535a013c244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367298278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a6667e5fdcdc95a6e2c6149136742302e686bca947665fe721825430e8e837`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:655b7ff6f79a823125a6f22dacb056ef3cd9ab7e8eb5ffc6594ff4745e276b8b`  
		Last Modified: Tue, 24 Dec 2024 21:37:11 GMT  
		Size: 52.4 MB (52425570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0f4612c729fd6c76a1191b59daef982c8369d9881af926e8193cfc3d012f9`  
		Last Modified: Wed, 25 Dec 2024 01:50:48 GMT  
		Size: 21.0 MB (21033507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e18c9c2923a1302f47d950f9dac6c92729acb289e93f1f208c03390958b352b`  
		Last Modified: Wed, 25 Dec 2024 08:14:04 GMT  
		Size: 67.1 MB (67110988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd821e8af16ec0695d34e8b63a23dcb9f336977326363b00993a56776751923`  
		Last Modified: Wed, 25 Dec 2024 11:24:38 GMT  
		Size: 226.7 MB (226728213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:842f61f3c350b79feee3a175b3347a4cf0127c9b8b53232b14e73f37c7738226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7586fd03028640d71914d98a800ebc45887d4e8c88d3ffa96cf5de6cb72808ac`

```dockerfile
```

-	Layers:
	-	`sha256:dd038a982d16dec6cc62538849dada44a648bc34955fb2908189d6f0148319c9`  
		Last Modified: Wed, 25 Dec 2024 11:24:33 GMT  
		Size: 17.0 MB (16992168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:955bf5d529410dde264b0944c65d725f97847e73cba4bd5fbe378ae01b91dcce`  
		Last Modified: Wed, 25 Dec 2024 11:24:33 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d7e76776e86187e4f361b6f4b01f753c706558bbe91fdc332bf697b6fcd714dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384023541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac787fbc8d57f120a4646f3c36e8524f40628442559a5c613be70991af18ba8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099da81c5d3f4771071b424bb19cc8bfc272821672d87e1978f2f206f3040f4f`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53029057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26fe834ebc7804c0441c6204e790d670676126e97ebaad982188f420a6aa9d5`  
		Size: 22.5 MB (22510156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb826681a9ebc8783590b4b5076ad7abcfca5c59d820cfc6e4d1027f2e2804f`  
		Last Modified: Tue, 24 Dec 2024 23:16:11 GMT  
		Size: 68.8 MB (68817374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f84fc4c254042aad982cd12f1e994ea23225a130e6d27f6c46590fe1093ecc8`  
		Last Modified: Wed, 25 Dec 2024 00:15:40 GMT  
		Size: 239.7 MB (239666954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99dcc19ac33e8ebdcc099ab0e78319b285cf9513bdb943f4fe1b98ae486f83c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16885185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e282c5e0afdf948fbe7534ac0dc75f3103c7a59f9b97ec8df36c262985358788`

```dockerfile
```

-	Layers:
	-	`sha256:d82d93dadab5cdd3334cb13a4be9f1df68c26fa3da0a86c33de6afa7a8c8e872`  
		Last Modified: Wed, 25 Dec 2024 00:15:35 GMT  
		Size: 16.9 MB (16875014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1ab22491342b2da6b718c7973c6718c1901214e3bfaef8777461788bf5d3e0`  
		Last Modified: Wed, 25 Dec 2024 00:15:34 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9779c10e341fee951056ab86df9a5ef929b45c8760c01c93b3978fb06ef36031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352610159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8530884a0acabad2bed9b97119c64f2affce9da41270473fec5081e584965da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c43db2a2d96e4b42b073ee755704e1052dfc08d2fed2bad739906e6663926d9`  
		Last Modified: Tue, 24 Dec 2024 21:35:59 GMT  
		Size: 51.7 MB (51716844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb196cc5b6a238393d49fa4e93d6bc6fb9d8eb10a08514c2266839519f9d3f69`  
		Last Modified: Wed, 25 Dec 2024 11:49:41 GMT  
		Size: 21.7 MB (21727749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f68c6043110a4194987507fa740e27f0945cb8eaa1052f3742a94320b81d1`  
		Last Modified: Wed, 25 Dec 2024 19:21:22 GMT  
		Size: 66.0 MB (65981009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c292c9aee94f7deef7c4cc9d03d982d791a1b67c609e00133ce584b9a6a2bc`  
		Last Modified: Thu, 26 Dec 2024 01:04:07 GMT  
		Size: 213.2 MB (213184557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e00855bdcee6bae04d746065a5baf3c376d7aec8c0dae8c303dd231b6bbe0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be548f019a3a9346b1fca9e5eac0422c19614e7dcc9c32a665324496749b49a`

```dockerfile
```

-	Layers:
	-	`sha256:6c0476c5de7c6eb027a7099066d88a1542d79ed142aa32d213e9c3b1a6d2d720`  
		Last Modified: Thu, 26 Dec 2024 01:03:48 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bbe2e698dbd1ddb9fa4cf8177e032ec0ebae53c8576ceab293e5c3fea7262c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 MB (383612450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac45450e5124aada1826263ad122d103b3e1468912dad334cf538cfe4424ded`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7d0c0062851cd41c4b765bee1eaa246592e96d9c4a0268bfea5c5d2a73be0e62`  
		Last Modified: Wed, 25 Dec 2024 00:36:18 GMT  
		Size: 56.0 MB (56044104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e488722a9275f087219fc61d856ea4c4ed4b328a7554350726557ef4cf4353e`  
		Last Modified: Wed, 25 Dec 2024 06:15:57 GMT  
		Size: 22.8 MB (22784408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5632f8c74ae00f98037831a4cdd3b0a421b4a43e35eb95c52372989b2288740`  
		Last Modified: Wed, 25 Dec 2024 09:46:04 GMT  
		Size: 72.5 MB (72534331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99492dc1e2dd6266dbf4725aa7787b6f21c7b15ccfee8fe1652d578abe30ec8f`  
		Size: 232.2 MB (232249607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74a3efe172a8e1cdc301b9b901e714a44f1f6328b3f96fd30fa516b4f2ac7b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16898629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d84daf8e1c0b38eb85efa8979c2ec86823793a1eccb6aa4f1d7c3e3176454c1`

```dockerfile
```

-	Layers:
	-	`sha256:e7b78832f1c2d52c65a7254c9abc0d8bd618e474f71182f52f47be905580d1d6`  
		Last Modified: Wed, 25 Dec 2024 12:58:40 GMT  
		Size: 16.9 MB (16888405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdae38bf5c24c5df7cd900fc525ec96181acec4fa85707380ba09c5913c1e356`  
		Last Modified: Wed, 25 Dec 2024 12:58:40 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9c18ea725791e007beccd79df1848ee78699d7cd8f61c7741104ee1049464d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349191951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef66b3cf09aa6ee781b6e06c10fe590d740c7755549c210b7d44e01e18437e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1fe280a5056c1901421b5598ff050c78aa067b752ad527583fba85c589bb647`  
		Last Modified: Tue, 24 Dec 2024 21:37:42 GMT  
		Size: 52.2 MB (52167537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb20153a9b4c7c97b49477bb7e12772fe5782559f417bb6517d244a48d7108`  
		Last Modified: Wed, 25 Dec 2024 00:18:28 GMT  
		Size: 22.6 MB (22603773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07fbd06dbc0259f8b92d4683dee4083fe7d2a755f0c0ab5b7d6848714d1ec49`  
		Size: 68.2 MB (68159261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eba6d13f29d8648a29f93bae4679e6d4e413781eda1a680bf1ec99dedd5d614`  
		Last Modified: Wed, 25 Dec 2024 05:15:19 GMT  
		Size: 206.3 MB (206261380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:855cff196929d4f33b39acf7eedcc2318cb1187f0301d597902585e3ceed7211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16693001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0b3a75c950a934919fa95bf3ce9be098a211886186138ff41de4a0ce81b856`

```dockerfile
```

-	Layers:
	-	`sha256:063df13d5cd9bb320c17f7571bed74ede815fa433119cf1afe706d0c70deccc4`  
		Last Modified: Wed, 25 Dec 2024 05:15:15 GMT  
		Size: 16.7 MB (16682808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3885cde1d36d91fa09f3a634b7a4886a4a5377042ebb14886ee7b94aabe35b2b`  
		Last Modified: Wed, 25 Dec 2024 05:15:15 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
