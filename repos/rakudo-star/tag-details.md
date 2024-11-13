<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.10`](#rakudo-star202410)
-	[`rakudo-star:2024.10-alpine`](#rakudo-star202410-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.10`

```console
$ docker pull rakudo-star@sha256:5b9d6e4332887c913ee5f3347b8904b75ea6df28a941de853a4fcac2779e34bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.10` - linux; amd64

```console
$ docker pull rakudo-star@sha256:56ea13ab2b95c9d0c5fda6583133432701f30cce7d5f126d363ddb88ad1a6171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182785651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2f67964d5200c9c1a749d4a58c32cfaa895b77f79fa04754d2630c268dda87`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b96ce24bb3809ab881b3d24e09765f0a563523f27423bb4f2b7294952e9da`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b29cafaf5897aad00f3e6fcd016e24f88f6cc2b328b07524e5afb69825aee`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 44.8 MB (44756995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.10` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4022477969d69a8476e6376abf6ee24924be3fd452f9c548b1706223cc2c8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5005748dad72da5ab0f05d73a05d5eaa6af6b4df21123d346ce69bfd12e03c`

```dockerfile
```

-	Layers:
	-	`sha256:528ec97ed8fdeb83c0fcd6092e17f46ba29f5673ad49b46453b30488be09620d`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 7.8 MB (7770585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22010cb7fc4714e2b58f1645dfcab0c57a4f08ab5c37e6259799991f7f9bed52`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.10` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8c06cd46dd84e75b50c27d00b5f2b94260a27ede6e3c0360f3ff9b1a113d111a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182063280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5843e1099a2bcb2eaf00df778c322bc8f386ca297cf016daf59b7baed96e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2f87c9516ae0dc28261e149b81d9e4cc424267fad37ef84ad6a9b5f1233fb8`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e32e2436058f8504787c765f55d19fba5c9e587fc56af743fecf176fbefcbbc`  
		Last Modified: Wed, 30 Oct 2024 18:42:22 GMT  
		Size: 44.5 MB (44531184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.10` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a78c5fa882ccb53c2100ed39bf2c204f16aa2c74c13d7e2dfcddeab5f7338426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5f2f1275fcbf6c83c04d8773f58c60e78d7aee739cdabd2605c5d7efd2cf4f`

```dockerfile
```

-	Layers:
	-	`sha256:788ff2d1710ec2d63810c74e31c653c026abb40c0649fec3053b9d3ab49818bf`  
		Last Modified: Wed, 30 Oct 2024 18:42:21 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b04a3c6bd8a9100db4d43d7cf20ff82c7f14778e5c9e7ed031213924ffb2ebe`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2024.10-alpine`

```console
$ docker pull rakudo-star@sha256:96b6e846ea0363a41516c291f0ca6814e0284600c8db8678e3a86851834fc018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7a0263a8ffade1221c87899f5e8d7ba8066a86e4f85c243dc9e8cb25fdb6c84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48606207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440b682c2e0b3520b3d15efe8c10dfabf3bc2585701f09a29147bb9c7f2f498f`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dfa47862763866377a2d1aaed58105c775c77a8aeeeaaf652baa126fce7641`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c586b5823b429a5fb3e43e998858182600047be41ded3c56a629540d57986e8`  
		Last Modified: Tue, 12 Nov 2024 03:03:55 GMT  
		Size: 45.0 MB (44981342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2c76ef51344936ebdb1a34e3645b3e8cc1406477552ed6303982d3cdb0c55d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 KB (127574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e27b3867fe2438f2cd89e43867cb5ba01d4bd712c2f9f73a66954fa4f775660`

```dockerfile
```

-	Layers:
	-	`sha256:fbbb5f6a21953f6a4847761d00e100cceb29a2c9546d12910a96c08fdc42f07c`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bbdd312a1422ee946ebad760ca1bc5e1d477709c800a004a30fd0116840079`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 11.7 KB (11739 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.10-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2782645e65c2a736c06ebf9475a6404eb0819ab1e3bbe8a24cc272a377472ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48917127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0856ca9e328d30b7ee6947780e34eae1da64257aba51b0660635b37fab0f790`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576f6635b99097debf574c41b96ac90739500a159e29750e2689941ce737770`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27fbcb4d2d904ecd4fef1809e23e1bbd9eedf1f7ffc1b79c6c2721cfd8d8c7`  
		Last Modified: Tue, 12 Nov 2024 23:51:57 GMT  
		Size: 44.8 MB (44828438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.10-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:92164169449c44a0907f71d39494689ac85eb94fa830373a0c31e93e44515385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 KB (127703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea841651242f13700aca243fc6c3ffae029a119476c8848732049731b7074512`

```dockerfile
```

-	Layers:
	-	`sha256:4e51206864ba5a4e5e74c96107032f59c5b35289f595120a8e1797265429a198`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde8e240dd28cf6da688dbb2f983980761db5e88dd21e6a95b78f3382243cb9f`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:96b6e846ea0363a41516c291f0ca6814e0284600c8db8678e3a86851834fc018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7a0263a8ffade1221c87899f5e8d7ba8066a86e4f85c243dc9e8cb25fdb6c84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48606207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440b682c2e0b3520b3d15efe8c10dfabf3bc2585701f09a29147bb9c7f2f498f`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dfa47862763866377a2d1aaed58105c775c77a8aeeeaaf652baa126fce7641`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c586b5823b429a5fb3e43e998858182600047be41ded3c56a629540d57986e8`  
		Last Modified: Tue, 12 Nov 2024 03:03:55 GMT  
		Size: 45.0 MB (44981342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2c76ef51344936ebdb1a34e3645b3e8cc1406477552ed6303982d3cdb0c55d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 KB (127574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e27b3867fe2438f2cd89e43867cb5ba01d4bd712c2f9f73a66954fa4f775660`

```dockerfile
```

-	Layers:
	-	`sha256:fbbb5f6a21953f6a4847761d00e100cceb29a2c9546d12910a96c08fdc42f07c`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bbdd312a1422ee946ebad760ca1bc5e1d477709c800a004a30fd0116840079`  
		Last Modified: Tue, 12 Nov 2024 03:03:54 GMT  
		Size: 11.7 KB (11739 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2782645e65c2a736c06ebf9475a6404eb0819ab1e3bbe8a24cc272a377472ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48917127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0856ca9e328d30b7ee6947780e34eae1da64257aba51b0660635b37fab0f790`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 03:18:11 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576f6635b99097debf574c41b96ac90739500a159e29750e2689941ce737770`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27fbcb4d2d904ecd4fef1809e23e1bbd9eedf1f7ffc1b79c6c2721cfd8d8c7`  
		Last Modified: Tue, 12 Nov 2024 23:51:57 GMT  
		Size: 44.8 MB (44828438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:92164169449c44a0907f71d39494689ac85eb94fa830373a0c31e93e44515385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 KB (127703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea841651242f13700aca243fc6c3ffae029a119476c8848732049731b7074512`

```dockerfile
```

-	Layers:
	-	`sha256:4e51206864ba5a4e5e74c96107032f59c5b35289f595120a8e1797265429a198`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde8e240dd28cf6da688dbb2f983980761db5e88dd21e6a95b78f3382243cb9f`  
		Last Modified: Tue, 12 Nov 2024 23:51:55 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:5b9d6e4332887c913ee5f3347b8904b75ea6df28a941de853a4fcac2779e34bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:56ea13ab2b95c9d0c5fda6583133432701f30cce7d5f126d363ddb88ad1a6171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182785651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2f67964d5200c9c1a749d4a58c32cfaa895b77f79fa04754d2630c268dda87`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b96ce24bb3809ab881b3d24e09765f0a563523f27423bb4f2b7294952e9da`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b29cafaf5897aad00f3e6fcd016e24f88f6cc2b328b07524e5afb69825aee`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 44.8 MB (44756995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4022477969d69a8476e6376abf6ee24924be3fd452f9c548b1706223cc2c8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5005748dad72da5ab0f05d73a05d5eaa6af6b4df21123d346ce69bfd12e03c`

```dockerfile
```

-	Layers:
	-	`sha256:528ec97ed8fdeb83c0fcd6092e17f46ba29f5673ad49b46453b30488be09620d`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 7.8 MB (7770585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22010cb7fc4714e2b58f1645dfcab0c57a4f08ab5c37e6259799991f7f9bed52`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8c06cd46dd84e75b50c27d00b5f2b94260a27ede6e3c0360f3ff9b1a113d111a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182063280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5843e1099a2bcb2eaf00df778c322bc8f386ca297cf016daf59b7baed96e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2f87c9516ae0dc28261e149b81d9e4cc424267fad37ef84ad6a9b5f1233fb8`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e32e2436058f8504787c765f55d19fba5c9e587fc56af743fecf176fbefcbbc`  
		Last Modified: Wed, 30 Oct 2024 18:42:22 GMT  
		Size: 44.5 MB (44531184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a78c5fa882ccb53c2100ed39bf2c204f16aa2c74c13d7e2dfcddeab5f7338426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5f2f1275fcbf6c83c04d8773f58c60e78d7aee739cdabd2605c5d7efd2cf4f`

```dockerfile
```

-	Layers:
	-	`sha256:788ff2d1710ec2d63810c74e31c653c026abb40c0649fec3053b9d3ab49818bf`  
		Last Modified: Wed, 30 Oct 2024 18:42:21 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b04a3c6bd8a9100db4d43d7cf20ff82c7f14778e5c9e7ed031213924ffb2ebe`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:5b9d6e4332887c913ee5f3347b8904b75ea6df28a941de853a4fcac2779e34bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:56ea13ab2b95c9d0c5fda6583133432701f30cce7d5f126d363ddb88ad1a6171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182785651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2f67964d5200c9c1a749d4a58c32cfaa895b77f79fa04754d2630c268dda87`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4b96ce24bb3809ab881b3d24e09765f0a563523f27423bb4f2b7294952e9da`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b29cafaf5897aad00f3e6fcd016e24f88f6cc2b328b07524e5afb69825aee`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 44.8 MB (44756995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4022477969d69a8476e6376abf6ee24924be3fd452f9c548b1706223cc2c8b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5005748dad72da5ab0f05d73a05d5eaa6af6b4df21123d346ce69bfd12e03c`

```dockerfile
```

-	Layers:
	-	`sha256:528ec97ed8fdeb83c0fcd6092e17f46ba29f5673ad49b46453b30488be09620d`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 7.8 MB (7770585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22010cb7fc4714e2b58f1645dfcab0c57a4f08ab5c37e6259799991f7f9bed52`  
		Last Modified: Tue, 12 Nov 2024 06:11:17 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8c06cd46dd84e75b50c27d00b5f2b94260a27ede6e3c0360f3ff9b1a113d111a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182063280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5843e1099a2bcb2eaf00df778c322bc8f386ca297cf016daf59b7baed96e3`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
MAINTAINER Rob Hoelz
# Mon, 28 Oct 2024 03:18:11 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ARG rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
ENV rakudo_version=2024.10-01
# Mon, 28 Oct 2024 03:18:11 GMT
# ARGS: rakudo_version=2024.10-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 28 Oct 2024 03:18:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2f87c9516ae0dc28261e149b81d9e4cc424267fad37ef84ad6a9b5f1233fb8`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e32e2436058f8504787c765f55d19fba5c9e587fc56af743fecf176fbefcbbc`  
		Last Modified: Wed, 30 Oct 2024 18:42:22 GMT  
		Size: 44.5 MB (44531184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a78c5fa882ccb53c2100ed39bf2c204f16aa2c74c13d7e2dfcddeab5f7338426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5f2f1275fcbf6c83c04d8773f58c60e78d7aee739cdabd2605c5d7efd2cf4f`

```dockerfile
```

-	Layers:
	-	`sha256:788ff2d1710ec2d63810c74e31c653c026abb40c0649fec3053b9d3ab49818bf`  
		Last Modified: Wed, 30 Oct 2024 18:42:21 GMT  
		Size: 7.8 MB (7776924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b04a3c6bd8a9100db4d43d7cf20ff82c7f14778e5c9e7ed031213924ffb2ebe`  
		Last Modified: Wed, 30 Oct 2024 18:42:20 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json
