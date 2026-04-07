## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:0b20b69dc0b162d4055e318d79f56b68dc0f03c4ef44ce2854fbef5c5a34902d
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f64c5d0e2a2c8ac44d1c5923f8a0ae8352ae72602802f00835b84a5657eedd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350219088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6a897cd90fc698960b870857f4a7be94111fe4b8f0b80c89dce06f5c3707cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:23:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf18cd16b2dae064e3a3c52f418c924e5dbc6ee6c8435f830ab8926bcc861a`  
		Last Modified: Tue, 07 Apr 2026 01:47:08 GMT  
		Size: 27.0 MB (27034235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28538354df54ea4ac8c75c1aa2be2d2de1b9c1def81dccc0bcde292235f5b8ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:46 GMT  
		Size: 76.4 MB (76406935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7ea213e1f10a447f1470f2f972620df55871be5649a005c02aa3cf61edf95`  
		Last Modified: Tue, 07 Apr 2026 03:24:09 GMT  
		Size: 198.2 MB (198190834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4c19c48ee9f8ca6e228bfe0d9c947829ac61099deb80b55367cc0e5bd9f1af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16826238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5021fe321c53c22b26904de570d098aa895c1a44f628a4840d2ae8b8f9ff2785`

```dockerfile
```

-	Layers:
	-	`sha256:ebb91b7ee9fa2af0f40adf0855e119e150396643d19bc0c9abdc07467fe915ac`  
		Last Modified: Tue, 07 Apr 2026 03:24:04 GMT  
		Size: 16.8 MB (16816093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b51f6dfdb438a53f5450e22ed32d9802fac22666a9a335357995475ba0ed12`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5508077d580486380e5359dacacc3fe15fed6d842048a48f0420a4bbb568d1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295424752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae1a07e55d7ba665d3dc28b3f91b29f67033a699a01a2f3b867ff03f09f51b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:28:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94c1a7288fb6578b9efe4cfec6d86c90bcbd7f6b3ded72757e8150ba2d22a63b`  
		Last Modified: Tue, 07 Apr 2026 00:59:45 GMT  
		Size: 45.5 MB (45540788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431662b04e5e4d9f2ef3d5f7c7e2caee0a1ec1674e5c8149f9c8cd948a2576c6`  
		Last Modified: Tue, 07 Apr 2026 02:01:50 GMT  
		Size: 24.7 MB (24727230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed09a6e73a79c8aa370c8a0869b12618204a2b6df06735ab9815b49b7b49df83`  
		Last Modified: Tue, 07 Apr 2026 03:49:36 GMT  
		Size: 71.0 MB (70996320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7996855147a367bb224f9f747951680da006ec30b3029d1189ee61511eeedf62`  
		Last Modified: Tue, 07 Apr 2026 04:29:19 GMT  
		Size: 154.2 MB (154160414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2fd0b505184c2ac622570102db6ba1f10a37c793b5a70fe906482f077c7080b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16581364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb98da27f32d08188f192ef54d7bd316a02041e6d602bb682067220422d925a0`

```dockerfile
```

-	Layers:
	-	`sha256:6e3211dbbcef6c0be4e5e7b31d831e1fc9f28e596140e0419eab1f9b2f96316a`  
		Last Modified: Tue, 07 Apr 2026 04:29:16 GMT  
		Size: 16.6 MB (16571155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987d96c23c068a2ed84dfe7266536cf8df7b76995f7129542d99ab864b808a80`  
		Last Modified: Tue, 07 Apr 2026 04:29:15 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dfbe7532368f2b00da7cb84e16a979434bae0f40ea2006cf81b4f3f0b3f99f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338267344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da549aa47dd7dbd5c09a623f456065d0f783cc9c2872cc1e4a57a3e11fc8f50`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:35:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf67292a85a4af897784b09f019ed45150697232130ae9fa282c0d04d42db8bf`  
		Last Modified: Tue, 07 Apr 2026 01:50:18 GMT  
		Size: 26.3 MB (26330750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1267bd01c4aae412822d148a245b888f2dd03e33cf999c672da10ad2d5724bf6`  
		Last Modified: Tue, 07 Apr 2026 02:53:51 GMT  
		Size: 75.7 MB (75660925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594ec228052aa6bf996806e6837979a05228b32fae016169fc10d8c6b87d211`  
		Last Modified: Tue, 07 Apr 2026 03:36:00 GMT  
		Size: 187.6 MB (187632313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:681aba3544e3c6d11f2d2dd3e59dbe01a1d99319c5d8b4fb32604bf59a68c04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16908696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db50772c5570042079d125fe1f16cc71e8637adb0ccf7978ce7acba2427f08e`

```dockerfile
```

-	Layers:
	-	`sha256:6cf74f98245a7ecc28ea02728a8a482b46c21cdc1b17f616dcc75e70e2c2e864`  
		Last Modified: Tue, 07 Apr 2026 03:35:57 GMT  
		Size: 16.9 MB (16898471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f228a776ed0026795476ad457770ef899e344a2457cde5e94ae7969cbbd815a3`  
		Last Modified: Tue, 07 Apr 2026 03:35:56 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d6e0d77b9378976fe41c7d13c179d46d37c56c9f7a4dd7f7f19e5ae1d0143fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 MB (357808993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee448bbc92d9e12a7f0c1d7ea304c8b1101913b88e627316ca4b7ef8aaa1562`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:40:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74970d6f811b29c802a9f3c8d694bfd2f422255c20b66bcc271ba0c7bcc9dbfc`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 28.3 MB (28298911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d376180d010f10a41a07c62fb3fa00f2442ee96ea8b7248d80a02311ec598b1d`  
		Last Modified: Tue, 07 Apr 2026 02:41:15 GMT  
		Size: 78.6 MB (78591062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e8c7efd81c10b99e8acea59976a68692a3afa02433ab1f09c4e0b579ad085`  
		Last Modified: Tue, 07 Apr 2026 03:20:18 GMT  
		Size: 201.0 MB (201040631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06aad3fe0cb2f35fe08e320c5b6eddc53c67594abcc8c7e33f1f7b15009a4c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16795289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3896e91b40abd623263133a3c71e928d88f50eebfb30849299e75d7b7ad3ef07`

```dockerfile
```

-	Layers:
	-	`sha256:c4e0d079aeebd234a19c6742e8b13949ee301b0103d103791cf29377fd887ac2`  
		Last Modified: Tue, 07 Apr 2026 03:20:14 GMT  
		Size: 16.8 MB (16785167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae2db61b08e25ef9f0ce089c0261a2df17a81f23a5d2d94ab5898da67c6455d`  
		Last Modified: Tue, 07 Apr 2026 03:20:13 GMT  
		Size: 10.1 KB (10122 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bb1d87111f2bd88d096d27a77279b8b5a95adb50edc21b2cd9c37691cb973a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356839033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8e575940d6b72da96ba93f2587b24ce98740afc0b4896e8e6fa48c921b46e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1773619200'
# Tue, 17 Mar 2026 01:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 08:20:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75936ac254db13d0215c75f5fabecfedea28136e3ee0cacb89bd8884668a56af`  
		Last Modified: Mon, 16 Mar 2026 21:51:49 GMT  
		Size: 53.9 MB (53863314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e0924d7ad541b2109556dcbe1d5d7994260b154430061685df2536f4aafd6`  
		Last Modified: Tue, 17 Mar 2026 01:50:07 GMT  
		Size: 29.3 MB (29334407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9adfa45e921c3124cd11880041b79cbc945f57ca5ff667ef09fa57d6468ae2`  
		Last Modified: Tue, 17 Mar 2026 06:04:44 GMT  
		Size: 82.1 MB (82088651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aabf1673a6b603b7d1c93584062c5ca37959e57baf0818eda272903a290e186`  
		Last Modified: Tue, 17 Mar 2026 08:21:33 GMT  
		Size: 191.6 MB (191552661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54cb92ef585b9d6c263657ed0e6b0ed4c09382af253eedc80cae411c06e7aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16753514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4477dc70db1ea413944ec5187fdf4d212bb1c016a87b6c72622a39d8fd18f70`

```dockerfile
```

-	Layers:
	-	`sha256:0f740aaae7dbf8dbb0ae942e474e2473b604791bd2d0b5b56a4a8a337364b20f`  
		Last Modified: Tue, 17 Mar 2026 08:21:30 GMT  
		Size: 16.7 MB (16743337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95de70e68ce189a199350c70fda205809b57bd46ccbd9664dfc0a57f8b5c9459`  
		Last Modified: Tue, 17 Mar 2026 08:21:28 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8ee27409effb0bb31110e7e6a52a9a105052c83588c758956edfc1be2ffa069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465709803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac2ba853441ac0499dd769e7c68f73fb5728fa498e7e8762bc74eed0176ce30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 18 Mar 2026 04:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:12:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3fb5c15cbddc0ebbd7afd8ce992f6bfd6f0d5d4b1d5f4e672c5fc7451f1119d`  
		Last Modified: Mon, 16 Mar 2026 21:55:37 GMT  
		Size: 46.7 MB (46721467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059cd42e31b5d0cd1848f67940ca871c5e491654382eb483e7231a6e0aedfb85`  
		Last Modified: Mon, 16 Mar 2026 22:28:45 GMT  
		Size: 26.6 MB (26599402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1365cfbe0dd7752051c14b1a8c2b3faa3e2ab8a5452bc20f8b0ce87ad22e6be`  
		Last Modified: Wed, 18 Mar 2026 05:03:15 GMT  
		Size: 75.9 MB (75941012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f199a3049067221fbc475c687e4f08d9835441296ebfa59161e122a13326d63`  
		Last Modified: Thu, 19 Mar 2026 05:28:13 GMT  
		Size: 316.4 MB (316447922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27389e3da068e62d575dffdecc0d87a0c2207f09e836e834bbc055b5569ce1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16847040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5bcd3c31054493235c78b521fdf8496fec4d546752984ed1a52f14d7550dea`

```dockerfile
```

-	Layers:
	-	`sha256:8c771bdcd413908c84e053df3ccddf18daf9742ce24731fe06a552e285db546c`  
		Last Modified: Thu, 19 Mar 2026 05:27:28 GMT  
		Size: 16.8 MB (16836864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5db77b5f5611bcb3b8b2abb9cc1da350979c9b85c3130376ccba1313cb6dc3c`  
		Last Modified: Thu, 19 Mar 2026 05:27:23 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5cd0d7b94edc865781b69e001cc26d5f0ee3539b77471b24c96addb00d7f19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322688748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e47ef10472e91d7a27d2d493506e9aaa3911818cee007509de448ff13f901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 03:04:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d387cf27b8c74bb29905817ad867265b401af02fdbc21b522a98041e86095a47`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 48.3 MB (48291595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71640c6f0517962fef2d2cecd2252a1ad50dd36dcdfc5949b497510671693745`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 26.8 MB (26816201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d200d226dcb1e9ec18c10fb8ae6afd2e2e5f3a76506193fd7ffbd528f5de7`  
		Last Modified: Tue, 07 Apr 2026 04:55:09 GMT  
		Size: 76.9 MB (76879572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384dfb42b1fe626978c0fe2c478bf62e09ade9f0d508ccad09d28365801b200a`  
		Last Modified: Tue, 07 Apr 2026 06:01:10 GMT  
		Size: 170.7 MB (170701380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:327b60f036397618a25e6f1ce57a4ab54fa79db9ad67db03bda83bc19a81b2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16581169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2d3f9505b7dbb18755b6aa215e745be96632ee53c930e23455729e68039ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c496478fd18b9cf287fe256d7875870060202f6d2d89954646a01969268fe144`  
		Last Modified: Tue, 07 Apr 2026 06:01:08 GMT  
		Size: 16.6 MB (16571024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b1159b3f2d8a4b8a3e2d8a7b0aa614331d6be331c3d9d487a2815e19bbac96`  
		Last Modified: Tue, 07 Apr 2026 06:01:03 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
