## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:2a9f27b368d8bd2d969f6c6871302cb2a79f06266e85607eeb15cb912ae115ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1c9f43999dba27d8f10e4a1ef5ae0b9a2634ba6145ae7d70e4a6b46152d4ce7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179105550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b420452ed4b48505f373339d2d6ead51a066ad207462c287c80742aba0893ae7`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7cff01b997fa565dc9bc379ff5a67015df215692faead9f74af83d3b951e04`  
		Last Modified: Wed, 25 Dec 2024 00:30:59 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c77848a5a21a058b19ddd7567940996984e4b60a9fc2b9f4e9181bc782f67`  
		Last Modified: Wed, 25 Dec 2024 00:31:00 GMT  
		Size: 42.3 MB (42348360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4ff77b9b0580ca70ef60f52616f15e42edc6ce2f937c05b298a94507d8873869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa49df6fc0ad4f2c518e634152237899ee8f58a0f8db62480b2b94d278db018a`

```dockerfile
```

-	Layers:
	-	`sha256:c9b8af537772e271ca0c66823127aace5f173d70fd3deab2b754b62f5fa37de5`  
		Last Modified: Wed, 25 Dec 2024 00:31:00 GMT  
		Size: 7.8 MB (7758951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bded357a0f8efc7b1c7c740de1bca7481040e83a75ce8b0b1b74fd989c48988`  
		Last Modified: Wed, 25 Dec 2024 00:30:59 GMT  
		Size: 13.0 KB (13026 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2f799523bee710b36ed8eae058dcc166d2b7e30d04438f81530d7342a4e46e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176692256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d5141a838e54b7682566a33ff1c12da2edcd1f08dac0e786924f7891bfd30a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5194c6cd41deb1fd070d925c9f9fcd89340c0dc4c2a4708150c38c0f4487186e`  
		Last Modified: Wed, 25 Dec 2024 12:22:53 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0433fc466e6bf75a60d0764aacda7117b7bbcbfb8aa7fb83e6c832f9a89076`  
		Last Modified: Wed, 25 Dec 2024 12:22:55 GMT  
		Size: 40.6 MB (40610316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:90d46ec55ec13b1bb03ef179bd1b7781c0ce64901e56ad6c16649e8386112797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b8e26f5786e5ee8c24f9993704576778966913331146d0d940fff7e79ac921`

```dockerfile
```

-	Layers:
	-	`sha256:750b4f7165898c2e4b3cbf92419da1f3319d7bba516b9ad163a139126c441c6f`  
		Last Modified: Wed, 25 Dec 2024 12:22:54 GMT  
		Size: 7.8 MB (7765356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8efcf291858ae16ccdf3a6fc4f08a3fda4a0ee0e5ca85c17d355d9b40a4a72`  
		Last Modified: Wed, 25 Dec 2024 12:22:53 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json
