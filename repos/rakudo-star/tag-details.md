<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2026.03-alpine`](#rakudo-star202603-alpine)
-	[`rakudo-star:2026.03-bookworm`](#rakudo-star202603-bookworm)
-	[`rakudo-star:2026.03-trixie`](#rakudo-star202603-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2026.03-alpine`

```console
$ docker pull rakudo-star@sha256:8f2e86af88503f29cb269956ba5019ff051c361ca5a0075e30af27673ac1aa94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:2be3f270ca4b1744f65bedc5ee12ec21ea9f9f68867d281ac6d2e20309d6e48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52840569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8c7552cfb8bfdff23f366b7dea22e95a272d55d113eece60b756edeceeca15`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:16:47 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 09 Jun 2026 20:35:21 GMT
ARG rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:35:21 GMT
ENV rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Jun 2026 20:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384246d0ee0439f0e83319d9263de291171fc8278c6b811139681d641b4b093c`  
		Last Modified: Tue, 09 Jun 2026 20:35:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d659d1a5f78defdcdb1d2f3afd9979661742d6a25e21a9668546cc023d846f`  
		Last Modified: Tue, 09 Jun 2026 20:35:34 GMT  
		Size: 49.0 MB (48972865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:14eb80d7691f750ef08d6ef4a1032a30346b747753d7043175ceaea7fd1c390c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127402c75aff25a0020c7f3282830f93aa4ff7b6c59c5f9dc44a66f70198ffb4`

```dockerfile
```

-	Layers:
	-	`sha256:2347a0d1619673819d890aee934e2e50f98b56c7d80d570ce0fb935a20ba9aa1`  
		Last Modified: Tue, 09 Jun 2026 20:35:33 GMT  
		Size: 185.4 KB (185363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddd9302cdbea7f1784372476752fe9da85ab4762d9888919e02cf36819ff2c2`  
		Last Modified: Tue, 09 Jun 2026 20:35:33 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:848d021898ddc67449437a6c87d11929366b2b1b8e1610374ea8b3e4e0d0b22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52907062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf854218ade9ad91635ac3258f494591b10b938d4d7b05101c77390540b81c3`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:16:43 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 09 Jun 2026 20:37:56 GMT
ARG rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:37:56 GMT
ENV rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:37:56 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:37:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Jun 2026 20:37:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ee773cfa75add60e28e0aa6c1a8db1aaaeb7437375f872531223c17132b44`  
		Last Modified: Tue, 09 Jun 2026 20:38:13 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85392b69bc9874e9f8ff3eacd8e786fe69ada5ea7612e50c0a6514c5ab03b9a3`  
		Last Modified: Tue, 09 Jun 2026 20:38:15 GMT  
		Size: 48.7 MB (48703786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2371c551895cd3e7484cbd7dd664c5b21a88382e440195325d7d89a53bb5ae24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 KB (196558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d758e0ec4922fd2e08023ce3a7cdb1dbc272dde938782ed7da9df419b91293`

```dockerfile
```

-	Layers:
	-	`sha256:2c7a23d10094ca2cb503e4ad44dc508dd874e4e8e5dc4ec481ca39da3b4093f7`  
		Last Modified: Tue, 09 Jun 2026 20:38:08 GMT  
		Size: 184.7 KB (184745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8923402c88ce90c0e535ed8a28e716143bd98be63e2d5d5c4584e70289bf203`  
		Last Modified: Tue, 09 Jun 2026 20:38:08 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-bookworm`

```console
$ docker pull rakudo-star@sha256:45ac99f147f00b2a0fb6077c0eb6eb474fab52531ed61ca14593ad907c57494b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:829985b30a7121392bd72afa2ca81c507aba27834c7f371808ceddabfb1c6f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179318413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc9657cf099ae6c0a6edc1ae958ff2c4407430690cc37440f4a740adfb72744`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:19:25 GMT
MAINTAINER Rob Hoelz
# Thu, 11 Jun 2026 03:19:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:25 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:25 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:37:44 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:37:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:37:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed6cae31b41296b0655eb517dd02a3710bcb2e54c003084ff93e7b68f9513b2`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63a5a2cc6ddf4f13666b5906df2cd95ebb3165cdf1fbb63ad3f60711845a68`  
		Last Modified: Thu, 11 Jun 2026 03:38:00 GMT  
		Size: 42.4 MB (42365017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f36c8e4f1bac49f26f086784e1f69eabacf0a2fa1fbff3619530f1a474067732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4d2b7001891f2095d841abcbc736563af0413843adb643217edbb4e37d56a4`

```dockerfile
```

-	Layers:
	-	`sha256:677ba7bbc499e5152049b550cdae3151175187888dc29f8d7093efb37bbe19a0`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 8.0 MB (7968487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa596996be8fac250f7776ac14d06d2639ec0a89e18054e6e99a2678213bd36`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:957e62e865fe46f0d8fa9c78cea9f2b2c2f7f6f1ebca8d6f9a1897e5fe0f5407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176865868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ed0f7b419faec3e35c68b50d102490e69a0e29ed1d27d94ac78c4bab10ba41`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:19:35 GMT
MAINTAINER Rob Hoelz
# Thu, 11 Jun 2026 03:19:35 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:35 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:35 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:38:51 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:38:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:38:51 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba543629361f82fcbc09525073b37b91b203f213f38db43d4e17e446776d6b4`  
		Last Modified: Thu, 11 Jun 2026 03:39:06 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc8fe71151bccdd9857b8f3b63941470725346e2ee35219fb86b7fdad466f8`  
		Last Modified: Thu, 11 Jun 2026 03:39:07 GMT  
		Size: 40.4 MB (40372441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a554445a235b6bc9c15e25cd90fecd8201253c84cd7b65974c08d5ad71616b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121ed5702cbae663acc2798d7922101d9f689dbe304ae94fa9e150731b58a237`

```dockerfile
```

-	Layers:
	-	`sha256:9b5c6485a776680f0b531a5424cd0b9a4fc4ed43ac21f198b5da01769fdb3b39`  
		Last Modified: Thu, 11 Jun 2026 03:39:07 GMT  
		Size: 8.0 MB (7974880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30efbf92c7fa93c0df2c45e13df3cd206137ffe03d9d251aac3c2d41a9501ae0`  
		Last Modified: Thu, 11 Jun 2026 03:39:06 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:e388a18ddedb3ecf448cfadc0c9a984ed8aad4c1dd149aececb6fc513e9c9fb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

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

### `rakudo-star:2026.03-trixie` - unknown; unknown

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

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

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

### `rakudo-star:2026.03-trixie` - unknown; unknown

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

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:8f2e86af88503f29cb269956ba5019ff051c361ca5a0075e30af27673ac1aa94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:2be3f270ca4b1744f65bedc5ee12ec21ea9f9f68867d281ac6d2e20309d6e48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52840569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8c7552cfb8bfdff23f366b7dea22e95a272d55d113eece60b756edeceeca15`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:16:47 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 09 Jun 2026 20:35:21 GMT
ARG rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:35:21 GMT
ENV rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Jun 2026 20:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384246d0ee0439f0e83319d9263de291171fc8278c6b811139681d641b4b093c`  
		Last Modified: Tue, 09 Jun 2026 20:35:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d659d1a5f78defdcdb1d2f3afd9979661742d6a25e21a9668546cc023d846f`  
		Last Modified: Tue, 09 Jun 2026 20:35:34 GMT  
		Size: 49.0 MB (48972865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:14eb80d7691f750ef08d6ef4a1032a30346b747753d7043175ceaea7fd1c390c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127402c75aff25a0020c7f3282830f93aa4ff7b6c59c5f9dc44a66f70198ffb4`

```dockerfile
```

-	Layers:
	-	`sha256:2347a0d1619673819d890aee934e2e50f98b56c7d80d570ce0fb935a20ba9aa1`  
		Last Modified: Tue, 09 Jun 2026 20:35:33 GMT  
		Size: 185.4 KB (185363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddd9302cdbea7f1784372476752fe9da85ab4762d9888919e02cf36819ff2c2`  
		Last Modified: Tue, 09 Jun 2026 20:35:33 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:848d021898ddc67449437a6c87d11929366b2b1b8e1610374ea8b3e4e0d0b22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52907062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf854218ade9ad91635ac3258f494591b10b938d4d7b05101c77390540b81c3`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 20:16:43 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 09 Jun 2026 20:37:56 GMT
ARG rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:37:56 GMT
ENV rakudo_version=2026.03-01
# Tue, 09 Jun 2026 20:37:56 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 09 Jun 2026 20:37:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 09 Jun 2026 20:37:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ee773cfa75add60e28e0aa6c1a8db1aaaeb7437375f872531223c17132b44`  
		Last Modified: Tue, 09 Jun 2026 20:38:13 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85392b69bc9874e9f8ff3eacd8e786fe69ada5ea7612e50c0a6514c5ab03b9a3`  
		Last Modified: Tue, 09 Jun 2026 20:38:15 GMT  
		Size: 48.7 MB (48703786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2371c551895cd3e7484cbd7dd664c5b21a88382e440195325d7d89a53bb5ae24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 KB (196558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d758e0ec4922fd2e08023ce3a7cdb1dbc272dde938782ed7da9df419b91293`

```dockerfile
```

-	Layers:
	-	`sha256:2c7a23d10094ca2cb503e4ad44dc508dd874e4e8e5dc4ec481ca39da3b4093f7`  
		Last Modified: Tue, 09 Jun 2026 20:38:08 GMT  
		Size: 184.7 KB (184745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8923402c88ce90c0e535ed8a28e716143bd98be63e2d5d5c4584e70289bf203`  
		Last Modified: Tue, 09 Jun 2026 20:38:08 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:45ac99f147f00b2a0fb6077c0eb6eb474fab52531ed61ca14593ad907c57494b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:829985b30a7121392bd72afa2ca81c507aba27834c7f371808ceddabfb1c6f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179318413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc9657cf099ae6c0a6edc1ae958ff2c4407430690cc37440f4a740adfb72744`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:19:25 GMT
MAINTAINER Rob Hoelz
# Thu, 11 Jun 2026 03:19:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:25 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:25 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:37:44 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:37:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:37:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed6cae31b41296b0655eb517dd02a3710bcb2e54c003084ff93e7b68f9513b2`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63a5a2cc6ddf4f13666b5906df2cd95ebb3165cdf1fbb63ad3f60711845a68`  
		Last Modified: Thu, 11 Jun 2026 03:38:00 GMT  
		Size: 42.4 MB (42365017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f36c8e4f1bac49f26f086784e1f69eabacf0a2fa1fbff3619530f1a474067732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4d2b7001891f2095d841abcbc736563af0413843adb643217edbb4e37d56a4`

```dockerfile
```

-	Layers:
	-	`sha256:677ba7bbc499e5152049b550cdae3151175187888dc29f8d7093efb37bbe19a0`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 8.0 MB (7968487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa596996be8fac250f7776ac14d06d2639ec0a89e18054e6e99a2678213bd36`  
		Last Modified: Thu, 11 Jun 2026 03:37:59 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:957e62e865fe46f0d8fa9c78cea9f2b2c2f7f6f1ebca8d6f9a1897e5fe0f5407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176865868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ed0f7b419faec3e35c68b50d102490e69a0e29ed1d27d94ac78c4bab10ba41`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:19:35 GMT
MAINTAINER Rob Hoelz
# Thu, 11 Jun 2026 03:19:35 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 11 Jun 2026 03:19:35 GMT
ARG rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:19:35 GMT
ENV rakudo_version=2026.03-01
# Thu, 11 Jun 2026 03:38:51 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 03:38:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 11 Jun 2026 03:38:51 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba543629361f82fcbc09525073b37b91b203f213f38db43d4e17e446776d6b4`  
		Last Modified: Thu, 11 Jun 2026 03:39:06 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fc8fe71151bccdd9857b8f3b63941470725346e2ee35219fb86b7fdad466f8`  
		Last Modified: Thu, 11 Jun 2026 03:39:07 GMT  
		Size: 40.4 MB (40372441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a554445a235b6bc9c15e25cd90fecd8201253c84cd7b65974c08d5ad71616b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121ed5702cbae663acc2798d7922101d9f689dbe304ae94fa9e150731b58a237`

```dockerfile
```

-	Layers:
	-	`sha256:9b5c6485a776680f0b531a5424cd0b9a4fc4ed43ac21f198b5da01769fdb3b39`  
		Last Modified: Thu, 11 Jun 2026 03:39:07 GMT  
		Size: 8.0 MB (7974880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30efbf92c7fa93c0df2c45e13df3cd206137ffe03d9d251aac3c2d41a9501ae0`  
		Last Modified: Thu, 11 Jun 2026 03:39:06 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e388a18ddedb3ecf448cfadc0c9a984ed8aad4c1dd149aececb6fc513e9c9fb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

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

### `rakudo-star:latest` - unknown; unknown

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

### `rakudo-star:latest` - linux; arm64 variant v8

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

### `rakudo-star:latest` - unknown; unknown

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
