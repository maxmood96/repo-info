## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:e388a18ddedb3ecf448cfadc0c9a984ed8aad4c1dd149aececb6fc513e9c9fb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:4af5065612835ff05021cc106964fd0d854cfc7938eab973fbda221c8022c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185114828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429d1e765fb3b71341f046dc4d4907eaaeb2dacb22c3712a108646eb96ce64e7`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:19:14 GMT
MAINTAINER AntonOks
# Thu, 11 Jun 2026 03:19:14 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:14 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:14 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:35:08 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:35:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:35:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12693a7f02e4ce80eb7da288870fe321fc86dcb6c0b3fe206f6ced1bca4c979`  
		Last Modified: Thu, 11 Jun 2026 03:35:23 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc49d76d8515de656969c11dd0af6ce24bad99d10b0bfa95e5d0b510099af8ad`  
		Last Modified: Thu, 11 Jun 2026 03:35:24 GMT  
		Size: 42.4 MB (42374547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3001b5415a74a936045e7fd677aceb94afe7180a2741b23964afcec722d2ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17028c80b153ce9f49116b07585354575859c4b04b97e169ea9c28fb1879a23d`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb72e0adfb49a7584fcd052fbc20d33363bc41ab3c9f978a09e0722f108a59`  
		Last Modified: Thu, 11 Jun 2026 03:35:23 GMT  
		Size: 7.8 MB (7770924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de25cd5dd72f012e9da1e8f1697eb637e23d0c678e5417e450d3b364bfa8b4c3`  
		Last Modified: Thu, 11 Jun 2026 03:35:23 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8978ad305487f08121437887e11f55a7c895f114789570d2f2b3dc8f7f5c5901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182609327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca8a4858738660bdc936f6dabcc67da28219127aa0c3e87d759cf0d725ba15a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:19:29 GMT
MAINTAINER AntonOks
# Thu, 11 Jun 2026 03:19:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:29 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:29 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:39:19 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:39:19 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2132da23d405b4eb76cce85dbae0f90bf2bb73b45722d82e187553bafe1a45c`  
		Last Modified: Thu, 11 Jun 2026 03:39:34 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb958fffdc4b069bf4e1c247aa55ad37b1471042809bfea885100fc938cd23b`  
		Last Modified: Thu, 11 Jun 2026 03:39:35 GMT  
		Size: 40.3 MB (40301073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:01ce9613322c9400f802223ffe0e5687175f578325435a8324738cbb468da2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a942201fe05cba3ca46c590223afca0b6a1e2da403480080d56f3142050089c7`

```dockerfile
```

-	Layers:
	-	`sha256:495b591ea3fffa03cea02071c538a78d0fa7b20426d9ea013271cf2607de0938`  
		Last Modified: Thu, 11 Jun 2026 03:39:34 GMT  
		Size: 7.8 MB (7777962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc3dbfbcbad7ab8dacb9340d1fd6cf6af9563665a44c48a1ebc44e53cb88384`  
		Last Modified: Thu, 11 Jun 2026 03:39:34 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
