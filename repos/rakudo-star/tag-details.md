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
$ docker pull rakudo-star@sha256:47471542197ec18986408525d4e60767e13408fe1cc4a5189fd42fce9d9bd32b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:49ac5f717e5894d3dd9031cfcdc2d234cb1851e0b3dfa2f6b7d078ba9c6976ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52848910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32337d12bcd5ddc338959cd6b7648a0540161b6ffc9980ec7976a0015faecf66`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:20:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 16 Jun 2026 00:38:51 GMT
ARG rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:38:51 GMT
ENV rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:38:51 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 00:38:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 16 Jun 2026 00:38:51 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d4423881da9746e34dcee6f795e2a4b95d273726a5e02ff4e9e0bbe93de9e`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6a325e3cac375651908f9aaaa1b08af0124d54f3ef4f8f701607f590c5689d`  
		Last Modified: Tue, 16 Jun 2026 00:39:04 GMT  
		Size: 49.0 MB (49001573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:255225224384b9a2bb9b558338194a4c43451cf0adb4f785041f790c33d18cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbad4f83f2b3724802bd6c0967df5c350324eb704f43804a52a21207083c520`

```dockerfile
```

-	Layers:
	-	`sha256:475ec7d0e837749a9b1a123477b7e094a30d9ba0501ee5d20a1c5edd28df1f6f`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 185.4 KB (185363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca4b3bb6b207787d6f18249e1671e5eb2a159124a8660f95b8d4f47fe359047`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c830c74f895e4c7b847e2f6b126e68eab62542451317ba9838e0c4505ffe070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52910445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43609fcbd4c16bbbe54046fdc52082193de7e2b037fc2f98b3df641c09b27428`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:20:37 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 16 Jun 2026 00:41:10 GMT
ARG rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:41:10 GMT
ENV rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:41:10 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 00:41:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 16 Jun 2026 00:41:10 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba47cbeed4ca8e9d85d016103200ab5d96f4ad81840b654251b18eb584c6d47`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caa54e5fe82f1206203feae3d0c8296f23bed68e6a47715faa870a518acd000`  
		Last Modified: Tue, 16 Jun 2026 00:41:23 GMT  
		Size: 48.7 MB (48726461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:05e35cac90ae951f92bd1229803323f9c455c4e464985b9b3389ebeccd29a0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 KB (196558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26e150506308d1f82e93a47a77dda8c7dab4a6a5ac0a41ccef3338cf90fa0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d0bb0edfeec7e152dbcd0d92323d822a2b49e18fe37478b247c4ff48cde8de82`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
		Size: 184.7 KB (184745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf4501f1a03d7ace35b54b93755ec3809e839676e2b398046e34c8dd79e1886`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
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
$ docker pull rakudo-star@sha256:47471542197ec18986408525d4e60767e13408fe1cc4a5189fd42fce9d9bd32b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:49ac5f717e5894d3dd9031cfcdc2d234cb1851e0b3dfa2f6b7d078ba9c6976ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52848910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32337d12bcd5ddc338959cd6b7648a0540161b6ffc9980ec7976a0015faecf66`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:20:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 16 Jun 2026 00:38:51 GMT
ARG rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:38:51 GMT
ENV rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:38:51 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 00:38:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 16 Jun 2026 00:38:51 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d4423881da9746e34dcee6f795e2a4b95d273726a5e02ff4e9e0bbe93de9e`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6a325e3cac375651908f9aaaa1b08af0124d54f3ef4f8f701607f590c5689d`  
		Last Modified: Tue, 16 Jun 2026 00:39:04 GMT  
		Size: 49.0 MB (49001573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:255225224384b9a2bb9b558338194a4c43451cf0adb4f785041f790c33d18cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbad4f83f2b3724802bd6c0967df5c350324eb704f43804a52a21207083c520`

```dockerfile
```

-	Layers:
	-	`sha256:475ec7d0e837749a9b1a123477b7e094a30d9ba0501ee5d20a1c5edd28df1f6f`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 185.4 KB (185363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca4b3bb6b207787d6f18249e1671e5eb2a159124a8660f95b8d4f47fe359047`  
		Last Modified: Tue, 16 Jun 2026 00:39:03 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c830c74f895e4c7b847e2f6b126e68eab62542451317ba9838e0c4505ffe070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52910445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43609fcbd4c16bbbe54046fdc52082193de7e2b037fc2f98b3df641c09b27428`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:20:37 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Tue, 16 Jun 2026 00:41:10 GMT
ARG rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:41:10 GMT
ENV rakudo_version=2026.03-01
# Tue, 16 Jun 2026 00:41:10 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 00:41:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 16 Jun 2026 00:41:10 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba47cbeed4ca8e9d85d016103200ab5d96f4ad81840b654251b18eb584c6d47`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caa54e5fe82f1206203feae3d0c8296f23bed68e6a47715faa870a518acd000`  
		Last Modified: Tue, 16 Jun 2026 00:41:23 GMT  
		Size: 48.7 MB (48726461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:05e35cac90ae951f92bd1229803323f9c455c4e464985b9b3389ebeccd29a0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 KB (196558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26e150506308d1f82e93a47a77dda8c7dab4a6a5ac0a41ccef3338cf90fa0cc`

```dockerfile
```

-	Layers:
	-	`sha256:d0bb0edfeec7e152dbcd0d92323d822a2b49e18fe37478b247c4ff48cde8de82`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
		Size: 184.7 KB (184745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf4501f1a03d7ace35b54b93755ec3809e839676e2b398046e34c8dd79e1886`  
		Last Modified: Tue, 16 Jun 2026 00:41:22 GMT  
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
