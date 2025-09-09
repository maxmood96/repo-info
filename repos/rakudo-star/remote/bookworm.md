## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:f0179059c87b13ee3709721557ecb62a05157feeefb086377f8fdb82f24024d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

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

### `rakudo-star:bookworm` - unknown; unknown

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

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0991412639d8865298a5716a356008199765da37b7c184b2e16f8183bd9af278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b08c4ee48cad4cf2ef299958fb3c55c290fc0a741bd4bc1f1da8ab2c478424`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfaf00c9ad5a96e1314ec3213ad52c713c70ad447811d7ba6a2a0af99925559`  
		Last Modified: Wed, 13 Aug 2025 22:54:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac1f6f293558a2ad4aebcba81169189a0e1a017314a3135bd5bc01ada741d8`  
		Last Modified: Wed, 13 Aug 2025 22:54:40 GMT  
		Size: 39.8 MB (39793236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1a51b405e0de690d4b2e69ad2bfae67d469caf7288ee63796056a18913774b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5081688c95b247d88c9d8dba9d478fde974d8d010380c7aa6d5959a17dac1a6`

```dockerfile
```

-	Layers:
	-	`sha256:077b1ce50c2e380e49695a9865785ef314cdcb14af3814260249ced26e6a496f`  
		Last Modified: Thu, 14 Aug 2025 01:33:22 GMT  
		Size: 8.0 MB (7967726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d1b5a6cd1363d5df88b3d0ac564b5125eed86ab2c9c62d2728817333d7fb65`  
		Last Modified: Thu, 14 Aug 2025 01:33:23 GMT  
		Size: 13.1 KB (13142 bytes)  
		MIME: application/vnd.in-toto+json
