## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:96099aec728521f5a11d5b17a195c8c6b3bec3188c76080805a71eccbfdba0ea
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
		Last Modified: Wed, 25 Dec 2024 04:51:05 GMT  
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
$ docker pull buildpack-deps@sha256:c54092137aef82673b628701fffae1d7bb5cdee16036652cf8c5680b2311507d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320566678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69e8784e9a9a24c7018a57f98312596b243e702223ff357301ebb75ff9f02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2250e50c3b0d1679c6a6f0905a6bb14cdf995965365d96a0ed0af0a1cabeda41`  
		Last Modified: Tue, 03 Dec 2024 20:11:47 GMT  
		Size: 193.0 MB (193044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f0d17f8af67e79adb9ba470f17c5f6f7b4423ebee7b062e14e0213e7ddd14ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16741713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbf3a659f9762253c3305e4a0dcd4ebf822c59152a12c4d414fb236c480a1c`

```dockerfile
```

-	Layers:
	-	`sha256:021ec9171dbfc19c071bd17673d2e89c9aa2b95717e117707175c7f3598da4f0`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 16.7 MB (16731460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e86dd2f315ea5820a2680250233eb394bd4e588be2acb1a7a10b9232f138f95`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37a190a761023c4e140ccf9149b71929db84f08fec40f69f81803e339f665a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366490575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbec0ffdb40aa93cc2227f7e64678ce9711e69280737c2d9d4a8a2a696b515e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95ee2ae477988acf1c4f6dcfc88e1ae5a55fd73cb1208a350d7951447cd5c2`  
		Last Modified: Tue, 03 Dec 2024 16:25:24 GMT  
		Size: 226.8 MB (226790649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b69fd275d0a8e244814ebfebaa3277de3c5c799239fc1179eeb59b49cff6bb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17061306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d61e81a066f2bf03ec9ede670c559770001733b72dccaee56894ce1afe09a2`

```dockerfile
```

-	Layers:
	-	`sha256:10fd39fd24a909e9e91ac353e116e838d10121424f2fb2dd2eb94b5253aef4c7`  
		Last Modified: Tue, 03 Dec 2024 16:25:20 GMT  
		Size: 17.1 MB (17051033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781c922e20f55229b5dc779d96f6a85737b2f5c7ab8068980abbb055be1f8609`  
		Last Modified: Tue, 03 Dec 2024 16:25:19 GMT  
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
		Last Modified: Tue, 24 Dec 2024 22:14:48 GMT  
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
$ docker pull buildpack-deps@sha256:6aed94b346224a907374352ffe52a244f6fb845bb6fa77af0dbf33caabf6b925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349523155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8a6f92b61aee8dc5319671b6c4838f2c5cc076f392dd5e5a5ed52f09243017`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cc02c1e97f3987f1a40bace25f4f97248212c53b960fbe66ac9c773ce7ca2`  
		Last Modified: Wed, 04 Dec 2024 04:58:21 GMT  
		Size: 211.2 MB (211218722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62a3dabe91f7108ef0c06eb9b6acea0b172d897697c9160cdbcb678f3da17ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3266f96a84806158d2d80e622846075de301f496c29d3f3045aa367a97adb73`

```dockerfile
```

-	Layers:
	-	`sha256:daa5a4b1199b129238891d666d4691b1ba0ccaa01bbdc77033f58a0747a4a008`  
		Last Modified: Wed, 04 Dec 2024 04:58:02 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6664a3df9dc9bec277c19ee01729befd3ce661e183f2a0d86777890babc7a779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382552567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645f0cf430b3644a88d2853e79a959d668b36a2196104d494e19ca8ee0e1e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52a720b71dddcb2a25df1c62f4df5be637ee1b44f6c72e886501e695c3e8491`  
		Last Modified: Tue, 03 Dec 2024 16:21:25 GMT  
		Size: 232.1 MB (232135861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46c273b1c0cfbdacdd361fa947c0ae293856b1182058b608e17adb484abd5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972b3130f5c0e09be05cbf098c2fe9f102fb226330c6a9f77a9e59b4e34ab07`

```dockerfile
```

-	Layers:
	-	`sha256:a680bd893b317b1e20138c7cae82c062fd4718a73928c1fe154c9a60ac52e652`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 16.9 MB (16946559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3348c230fc094aec79e85591b44365b40fe471dceb5ef063384a1515e5721ca6`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 10.2 KB (10225 bytes)  
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
		Last Modified: Wed, 25 Dec 2024 03:31:21 GMT  
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
