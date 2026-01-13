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
		Last Modified: Sun, 28 Dec 2025 08:33:20 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
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
$ docker pull rakudo-star@sha256:ca170afeac468254fcea99227ef661c58d10a02e2ae5a1d5b57bf823b766bc14
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
		Last Modified: Tue, 13 Jan 2026 03:53:38 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41557472c245a24a8e79e7a60a3b3a9acc49b60b1de59751dff57e34918c797`  
		Last Modified: Tue, 13 Jan 2026 05:05:47 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:34:15 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:91c85350f60e78dd4d5dcd09a420b7fe83a8a177fc13a6f78a97a856338f21f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174127585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9a65ba2af6ce3866e60e7e3deeb8a143ff014c95b002d33612c3c73610de1e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:44:48 GMT
MAINTAINER Rob Hoelz
# Tue, 30 Dec 2025 02:44:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:44:48 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:44:48 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 03:03:52 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 03:03:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 03:03:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26720327245925d8b488db7fb116fd72a91cee5660a19e90d92c59fa5dc0a068`  
		Last Modified: Tue, 30 Dec 2025 03:04:24 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144f754970ff187a944b30183bdf780802dc35b5b9b49ef9f9f5c52be554098`  
		Last Modified: Tue, 30 Dec 2025 03:04:27 GMT  
		Size: 37.8 MB (37795652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9664921f70837002543c65835eb7c5c3b4c759dee062c27991ed2ca4b8aed3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e39c3a76554f6adcb30571f2c132b910228804639b3be7fcc54eb4c7e6cf52f`

```dockerfile
```

-	Layers:
	-	`sha256:881525199aed0a5227d524c63129d62174d4a1de839a1bc3a71dfc8ae815d882`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6dee3cf2308f72909d75f4f349d8e5bb8529b7d13d3b7a82d9457d5c52b6628`  
		Last Modified: Tue, 30 Dec 2025 05:33:35 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.12-trixie`

