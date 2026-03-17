## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:a946eecc901c6765c88884cf5e44749f67b29fb055bcb94d585939aede80e66c
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
$ docker pull buildpack-deps@sha256:365cb38fb9f0ce1fe9981df70fd0ae11ce99bfa72103d2f281c70f59f54ff9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297661853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f140782cee92e2a994d4ac82ae1c1689db8154a187a3323100c02df7decbbe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97ecb7dc5149349428e562613e6adb43b3de4d352c854673428e628da358370f`  
		Last Modified: Tue, 24 Feb 2026 18:42:32 GMT  
		Size: 45.7 MB (45650224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e80713e8851bb16d17addabd13dbf94a64b8f2f71fc35c153fe3f3d905e74e`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 25.0 MB (24955977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d1a2065fd70a28d49320af562c84c6c88558fd52605edf4ce3664dceb810e2`  
		Last Modified: Tue, 24 Feb 2026 21:35:17 GMT  
		Size: 71.2 MB (71203492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1063234b7a833bfaa251e2c821c25412fce82d954369e73121c64cfd066676`  
		Last Modified: Tue, 24 Feb 2026 22:17:30 GMT  
		Size: 155.9 MB (155852160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5fab2bf218b2b7a441d677a5f26ba4be073c46d5237f0dc7eb5710b6c53d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa77335c285ffb6ca4beb92d8628718157c31b4e14ea2e41b65928af6f424645`

```dockerfile
```

-	Layers:
	-	`sha256:ac60819825e4b563d539722bac9b57c33e69c9dede0a81b6d9f44dc45fe5825c`  
		Last Modified: Tue, 24 Feb 2026 22:17:28 GMT  
		Size: 16.6 MB (16624742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58041539d1dbdb535f3276472d0038b3cf5a73044e05dfd1901a5f9094fe3353`  
		Last Modified: Tue, 24 Feb 2026 22:17:27 GMT  
		Size: 10.2 KB (10197 bytes)  
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
$ docker pull buildpack-deps@sha256:41093b13a9e85d2725c70b7a78ac5df769730ee2c941768e19f80130be8dcffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.0 MB (325013608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdbfceef9616e4a93f80e62a8da5c5c57e56aff18d7cfb4922334860de280f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:57:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:14:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b79b6ca78edd108b2b500a1c2abe8a5f5b6dee5dce46c5bd663b643e7c568362`  
		Last Modified: Tue, 24 Feb 2026 18:42:12 GMT  
		Size: 48.4 MB (48447710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694122fd04e83fa7d8372df97237755c6e7de35a0f627724e622c594e1610bc1`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 27.1 MB (27050121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e410942f5d531e0acfa92cbd6cc91daf0d23e2cfcc176a01bae68615afa926`  
		Last Modified: Tue, 24 Feb 2026 23:53:52 GMT  
		Size: 77.3 MB (77293315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a272a36700b511428072242a5821580bb7b3e7beac8b4bf0f83527ddc6e7d97b`  
		Last Modified: Wed, 25 Feb 2026 02:15:45 GMT  
		Size: 172.2 MB (172222462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:974b121346b3f06527563a5f0f3b6ccfcc5ea43ed324bcee906ea6d1ca1f8d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16633697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f65dd096dacaa6928ff9fd405344b4fc62651dab622524eda42dd78b9bb59bd`

```dockerfile
```

-	Layers:
	-	`sha256:f882436c8471c7eb15b39d140d2866ba8c8f5f975e8d127acfecafff886d89e5`  
		Last Modified: Wed, 25 Feb 2026 02:15:41 GMT  
		Size: 16.6 MB (16623564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e050717c1aca8fcc8ea97f7bcd597aa702d1d0c58e7cb432b7ebf692436c2e29`  
		Last Modified: Wed, 25 Feb 2026 02:15:41 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
