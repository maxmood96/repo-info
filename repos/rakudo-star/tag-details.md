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
$ docker pull rakudo-star@sha256:06ef8ec097c6592b8080c2b13c11d3004a358d964760299c07151c19359f5df4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7de6be39bf186e6563c7df23b2a3e5f653f4a78d17d4336a1895ce31f6eb7ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179207237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7183cad597e1b270843dbb7dac99cd87c78d831529b942f938d3b274ade39f00`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:48 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:17:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:48 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:48 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9e1ed62d1a2b5c8a006b91e2cfec6c234d1bfb20a80fb6fadd8782ff34205`  
		Last Modified: Wed, 20 May 2026 01:35:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a22c6e2e18ef08a22ad402278980a00c2b82a46d8b4505fd45ea6e321d8b`  
		Last Modified: Wed, 20 May 2026 01:35:37 GMT  
		Size: 42.3 MB (42260740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdee54e2758e904e9dd9287f0a8dacdf40e5da1ae9b7ccd0562d70fb2c394b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd56cfd53cd90d1f72f3b9d83f3b602e32de3df901d469636442ae41c613d280`

```dockerfile
```

-	Layers:
	-	`sha256:9cfa43c350e509b638aa4fc9fa6f9a7972f352946dfe35aff284da8f15f80115`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 8.0 MB (7968469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6725920fbf99229bb0d0f639ddfe62c7a6490d22e24d569436d53f014f61469c`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1abc370570a269136227dc51b3e28354421ec1ca918882db09db4a997584927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176745246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfaf60ff8c386577acf039c6c5c271618294a3b7c9fcd83788afd1321f5c578`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:18:31 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:18:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:18:31 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:18:31 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:40:11 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:40:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:40:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d58c84cc7c70bdc8bae0194bf29f3d91c0ee0a3eb12a28d3b4a6b23b6ea85`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cf77ab180fe31092f29408e53e5a9332097ad1f5c1a9b14a2aeb6aa29195c`  
		Last Modified: Wed, 20 May 2026 01:40:28 GMT  
		Size: 40.3 MB (40261528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c2c3f686ad7c93a0a2ef02ea3828b140a2a69a8a84308c4088cfce5a60cf9b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f842b4e1edc00468fb458b32fab00137e8a3dd4466fc3e9413b4343eb38e76f`

```dockerfile
```

-	Layers:
	-	`sha256:70dc6fba4295dcfcc71b458c1d854a3b1f86b371939b7d4945a9b59a5f7f37cc`  
		Last Modified: Wed, 20 May 2026 01:40:27 GMT  
		Size: 8.0 MB (7974862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e549d5f20adf24258b84d6de791af46d94b2202cd155d016049584c09d4fee50`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
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
$ docker pull rakudo-star@sha256:06ef8ec097c6592b8080c2b13c11d3004a358d964760299c07151c19359f5df4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7de6be39bf186e6563c7df23b2a3e5f653f4a78d17d4336a1895ce31f6eb7ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179207237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7183cad597e1b270843dbb7dac99cd87c78d831529b942f938d3b274ade39f00`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:48 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:17:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:48 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:48 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9e1ed62d1a2b5c8a006b91e2cfec6c234d1bfb20a80fb6fadd8782ff34205`  
		Last Modified: Wed, 20 May 2026 01:35:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a22c6e2e18ef08a22ad402278980a00c2b82a46d8b4505fd45ea6e321d8b`  
		Last Modified: Wed, 20 May 2026 01:35:37 GMT  
		Size: 42.3 MB (42260740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdee54e2758e904e9dd9287f0a8dacdf40e5da1ae9b7ccd0562d70fb2c394b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd56cfd53cd90d1f72f3b9d83f3b602e32de3df901d469636442ae41c613d280`

```dockerfile
```

-	Layers:
	-	`sha256:9cfa43c350e509b638aa4fc9fa6f9a7972f352946dfe35aff284da8f15f80115`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 8.0 MB (7968469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6725920fbf99229bb0d0f639ddfe62c7a6490d22e24d569436d53f014f61469c`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1abc370570a269136227dc51b3e28354421ec1ca918882db09db4a997584927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176745246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfaf60ff8c386577acf039c6c5c271618294a3b7c9fcd83788afd1321f5c578`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:18:31 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:18:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:18:31 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:18:31 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:40:11 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:40:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:40:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d58c84cc7c70bdc8bae0194bf29f3d91c0ee0a3eb12a28d3b4a6b23b6ea85`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cf77ab180fe31092f29408e53e5a9332097ad1f5c1a9b14a2aeb6aa29195c`  
		Last Modified: Wed, 20 May 2026 01:40:28 GMT  
		Size: 40.3 MB (40261528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c2c3f686ad7c93a0a2ef02ea3828b140a2a69a8a84308c4088cfce5a60cf9b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f842b4e1edc00468fb458b32fab00137e8a3dd4466fc3e9413b4343eb38e76f`

```dockerfile
```

-	Layers:
	-	`sha256:70dc6fba4295dcfcc71b458c1d854a3b1f86b371939b7d4945a9b59a5f7f37cc`  
		Last Modified: Wed, 20 May 2026 01:40:27 GMT  
		Size: 8.0 MB (7974862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e549d5f20adf24258b84d6de791af46d94b2202cd155d016049584c09d4fee50`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
