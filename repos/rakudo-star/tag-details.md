<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.10-alpine`](#rakudo-star202510-alpine)
-	[`rakudo-star:2025.10-bookworm`](#rakudo-star202510-bookworm)
-	[`rakudo-star:2025.10-trixie`](#rakudo-star202510-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2025.10-alpine`

```console
$ docker pull rakudo-star@sha256:8ef1d4ea5b2e70dba5fd466e359145053521ca548a99e672d2e49a8ac40d6c46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:11f59eb0dc173ca4e3dcea332ae9143a72a12ba9b9e2fddb0410fdc13f82d24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53175061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38aeadaeac66f5b8e7f04d4fc4de659b9967dc4e20d6dda6e5748bd3870e36a1`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:40:24 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 18 Dec 2025 00:55:48 GMT
ARG rakudo_version=2025.10-01
# Thu, 18 Dec 2025 00:55:48 GMT
ENV rakudo_version=2025.10-01
# Thu, 18 Dec 2025 00:55:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 00:55:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 18 Dec 2025 00:55:48 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74368d71099ab1a990d13ccc94322216d7aa2865eea9f33a0c548a1b9d80901`  
		Last Modified: Thu, 18 Dec 2025 00:56:06 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ecdef4ec727570cb17476e5a7ddffec17cc0b332f88f306817830f47141e0`  
		Last Modified: Thu, 18 Dec 2025 00:56:12 GMT  
		Size: 49.3 MB (49314011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d92414ca1ce5442ec49b49ab0666b80d80cc054e2f417d5f016eaafdb5d02c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298de96ccdc5e8d5d54f30f717f074dea23c9f52b504c2c849b58c9926d7d64b`

```dockerfile
```

-	Layers:
	-	`sha256:864f884ecf7b2070a94119061313ee9981ec86376391313659efcf8e34d531df`  
		Last Modified: Thu, 18 Dec 2025 02:33:22 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f46104cc3e416d04fcd477c0a801e3105c4939e05957cb8aebdc22ac21baa6e`  
		Last Modified: Thu, 18 Dec 2025 02:33:22 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7e35f9fe9cfe33c0a8ddeccb0855945bec0b588b1c9446730ba1deba219f5092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069b70464b1cf7b4b67187a7d79a990b184d1c559dd4bffe7d3d65a2f3fb5c39`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:26 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 18 Dec 2025 01:07:20 GMT
ARG rakudo_version=2025.10-01
# Thu, 18 Dec 2025 01:07:20 GMT
ENV rakudo_version=2025.10-01
# Thu, 18 Dec 2025 01:07:20 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 18 Dec 2025 01:07:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7812f485e0ad950ac0954a3cd267a8b9def09b4443f36612b5857f35fae9682b`  
		Last Modified: Thu, 18 Dec 2025 01:07:50 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e373024f0f1429a12f227e392e91a506eb399bc55c3452b4d58fe72a24aa44`  
		Last Modified: Thu, 18 Dec 2025 01:07:57 GMT  
		Size: 49.1 MB (49056186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0cb1c295f716a26b8aff74ce077e3a9f414b09c2deb13ac4a470b6e7d738f861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f21f2525b7ec1c3b6b3df98ad7535d035e6b87a73279eaeacc106fd8eddb9`

```dockerfile
```

-	Layers:
	-	`sha256:40d8ec7e3108483e4af33f707fcc13a9ed4405f1a466e7a35ea3223f50c2ced2`  
		Last Modified: Thu, 18 Dec 2025 02:33:26 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b231bb5b7b340404d8dce9d85d02fab83e8f2099a6f23b3d6d935bfd99afee3`  
		Last Modified: Thu, 18 Dec 2025 02:33:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-bookworm`

