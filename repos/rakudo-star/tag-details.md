<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.08.1`](#rakudo-star2025081)
-	[`rakudo-star:2025.08.1-alpine`](#rakudo-star2025081-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2025.08.1`

```console
$ docker pull rakudo-star@sha256:b6a7da7dac8b9e131e3682bdb5e9ff0690743fc627d3050f62af876a8189837b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.08.1` - linux; amd64

```console
$ docker pull rakudo-star@sha256:352ff420643450a16c43c87e1f97c6cee6fba5878726663e0950d6c0c115c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179586236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1dffda3d5add728b06f03469d28f251eb67ab9b171d30c04f0061ab847921`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903144137f176adb6f6e7c4718d2985a73a4b27dd92430b0a084d15e5c1b6e03`  
		Last Modified: Tue, 30 Sep 2025 06:59:27 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639f94a1cf9c9440c4647c9dcce6fd056e621dbc18e14fb69e55a428660836e`  
		Last Modified: Tue, 30 Sep 2025 06:59:39 GMT  
		Size: 42.7 MB (42679158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b90d05e6e04cbef1312bded53965e20d9b691483c40cd5f324604d5284292b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b7c33c20bf8b444e47b3e302fa7d1e8d68f16cd7ce038b7e8339f7eef66f9b`

```dockerfile
```

-	Layers:
	-	`sha256:6226809132fd8016d4031ab62b05d22d8d5d5b887a0dff6300d567f17bb085cb`  
		Last Modified: Tue, 30 Sep 2025 22:34:39 GMT  
		Size: 8.0 MB (7968098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6210ccaa092d4cbccf0a7eaa2daa60a5d42f65d2125251661ae64ce3e777e3`  
		Last Modified: Tue, 30 Sep 2025 22:34:40 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.08.1` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e0d78e750de6020465ce58266057014eb1e2afbaf3112cd40a2243e3f7fdcf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174805814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d87c8045f21ed831afe731cb7e9e9d5e52d47606d54000b318f583cd95540a2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d139930d275e25202057291e255414c5f87a65fee9857b0090e23c8f6b891dd`  
		Last Modified: Tue, 23 Sep 2025 23:39:43 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946a877e06c073a10dc6064705cd60342bf993e637786ad2f99fd75b3929cd3`  
		Last Modified: Tue, 23 Sep 2025 23:39:50 GMT  
		Size: 38.5 MB (38477585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b2512d518b32ea83fdd5a1902b4932494ce93cf422359666669ce4ad457697e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7172d2e14bafe74b9226e7d908da004d929102ae80f5c0eafe122a47e60dfdef`

```dockerfile
```

-	Layers:
	-	`sha256:2c5eff7ced831e5b637a9f6a69eef304474dbdadfc1907e2f77aca4bc1dfe679`  
		Last Modified: Wed, 24 Sep 2025 01:33:17 GMT  
		Size: 8.0 MB (7974503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199ab47f85f47acb7638b2eed3af25708761495cd2451d453b657d1980318bcb`  
		Last Modified: Wed, 24 Sep 2025 01:33:18 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.08.1-alpine`

```console
$ docker pull rakudo-star@sha256:2b39271d492752380a7d4647486eb10fbf67d17d4ea7e4fe240c228ddd13e6d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.08.1-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:608edc32872b4e50c2d712294cb707659cba72f146cd21fdffb4c206ce61b955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52759913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1826a4cc297ef2f0e480423e85ba3d76cbcd2ce488b06d7dd6bf1041aeaef65`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 22:27:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5d4e246a1e52a3a492a6351e8e36572b7a313be8bb0e35bb8c35596466c3c`  
		Last Modified: Wed, 24 Sep 2025 02:39:58 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e059c2792c094958defc0e41852ca6b1c8a7bc4b18e773f080236c84fcc5fb`  
		Last Modified: Wed, 24 Sep 2025 02:40:02 GMT  
		Size: 49.0 MB (48959277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7312eb4a03b32aae3d4ffedfb27fab4c7cb92e96c34298ebe8bf4fdb3ab852bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c92e9f0e40e0fa8dd074c85c40fd879619239547b61432fb34de17a6a0af43f`

```dockerfile
```

-	Layers:
	-	`sha256:e5e9b384690d77bba15667a9ba3a78ced9e52fc15c8cadcefebf61c623cb36c6`  
		Last Modified: Wed, 24 Sep 2025 04:33:21 GMT  
		Size: 186.0 KB (186024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1ae36e79e36fa4f270799865a863b2b6629d0aead057921c97320ce877f1f2`  
		Last Modified: Wed, 24 Sep 2025 04:33:21 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.08.1-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a9f51dde9679a0f880dbc4b322db523e324358faf7e2c193b642a9f5f0667eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52867285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aed50259288c8d8e91bc9eb06d67ab8868c80cc890acb1ca09493c186adf30e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 22:27:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbdad542f1832bba5c94ef01c74d7be7bf3c61301ebbcf451e2da0dd184cf7`  
		Last Modified: Tue, 23 Sep 2025 23:43:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096970a951996d351b9326417b79a004409a7f7d181ce9696c2a6fcda8cbd039`  
		Last Modified: Tue, 23 Sep 2025 23:43:53 GMT  
		Size: 48.7 MB (48735587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:29d9c3a55ca997c5f3a628b56982cb4ab9110c346702363b280bbcd78dd7921d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecaa838c0222b8bfb4ea1e9f38566bd026f185a5a4796bb40ff0812e16e4267`

```dockerfile
```

-	Layers:
	-	`sha256:46dea7763507674cacdab410b5f3af80fa4a7b70bf84cb0e4737c2bb6c536265`  
		Last Modified: Wed, 24 Sep 2025 01:33:21 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659f7d3adfe9b6e9cf9da658336527238b2bdc2e62f9d2f4a918111c6c8de202`  
		Last Modified: Wed, 24 Sep 2025 01:33:22 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:2b39271d492752380a7d4647486eb10fbf67d17d4ea7e4fe240c228ddd13e6d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:608edc32872b4e50c2d712294cb707659cba72f146cd21fdffb4c206ce61b955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52759913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1826a4cc297ef2f0e480423e85ba3d76cbcd2ce488b06d7dd6bf1041aeaef65`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 22:27:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5d4e246a1e52a3a492a6351e8e36572b7a313be8bb0e35bb8c35596466c3c`  
		Last Modified: Wed, 24 Sep 2025 02:39:58 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e059c2792c094958defc0e41852ca6b1c8a7bc4b18e773f080236c84fcc5fb`  
		Last Modified: Wed, 24 Sep 2025 02:40:02 GMT  
		Size: 49.0 MB (48959277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7312eb4a03b32aae3d4ffedfb27fab4c7cb92e96c34298ebe8bf4fdb3ab852bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c92e9f0e40e0fa8dd074c85c40fd879619239547b61432fb34de17a6a0af43f`

```dockerfile
```

-	Layers:
	-	`sha256:e5e9b384690d77bba15667a9ba3a78ced9e52fc15c8cadcefebf61c623cb36c6`  
		Last Modified: Wed, 24 Sep 2025 04:33:21 GMT  
		Size: 186.0 KB (186024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1ae36e79e36fa4f270799865a863b2b6629d0aead057921c97320ce877f1f2`  
		Last Modified: Wed, 24 Sep 2025 04:33:21 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a9f51dde9679a0f880dbc4b322db523e324358faf7e2c193b642a9f5f0667eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52867285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aed50259288c8d8e91bc9eb06d67ab8868c80cc890acb1ca09493c186adf30e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 22:27:44 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbdad542f1832bba5c94ef01c74d7be7bf3c61301ebbcf451e2da0dd184cf7`  
		Last Modified: Tue, 23 Sep 2025 23:43:49 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096970a951996d351b9326417b79a004409a7f7d181ce9696c2a6fcda8cbd039`  
		Last Modified: Tue, 23 Sep 2025 23:43:53 GMT  
		Size: 48.7 MB (48735587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:29d9c3a55ca997c5f3a628b56982cb4ab9110c346702363b280bbcd78dd7921d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecaa838c0222b8bfb4ea1e9f38566bd026f185a5a4796bb40ff0812e16e4267`

```dockerfile
```

-	Layers:
	-	`sha256:46dea7763507674cacdab410b5f3af80fa4a7b70bf84cb0e4737c2bb6c536265`  
		Last Modified: Wed, 24 Sep 2025 01:33:21 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659f7d3adfe9b6e9cf9da658336527238b2bdc2e62f9d2f4a918111c6c8de202`  
		Last Modified: Wed, 24 Sep 2025 01:33:22 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:b6a7da7dac8b9e131e3682bdb5e9ff0690743fc627d3050f62af876a8189837b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:352ff420643450a16c43c87e1f97c6cee6fba5878726663e0950d6c0c115c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179586236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1dffda3d5add728b06f03469d28f251eb67ab9b171d30c04f0061ab847921`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903144137f176adb6f6e7c4718d2985a73a4b27dd92430b0a084d15e5c1b6e03`  
		Last Modified: Tue, 30 Sep 2025 06:59:27 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639f94a1cf9c9440c4647c9dcce6fd056e621dbc18e14fb69e55a428660836e`  
		Last Modified: Tue, 30 Sep 2025 06:59:39 GMT  
		Size: 42.7 MB (42679158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b90d05e6e04cbef1312bded53965e20d9b691483c40cd5f324604d5284292b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b7c33c20bf8b444e47b3e302fa7d1e8d68f16cd7ce038b7e8339f7eef66f9b`

```dockerfile
```

-	Layers:
	-	`sha256:6226809132fd8016d4031ab62b05d22d8d5d5b887a0dff6300d567f17bb085cb`  
		Last Modified: Tue, 30 Sep 2025 22:34:39 GMT  
		Size: 8.0 MB (7968098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6210ccaa092d4cbccf0a7eaa2daa60a5d42f65d2125251661ae64ce3e777e3`  
		Last Modified: Tue, 30 Sep 2025 22:34:40 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e0d78e750de6020465ce58266057014eb1e2afbaf3112cd40a2243e3f7fdcf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174805814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d87c8045f21ed831afe731cb7e9e9d5e52d47606d54000b318f583cd95540a2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d139930d275e25202057291e255414c5f87a65fee9857b0090e23c8f6b891dd`  
		Last Modified: Tue, 23 Sep 2025 23:39:43 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d946a877e06c073a10dc6064705cd60342bf993e637786ad2f99fd75b3929cd3`  
		Last Modified: Tue, 23 Sep 2025 23:39:50 GMT  
		Size: 38.5 MB (38477585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b2512d518b32ea83fdd5a1902b4932494ce93cf422359666669ce4ad457697e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7172d2e14bafe74b9226e7d908da004d929102ae80f5c0eafe122a47e60dfdef`

```dockerfile
```

-	Layers:
	-	`sha256:2c5eff7ced831e5b637a9f6a69eef304474dbdadfc1907e2f77aca4bc1dfe679`  
		Last Modified: Wed, 24 Sep 2025 01:33:17 GMT  
		Size: 8.0 MB (7974503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199ab47f85f47acb7638b2eed3af25708761495cd2451d453b657d1980318bcb`  
		Last Modified: Wed, 24 Sep 2025 01:33:18 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:17dd83f15c978a5a80571e1f958ae25cb1d67a16f24f6bc2c640295da7f1016b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:352ff420643450a16c43c87e1f97c6cee6fba5878726663e0950d6c0c115c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179586236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1dffda3d5add728b06f03469d28f251eb67ab9b171d30c04f0061ab847921`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903144137f176adb6f6e7c4718d2985a73a4b27dd92430b0a084d15e5c1b6e03`  
		Last Modified: Tue, 30 Sep 2025 06:59:27 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639f94a1cf9c9440c4647c9dcce6fd056e621dbc18e14fb69e55a428660836e`  
		Last Modified: Tue, 30 Sep 2025 06:59:39 GMT  
		Size: 42.7 MB (42679158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b90d05e6e04cbef1312bded53965e20d9b691483c40cd5f324604d5284292b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b7c33c20bf8b444e47b3e302fa7d1e8d68f16cd7ce038b7e8339f7eef66f9b`

```dockerfile
```

-	Layers:
	-	`sha256:6226809132fd8016d4031ab62b05d22d8d5d5b887a0dff6300d567f17bb085cb`  
		Last Modified: Tue, 30 Sep 2025 22:34:39 GMT  
		Size: 8.0 MB (7968098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6210ccaa092d4cbccf0a7eaa2daa60a5d42f65d2125251661ae64ce3e777e3`  
		Last Modified: Tue, 30 Sep 2025 22:34:40 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f1be86e9027bbb58a6d679c0bb7351d20f4a7662390d7bea5e9519731515670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177082402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896fe49690bd4a9516398fb4ef0910af5ad7a402bef870f42bbe1ab50c50d891`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b4abcc1f357c7e316def7b4750dd45497bdc2dbd28bb3dafcb05c4042483e9`  
		Last Modified: Tue, 30 Sep 2025 03:29:05 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eff6486d000d63e18b5f0d1576ec9e2467b25ef11a16734684fd9ceefaa3b2`  
		Last Modified: Tue, 30 Sep 2025 20:16:03 GMT  
		Size: 40.8 MB (40754314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:214fdb0f02b73a54cbcc92ccdfe23551d646f430e4c41f8365c4f547af222cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65513711243a0a8f6e5408903985e8ae401e727bac7a69647cd90ad061f8bfc0`

```dockerfile
```

-	Layers:
	-	`sha256:e1ce5dd2387b853a972e2b9c5e10c2c67c640d874734d9f1fbc47057a37716c2`  
		Last Modified: Tue, 30 Sep 2025 13:33:26 GMT  
		Size: 8.0 MB (7974503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cc0c2538fb51e00c0fdf3e0f406e45ffa84bb15f320d994f8123a3365b29a2`  
		Last Modified: Tue, 30 Sep 2025 13:33:27 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json
