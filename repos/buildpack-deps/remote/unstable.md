## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:ee00c4343df5e77dc5b45029db9e8f1e209ab8bc0b89f0ceb5531a1eeeb0703e
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
$ docker pull buildpack-deps@sha256:0dee52c6cedaa0d4ae0dc2ba5557e7912e7016272f3396fd5305bd8925c4febc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353405806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef12be07fe5681d484d99bf9ae5867405759e5da1b8dc97ad6e3613eed428f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:41:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bdf1cc0f4003e9838db969a7f68f358aa3694f09878b6330bfb2bfae2ae4e1`  
		Last Modified: Wed, 24 Jun 2026 01:41:40 GMT  
		Size: 28.0 MB (27989488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77188881b92a70e569a04653be1cc5a84ad94e829327ec62634c158933342f`  
		Last Modified: Wed, 24 Jun 2026 02:29:06 GMT  
		Size: 78.1 MB (78104952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ddef2f9cfbe701150a57490827ffa49c3477493f6ec0eb0a6bf867c9abb40`  
		Last Modified: Wed, 24 Jun 2026 03:18:19 GMT  
		Size: 198.5 MB (198532987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a2d1a7347b836d94409a24a34760f63220a76cc5b2b05c12cb771d3bf67748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16899795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb47849fc8358ee0f748fe32afef2d2b2fc3c711ba22348530908cf626b1aa2`

```dockerfile
```

-	Layers:
	-	`sha256:e12df4538e0677f1ca9d7e853b550d3e0f0077d49bc6d2bb3294a99a571ca8ec`  
		Last Modified: Wed, 24 Jun 2026 03:18:14 GMT  
		Size: 16.9 MB (16889662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6e10af94caac90d8adb50c93d44ca645d9cf6ecc870a59b61e552d0a8404a`  
		Last Modified: Wed, 24 Jun 2026 03:18:13 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d0bdf77ae0ef0e06930949e12aa64d9020527af61284410882433520f6955c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299028341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7559bff23c23f1fe0fe7ef72fea4353a86a2624876929a2a963e8991ce285c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:19:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d675c589a8a116f3580b1211f18fa575a815f4d2314413ec9c2112d3a61d24a6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 45.7 MB (45678632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0274b6b7737c2b06a1765a2a054ed7c230000ea352ee09b5b9399df372d1dcb2`  
		Last Modified: Wed, 24 Jun 2026 02:24:52 GMT  
		Size: 25.4 MB (25374390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37df253c6d6f378f0518d7aaea7ba33d75f20fbe83a7121d649368c54d82652`  
		Last Modified: Wed, 24 Jun 2026 03:55:35 GMT  
		Size: 72.5 MB (72534381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b76d245c63dbae7d6b2f3b8866b079d7edfa4853e6f4b265430b949667f96d`  
		Last Modified: Wed, 24 Jun 2026 04:19:43 GMT  
		Size: 155.4 MB (155440938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89d45ef9150e90d02927333e8a6a789885483a2aabfccf1958966636af28e121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16681489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdeca5c3c3ed8802edadb960ed407518a4568dcbe01d98ed517b6b8340bca1a`

```dockerfile
```

-	Layers:
	-	`sha256:a3edc310d959febe762d2e53f4c8756fef48720dec62ecf5c30dfda6b2380ee9`  
		Last Modified: Wed, 24 Jun 2026 04:19:39 GMT  
		Size: 16.7 MB (16671292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ba0644343d9432556e1cd1d5df9deedbcdb38f4573ef5e93b4789402ca8b97`  
		Last Modified: Wed, 24 Jun 2026 04:19:38 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5d03f5d1c39ebe7fc842e9a3cebf10a0efe7955d4d43ba0e2ec6f29abfa0d73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341857988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68b49771112aa44f7a2f5a123dd507f4c8a4b7ac79590dcc7124487b3433493`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4fddf52615bf1690082a9d73cb8346614997b5b51315236c93a190fbd50fb899`  
		Last Modified: Wed, 24 Jun 2026 00:28:05 GMT  
		Size: 48.8 MB (48798835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfb65123f81cd28e0545a5e6f88cbd0f9d83e9d96851b068d4ef01e4482bd0`  
		Last Modified: Wed, 24 Jun 2026 01:45:17 GMT  
		Size: 27.2 MB (27192471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c9b6ebce9bb29252b4739ec42144f45c77d93770495e8ba1aae33ce9e58fdf`  
		Last Modified: Wed, 24 Jun 2026 02:35:47 GMT  
		Size: 77.2 MB (77220473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a89219f8dab5b732fb8d393960cceee262dad536008750d40830c7b7068488`  
		Last Modified: Wed, 24 Jun 2026 03:17:53 GMT  
		Size: 188.6 MB (188646209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e12251ad2dfa65433c4d3425c225a9a0e3b43ae114ba23e76e632e722c87f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17006035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec92823a7b2bf2b97c68ffb62f10cdd575f103f1031f6a929eafca16030e73cc`

```dockerfile
```

-	Layers:
	-	`sha256:e8fa8058d896935850fc6388bd5c827fe84519ede51b0bbaea4765b147fc97d5`  
		Last Modified: Wed, 24 Jun 2026 03:17:50 GMT  
		Size: 17.0 MB (16995822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e0b3a02d828c876b572e4c35680205ccd4c07a02ab0bf201d5c966852b396a`  
		Last Modified: Wed, 24 Jun 2026 03:17:49 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:90fd0f6e8e222d97b74513bda79e01bea2dc02c719c06f678d3e363a012d1cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.1 MB (361124386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0af389b6ea7d0f9c42e246196fb7600487e51ac9b5f9b57553b3d938e5a70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4172c1f095cffcf024eb812b3d434c5ab119bc7e7ccee1fb4953b378a0a4d2`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 29.1 MB (29117405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68037f55168642e1ecd0f5957b88e504644e3dce1e630af8a3fb3bd84570fb1`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 80.3 MB (80253950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a11eff80130d942a2ae7d02febd32a75242b63a6164c98651c3d42a4e065f`  
		Last Modified: Wed, 24 Jun 2026 03:18:18 GMT  
		Size: 201.7 MB (201672076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de7762590f3eec34b9f828fb964b032c9171b0763e07c0baa6d6c327951d186d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16868914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a4a1222b62eadcec6d73d35e8eaa35c6b2801b55e6a9443baa92424366d159`

```dockerfile
```

-	Layers:
	-	`sha256:c1729595adb238b29d0a4db061e82eede61836e6c17b9d5aaf48e7b579daa258`  
		Last Modified: Wed, 24 Jun 2026 03:18:14 GMT  
		Size: 16.9 MB (16858803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149d6e36363e94ecb8635e64afbf70abc83efd5d25672a54185dacd902e7a3fb`  
		Last Modified: Wed, 24 Jun 2026 03:18:13 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b3cd06f2c239c7a7e56b70a98cc0c71567cc12e375ddb6a47bccb23754494e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361798464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960aa340de5abcd491da7ab5903ae014f122a415230b8352be2290ad3c68347e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 03:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 09:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 11:41:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:207e1fc4a0d78092eada2cd0c9c038e7e28d176a37a4e995ec935b5f148a7e59`  
		Last Modified: Wed, 24 Jun 2026 00:29:01 GMT  
		Size: 54.1 MB (54097978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd980cdf87733c0ab6b7b8ac7237e7ffe3d5a175827f49d762e394ee883380`  
		Last Modified: Wed, 24 Jun 2026 03:26:38 GMT  
		Size: 30.2 MB (30172217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318bd778ee6617ca24d7be45e5c23eee9ba0bd8ef611556ae854c0b431747a89`  
		Last Modified: Wed, 24 Jun 2026 09:11:39 GMT  
		Size: 84.8 MB (84759730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b373345285b1a61ff3be9ee7dfd84e708d8aa92cd1f606a6916beaf90ace7`  
		Last Modified: Wed, 24 Jun 2026 11:43:02 GMT  
		Size: 192.8 MB (192768539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4860f55b866acb2a89b20b4196810468e70a7c26f4907f48b65a64396d05d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16872589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a03dacd393de27c11ef60b2458e2d78a71f142ccdc82d7d36b1d8763b83471`

```dockerfile
```

-	Layers:
	-	`sha256:cc98d954949c7d5fa512298b59e8f1145e6653336d0996db42ae3d70900e3a30`  
		Last Modified: Wed, 24 Jun 2026 11:42:56 GMT  
		Size: 16.9 MB (16862424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a225991956f58127b3a45f67a73daa22a0b7feed9cfd4cd11da6c5949125a3b`  
		Last Modified: Wed, 24 Jun 2026 11:42:55 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:495bf78e5e9766bbdbf308a4ae368af9cfadac38992bc8ca67d5bdb5efbe308b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.3 MB (485298470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e57f5964769dfdf5fd0c6572e619b3816667fc0e5b6ce4c4fbe02f2cee7419`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1782172800'
# Sat, 27 Jun 2026 16:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 29 Jun 2026 10:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 29 Jun 2026 15:59:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e8bae1b6870c9b437f01d25a862e15ba295e7a79fd96767c6645eb7fdef5abfe`  
		Last Modified: Wed, 24 Jun 2026 03:29:21 GMT  
		Size: 46.9 MB (46898250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5a3a6b67be6b5f648cdb0fc2f69f94d8fb9df5374644e5045cc659aa9911e`  
		Last Modified: Sat, 27 Jun 2026 16:18:18 GMT  
		Size: 27.3 MB (27296174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc4e8d8f6ac0dd209d4e4784f09a7509814776537d3815c90e55eb948ccaf68`  
		Last Modified: Mon, 29 Jun 2026 10:48:21 GMT  
		Size: 78.1 MB (78144376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c974cd6daf6d6e9ed6bf18be6e457c122f71c703e0efc2970992e355aaf3b7f`  
		Last Modified: Mon, 29 Jun 2026 16:15:28 GMT  
		Size: 333.0 MB (332959670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0edef9dc694956db21a04e55f5d0c18da9c2898359d1e3d667f377ea52af940b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17084780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5952e36474314c603b29235247c26336e6558190ab120d12e08f2a1c96615f`

```dockerfile
```

-	Layers:
	-	`sha256:c2c5830e32264b557a40a900100c97aeea5941e47ab61fb3bc4925435520a770`  
		Last Modified: Mon, 29 Jun 2026 16:14:41 GMT  
		Size: 17.1 MB (17074615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b3b37d661e53865189df7bcc3e7b5f8ef9b243bda071b09d945653276e7144`  
		Last Modified: Mon, 29 Jun 2026 16:14:35 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c8836badec86de995652672a15f534f92eb42dcac5caf01e04910515a1b67b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327095529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825a6ccd3119239716c4dec3a0f1e834f7da706429e950cd26d2635c4b8a1e0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 05:17:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9b72b44a72df002ca2c8ad8ccb65d46205892b54ff8d9ce0b5dd7be73544fe`  
		Last Modified: Wed, 24 Jun 2026 00:27:46 GMT  
		Size: 48.5 MB (48517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d84ec64f6d4462ee570697b4fa616aba8bdae3a994fb4acb8bbc6decb3dc15`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 27.6 MB (27576084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2315ca2dba4029f39e8aa110e548aabe9feb723a2f86c4188fe0abcb26f9073c`  
		Last Modified: Wed, 24 Jun 2026 04:30:52 GMT  
		Size: 78.6 MB (78635235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed21a99959c89bb3779d1b43e0e2dbf0cf54d34e9967f178453fd441e9284e5`  
		Last Modified: Wed, 24 Jun 2026 05:18:52 GMT  
		Size: 172.4 MB (172366414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e01a338c4bbe18fc5dfd675dc61e79039d52922ae15596627d0d15b0f4c9e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16675811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e215f195aafcaea6ad6fd758e178e9942c6c93246cd283d25a603af87c6074a8`

```dockerfile
```

-	Layers:
	-	`sha256:340eb4f3b756a6d4db0b57181d64a7acfcb8ddd494c3da5377b9da714d8769a3`  
		Last Modified: Wed, 24 Jun 2026 05:18:49 GMT  
		Size: 16.7 MB (16665678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b656349d95ddd4b61ccab65e03b3ce7096529dd8289df8ccf5ab3ffff84358d`  
		Last Modified: Wed, 24 Jun 2026 05:18:48 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
