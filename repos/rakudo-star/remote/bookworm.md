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
