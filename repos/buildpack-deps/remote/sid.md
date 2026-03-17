## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:00534542d0dcf2136f67efc8d7cbc75f723b26b33e77c99eb946aee3efaa3fe6
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
$ docker pull buildpack-deps@sha256:b8c05c1179c75d40d2e05c561a844bc5cb45624b9b527456d22df872b398af27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.4 MB (352376651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da500afb5f4019431d625536f0377d2728392a1f46748ada1ba44ccbd3abd39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:38:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a66b0373915b5b0ff298f6d01930222275f988f068d5fcb313d283986e46e2`  
		Last Modified: Mon, 16 Mar 2026 22:38:20 GMT  
		Size: 27.1 MB (27052911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c000813ac01f7ddd06b57be3d92ec5bc7055cb9bfbc652936c6c0f7b28c2295`  
		Last Modified: Mon, 16 Mar 2026 23:25:47 GMT  
		Size: 77.2 MB (77208242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be266a86a9347b734f79f2d6fba011ff4c8ace7e6b743f7d420ffb93a5cd450`  
		Last Modified: Tue, 17 Mar 2026 00:20:26 GMT  
		Size: 199.4 MB (199439028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87e98ee3615f4b1be3ad2c634d26e4bd250a8b6c7bd1b7925637ef69185ff38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16862546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffb576dd41bdf759276f078cd2b51eabf9580090eadb1fcb2974f2e2c315aa4`

```dockerfile
```

-	Layers:
	-	`sha256:58d5cb6577efbf8eb7cf2fd80018c6a4f927b9456db24393672bae5ba5b61d31`  
		Last Modified: Tue, 17 Mar 2026 00:20:23 GMT  
		Size: 16.9 MB (16852413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94332eeca62eed3fccf9b3de9c24d8a1fdaccc22081e9614334de350b73d9288`  
		Last Modified: Tue, 17 Mar 2026 00:20:22 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c0b603e7018b155a22291e861274bdba3c8575774bf7ad624b9d4c1157fd93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296408080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023a4aaa01a731522c6247dc9414d54433d9a2a98cf4c80cad43d7444d94ac98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 23:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f1150d74d9a03ef5fc137e050707adbd0a633a512d7e857d5d41c0f52ed63b6`  
		Last Modified: Mon, 16 Mar 2026 21:53:06 GMT  
		Size: 45.6 MB (45603619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1259f6d3d9e33f08f57016f1004a7104b71912ae731e4bade14636fa859034`  
		Last Modified: Mon, 16 Mar 2026 23:20:59 GMT  
		Size: 24.7 MB (24737768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22315ab69f88840faa8c9be9d5a3c56e2ef7ac97a80c1a3433e54ec2b7c14615`  
		Last Modified: Tue, 17 Mar 2026 00:51:49 GMT  
		Size: 71.7 MB (71706104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc295a20ebff3881856d95ee1f4992b71f7a1f46b7ca5a9d74864233c11c297`  
		Last Modified: Tue, 17 Mar 2026 01:16:35 GMT  
		Size: 154.4 MB (154360589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ff83f275f8fb1bcff4c8b05dd84ce2506e33227fe361b33f7db79ccfce427e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16617680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b31e084e8e5a94166dd1888a542a1fbb1a0731596eba67894b45d42d7fa9b`

```dockerfile
```

-	Layers:
	-	`sha256:c928b553b5565d2c461c02a634e65089fcc099b20dabafdb5329ab6a22ac1541`  
		Last Modified: Tue, 17 Mar 2026 01:16:31 GMT  
		Size: 16.6 MB (16607484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ebd425b647d7e71b1e9a09416a714cc4e0d9e0df04e4f72c18b09a99104250`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96577eafbe3c1a8192eb4263a20fe7c30f04b6faa88e43c605199cc44f7eed9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339269470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bdf4e96c9c3bcd537e770a7beca41a9b323a966aa7e23819008330c2d8e438`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4752dba1929fbf2811a63d55454ace7a1b8ccade962d6236fbef7e09ca8fde84`  
		Last Modified: Mon, 16 Mar 2026 22:40:42 GMT  
		Size: 26.3 MB (26348728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203999ee68abb17166cab30c231069e7d3b90af6038dcb2c20d38f95b99237`  
		Last Modified: Mon, 16 Mar 2026 23:31:04 GMT  
		Size: 76.4 MB (76392002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaaf5ab575ed4c054ea5aa70caa8ea0912a3f868399751f943f4e81106a31b3`  
		Last Modified: Tue, 17 Mar 2026 00:20:19 GMT  
		Size: 187.8 MB (187813565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83e7bc23cd93ff9bdf2a546861252f705edd664f19e9ae9d8ed938968908629d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c81cc8c1cd7afc56c90f6c16ad1b10830be30b842a378f17526f3043882669`

```dockerfile
```

-	Layers:
	-	`sha256:f0db115d44d1e8d0db1bd7e3ca3f5f8ef8f27d11988c332d6d6584ece87b1041`  
		Last Modified: Tue, 17 Mar 2026 00:20:15 GMT  
		Size: 16.9 MB (16935610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8674f3d04f6b0e62855a725158958857343c600f5e3f24522783c67c3538bd3`  
		Last Modified: Tue, 17 Mar 2026 00:20:14 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8fea769b850468fbae659aabc9dde7e253647361a28e6ed21754faab6b718c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360063202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476608bb69671cfe4cd0927c5e84d9bf1ffe4ca3e7f2c060278ba947ec731102`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981595a3cf9f38cbe3488cf7a822683f9aa76478cc3b84d65d23eeca02df1f21`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 28.3 MB (28318325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b742e9d3f7ff26075a954d57d40c471bb1e0e8efcc4391bd48ea5aaf2bf30b`  
		Last Modified: Mon, 16 Mar 2026 23:42:04 GMT  
		Size: 79.3 MB (79348339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad5af9cff477a00fc99aadba209ed09b234470c67036aeca1847cf79c10bd7`  
		Last Modified: Tue, 17 Mar 2026 00:20:48 GMT  
		Size: 202.4 MB (202448491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:990fe87c8ef04df0fa938a69a360db5ddb6101e5a48c181594c2f60390937e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c18379863c22a03e4e8578e3d47993f2380f8539960a5a5c0fcd1bcc725641`

```dockerfile
```

-	Layers:
	-	`sha256:16d69631f62e4b334879048cd9b0d62a7fb5e81bffb44e13046e856e428dcdb4`  
		Last Modified: Tue, 17 Mar 2026 00:20:44 GMT  
		Size: 16.8 MB (16821465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74582174aca3df8c86ac912cf80e887a6c80bc450c5de9e373e60dce6caae919`  
		Last Modified: Tue, 17 Mar 2026 00:20:43 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e0fbbf01136c15abe56eb5888ebb6b170f76c5a9a5cca900243188cfbb8d0fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359314321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c96dfb801a9f59435a60ef83441994946316045bab11c69f66d54222112c2e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 21:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 06:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98cf99f8e5f75111e243f4d3c092140d6c7618c5cce72eba92c5c2c4d8f97f2a`  
		Last Modified: Tue, 24 Feb 2026 18:43:36 GMT  
		Size: 53.7 MB (53670202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9c8da854a9fd9a96b0f203229509ae404e6f58b91c885234945a59771f957`  
		Last Modified: Tue, 24 Feb 2026 21:22:11 GMT  
		Size: 29.5 MB (29548376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc47532acbd1991339e90a90c711d95b92c082fb73f850ffee6b01a924a16006`  
		Last Modified: Wed, 25 Feb 2026 02:58:58 GMT  
		Size: 82.8 MB (82847193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad43391b70867902380ce0b486013fdce98ea0dd3710eeafd7e6d91cc81128a`  
		Last Modified: Wed, 25 Feb 2026 06:23:07 GMT  
		Size: 193.2 MB (193248550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e7120a91a33a53353ebed334c031b7471579e6bbd348706b7f067464a54bfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16831248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbc315bea4dedb868b4ee4a3882134963227ccbe8c9fa1bbf9aa71ea648c4f2`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f998a915b31d936798e01dc9d1d0eca3a351f53a0d23da54f610745394f36`  
		Last Modified: Wed, 25 Feb 2026 06:23:03 GMT  
		Size: 16.8 MB (16821083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53993ce37805975477cb0120276394ac28a8954de60311b1c9a9bfbb59acccce`  
		Last Modified: Wed, 25 Feb 2026 06:23:02 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:53b862af30efd4fba9d8190243a951c1e155fb65dd67bd48c509c20b09ace6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.3 MB (468328525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d304b95134cb48e68e5d79c7568d9b5eba57f25fe3c40b932960a90e0e99f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1771804800'
# Thu, 26 Feb 2026 21:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Mar 2026 00:31:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8883acc64dfc3047a79b0cc247a530d5064df45ee191c83ce50326e6f5321005`  
		Last Modified: Tue, 24 Feb 2026 18:46:58 GMT  
		Size: 46.9 MB (46910148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b9883d58655e16546eb41ce58204eed0527238cddce201073b9d732ba7588`  
		Last Modified: Thu, 26 Feb 2026 21:41:52 GMT  
		Size: 26.8 MB (26806123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202039b395ebb26fa9a04d9b4a8e961a4af2796808d884eed34b1431f00203d6`  
		Last Modified: Sat, 28 Feb 2026 19:56:03 GMT  
		Size: 75.1 MB (75144938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999fa1ce29db3affc4ac7c804a9c750fe608db660c5be3882bbd8a92dbc4ad64`  
		Last Modified: Tue, 03 Mar 2026 00:46:54 GMT  
		Size: 319.5 MB (319467316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e60b3d207ff580dd916303b71f7c5d0c7a82d71647b5b5896841e79f9bd4e91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16883448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c434ab40f549b9f0f72e1bba6432b8f65c75895f19c5497dfe9e52a0ea26cec9`

```dockerfile
```

-	Layers:
	-	`sha256:1eda3dd79132299b4d53c14fa3515f4c4ffef2a6f83bd78d8acc505a629b4568`  
		Last Modified: Tue, 03 Mar 2026 00:46:10 GMT  
		Size: 16.9 MB (16873283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e2d2ca23399a63b52afc6aac768f26cfbebe3c6854e0154309b653c6653394`  
		Last Modified: Tue, 03 Mar 2026 00:46:06 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:69c7a69b726ac35d0f2f72642d3cbbbbbd8f34d41bf34e35a92bef022b877b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323817145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c6bfee2056c487729ce38cb9709cb2fc8b83f611cfed869b28c64a64c32bdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 23:44:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:482c46a36656e92b7b7c495e1cb10adef503faba16aa28d7d632151eae2fb484`  
		Last Modified: Mon, 16 Mar 2026 21:52:04 GMT  
		Size: 48.4 MB (48373236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb43dc80984b0dc36163a89a02cfff6cafa23a4f4f70d13b75a21f64e7363b44`  
		Last Modified: Mon, 16 Mar 2026 23:45:15 GMT  
		Size: 26.8 MB (26838808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a023de4e5ac0909d69c57acb3670fea0a262c2619c715afe475d5ef441997d`  
		Last Modified: Tue, 17 Mar 2026 01:34:31 GMT  
		Size: 77.7 MB (77727754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4023e3dcc7d3743f7f74ea84afa1442a271a8ab01322b4bb0e667f56e9d0aba9`  
		Last Modified: Tue, 17 Mar 2026 02:19:01 GMT  
		Size: 170.9 MB (170877347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5cdfce87e353caa596877443f23192a205e846ba15ccac402ef494ce5a6b7f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16615851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc947285cafb79e5c2f00a90acc9b449340fe490daefcc6e1b05fb5c9ccc1ab`

```dockerfile
```

-	Layers:
	-	`sha256:f3eb0e78b24ab99309fcf22ab471947b35bca59e862704018194a61665ccb8c0`  
		Last Modified: Tue, 17 Mar 2026 02:18:57 GMT  
		Size: 16.6 MB (16605718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0884856bc3328dfe300ff91c0e0dac83c52b7c3f84a4b46bf4ce1226acf675`  
		Last Modified: Tue, 17 Mar 2026 02:18:57 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
