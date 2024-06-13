## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:5767d845f9407554b497e5e9a8ab534a1130d7032258869bb26f9316b8f06f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:642f6d12a9c57d12423ab761bef9f6ef3e82a9690c0e74b726d73689ff79d57d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181454176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5f4d20d49e0b6bef98f95a40dec349956f6ad4e580e9d0ddfa6c650ef8c43c`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:43 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 13 Jun 2024 01:20:44 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 11:04:53 GMT
MAINTAINER Rob Hoelz
# Thu, 13 Jun 2024 11:04:54 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 13 Jun 2024 11:04:54 GMT
ARG rakudo_version=2024.05-01
# Thu, 13 Jun 2024 11:04:54 GMT
ENV rakudo_version=2024.05-01
# Thu, 13 Jun 2024 11:25:59 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 11:26:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 13 Jun 2024 11:26:00 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425debfb35cb62e4a4d887e6cc0da0b8c298ee34fe2303464d483c3c148103e5`  
		Last Modified: Thu, 13 Jun 2024 11:26:13 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd91cfa3757a8b95d4d74e138d821e6e6c92a64942edcad76725fd370495898`  
		Last Modified: Thu, 13 Jun 2024 11:26:21 GMT  
		Size: 43.7 MB (43682225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8f9c94071c63573cf1803694e53411313f3cc70133d98f21fbb5f7b33cae2a0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180690892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9ba0abf7ddaea3d75e5ea995198c7ab337a57b79e2f8a350420e78cfce86e`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 08:25:21 GMT
MAINTAINER Rob Hoelz
# Thu, 13 Jun 2024 08:25:22 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 13 Jun 2024 08:25:22 GMT
ARG rakudo_version=2024.05-01
# Thu, 13 Jun 2024 08:25:22 GMT
ENV rakudo_version=2024.05-01
# Thu, 13 Jun 2024 08:43:05 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 08:43:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 13 Jun 2024 08:43:06 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b996698ee9456c430b0459fb22796f367cf75a685ffc022bdde00e5f183ca6a`  
		Last Modified: Thu, 13 Jun 2024 08:43:24 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb8e8ac3c1e2d97010be518dcb4ecb64805ab50f61182d4d5942ca275029d03`  
		Last Modified: Thu, 13 Jun 2024 08:43:31 GMT  
		Size: 43.5 MB (43492918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
