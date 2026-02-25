## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:6b64ed5b1e32212b6069da69ade6fbf87bd92bab2658767b90c664ad3d024707
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
$ docker pull buildpack-deps@sha256:e93045f462e0b6624a16edc689086d043a00941981aa1add866faa18a297d201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351986667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ba54dc40a9db6b65848210c2351d99c74e8c7391f1ab54930866aa432be9ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:19:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:38:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a3b9aa5dd67fed7efa597566954b806b6c17ff4757052490684a87ba9c100`  
		Last Modified: Tue, 24 Feb 2026 19:20:08 GMT  
		Size: 27.3 MB (27263732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee694f6c4343c44df75d6ec35f4054147fa9bad772a564b5f1de4cfec3c634b`  
		Last Modified: Tue, 24 Feb 2026 20:04:30 GMT  
		Size: 76.7 MB (76661494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f684dc9491aa6e09cfaee0f1f71aae624af4aefac394de5f04568139c80bf4d`  
		Last Modified: Tue, 24 Feb 2026 20:38:59 GMT  
		Size: 199.4 MB (199394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6443a8669f2fbda7423a480a61e83672f29fb947a8198e6879b88308bff389d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16879764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134d42fb7205feaff9b5c26598ced64c9a59d19b72a6bc2c6314949c02eca3d8`

```dockerfile
```

-	Layers:
	-	`sha256:1296c1b36463d9542e023c831d9456d0e81e63366327f5ede3920a261e8efa64`  
		Last Modified: Tue, 24 Feb 2026 20:38:55 GMT  
		Size: 16.9 MB (16869631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8659bea8d63fa9a892b525e7f529d19b20a2b6862d9a603ddfc269a72ff9a7e2`  
		Last Modified: Tue, 24 Feb 2026 20:38:55 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

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

### `buildpack-deps:unstable` - unknown; unknown

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

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6123a04cdcf8f9b25ce9f100df53cae254ccb216b00001dafb903e67a37fabe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340354345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb21b1d7f21c8aebafbc32bf52269ff87749c8f886cfb1171c089555bbc9271`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:30:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:61a95a2f6784ce634817550699b53ea6f85b093ca9ec55f99c5217b534acfb51`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 48.7 MB (48709262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9febf2eebdcd541e5079a4d79c0089d659ae0df279b4c59ab388cf9f3a36d6a`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 26.6 MB (26557741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76037322e25656a045c471e5f5d50ba4bbe0de66d0473628ebbabf140ff1d0c6`  
		Last Modified: Tue, 24 Feb 2026 20:15:03 GMT  
		Size: 75.9 MB (75942761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc77708304602615740bef240dcf81c20dd903c76a48bb304e182499692d23`  
		Last Modified: Tue, 24 Feb 2026 21:31:14 GMT  
		Size: 189.1 MB (189144581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9bdfcd7860f7e3da0cd1cec10dc657d3eee42988f8690ea3a9c7a7132af4215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b228156699c5b2cb0f83618aa398f3eed649ec2fa824ca2baf81309643b32457`

```dockerfile
```

-	Layers:
	-	`sha256:7fed6d4647bf7dd6391de88e0e775f8a0ff6a120306396c1d4dd80e68ab3b074`  
		Last Modified: Tue, 24 Feb 2026 21:31:11 GMT  
		Size: 17.0 MB (16956664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b264a78a085c92ad342cfc08bc04acac2e1fbc78edee8ba5028aba1cefe8591`  
		Last Modified: Tue, 24 Feb 2026 21:31:10 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c45c85a761e02092eb1146e9c3d84b08c4ceb72ee103e281689f809f84ac9ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359882168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ee60bca2d33175a25dd8ad5ba531b0f0e132eff3ece6f73098852061e0d46f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:19:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3559a7084ebe893d133871358dab0d079615e3eaacd04f900b699ede2f39f35d`  
		Last Modified: Tue, 24 Feb 2026 19:25:03 GMT  
		Size: 28.5 MB (28522446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24f85b42485f9731950f1b8fa7613f52dc2e2ad73698b31dbb6e317dd54b8fe`  
		Last Modified: Tue, 24 Feb 2026 19:57:26 GMT  
		Size: 78.7 MB (78650294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bc3930ab66ad776f10019489a6aa1c6007ff2294c20efe0dd69486b9e08f6e`  
		Last Modified: Tue, 24 Feb 2026 20:19:41 GMT  
		Size: 202.7 MB (202687313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b4e34459401578e7ef5fb3faf905ffc5d3f165f1e6dcb5af728bbe31163a631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16848814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d80ada1cf8cc6c227effd73a144669c462fc150b6a9708a422c4d77d718450`

```dockerfile
```

-	Layers:
	-	`sha256:b797b306a7b828103283952d33cad6c8ea272fcbae4615b959842abf417c382d`  
		Last Modified: Tue, 24 Feb 2026 20:19:37 GMT  
		Size: 16.8 MB (16838703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53d2471c2a462e3ccf6366e8ba829dc52779ee5779d16dff694e005ba4242bf`  
		Last Modified: Tue, 24 Feb 2026 20:19:36 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

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

### `buildpack-deps:unstable` - unknown; unknown

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

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:20880887ac662555b4405ffdd286802836b4fd3cfc33843f00d2b613d1b80a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462333400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4886d743725242558ab6174a9b21bbba6fa1a183af4e894e7e4121607f529141`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1769990400'
# Thu, 05 Feb 2026 03:14:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:50:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Feb 2026 23:29:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48f09a2bb3a57a16959e5ae66db8cd1e1c1ed0c93449352dcc6fc0b64e55cbda`  
		Last Modified: Tue, 03 Feb 2026 07:02:16 GMT  
		Size: 46.9 MB (46890143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0416dc273ac7c8750810633c99f22464f2e2bb48f2a6515852ce21ac1a4a7c0`  
		Last Modified: Thu, 05 Feb 2026 03:16:37 GMT  
		Size: 26.8 MB (26767187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40443e0d15d0b1f4d6ccc3b2b45d939f99796b01564ba57c27e672dd399d532d`  
		Last Modified: Fri, 06 Feb 2026 07:54:03 GMT  
		Size: 67.3 MB (67275341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cdc8b06a575176b654014f8c626ecc2dff3faf8ec6c469d72566176d07778`  
		Last Modified: Sat, 07 Feb 2026 23:44:45 GMT  
		Size: 321.4 MB (321400729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0d4579da7f359de22d382693a17dcf77cf96273501fd28bbe3d8f602e387531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a34649c1bbe6b01a98eee444db3243e19fb2cce94e43dea28ad51aae8cfe46c`

```dockerfile
```

-	Layers:
	-	`sha256:ec368744b27916b048f23654ac05dc0f453bc1485f8d2c9832777d8625797caa`  
		Last Modified: Sat, 07 Feb 2026 23:44:00 GMT  
		Size: 16.4 MB (16404187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0119ac7dbb6dca55b1bc23a643aee0d64af276db814c1b0de6a0516d026c0c5`  
		Last Modified: Sat, 07 Feb 2026 23:43:56 GMT  
		Size: 10.2 KB (10164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

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

### `buildpack-deps:unstable` - unknown; unknown

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