```console
$ docker pull rakudo-star@sha256:8b142a015b5f8b8b729be904d908892ef6f038506d90a0664de6b1f1d2b9d6ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f721460ed94f10a1dda3e6a39c6fd70ae67f247c3e792a6aa375148a836245d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179572749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c8cb0c409d7c63de7f6c7baadddd1f6d5085de8dea29500dafed1b94cc1392`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:51:51 GMT
MAINTAINER Rob Hoelz
# Tue, 09 Dec 2025 00:51:51 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:51 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:51 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:11:30 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:11:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:11:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69427762d12ec35fb419603f01b95d615ea72fdf87a6cb151d82449f51bdb9f`  
		Last Modified: Tue, 09 Dec 2025 01:12:05 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629eb215110acfe1945f458af65c5c7479214de15f034ec28aa55023f8cf8a49`  
		Last Modified: Tue, 09 Dec 2025 01:12:12 GMT  
		Size: 42.7 MB (42662923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e7cff047c4e99f301ad97cfefde0e891726d4a079c7b80f3a2f8fef8d5dec820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a780f13c0ab2627ce1dd410888b048db6755befb5a333769e2b9e0a3faaa6e0c`

```dockerfile
```

-	Layers:
	-	`sha256:664c56d338bc9cb26f34c3950fbdd0899ce2172366cc5c5aa65da19a5b3ed95c`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a86435e07ae2642594f71b12c5493d22eee59651247ac4251ed4ecff8f6d43`  
		Last Modified: Tue, 09 Dec 2025 02:33:49 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:73cd40ab629fce040061bf1475a3b2614c70431241681f975f75d9cfb1c10292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177165402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024dfb933cdbf5fb7a8aafe3b09d98b506c54bc9526dd95af5165b9224b2c162`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER Rob Hoelz
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:43:50 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:43:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:43:50 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f625aa51dbcb747572d05d88bf7cc1234fffeadf91da33d19c366e96f05c0d`  
		Last Modified: Tue, 09 Dec 2025 01:44:18 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7552752d30d35fb0a328d5a9020d17cf9a9bf62769e1405dc6f6728ba2ef95c3`  
		Last Modified: Tue, 09 Dec 2025 01:44:20 GMT  
		Size: 40.8 MB (40833361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e58738793f358da54ed422b54e8110673e9198d07647191b1e0de54400ae78b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e275b11c3c00e8236cb6258ed788d702e24308081de2feaac427daf1d4127`

```dockerfile
```

-	Layers:
	-	`sha256:a7827e4feb57b1654a44af7c891389039ba56775f2b10bc4ac2561a30582dbbe`  
		Last Modified: Tue, 09 Dec 2025 05:33:30 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c79cb03b7dc10ca485cde1503d99a11b6f0777dd16537ecc639931320cb5e3f`  
		Last Modified: Tue, 09 Dec 2025 05:33:31 GMT  
		Size: 12.8 KB (12796 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-trixie`

```console
$ docker pull rakudo-star@sha256:a544b2f161b37ae2783f967ddd990522d45e73b75aabe83b850fcb3ad254accf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e7b45f3cd7ab812ae3637c17232519bb39dee4ed8f80eb2aec2f44a371d8f70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185426245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e147f329e22e06183c45cb4d918a05979096277b0571eb09d5db0d5ac8771bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 00:51:28 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:28 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:07:15 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:07:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:07:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e2fa53da7fb32f2efff992e980c1df2af29150be96ca181e72e7b6914493d`  
		Last Modified: Tue, 09 Dec 2025 01:07:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a86b01210135bc5548f563542a13ad1fe8a73b4d29a59ef46a77f09fa465f`  
		Last Modified: Tue, 09 Dec 2025 01:07:44 GMT  
		Size: 42.7 MB (42740978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1bf6859dc52a3ba7f34cb8b9303f9990462845609c1889c223798eb4b81237cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0ac35cb7daefab1768a4e3cfe41587e4d84361689533b0e6d59e0e7828d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:16978ee8723517d7dcc22296d0704b77f3d299d615b98360b69a797eaa06dc13`  
		Last Modified: Tue, 09 Dec 2025 02:33:55 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922a732d1a0bfcefb16fcafe9cb57ca1673dd2b74e2ef38ddb9b96ad514dab87`  
		Last Modified: Tue, 09 Dec 2025 02:33:56 GMT  
		Size: 13.0 KB (12991 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e3b3fef13d1f29b09acf0c555dea91b6e0699d443cd312030926ae3e46b8ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183056558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fc0b355649f63ed18d485a3fe60b488f4f1bd57c6ec0e40f846b6579400d80`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:42:16 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:42:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:42:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70bb4683a0e3c06330cd1201aef1a2871d8cdcfbc68246766951a3cb9ab93c`  
		Last Modified: Tue, 09 Dec 2025 01:42:44 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c755f7599d208bcabfaefa4aa0d9af367e28a569e38fb23d1423699abd8982`  
		Last Modified: Tue, 09 Dec 2025 01:42:47 GMT  
		Size: 40.8 MB (40797141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:79a53978fd34e34bbe25a0a225125cd21f655b393511c5101ae8303619f0db3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5055dc7329e70b90a1d8d528df86fbf0f5009a1b11a304e7270348ea5cf50`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0e9561ba045229e9252dedfcd6ec04acee7311af65e7d35ab8552f8ee1b75`  
		Last Modified: Tue, 09 Dec 2025 05:33:37 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e98075ab4ace7c2f9d9ce885d2fdc0801b0bd95eb3d37b4ef053f0fb947a8e1`  
		Last Modified: Tue, 09 Dec 2025 05:33:38 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:8ef1d4ea5b2e70dba5fd466e359145053521ca548a99e672d2e49a8ac40d6c46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:11f59eb0dc173ca4e3dcea332ae9143a72a12ba9b9e2fddb0410fdc13f82d24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53175061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38aeadaeac66f5b8e7f04d4fc4de659b9967dc4e20d6dda6e5748bd3870e36a1`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:40:24 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 18 Dec 2025 00:55:48 GMT
ARG rakudo_version=2025.10-01
# Thu, 18 Dec 2025 00:55:48 GMT
ENV rakudo_version=2025.10-01
# Thu, 18 Dec 2025 00:55:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 00:55:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 18 Dec 2025 00:55:48 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74368d71099ab1a990d13ccc94322216d7aa2865eea9f33a0c548a1b9d80901`  
		Last Modified: Thu, 18 Dec 2025 00:56:06 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ecdef4ec727570cb17476e5a7ddffec17cc0b332f88f306817830f47141e0`  
		Last Modified: Thu, 18 Dec 2025 00:56:12 GMT  
		Size: 49.3 MB (49314011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d92414ca1ce5442ec49b49ab0666b80d80cc054e2f417d5f016eaafdb5d02c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298de96ccdc5e8d5d54f30f717f074dea23c9f52b504c2c849b58c9926d7d64b`

```dockerfile
```

-	Layers:
	-	`sha256:864f884ecf7b2070a94119061313ee9981ec86376391313659efcf8e34d531df`  
		Last Modified: Thu, 18 Dec 2025 02:33:22 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f46104cc3e416d04fcd477c0a801e3105c4939e05957cb8aebdc22ac21baa6e`  
		Last Modified: Thu, 18 Dec 2025 02:33:22 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7e35f9fe9cfe33c0a8ddeccb0855945bec0b588b1c9446730ba1deba219f5092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069b70464b1cf7b4b67187a7d79a990b184d1c559dd4bffe7d3d65a2f3fb5c39`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:26 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 18 Dec 2025 01:07:20 GMT
ARG rakudo_version=2025.10-01
# Thu, 18 Dec 2025 01:07:20 GMT
ENV rakudo_version=2025.10-01
# Thu, 18 Dec 2025 01:07:20 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 18 Dec 2025 01:07:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7812f485e0ad950ac0954a3cd267a8b9def09b4443f36612b5857f35fae9682b`  
		Last Modified: Thu, 18 Dec 2025 01:07:50 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e373024f0f1429a12f227e392e91a506eb399bc55c3452b4d58fe72a24aa44`  
		Last Modified: Thu, 18 Dec 2025 01:07:57 GMT  
		Size: 49.1 MB (49056186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0cb1c295f716a26b8aff74ce077e3a9f414b09c2deb13ac4a470b6e7d738f861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f21f2525b7ec1c3b6b3df98ad7535d035e6b87a73279eaeacc106fd8eddb9`

```dockerfile
```

-	Layers:
	-	`sha256:40d8ec7e3108483e4af33f707fcc13a9ed4405f1a466e7a35ea3223f50c2ced2`  
		Last Modified: Thu, 18 Dec 2025 02:33:26 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b231bb5b7b340404d8dce9d85d02fab83e8f2099a6f23b3d6d935bfd99afee3`  
		Last Modified: Thu, 18 Dec 2025 02:33:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:8b142a015b5f8b8b729be904d908892ef6f038506d90a0664de6b1f1d2b9d6ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f721460ed94f10a1dda3e6a39c6fd70ae67f247c3e792a6aa375148a836245d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179572749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c8cb0c409d7c63de7f6c7baadddd1f6d5085de8dea29500dafed1b94cc1392`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:51:51 GMT
MAINTAINER Rob Hoelz
# Tue, 09 Dec 2025 00:51:51 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:51 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:51 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:11:30 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:11:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:11:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69427762d12ec35fb419603f01b95d615ea72fdf87a6cb151d82449f51bdb9f`  
		Last Modified: Tue, 09 Dec 2025 01:12:05 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629eb215110acfe1945f458af65c5c7479214de15f034ec28aa55023f8cf8a49`  
		Last Modified: Tue, 09 Dec 2025 01:12:12 GMT  
		Size: 42.7 MB (42662923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e7cff047c4e99f301ad97cfefde0e891726d4a079c7b80f3a2f8fef8d5dec820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a780f13c0ab2627ce1dd410888b048db6755befb5a333769e2b9e0a3faaa6e0c`

```dockerfile
```

-	Layers:
	-	`sha256:664c56d338bc9cb26f34c3950fbdd0899ce2172366cc5c5aa65da19a5b3ed95c`  
		Last Modified: Tue, 09 Dec 2025 02:33:48 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a86435e07ae2642594f71b12c5493d22eee59651247ac4251ed4ecff8f6d43`  
		Last Modified: Tue, 09 Dec 2025 02:33:49 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:73cd40ab629fce040061bf1475a3b2614c70431241681f975f75d9cfb1c10292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177165402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024dfb933cdbf5fb7a8aafe3b09d98b506c54bc9526dd95af5165b9224b2c162`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER Rob Hoelz
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:43:50 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:43:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:43:50 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f625aa51dbcb747572d05d88bf7cc1234fffeadf91da33d19c366e96f05c0d`  
		Last Modified: Tue, 09 Dec 2025 01:44:18 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7552752d30d35fb0a328d5a9020d17cf9a9bf62769e1405dc6f6728ba2ef95c3`  
		Last Modified: Tue, 09 Dec 2025 01:44:20 GMT  
		Size: 40.8 MB (40833361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e58738793f358da54ed422b54e8110673e9198d07647191b1e0de54400ae78b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e275b11c3c00e8236cb6258ed788d702e24308081de2feaac427daf1d4127`

```dockerfile
```

-	Layers:
	-	`sha256:a7827e4feb57b1654a44af7c891389039ba56775f2b10bc4ac2561a30582dbbe`  
		Last Modified: Tue, 09 Dec 2025 05:33:30 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c79cb03b7dc10ca485cde1503d99a11b6f0777dd16537ecc639931320cb5e3f`  
		Last Modified: Tue, 09 Dec 2025 05:33:31 GMT  
		Size: 12.8 KB (12796 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:a544b2f161b37ae2783f967ddd990522d45e73b75aabe83b850fcb3ad254accf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e7b45f3cd7ab812ae3637c17232519bb39dee4ed8f80eb2aec2f44a371d8f70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185426245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e147f329e22e06183c45cb4d918a05979096277b0571eb09d5db0d5ac8771bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 00:51:28 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:28 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:07:15 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:07:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:07:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e2fa53da7fb32f2efff992e980c1df2af29150be96ca181e72e7b6914493d`  
		Last Modified: Tue, 09 Dec 2025 01:07:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a86b01210135bc5548f563542a13ad1fe8a73b4d29a59ef46a77f09fa465f`  
		Last Modified: Tue, 09 Dec 2025 01:07:44 GMT  
		Size: 42.7 MB (42740978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1bf6859dc52a3ba7f34cb8b9303f9990462845609c1889c223798eb4b81237cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0ac35cb7daefab1768a4e3cfe41587e4d84361689533b0e6d59e0e7828d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:16978ee8723517d7dcc22296d0704b77f3d299d615b98360b69a797eaa06dc13`  
		Last Modified: Tue, 09 Dec 2025 02:33:55 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922a732d1a0bfcefb16fcafe9cb57ca1673dd2b74e2ef38ddb9b96ad514dab87`  
		Last Modified: Tue, 09 Dec 2025 02:33:56 GMT  
		Size: 13.0 KB (12991 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e3b3fef13d1f29b09acf0c555dea91b6e0699d443cd312030926ae3e46b8ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183056558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fc0b355649f63ed18d485a3fe60b488f4f1bd57c6ec0e40f846b6579400d80`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:42:16 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:42:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:42:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70bb4683a0e3c06330cd1201aef1a2871d8cdcfbc68246766951a3cb9ab93c`  
		Last Modified: Tue, 09 Dec 2025 01:42:44 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c755f7599d208bcabfaefa4aa0d9af367e28a569e38fb23d1423699abd8982`  
		Last Modified: Tue, 09 Dec 2025 01:42:47 GMT  
		Size: 40.8 MB (40797141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:79a53978fd34e34bbe25a0a225125cd21f655b393511c5101ae8303619f0db3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5055dc7329e70b90a1d8d528df86fbf0f5009a1b11a304e7270348ea5cf50`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0e9561ba045229e9252dedfcd6ec04acee7311af65e7d35ab8552f8ee1b75`  
		Last Modified: Tue, 09 Dec 2025 05:33:37 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e98075ab4ace7c2f9d9ce885d2fdc0801b0bd95eb3d37b4ef053f0fb947a8e1`  
		Last Modified: Tue, 09 Dec 2025 05:33:38 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:a544b2f161b37ae2783f967ddd990522d45e73b75aabe83b850fcb3ad254accf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e7b45f3cd7ab812ae3637c17232519bb39dee4ed8f80eb2aec2f44a371d8f70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185426245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e147f329e22e06183c45cb4d918a05979096277b0571eb09d5db0d5ac8771bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 00:51:28 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 00:51:28 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 00:51:28 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:07:15 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:07:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:07:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e2fa53da7fb32f2efff992e980c1df2af29150be96ca181e72e7b6914493d`  
		Last Modified: Tue, 09 Dec 2025 01:07:37 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78a86b01210135bc5548f563542a13ad1fe8a73b4d29a59ef46a77f09fa465f`  
		Last Modified: Tue, 09 Dec 2025 01:07:44 GMT  
		Size: 42.7 MB (42740978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1bf6859dc52a3ba7f34cb8b9303f9990462845609c1889c223798eb4b81237cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0ac35cb7daefab1768a4e3cfe41587e4d84361689533b0e6d59e0e7828d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:16978ee8723517d7dcc22296d0704b77f3d299d615b98360b69a797eaa06dc13`  
		Last Modified: Tue, 09 Dec 2025 02:33:55 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922a732d1a0bfcefb16fcafe9cb57ca1673dd2b74e2ef38ddb9b96ad514dab87`  
		Last Modified: Tue, 09 Dec 2025 02:33:56 GMT  
		Size: 13.0 KB (12991 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e3b3fef13d1f29b09acf0c555dea91b6e0699d443cd312030926ae3e46b8ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183056558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fc0b355649f63ed18d485a3fe60b488f4f1bd57c6ec0e40f846b6579400d80`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
MAINTAINER AntonOks
# Tue, 09 Dec 2025 01:22:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 09 Dec 2025 01:22:13 GMT
ARG rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:22:13 GMT
ENV rakudo_version=2025.10-01
# Tue, 09 Dec 2025 01:42:16 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 09 Dec 2025 01:42:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Dec 2025 01:42:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b70bb4683a0e3c06330cd1201aef1a2871d8cdcfbc68246766951a3cb9ab93c`  
		Last Modified: Tue, 09 Dec 2025 01:42:44 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c755f7599d208bcabfaefa4aa0d9af367e28a569e38fb23d1423699abd8982`  
		Last Modified: Tue, 09 Dec 2025 01:42:47 GMT  
		Size: 40.8 MB (40797141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:79a53978fd34e34bbe25a0a225125cd21f655b393511c5101ae8303619f0db3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5055dc7329e70b90a1d8d528df86fbf0f5009a1b11a304e7270348ea5cf50`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0e9561ba045229e9252dedfcd6ec04acee7311af65e7d35ab8552f8ee1b75`  
		Last Modified: Tue, 09 Dec 2025 05:33:37 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e98075ab4ace7c2f9d9ce885d2fdc0801b0bd95eb3d37b4ef053f0fb947a8e1`  
		Last Modified: Tue, 09 Dec 2025 05:33:38 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
