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
$ docker pull rakudo-star@sha256:4b1ba41dc735375eb0f59d178c4c1b83612b8852c0412904fb196131f7a54f71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e8d0b0551dd6d7e29339b9b3b5556128d4428da9f73acc6e04a2a2547071f8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176664290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6799b6f107474de8cee4d63e3fce66c7937f9cdeb31fd126c41999adccfb2d67`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Dec 2025 05:51:13 GMT
MAINTAINER Rob Hoelz
# Sun, 28 Dec 2025 05:51:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:13 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:13 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:49 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffff8855009578229b73d658190669884716a772b7ea03fc6dfe4499715c128`  
		Last Modified: Sun, 28 Dec 2025 06:05:11 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267adcdb7b34c0bba02ef36e2eba2efa621882068fc2b6f7e64f83894fb7a24`  
		Last Modified: Sun, 28 Dec 2025 06:05:16 GMT  
		Size: 39.8 MB (39754457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cd41aeec76fcd05354986cf47255ec9ea93893c6a542e45d04fa2658888dc934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab4710b2795f1f0e9bd99fc83d5e31a9d49e909d7a332580eb0f9f682e502c4`

```dockerfile
```

-	Layers:
	-	`sha256:cf09c9b6e43e1c484c5141e04e46ae23493b95b109ca05601ad311146a15b7e7`  
		Last Modified: Sun, 28 Dec 2025 08:33:29 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f0869668bc3e1cfe1ce6dd3289ade54a7ae1b232183bab66d0461e13df802c`  
		Last Modified: Sun, 28 Dec 2025 08:33:30 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:550a0be23df2a0fb87c855759834b8d8e500d9071bd22d2deb25f0e2f66ac538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174128477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4847cfd1046da661846018cc93f85c9cadaf6c3168feb1e657ef3287071476`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Dec 2025 05:52:48 GMT
MAINTAINER Rob Hoelz
# Sun, 28 Dec 2025 05:52:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:48 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:48 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:11:18 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:11:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:11:18 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a0fe8ec3e714678196937525cf83b878e958b9a2955403237aa25ff3e1103`  
		Last Modified: Sun, 28 Dec 2025 06:11:41 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae45635f620176965a51223386f46e9bf93a2f4d05c3fbc3c1961113a278fcbf`  
		Last Modified: Sun, 28 Dec 2025 06:11:44 GMT  
		Size: 37.8 MB (37796429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bf68fc565e5ae0115ff1efc764f0d825ec3646c928418cf17ba790ed6f8ba75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4524e914e44bc1ab4624337731fd7cf781033107d7bb744b9a7af2828b9db89`

```dockerfile
```

-	Layers:
	-	`sha256:b6f85b1d75a9bbb4fc68d40606f23a178786ca35bf298c70b8dbf1fce4cba64f`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68686b0ad2338b237714abaadca51a766e1bc6451fcae3afc98ef5b88b189f37`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.12-trixie`