```console
$ docker pull rakudo-star@sha256:ba29db88ffcf9bed704225716fe755cf30f7db3351c6fa676e5dba70e952dad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1d2976087dbb6d5b6ad925bd50817cc52c1a8bb74f10e4a26027e5228ec101e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182464094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04794bf5ff584f03d14b88d80cf74b84b4a28765f5cf03f6b1fa596d00416bda`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:45:20 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:45:20 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:59:54 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 02:59:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 02:59:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd65e4d82af3b14eee9c6df49a5ae33648336694b1e48e13d4ed108d09d8ea2`  
		Last Modified: Tue, 30 Dec 2025 03:00:17 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f5db4fe6775b11f1e1c18d6f7d56100538b7e93e1dedac5cd13b03d7076c3`  
		Last Modified: Tue, 30 Dec 2025 03:00:22 GMT  
		Size: 39.8 MB (39780050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:67c62be955ed2dab036404f5d79786090bfadebb7dca48c7e828ffaecc25863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd661138391ad07c3fd90fa52c7b3272eeb9b53c5c225112ee027fbdb65ba0a`

```dockerfile
```

-	Layers:
	-	`sha256:20ae3b812329e323e2f2f8cad6caab724f7c3b27cfda9735660c01ec8e5898c6`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1298672bd4027c2a28085385d1e0e373e7b2b1b8f1b16b352a7f77dadfb1694`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:47cef26b5ffec230c092cbef5599db08ca35c9b221c1fcf0ad3a429c3eddaef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180001543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bfa213774b801104da8345c7f50e05dff5d18875f8d41cc6324421d4b95233`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:44:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:44:31 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 03:03:25 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 03:03:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 03:03:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb761965deec88b759ada468a4188bbd4bb068eb7fb5e3214a28b4d708135c`  
		Last Modified: Tue, 30 Dec 2025 03:03:58 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c639bb98abdb3d5de8c0783a2f3fdf468b161b84191ff301bddfd060a3872ea`  
		Last Modified: Tue, 30 Dec 2025 03:04:02 GMT  
		Size: 37.7 MB (37743277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:dc4646bac1b0f274c6e87232183c1b14212c913d4de32b920fbf51a454262c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48891997668b8af7c7668c78bd1e4145a1874adaa785561d600a9fdc51bc71`

```dockerfile
```

-	Layers:
	-	`sha256:69a129d518039839c06e07468bbf10bc6e584f599202a6dd87e5f97e572c77d9`  
		Last Modified: Tue, 30 Dec 2025 05:33:41 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03feb99a1869db79b6c37c4c2497333e1099068261d84e481a62338f895aecf4`  
		Last Modified: Tue, 30 Dec 2025 05:33:50 GMT  
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
		Last Modified: Sun, 28 Dec 2025 08:33:20 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
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
$ docker pull rakudo-star@sha256:ca170afeac468254fcea99227ef661c58d10a02e2ae5a1d5b57bf823b766bc14
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
		Last Modified: Tue, 13 Jan 2026 03:53:38 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41557472c245a24a8e79e7a60a3b3a9acc49b60b1de59751dff57e34918c797`  
		Last Modified: Tue, 13 Jan 2026 05:05:47 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:34:15 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:91c85350f60e78dd4d5dcd09a420b7fe83a8a177fc13a6f78a97a856338f21f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174127585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9a65ba2af6ce3866e60e7e3deeb8a143ff014c95b002d33612c3c73610de1e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:44:48 GMT
MAINTAINER Rob Hoelz
# Tue, 30 Dec 2025 02:44:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:44:48 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:44:48 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 03:03:52 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 03:03:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 03:03:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26720327245925d8b488db7fb116fd72a91cee5660a19e90d92c59fa5dc0a068`  
		Last Modified: Tue, 30 Dec 2025 03:04:24 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144f754970ff187a944b30183bdf780802dc35b5b9b49ef9f9f5c52be554098`  
		Last Modified: Tue, 30 Dec 2025 03:04:27 GMT  
		Size: 37.8 MB (37795652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9664921f70837002543c65835eb7c5c3b4c759dee062c27991ed2ca4b8aed3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e39c3a76554f6adcb30571f2c132b910228804639b3be7fcc54eb4c7e6cf52f`

```dockerfile
```

-	Layers:
	-	`sha256:881525199aed0a5227d524c63129d62174d4a1de839a1bc3a71dfc8ae815d882`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6dee3cf2308f72909d75f4f349d8e5bb8529b7d13d3b7a82d9457d5c52b6628`  
		Last Modified: Tue, 30 Dec 2025 05:33:35 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:ba29db88ffcf9bed704225716fe755cf30f7db3351c6fa676e5dba70e952dad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1d2976087dbb6d5b6ad925bd50817cc52c1a8bb74f10e4a26027e5228ec101e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182464094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04794bf5ff584f03d14b88d80cf74b84b4a28765f5cf03f6b1fa596d00416bda`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:45:20 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:45:20 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:59:54 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 02:59:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 02:59:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd65e4d82af3b14eee9c6df49a5ae33648336694b1e48e13d4ed108d09d8ea2`  
		Last Modified: Tue, 30 Dec 2025 03:00:17 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f5db4fe6775b11f1e1c18d6f7d56100538b7e93e1dedac5cd13b03d7076c3`  
		Last Modified: Tue, 30 Dec 2025 03:00:22 GMT  
		Size: 39.8 MB (39780050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:67c62be955ed2dab036404f5d79786090bfadebb7dca48c7e828ffaecc25863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd661138391ad07c3fd90fa52c7b3272eeb9b53c5c225112ee027fbdb65ba0a`

```dockerfile
```

-	Layers:
	-	`sha256:20ae3b812329e323e2f2f8cad6caab724f7c3b27cfda9735660c01ec8e5898c6`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1298672bd4027c2a28085385d1e0e373e7b2b1b8f1b16b352a7f77dadfb1694`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:47cef26b5ffec230c092cbef5599db08ca35c9b221c1fcf0ad3a429c3eddaef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180001543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bfa213774b801104da8345c7f50e05dff5d18875f8d41cc6324421d4b95233`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:44:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:44:31 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 03:03:25 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 03:03:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 03:03:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb761965deec88b759ada468a4188bbd4bb068eb7fb5e3214a28b4d708135c`  
		Last Modified: Tue, 30 Dec 2025 03:03:58 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c639bb98abdb3d5de8c0783a2f3fdf468b161b84191ff301bddfd060a3872ea`  
		Last Modified: Tue, 30 Dec 2025 03:04:02 GMT  
		Size: 37.7 MB (37743277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:dc4646bac1b0f274c6e87232183c1b14212c913d4de32b920fbf51a454262c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48891997668b8af7c7668c78bd1e4145a1874adaa785561d600a9fdc51bc71`

```dockerfile
```

-	Layers:
	-	`sha256:69a129d518039839c06e07468bbf10bc6e584f599202a6dd87e5f97e572c77d9`  
		Last Modified: Tue, 30 Dec 2025 05:33:41 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03feb99a1869db79b6c37c4c2497333e1099068261d84e481a62338f895aecf4`  
		Last Modified: Tue, 30 Dec 2025 05:33:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:ba29db88ffcf9bed704225716fe755cf30f7db3351c6fa676e5dba70e952dad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1d2976087dbb6d5b6ad925bd50817cc52c1a8bb74f10e4a26027e5228ec101e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182464094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04794bf5ff584f03d14b88d80cf74b84b4a28765f5cf03f6b1fa596d00416bda`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:45:20 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:45:20 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:59:54 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 02:59:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 02:59:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd65e4d82af3b14eee9c6df49a5ae33648336694b1e48e13d4ed108d09d8ea2`  
		Last Modified: Tue, 30 Dec 2025 03:00:17 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f5db4fe6775b11f1e1c18d6f7d56100538b7e93e1dedac5cd13b03d7076c3`  
		Last Modified: Tue, 30 Dec 2025 03:00:22 GMT  
		Size: 39.8 MB (39780050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:67c62be955ed2dab036404f5d79786090bfadebb7dca48c7e828ffaecc25863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd661138391ad07c3fd90fa52c7b3272eeb9b53c5c225112ee027fbdb65ba0a`

```dockerfile
```

-	Layers:
	-	`sha256:20ae3b812329e323e2f2f8cad6caab724f7c3b27cfda9735660c01ec8e5898c6`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1298672bd4027c2a28085385d1e0e373e7b2b1b8f1b16b352a7f77dadfb1694`  
		Last Modified: Tue, 30 Dec 2025 05:33:34 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:47cef26b5ffec230c092cbef5599db08ca35c9b221c1fcf0ad3a429c3eddaef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180001543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bfa213774b801104da8345c7f50e05dff5d18875f8d41cc6324421d4b95233`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
MAINTAINER AntonOks
# Tue, 30 Dec 2025 02:44:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 30 Dec 2025 02:44:31 GMT
ARG rakudo_version=2025.12-01
# Tue, 30 Dec 2025 02:44:31 GMT
ENV rakudo_version=2025.12-01
# Tue, 30 Dec 2025 03:03:25 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 03:03:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 30 Dec 2025 03:03:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb761965deec88b759ada468a4188bbd4bb068eb7fb5e3214a28b4d708135c`  
		Last Modified: Tue, 30 Dec 2025 03:03:58 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c639bb98abdb3d5de8c0783a2f3fdf468b161b84191ff301bddfd060a3872ea`  
		Last Modified: Tue, 30 Dec 2025 03:04:02 GMT  
		Size: 37.7 MB (37743277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:dc4646bac1b0f274c6e87232183c1b14212c913d4de32b920fbf51a454262c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a48891997668b8af7c7668c78bd1e4145a1874adaa785561d600a9fdc51bc71`

```dockerfile
```

-	Layers:
	-	`sha256:69a129d518039839c06e07468bbf10bc6e584f599202a6dd87e5f97e572c77d9`  
		Last Modified: Tue, 30 Dec 2025 05:33:41 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03feb99a1869db79b6c37c4c2497333e1099068261d84e481a62338f895aecf4`  
		Last Modified: Tue, 30 Dec 2025 05:33:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
