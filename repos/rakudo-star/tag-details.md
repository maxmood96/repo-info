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
$ docker pull rakudo-star@sha256:a2f6e7033e1e57ae5951ec0fc8a395c4e9fcfc1f8583005fbaf8db92f746f7f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c8c976ca3fc139d061d848201f107b3b9c72d8a5022a71090ae196846165dc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53201174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d45ee45f329ed7a83b2cdaa7e446367b0a345d03da8b1533f7c8061fcc8085`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:03:16 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:19:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea966dcb91608765a4b518e719c4b74c2fa933682229f548b6952421f033d9e`  
		Last Modified: Wed, 03 Dec 2025 20:20:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c87c769308d01dd4494173151acd529862506a291feb41229eb3f0b8ef37d`  
		Last Modified: Wed, 03 Dec 2025 20:20:15 GMT  
		Size: 49.3 MB (49340915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:087a8b78029e8a16023aa2e8c6d5b5b100dbb00a3a49d378d47d218ed27eaac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa296b0f199a17f3a46901d18750d69929f7190f46e9606cb1b956ec0ef3fe`

```dockerfile
```

-	Layers:
	-	`sha256:c57e1b14a07da6455345eb2c43f7807ee74ec4291de17eed32e9fa4f489459ac`  
		Last Modified: Wed, 03 Dec 2025 23:33:50 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4f9f7c2166835f05a85e7a8704f8ade738381ce9655da6a96f0f3805fc2a98`  
		Last Modified: Wed, 03 Dec 2025 23:33:51 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.10-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c2fc729067afec561672c23fb3aae61e71b287f76a0b521787a91fa82abbd7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f416b4aac7673c941ca50990f89b25a7c71d1dede8d0d564cd2f5105f1b8b2f4`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:02:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:23:50 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6746cc9aada545857a96583e349746c29ac6a577f1b0cd17c0f98f56a770941c`  
		Last Modified: Wed, 03 Dec 2025 20:24:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e038c16be749f056d0c640d52d6dc8af117865f2d7a96b4599ab257abd1283f`  
		Last Modified: Wed, 03 Dec 2025 20:24:25 GMT  
		Size: 49.1 MB (49064665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5c3c99acb4d4bec7013352ab55061309ca9b4f68e316e872d8c13a5d977810b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7981983392dfb5d8c28ed760600dbc4823be84e9df1cf242ed69688b816a6`

```dockerfile
```

-	Layers:
	-	`sha256:84621f879b0599da41a08ac876eaf36de8f6a432d0a0af329c2e3a8e54ac08c3`  
		Last Modified: Wed, 03 Dec 2025 23:33:54 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e042e15077c32fa7beb783e769edd275673015610276c6fafc8443bd53a7f`  
		Last Modified: Wed, 03 Dec 2025 23:33:55 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-bookworm`

```console
$ docker pull rakudo-star@sha256:f13cd605b907f142325cbe0e03b5b6bf58cf29970257b54bca2c1dad07477845
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
$ docker pull rakudo-star@sha256:368420af7d0faa09b4fa195da19abe29c3c05ec37b4632dfc56eb95da42b554c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177037798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e74491ed48760a1b101d7bf1b6cb09ccea7de015598101173d566e98e70d284`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 06:42:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:55 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:02:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:02:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c1c1b725841787fd7038584369f950d375aedcf4cc13643e935cf8c171d07`  
		Last Modified: Tue, 18 Nov 2025 07:02:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a50301ff18d06ad0ffe79237a9e1529ebb67a00bdb4a4bc1b50226557f615`  
		Last Modified: Tue, 18 Nov 2025 07:02:54 GMT  
		Size: 40.7 MB (40705685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1e6c5dde9f23ada08e21de637bc6c0faab6d2b5432de3baabcce658f65f8aa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035fbbb62f94bffdc2007c1a9c1f3fc38f7c7a9b952c8978919e34889fc1b393`

```dockerfile
```

-	Layers:
	-	`sha256:ace36da9f2459ea443ce6c0948d677de8f41c5b57b729c3fd61f4a8920252e9e`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d5463174acd51aa000f9f914dab27d1741bad86910b652e4f6fb696e92a888`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.10-trixie`

```console
$ docker pull rakudo-star@sha256:96b9cf99a6eeff8605ae0aedfc1c8ac6ebd2ebcc99f57af9b7675dbcfa3ddea8
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
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.10-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:a2f6e7033e1e57ae5951ec0fc8a395c4e9fcfc1f8583005fbaf8db92f746f7f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c8c976ca3fc139d061d848201f107b3b9c72d8a5022a71090ae196846165dc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53201174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d45ee45f329ed7a83b2cdaa7e446367b0a345d03da8b1533f7c8061fcc8085`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:03:16 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:19:47 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:19:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:19:47 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea966dcb91608765a4b518e719c4b74c2fa933682229f548b6952421f033d9e`  
		Last Modified: Wed, 03 Dec 2025 20:20:12 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c87c769308d01dd4494173151acd529862506a291feb41229eb3f0b8ef37d`  
		Last Modified: Wed, 03 Dec 2025 20:20:15 GMT  
		Size: 49.3 MB (49340915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:087a8b78029e8a16023aa2e8c6d5b5b100dbb00a3a49d378d47d218ed27eaac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa296b0f199a17f3a46901d18750d69929f7190f46e9606cb1b956ec0ef3fe`

```dockerfile
```

-	Layers:
	-	`sha256:c57e1b14a07da6455345eb2c43f7807ee74ec4291de17eed32e9fa4f489459ac`  
		Last Modified: Wed, 03 Dec 2025 23:33:50 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4f9f7c2166835f05a85e7a8704f8ade738381ce9655da6a96f0f3805fc2a98`  
		Last Modified: Wed, 03 Dec 2025 23:33:51 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c2fc729067afec561672c23fb3aae61e71b287f76a0b521787a91fa82abbd7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f416b4aac7673c941ca50990f89b25a7c71d1dede8d0d564cd2f5105f1b8b2f4`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 20:02:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ARG rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
ENV rakudo_version=2025.10-01
# Wed, 03 Dec 2025 20:23:50 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 03 Dec 2025 20:23:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Dec 2025 20:23:50 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6746cc9aada545857a96583e349746c29ac6a577f1b0cd17c0f98f56a770941c`  
		Last Modified: Wed, 03 Dec 2025 20:24:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e038c16be749f056d0c640d52d6dc8af117865f2d7a96b4599ab257abd1283f`  
		Last Modified: Wed, 03 Dec 2025 20:24:25 GMT  
		Size: 49.1 MB (49064665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5c3c99acb4d4bec7013352ab55061309ca9b4f68e316e872d8c13a5d977810b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7981983392dfb5d8c28ed760600dbc4823be84e9df1cf242ed69688b816a6`

```dockerfile
```

-	Layers:
	-	`sha256:84621f879b0599da41a08ac876eaf36de8f6a432d0a0af329c2e3a8e54ac08c3`  
		Last Modified: Wed, 03 Dec 2025 23:33:54 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e042e15077c32fa7beb783e769edd275673015610276c6fafc8443bd53a7f`  
		Last Modified: Wed, 03 Dec 2025 23:33:55 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:f13cd605b907f142325cbe0e03b5b6bf58cf29970257b54bca2c1dad07477845
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
$ docker pull rakudo-star@sha256:368420af7d0faa09b4fa195da19abe29c3c05ec37b4632dfc56eb95da42b554c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177037798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e74491ed48760a1b101d7bf1b6cb09ccea7de015598101173d566e98e70d284`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
MAINTAINER Rob Hoelz
# Tue, 18 Nov 2025 06:42:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:55 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:55 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:02:26 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:02:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2c1c1b725841787fd7038584369f950d375aedcf4cc13643e935cf8c171d07`  
		Last Modified: Tue, 18 Nov 2025 07:02:50 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a50301ff18d06ad0ffe79237a9e1529ebb67a00bdb4a4bc1b50226557f615`  
		Last Modified: Tue, 18 Nov 2025 07:02:54 GMT  
		Size: 40.7 MB (40705685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1e6c5dde9f23ada08e21de637bc6c0faab6d2b5432de3baabcce658f65f8aa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035fbbb62f94bffdc2007c1a9c1f3fc38f7c7a9b952c8978919e34889fc1b393`

```dockerfile
```

-	Layers:
	-	`sha256:ace36da9f2459ea443ce6c0948d677de8f41c5b57b729c3fd61f4a8920252e9e`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d5463174acd51aa000f9f914dab27d1741bad86910b652e4f6fb696e92a888`  
		Last Modified: Tue, 18 Nov 2025 08:33:43 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:96b9cf99a6eeff8605ae0aedfc1c8ac6ebd2ebcc99f57af9b7675dbcfa3ddea8
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
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:96b9cf99a6eeff8605ae0aedfc1c8ac6ebd2ebcc99f57af9b7675dbcfa3ddea8
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
$ docker pull rakudo-star@sha256:25468224abbc2e32aee53f05248dea53ed0d32e327d9383a5ae0c423fb2c023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182964743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3c02669e673ade7194607a141bc72bd300566c7f6c91ab7cac23f09e2d028b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
MAINTAINER AntonOks
# Tue, 18 Nov 2025 06:42:56 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 18 Nov 2025 06:42:56 GMT
ARG rakudo_version=2025.10-01
# Tue, 18 Nov 2025 06:42:56 GMT
ENV rakudo_version=2025.10-01
# Tue, 18 Nov 2025 07:01:48 GMT
# ARGS: rakudo_version=2025.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 07:01:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 18 Nov 2025 07:01:48 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1925aa376fcb1a7162d40d27685f7d752f9d7c57f07ba5774f5e02dee95c95`  
		Last Modified: Tue, 18 Nov 2025 07:02:27 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fc607bdb37f40b856cd79db20616896d0a315358c7d5387bed8595d25138ad`  
		Last Modified: Tue, 18 Nov 2025 07:02:31 GMT  
		Size: 40.7 MB (40705496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdadf93684c38f6c33be22b3dcfdbcf518d1c99047ba873707002a1553f7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c05f82fecc6daaf2316b3eb10b83cb203f62d544a248acd69a3435668ecad4`

```dockerfile
```

-	Layers:
	-	`sha256:4f6b3900ff2c89fc3eb95492eda4ef5a7c18003a9e50edc78a7de1cb29e7c1d2`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd882ab499de310fba89d437fbeef70a85cb89869a18c92296c43291513082`  
		Last Modified: Tue, 18 Nov 2025 08:33:46 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
