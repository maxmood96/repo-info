<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.12-alpine`](#rakudo-star202512-alpine)
-	[`rakudo-star:2025.12-bookworm`](#rakudo-star202512-bookworm)
-	[`rakudo-star:2025.12-trixie`](#rakudo-star202512-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2025.12-alpine`

```console
$ docker pull rakudo-star@sha256:3cd4b7bb2b4e7869943316e3360fc6f3088f186bec05bc87fa07371aac38ffaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:153873a28b70a5350cd24213f82f7d36e0cd45749a7e5830bc57fc2554919ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50209771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec18b184e1c37a8e0406447715868d6e31bb613dce4fa76760fb9dda54b8f02`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Sun, 28 Dec 2025 05:51:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Sun, 28 Dec 2025 06:04:56 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:56 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:56 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Sun, 28 Dec 2025 06:04:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b26f10f97b04dc7bfd04bcffe90fc6e2e3fe8a9d5793c2a4b9eb90484c21b7`  
		Last Modified: Sun, 28 Dec 2025 06:05:11 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f000c3370bee01d2f2e8004d353baa484ef2b0c09f6fce128b37a58e8cd7ff8`  
		Last Modified: Sun, 28 Dec 2025 06:05:17 GMT  
		Size: 46.3 MB (46348720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:93f708e4e9e140c72050fbf7d443eab43cb41baeb7bd6c28fb2a5170172d47c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ff79082f79a8277ec9bf1dda1ec8b912624582eef27581e4fc0ab468687e78`

```dockerfile
```

-	Layers:
	-	`sha256:417793d17f5c4772234cd81e4c21927a0905cfdbec560c0cd8d7bfc9b8f120dc`  
		Last Modified: Sun, 28 Dec 2025 06:05:06 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81bbdba0f6cff7ee180c88f6fd451323a8904217a2ba5f8c0eb2b8a2a6180992`  
		Last Modified: Sun, 28 Dec 2025 08:33:21 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f9425c53293b1c04b177f8d176ec190a099114d727f9a34a61c177eaa1569ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea41bbff6270593d2f71a0bc560f380d42b047551e8a0a815488262bb9cac6`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Sun, 28 Dec 2025 05:53:14 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bd0463e9cce2cf2e69d321d68c112c55ed5938ad6e0f7eadc43a0422d15dd9`  
		Last Modified: Sun, 28 Dec 2025 06:13:12 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a9b3b72876e783969531d568fd8ba185daac1d1319d9dde5cd4a874f5164a`  
		Last Modified: Sun, 28 Dec 2025 06:13:14 GMT  
		Size: 46.1 MB (46085744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b5f6805a4e7f72b8f1b5ed0a029c869f93444b938cb54a6bb2d6747bfaf61666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2097dbf45017e07c2140d46770b097116e7b1f327c83a1b833d6563291c428e`

```dockerfile
```

-	Layers:
	-	`sha256:9419e7a131a2ff381aeb74d53e3b0c551978012aa19c905ae79e781a4931a1e5`  
		Last Modified: Sun, 28 Dec 2025 08:33:37 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07e7c349f0d6d1151c4618b66c26b64dd91dc52cfb0cb17d816c0c09f4ce49d`  
		Last Modified: Sun, 28 Dec 2025 08:33:38 GMT  
		Size: 11.8 KB (11812 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.12-bookworm`

```console
$ docker pull rakudo-star@sha256:e1b7c8b2a926900bc080f97adaff0f9492d5a7d031c2b4156a81c2787ada5ab2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7cc41922ad24d83c9ad0b068ef53ee29a432224321c77b990376d5831bc1f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177959156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff073bd5d1c9ce08cc710c64f93743f39c221e9f4713e5a86a2b38af077870bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:43 GMT
MAINTAINER Rob Hoelz
# Tue, 13 Jan 2026 04:51:43 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:51:43 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:51:43 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:05:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:05:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:05:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41557472c245a24a8e79e7a60a3b3a9acc49b60b1de59751dff57e34918c797`  
		Last Modified: Tue, 13 Jan 2026 05:05:40 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b6ba7c20f1977b9a8e57f72d7dbc7c5897d6cd82337fccb8ac61d660cad1f3`  
		Last Modified: Tue, 13 Jan 2026 05:05:51 GMT  
		Size: 41.0 MB (41041597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:dbac38226426c19f110ef4b97795a1058b9215817105ba62b5d31ddbed412b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbe4a2f07569b5c6aaa2bc0838bb71c2fbee52c70b2a20f5459555156b9e97`

```dockerfile
```

-	Layers:
	-	`sha256:e62eb3be758906c6218959239f00fc1be271f52e6e26c816ef4813ff07717edf`  
		Last Modified: Tue, 13 Jan 2026 05:34:14 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd63f4285767f6f45d525f7a8606ac1f3764db68254c6b810f462e125f409e2a`  
		Last Modified: Tue, 13 Jan 2026 05:05:39 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:fb6fd2148353aca10bcf4646d6b6caa4005d57aae3c5218bd98f2d26382d6057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175526963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431c71b9d7bc00b814cdfbb5caa66e50a37a91258c6a4fab7d13b6b37d9a4131`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:15:03 GMT
MAINTAINER Rob Hoelz
# Tue, 13 Jan 2026 06:15:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 06:15:03 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 06:15:03 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 06:35:02 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 06:35:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 06:35:02 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b29c96f901b7ac597345a95ee6e4c61ec588c07cf17c477464cbcd803d24f84`  
		Last Modified: Tue, 13 Jan 2026 06:35:35 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c237b39c14655402b91c30f8c3a422a96e24297fb61818eac59568bab5aa3e`  
		Last Modified: Tue, 13 Jan 2026 06:35:19 GMT  
		Size: 39.1 MB (39073378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:682692bc15108c2f5d78d814df73970619f3893fa98a1d3305fd626a67f382cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7736b3c969a40de2060f1a39540832b19768db5494170c915d200be458b5f288`

```dockerfile
```

-	Layers:
	-	`sha256:26f5138efc4c550b04fda36e228217f06bd449ed644c57be958368d2e66745a6`  
		Last Modified: Tue, 13 Jan 2026 08:33:36 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3371f29ada3e0bc0d159e6d5f072ab6d9f8a3c18eacb577c5809c6bd5888c7`  
		Last Modified: Tue, 13 Jan 2026 08:33:37 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.12-trixie`

```console
$ docker pull rakudo-star@sha256:32b03d99996f48f0cb7a76210cbc15587332d34e64ed64b1dde6ecc2aee79ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1913d5a6708b4b23836a7f28855b3351491007ce776677636676d0545a6b2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183744853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69948b7fce81a1caa4638d8cdcd8177db8b8eadb4af3ea9c51ab79b314dc9c12`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:09 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:09 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:11:20 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:11:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:11:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01cbdac3b04d00eaa93ad86998b12ba5a5f3d9a66ea8380fed96313151b51a`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f469fcb6a85a93a8a19d82974f30cc72d37a6c31f8c65145e0b7fce118b17`  
		Last Modified: Tue, 13 Jan 2026 05:11:37 GMT  
		Size: 41.1 MB (41055806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3925bcbabc7786bb36dd08e7006ae8a4abe2b509d00559e5448b3c05c629be3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93057dc1878fb1721ed0c6411338dec3f0cd49f2571ae84c89f18cbc47c86a67`

```dockerfile
```

-	Layers:
	-	`sha256:aff6d86459b32171bf9d1f38e859bcccd85b20f86cb01fcf2f94c2f53649be96`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac84df776170f963d38882ed9823bd9fe7a0dabc0c6ca0014b03649ab05adb7`  
		Last Modified: Tue, 13 Jan 2026 08:33:39 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:539a8ecaba69699a71f71b6835032a6a6668a740b3036b02fb408c926a0ffb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181358138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55adc0ddfe68d7c51bab00978f7b49f2832e08f8ed662c5ad4969ca04079a71e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:26 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:26 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:16:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:16:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:16:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a74db4adc441ee4f4a20a76a81486cf86690fcadbcb2438f1a1f01f9400553`  
		Last Modified: Tue, 13 Jan 2026 05:16:57 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea8f1d780b2af1c916a38924b84651302113534657977d2bc3bac79a5260177`  
		Last Modified: Tue, 13 Jan 2026 05:16:41 GMT  
		Size: 39.1 MB (39092668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:554e796f3db2eea8d9cc2a90d10153d186a4a7c0a08de916e0699c2e50ee7656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106415619fced3d04c82d8bf055f8faadceac68fc317ff56d194b1aab5963419`

```dockerfile
```

-	Layers:
	-	`sha256:bce7de2b35bb4d546c1c65152cf7894ec31af56d277519ee5fb07ccc7a647733`  
		Last Modified: Tue, 13 Jan 2026 08:33:47 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236481e610cf6e64fd4c21b1254cfe2e68a0c3332c2dd4f415c895d961bc57a3`  
		Last Modified: Tue, 13 Jan 2026 08:33:48 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:3cd4b7bb2b4e7869943316e3360fc6f3088f186bec05bc87fa07371aac38ffaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:153873a28b70a5350cd24213f82f7d36e0cd45749a7e5830bc57fc2554919ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50209771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec18b184e1c37a8e0406447715868d6e31bb613dce4fa76760fb9dda54b8f02`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Sun, 28 Dec 2025 05:51:19 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Sun, 28 Dec 2025 06:04:56 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:56 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:56 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Sun, 28 Dec 2025 06:04:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:56 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b26f10f97b04dc7bfd04bcffe90fc6e2e3fe8a9d5793c2a4b9eb90484c21b7`  
		Last Modified: Sun, 28 Dec 2025 06:05:11 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f000c3370bee01d2f2e8004d353baa484ef2b0c09f6fce128b37a58e8cd7ff8`  
		Last Modified: Sun, 28 Dec 2025 06:05:17 GMT  
		Size: 46.3 MB (46348720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:93f708e4e9e140c72050fbf7d443eab43cb41baeb7bd6c28fb2a5170172d47c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ff79082f79a8277ec9bf1dda1ec8b912624582eef27581e4fc0ab468687e78`

```dockerfile
```

-	Layers:
	-	`sha256:417793d17f5c4772234cd81e4c21927a0905cfdbec560c0cd8d7bfc9b8f120dc`  
		Last Modified: Sun, 28 Dec 2025 06:05:06 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81bbdba0f6cff7ee180c88f6fd451323a8904217a2ba5f8c0eb2b8a2a6180992`  
		Last Modified: Sun, 28 Dec 2025 08:33:21 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f9425c53293b1c04b177f8d176ec190a099114d727f9a34a61c177eaa1569ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea41bbff6270593d2f71a0bc560f380d42b047551e8a0a815488262bb9cac6`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Sun, 28 Dec 2025 05:53:14 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:52 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Sun, 28 Dec 2025 06:12:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bd0463e9cce2cf2e69d321d68c112c55ed5938ad6e0f7eadc43a0422d15dd9`  
		Last Modified: Sun, 28 Dec 2025 06:13:12 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a9b3b72876e783969531d568fd8ba185daac1d1319d9dde5cd4a874f5164a`  
		Last Modified: Sun, 28 Dec 2025 06:13:14 GMT  
		Size: 46.1 MB (46085744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b5f6805a4e7f72b8f1b5ed0a029c869f93444b938cb54a6bb2d6747bfaf61666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2097dbf45017e07c2140d46770b097116e7b1f327c83a1b833d6563291c428e`

```dockerfile
```

-	Layers:
	-	`sha256:9419e7a131a2ff381aeb74d53e3b0c551978012aa19c905ae79e781a4931a1e5`  
		Last Modified: Sun, 28 Dec 2025 08:33:37 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07e7c349f0d6d1151c4618b66c26b64dd91dc52cfb0cb17d816c0c09f4ce49d`  
		Last Modified: Sun, 28 Dec 2025 08:33:38 GMT  
		Size: 11.8 KB (11812 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:e1b7c8b2a926900bc080f97adaff0f9492d5a7d031c2b4156a81c2787ada5ab2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7cc41922ad24d83c9ad0b068ef53ee29a432224321c77b990376d5831bc1f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177959156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff073bd5d1c9ce08cc710c64f93743f39c221e9f4713e5a86a2b38af077870bc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:43 GMT
MAINTAINER Rob Hoelz
# Tue, 13 Jan 2026 04:51:43 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:51:43 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:51:43 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:05:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:05:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:05:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41557472c245a24a8e79e7a60a3b3a9acc49b60b1de59751dff57e34918c797`  
		Last Modified: Tue, 13 Jan 2026 05:05:40 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b6ba7c20f1977b9a8e57f72d7dbc7c5897d6cd82337fccb8ac61d660cad1f3`  
		Last Modified: Tue, 13 Jan 2026 05:05:51 GMT  
		Size: 41.0 MB (41041597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:dbac38226426c19f110ef4b97795a1058b9215817105ba62b5d31ddbed412b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcbe4a2f07569b5c6aaa2bc0838bb71c2fbee52c70b2a20f5459555156b9e97`

```dockerfile
```

-	Layers:
	-	`sha256:e62eb3be758906c6218959239f00fc1be271f52e6e26c816ef4813ff07717edf`  
		Last Modified: Tue, 13 Jan 2026 05:34:14 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd63f4285767f6f45d525f7a8606ac1f3764db68254c6b810f462e125f409e2a`  
		Last Modified: Tue, 13 Jan 2026 05:05:39 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:fb6fd2148353aca10bcf4646d6b6caa4005d57aae3c5218bd98f2d26382d6057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175526963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431c71b9d7bc00b814cdfbb5caa66e50a37a91258c6a4fab7d13b6b37d9a4131`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:15:03 GMT
MAINTAINER Rob Hoelz
# Tue, 13 Jan 2026 06:15:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 06:15:03 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 06:15:03 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 06:35:02 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 06:35:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 06:35:02 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b29c96f901b7ac597345a95ee6e4c61ec588c07cf17c477464cbcd803d24f84`  
		Last Modified: Tue, 13 Jan 2026 06:35:35 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c237b39c14655402b91c30f8c3a422a96e24297fb61818eac59568bab5aa3e`  
		Last Modified: Tue, 13 Jan 2026 06:35:19 GMT  
		Size: 39.1 MB (39073378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:682692bc15108c2f5d78d814df73970619f3893fa98a1d3305fd626a67f382cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7736b3c969a40de2060f1a39540832b19768db5494170c915d200be458b5f288`

```dockerfile
```

-	Layers:
	-	`sha256:26f5138efc4c550b04fda36e228217f06bd449ed644c57be958368d2e66745a6`  
		Last Modified: Tue, 13 Jan 2026 08:33:36 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3371f29ada3e0bc0d159e6d5f072ab6d9f8a3c18eacb577c5809c6bd5888c7`  
		Last Modified: Tue, 13 Jan 2026 08:33:37 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:32b03d99996f48f0cb7a76210cbc15587332d34e64ed64b1dde6ecc2aee79ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1913d5a6708b4b23836a7f28855b3351491007ce776677636676d0545a6b2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183744853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69948b7fce81a1caa4638d8cdcd8177db8b8eadb4af3ea9c51ab79b314dc9c12`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:09 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:09 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:11:20 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:11:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:11:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01cbdac3b04d00eaa93ad86998b12ba5a5f3d9a66ea8380fed96313151b51a`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f469fcb6a85a93a8a19d82974f30cc72d37a6c31f8c65145e0b7fce118b17`  
		Last Modified: Tue, 13 Jan 2026 05:11:37 GMT  
		Size: 41.1 MB (41055806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3925bcbabc7786bb36dd08e7006ae8a4abe2b509d00559e5448b3c05c629be3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93057dc1878fb1721ed0c6411338dec3f0cd49f2571ae84c89f18cbc47c86a67`

```dockerfile
```

-	Layers:
	-	`sha256:aff6d86459b32171bf9d1f38e859bcccd85b20f86cb01fcf2f94c2f53649be96`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac84df776170f963d38882ed9823bd9fe7a0dabc0c6ca0014b03649ab05adb7`  
		Last Modified: Tue, 13 Jan 2026 08:33:39 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:539a8ecaba69699a71f71b6835032a6a6668a740b3036b02fb408c926a0ffb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181358138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55adc0ddfe68d7c51bab00978f7b49f2832e08f8ed662c5ad4969ca04079a71e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:26 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:26 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:16:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:16:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:16:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a74db4adc441ee4f4a20a76a81486cf86690fcadbcb2438f1a1f01f9400553`  
		Last Modified: Tue, 13 Jan 2026 05:16:57 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea8f1d780b2af1c916a38924b84651302113534657977d2bc3bac79a5260177`  
		Last Modified: Tue, 13 Jan 2026 05:16:41 GMT  
		Size: 39.1 MB (39092668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:554e796f3db2eea8d9cc2a90d10153d186a4a7c0a08de916e0699c2e50ee7656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106415619fced3d04c82d8bf055f8faadceac68fc317ff56d194b1aab5963419`

```dockerfile
```

-	Layers:
	-	`sha256:bce7de2b35bb4d546c1c65152cf7894ec31af56d277519ee5fb07ccc7a647733`  
		Last Modified: Tue, 13 Jan 2026 08:33:47 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236481e610cf6e64fd4c21b1254cfe2e68a0c3332c2dd4f415c895d961bc57a3`  
		Last Modified: Tue, 13 Jan 2026 08:33:48 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:32b03d99996f48f0cb7a76210cbc15587332d34e64ed64b1dde6ecc2aee79ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1913d5a6708b4b23836a7f28855b3351491007ce776677636676d0545a6b2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183744853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69948b7fce81a1caa4638d8cdcd8177db8b8eadb4af3ea9c51ab79b314dc9c12`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:09 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:09 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:09 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:11:20 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:11:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:11:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01cbdac3b04d00eaa93ad86998b12ba5a5f3d9a66ea8380fed96313151b51a`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f469fcb6a85a93a8a19d82974f30cc72d37a6c31f8c65145e0b7fce118b17`  
		Last Modified: Tue, 13 Jan 2026 05:11:37 GMT  
		Size: 41.1 MB (41055806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3925bcbabc7786bb36dd08e7006ae8a4abe2b509d00559e5448b3c05c629be3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93057dc1878fb1721ed0c6411338dec3f0cd49f2571ae84c89f18cbc47c86a67`

```dockerfile
```

-	Layers:
	-	`sha256:aff6d86459b32171bf9d1f38e859bcccd85b20f86cb01fcf2f94c2f53649be96`  
		Last Modified: Tue, 13 Jan 2026 05:11:35 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac84df776170f963d38882ed9823bd9fe7a0dabc0c6ca0014b03649ab05adb7`  
		Last Modified: Tue, 13 Jan 2026 08:33:39 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:539a8ecaba69699a71f71b6835032a6a6668a740b3036b02fb408c926a0ffb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181358138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55adc0ddfe68d7c51bab00978f7b49f2832e08f8ed662c5ad4969ca04079a71e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
MAINTAINER AntonOks
# Tue, 13 Jan 2026 04:56:26 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 13 Jan 2026 04:56:26 GMT
ARG rakudo_version=2025.12-01
# Tue, 13 Jan 2026 04:56:26 GMT
ENV rakudo_version=2025.12-01
# Tue, 13 Jan 2026 05:16:24 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 13 Jan 2026 05:16:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 13 Jan 2026 05:16:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a74db4adc441ee4f4a20a76a81486cf86690fcadbcb2438f1a1f01f9400553`  
		Last Modified: Tue, 13 Jan 2026 05:16:57 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea8f1d780b2af1c916a38924b84651302113534657977d2bc3bac79a5260177`  
		Last Modified: Tue, 13 Jan 2026 05:16:41 GMT  
		Size: 39.1 MB (39092668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:554e796f3db2eea8d9cc2a90d10153d186a4a7c0a08de916e0699c2e50ee7656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106415619fced3d04c82d8bf055f8faadceac68fc317ff56d194b1aab5963419`

```dockerfile
```

-	Layers:
	-	`sha256:bce7de2b35bb4d546c1c65152cf7894ec31af56d277519ee5fb07ccc7a647733`  
		Last Modified: Tue, 13 Jan 2026 08:33:47 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236481e610cf6e64fd4c21b1254cfe2e68a0c3332c2dd4f415c895d961bc57a3`  
		Last Modified: Tue, 13 Jan 2026 08:33:48 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
