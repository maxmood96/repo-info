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