```console
$ docker pull rakudo-star@sha256:588eeb71c889832b0753c41f5488d2cc4dfed9eb3097b6044fa4fe4b9780ebc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.12-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c327678130dc4cc21016b4797e7db4acc8eb0006237579dba5261f22be1cfdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182454535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa5465b728c615b686b632c67aa901e486ee8f5dd58d3b0366cb362f072128c`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:51:01 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:01 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:58 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:58 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95217a361e37efeac6ad41b978aeb38f999c166ef3a0bbb6b0ab96ec7039350e`  
		Last Modified: Sun, 28 Dec 2025 06:05:20 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34137921a2e46afb191b17ceaf28bb332e63dfd262869b8a6df6095e8b07d88`  
		Last Modified: Sun, 28 Dec 2025 06:05:25 GMT  
		Size: 39.8 MB (39769261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7ff558f7a81805375ec83bcbaec2db641d9102d0d2ddd22403c44878f3c72fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c9158dd4c950625b697fda25a60fa8fcc74176e78d462a30e65fa1aa0ddc17`

```dockerfile
```

-	Layers:
	-	`sha256:0991552a10ff7383368da1ed1ac2635b9bb9353bf4f84dc105a5df0fe63a6dd3`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cba456c68ea28728fa377a36e3a33ef283f7ddc75966f61b04398cdd96a3f5`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.12-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:133dceefe28117eaa25f7a676d1c698fd00d18fa172796f1f2a39fae3069b4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180073593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31e3b95f4f14b9f733a219207da8235471e91dded23d37fc28a8f9262518030`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:52:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:12 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:07 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:12:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8eec79c9a4e5bc4dd20acecdde355a57d33906fdf19b4ea9a45d404d180499`  
		Last Modified: Sun, 28 Dec 2025 06:12:30 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405a3fd297caf3404b3b4e80425f58185229292e66edc966cce2ae56b383137`  
		Last Modified: Sun, 28 Dec 2025 06:12:33 GMT  
		Size: 37.8 MB (37814168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.12-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b97dac5e2c1dfde6e85254a359111f71863a91f26ae517bc3431174a58b38593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b672b2980dc22eb95f9fca365a146ae75dc544a7afc8d9b79bdb9b06ff1d97`

```dockerfile
```

-	Layers:
	-	`sha256:3308fa553a2c791b08292e5777d2770bf27e2fa52106da0576049497294855d5`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97b1945a3b482a96aa0fa587c119d53041f70a1d62fbcdfdd3ba8ae6c77b7fb`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 13.1 KB (13099 bytes)  
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
$ docker pull rakudo-star@sha256:4b1ba41dc735375eb0f59d178c4c1b83612b8852c0412904fb196131f7a54f71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e8d0b0551dd6d7e29339b9b3b5556128d4428da9f73acc6e04a2a2547071f8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176664290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6799b6f107474de8cee4d63e3fce66c7937f9cdeb31fd126c41999adccfb2d67`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Dec 2025 05:51:13 GMT
MAINTAINER Rob Hoelz
# Sun, 28 Dec 2025 05:51:13 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:13 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:13 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:49 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffff8855009578229b73d658190669884716a772b7ea03fc6dfe4499715c128`  
		Last Modified: Sun, 28 Dec 2025 06:05:11 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267adcdb7b34c0bba02ef36e2eba2efa621882068fc2b6f7e64f83894fb7a24`  
		Last Modified: Sun, 28 Dec 2025 06:05:16 GMT  
		Size: 39.8 MB (39754457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cd41aeec76fcd05354986cf47255ec9ea93893c6a542e45d04fa2658888dc934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab4710b2795f1f0e9bd99fc83d5e31a9d49e909d7a332580eb0f9f682e502c4`

```dockerfile
```

-	Layers:
	-	`sha256:cf09c9b6e43e1c484c5141e04e46ae23493b95b109ca05601ad311146a15b7e7`  
		Last Modified: Sun, 28 Dec 2025 08:33:29 GMT  
		Size: 8.0 MB (7967804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f0869668bc3e1cfe1ce6dd3289ade54a7ae1b232183bab66d0461e13df802c`  
		Last Modified: Sun, 28 Dec 2025 08:33:30 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:550a0be23df2a0fb87c855759834b8d8e500d9071bd22d2deb25f0e2f66ac538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174128477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4847cfd1046da661846018cc93f85c9cadaf6c3168feb1e657ef3287071476`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Dec 2025 05:52:48 GMT
MAINTAINER Rob Hoelz
# Sun, 28 Dec 2025 05:52:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:48 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:48 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:11:18 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:11:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:11:18 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a0fe8ec3e714678196937525cf83b878e958b9a2955403237aa25ff3e1103`  
		Last Modified: Sun, 28 Dec 2025 06:11:41 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae45635f620176965a51223386f46e9bf93a2f4d05c3fbc3c1961113a278fcbf`  
		Last Modified: Sun, 28 Dec 2025 06:11:44 GMT  
		Size: 37.8 MB (37796429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bf68fc565e5ae0115ff1efc764f0d825ec3646c928418cf17ba790ed6f8ba75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4524e914e44bc1ab4624337731fd7cf781033107d7bb744b9a7af2828b9db89`

```dockerfile
```

-	Layers:
	-	`sha256:b6f85b1d75a9bbb4fc68d40606f23a178786ca35bf298c70b8dbf1fce4cba64f`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 8.0 MB (7974197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68686b0ad2338b237714abaadca51a766e1bc6451fcae3afc98ef5b88b189f37`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:588eeb71c889832b0753c41f5488d2cc4dfed9eb3097b6044fa4fe4b9780ebc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c327678130dc4cc21016b4797e7db4acc8eb0006237579dba5261f22be1cfdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182454535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa5465b728c615b686b632c67aa901e486ee8f5dd58d3b0366cb362f072128c`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:51:01 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:01 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:58 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:58 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95217a361e37efeac6ad41b978aeb38f999c166ef3a0bbb6b0ab96ec7039350e`  
		Last Modified: Sun, 28 Dec 2025 06:05:20 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34137921a2e46afb191b17ceaf28bb332e63dfd262869b8a6df6095e8b07d88`  
		Last Modified: Sun, 28 Dec 2025 06:05:25 GMT  
		Size: 39.8 MB (39769261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7ff558f7a81805375ec83bcbaec2db641d9102d0d2ddd22403c44878f3c72fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c9158dd4c950625b697fda25a60fa8fcc74176e78d462a30e65fa1aa0ddc17`

```dockerfile
```

-	Layers:
	-	`sha256:0991552a10ff7383368da1ed1ac2635b9bb9353bf4f84dc105a5df0fe63a6dd3`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cba456c68ea28728fa377a36e3a33ef283f7ddc75966f61b04398cdd96a3f5`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:133dceefe28117eaa25f7a676d1c698fd00d18fa172796f1f2a39fae3069b4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180073593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31e3b95f4f14b9f733a219207da8235471e91dded23d37fc28a8f9262518030`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:52:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:12 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:07 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:12:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8eec79c9a4e5bc4dd20acecdde355a57d33906fdf19b4ea9a45d404d180499`  
		Last Modified: Sun, 28 Dec 2025 06:12:30 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405a3fd297caf3404b3b4e80425f58185229292e66edc966cce2ae56b383137`  
		Last Modified: Sun, 28 Dec 2025 06:12:33 GMT  
		Size: 37.8 MB (37814168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b97dac5e2c1dfde6e85254a359111f71863a91f26ae517bc3431174a58b38593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b672b2980dc22eb95f9fca365a146ae75dc544a7afc8d9b79bdb9b06ff1d97`

```dockerfile
```

-	Layers:
	-	`sha256:3308fa553a2c791b08292e5777d2770bf27e2fa52106da0576049497294855d5`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97b1945a3b482a96aa0fa587c119d53041f70a1d62fbcdfdd3ba8ae6c77b7fb`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:588eeb71c889832b0753c41f5488d2cc4dfed9eb3097b6044fa4fe4b9780ebc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c327678130dc4cc21016b4797e7db4acc8eb0006237579dba5261f22be1cfdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182454535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa5465b728c615b686b632c67aa901e486ee8f5dd58d3b0366cb362f072128c`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:51:01 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:51:01 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:51:01 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:04:58 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:04:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:04:58 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95217a361e37efeac6ad41b978aeb38f999c166ef3a0bbb6b0ab96ec7039350e`  
		Last Modified: Sun, 28 Dec 2025 06:05:20 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34137921a2e46afb191b17ceaf28bb332e63dfd262869b8a6df6095e8b07d88`  
		Last Modified: Sun, 28 Dec 2025 06:05:25 GMT  
		Size: 39.8 MB (39769261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:7ff558f7a81805375ec83bcbaec2db641d9102d0d2ddd22403c44878f3c72fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c9158dd4c950625b697fda25a60fa8fcc74176e78d462a30e65fa1aa0ddc17`

```dockerfile
```

-	Layers:
	-	`sha256:0991552a10ff7383368da1ed1ac2635b9bb9353bf4f84dc105a5df0fe63a6dd3`  
		Last Modified: Sun, 28 Dec 2025 08:33:35 GMT  
		Size: 7.8 MB (7769499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cba456c68ea28728fa377a36e3a33ef283f7ddc75966f61b04398cdd96a3f5`  
		Last Modified: Sun, 28 Dec 2025 08:33:36 GMT  
		Size: 13.0 KB (12992 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:133dceefe28117eaa25f7a676d1c698fd00d18fa172796f1f2a39fae3069b4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180073593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31e3b95f4f14b9f733a219207da8235471e91dded23d37fc28a8f9262518030`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
MAINTAINER AntonOks
# Sun, 28 Dec 2025 05:52:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Sun, 28 Dec 2025 05:52:12 GMT
ARG rakudo_version=2025.12-01
# Sun, 28 Dec 2025 05:52:12 GMT
ENV rakudo_version=2025.12-01
# Sun, 28 Dec 2025 06:12:07 GMT
# ARGS: rakudo_version=2025.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 28 Dec 2025 06:12:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sun, 28 Dec 2025 06:12:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8eec79c9a4e5bc4dd20acecdde355a57d33906fdf19b4ea9a45d404d180499`  
		Last Modified: Sun, 28 Dec 2025 06:12:30 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405a3fd297caf3404b3b4e80425f58185229292e66edc966cce2ae56b383137`  
		Last Modified: Sun, 28 Dec 2025 06:12:33 GMT  
		Size: 37.8 MB (37814168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b97dac5e2c1dfde6e85254a359111f71863a91f26ae517bc3431174a58b38593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b672b2980dc22eb95f9fca365a146ae75dc544a7afc8d9b79bdb9b06ff1d97`

```dockerfile
```

-	Layers:
	-	`sha256:3308fa553a2c791b08292e5777d2770bf27e2fa52106da0576049497294855d5`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 7.8 MB (7777174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97b1945a3b482a96aa0fa587c119d53041f70a1d62fbcdfdd3ba8ae6c77b7fb`  
		Last Modified: Sun, 28 Dec 2025 08:33:42 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json
