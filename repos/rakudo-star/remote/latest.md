## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:859dca40ecfc4763ba39fb036bf9a77dcba5521ac72ae1c44681757dabef4014
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f419cc19bf96ab5fc54e9f63f00b7d88eb21e252b40d021480d312fb92f074b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178446832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b381f7262637b49aa74d59eb1e3f6639225cdd7bccf7502d743f02edb953313`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe1dba7dae228ec26a36f44bbc5eb3516641271be68bd68fb61b647357b116c`  
		Last Modified: Mon, 08 Sep 2025 22:51:48 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad93dc89a90d00b6fa7774ba033b2e06e8473d6b575ee273a9be7073cb85081`  
		Last Modified: Mon, 08 Sep 2025 23:16:32 GMT  
		Size: 41.5 MB (41540081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2115b4ca46d8069b9d0ed8d8e24b074061bb947db7f28bf4841caa84469cbcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2c9dda89d9eb261b8515cf9a2570b026db81a9cd47f45c39c29d1e564513a8`

```dockerfile
```

-	Layers:
	-	`sha256:63b3321805a680fed6e56d20d24468a6ffe644cb79e4c79a707681af52dfd60f`  
		Last Modified: Tue, 09 Sep 2025 01:33:18 GMT  
		Size: 8.0 MB (7968094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7e1a1af72bb011404ddebcf43329ee7d469c86dfc15c3e8632d092bd3c2232`  
		Last Modified: Tue, 09 Sep 2025 01:33:19 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

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

### `rakudo-star:latest` - unknown; unknown

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
