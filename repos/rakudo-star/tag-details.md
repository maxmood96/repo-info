<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.12`](#rakudo-star202412)
-	[`rakudo-star:2024.12-alpine`](#rakudo-star202412-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.12`

```console
$ docker pull rakudo-star@sha256:f1fd4d2e6682ba6c3ba30f9ee5aa60405bbe32e861de4e060650d39412658e26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12` - linux; amd64

```console
$ docker pull rakudo-star@sha256:82cc9bad23d5659d4e562379cd062708cd499ad66bfbf0bb82bf086b9d6ea5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179090720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e08e781f668c2916444f1ba3ed534613553ea30dcf91ffeda05f2e7754cd1`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe29766ae26f5e2e8f3589f65f27cf061a2d052c89ad59d461908ec410809dc`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6243ca2bba13d55ddd7a400f05e5fed627ea9ddaf3514fce16b56927b0635c27`  
		Last Modified: Tue, 17 Dec 2024 19:47:33 GMT  
		Size: 42.3 MB (42332885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a085b5d94b19c2eb3ca49296297374854fb428195d68f7bb636735767661e938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0b86f995be4d490629e235a3673ff08587a4fc313609efec70fea77ade34a5`

```dockerfile
```

-	Layers:
	-	`sha256:5c2cbce4ecc9de489f67d9f377a149718fbf9234ed92ee4ebcc4d2277e815995`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 7.8 MB (7758951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4e1f64b206d6ca9a385b443dac373b699447d7382742411f25ccbe8f635e7e`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:9e572fa986d127e967de7b730ed7a2d3b6b5e6b2989bb9838636df843e8fb2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cfd851f88de83b788c3b899d4f23712be8185725dd50a72b0e00823d5ad9d5`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd53db722957ccbb80cf3d0297408699bbf0ffd643d46fe671f4be49cbbd11d`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694298081aa06f62a897b3493923597fda95522876fa450a65006f5fbe4c0201`  
		Last Modified: Wed, 18 Dec 2024 00:08:30 GMT  
		Size: 40.6 MB (40601080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bc952e1a5911a7cc1d34368887490823b7175ca1ec0e0b557bc637145c213a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1a452cbbec8546b07fbed76b611d5a895000f7fe6f872d4ec07e3a8cf0bdf2`

```dockerfile
```

-	Layers:
	-	`sha256:9d4bfd9f1ac59b5b8ca3989161d3bb434587860436452a05ea887c7bf0bae3d0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 7.8 MB (7765356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f830cb40f934a3cbdbfacac3a427f98a4c626eef5f4d35ebd527ef9f7afbcbc0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2024.12-alpine`

```console
$ docker pull rakudo-star@sha256:9b5e9650062644cd651e7cac46ffb9e1cf2b941072774f052fd698fa295f404c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:d9f13e5cb361fbcc0edea12ea2cfe445ede7e8a703f79fffd1465ba6f16aba82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46208271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a3276a16a1c322f76eb837325627f48405ee3667d4474f9f91b7f5113ae72b`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65f7455a620b535d318c60252987d390556bcc59ecb5ca4bbc4ba383d4137d`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f906d564861a772f41695a44553bf201bd41d7c22c347b5f8ae2001db7c52897`  
		Last Modified: Tue, 17 Dec 2024 19:47:37 GMT  
		Size: 42.6 MB (42562868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d2c0d3c69456a88195a2731bbf4e995f890926446f0a4673e61d22073e5d7f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed484c84b352d64f90d6f4ae8bfc2619198ead1df3f0eb95f533908d24d30c7`

```dockerfile
```

-	Layers:
	-	`sha256:39f7d77067acdf69cbe24980455a14e7de3fe402531ee0ed4fda3b8dcad2d64a`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 120.7 KB (120720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c253be0f28475551c334cf5a296191de44283a1b3ea58c2f285c5a08ca2ef6`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 11.7 KB (11741 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:37960b4844d685339328cf088e9fec70d2cf675094c40e38e1c9c3c3d442235c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46397854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6afd0f0bf7ddad9f0a244bb952429f35cb4c83d833944d0628718664aa84f4`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cae69be859e511eac3a7225b53f0ab7e5c29ac998fce0aaf6ea2dfdb5eb72a`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358d950d08f053246db63fdbc290842d546c94b7851aa57035dad0806cbdcc9`  
		Last Modified: Tue, 17 Dec 2024 23:12:48 GMT  
		Size: 42.4 MB (42403708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d64faaf5a2804f67ec4beb9e9445c3a5b3d123f6f12914e46a21fcf6f155f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9642f997686b0e41e9a62a781df371bec7539c3751863d73b2d4a3d1634065`

```dockerfile
```

-	Layers:
	-	`sha256:57c5ab764879dc313358c371b39c24af52e4f43964c962b05d0ffd2fa08dcfbf`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45e918fc188de6a9f1db8846a297eaf85c57935af08ff31ce80e650558e87ef`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:9b5e9650062644cd651e7cac46ffb9e1cf2b941072774f052fd698fa295f404c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:d9f13e5cb361fbcc0edea12ea2cfe445ede7e8a703f79fffd1465ba6f16aba82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46208271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a3276a16a1c322f76eb837325627f48405ee3667d4474f9f91b7f5113ae72b`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65f7455a620b535d318c60252987d390556bcc59ecb5ca4bbc4ba383d4137d`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f906d564861a772f41695a44553bf201bd41d7c22c347b5f8ae2001db7c52897`  
		Last Modified: Tue, 17 Dec 2024 19:47:37 GMT  
		Size: 42.6 MB (42562868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d2c0d3c69456a88195a2731bbf4e995f890926446f0a4673e61d22073e5d7f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed484c84b352d64f90d6f4ae8bfc2619198ead1df3f0eb95f533908d24d30c7`

```dockerfile
```

-	Layers:
	-	`sha256:39f7d77067acdf69cbe24980455a14e7de3fe402531ee0ed4fda3b8dcad2d64a`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 120.7 KB (120720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c253be0f28475551c334cf5a296191de44283a1b3ea58c2f285c5a08ca2ef6`  
		Last Modified: Tue, 17 Dec 2024 19:47:36 GMT  
		Size: 11.7 KB (11741 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:37960b4844d685339328cf088e9fec70d2cf675094c40e38e1c9c3c3d442235c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46397854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6afd0f0bf7ddad9f0a244bb952429f35cb4c83d833944d0628718664aa84f4`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cae69be859e511eac3a7225b53f0ab7e5c29ac998fce0aaf6ea2dfdb5eb72a`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358d950d08f053246db63fdbc290842d546c94b7851aa57035dad0806cbdcc9`  
		Last Modified: Tue, 17 Dec 2024 23:12:48 GMT  
		Size: 42.4 MB (42403708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d64faaf5a2804f67ec4beb9e9445c3a5b3d123f6f12914e46a21fcf6f155f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9642f997686b0e41e9a62a781df371bec7539c3751863d73b2d4a3d1634065`

```dockerfile
```

-	Layers:
	-	`sha256:57c5ab764879dc313358c371b39c24af52e4f43964c962b05d0ffd2fa08dcfbf`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45e918fc188de6a9f1db8846a297eaf85c57935af08ff31ce80e650558e87ef`  
		Last Modified: Tue, 17 Dec 2024 23:12:46 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:f1fd4d2e6682ba6c3ba30f9ee5aa60405bbe32e861de4e060650d39412658e26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:82cc9bad23d5659d4e562379cd062708cd499ad66bfbf0bb82bf086b9d6ea5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179090720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e08e781f668c2916444f1ba3ed534613553ea30dcf91ffeda05f2e7754cd1`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe29766ae26f5e2e8f3589f65f27cf061a2d052c89ad59d461908ec410809dc`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6243ca2bba13d55ddd7a400f05e5fed627ea9ddaf3514fce16b56927b0635c27`  
		Last Modified: Tue, 17 Dec 2024 19:47:33 GMT  
		Size: 42.3 MB (42332885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a085b5d94b19c2eb3ca49296297374854fb428195d68f7bb636735767661e938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0b86f995be4d490629e235a3673ff08587a4fc313609efec70fea77ade34a5`

```dockerfile
```

-	Layers:
	-	`sha256:5c2cbce4ecc9de489f67d9f377a149718fbf9234ed92ee4ebcc4d2277e815995`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 7.8 MB (7758951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4e1f64b206d6ca9a385b443dac373b699447d7382742411f25ccbe8f635e7e`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:9e572fa986d127e967de7b730ed7a2d3b6b5e6b2989bb9838636df843e8fb2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cfd851f88de83b788c3b899d4f23712be8185725dd50a72b0e00823d5ad9d5`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd53db722957ccbb80cf3d0297408699bbf0ffd643d46fe671f4be49cbbd11d`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694298081aa06f62a897b3493923597fda95522876fa450a65006f5fbe4c0201`  
		Last Modified: Wed, 18 Dec 2024 00:08:30 GMT  
		Size: 40.6 MB (40601080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bc952e1a5911a7cc1d34368887490823b7175ca1ec0e0b557bc637145c213a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1a452cbbec8546b07fbed76b611d5a895000f7fe6f872d4ec07e3a8cf0bdf2`

```dockerfile
```

-	Layers:
	-	`sha256:9d4bfd9f1ac59b5b8ca3989161d3bb434587860436452a05ea887c7bf0bae3d0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 7.8 MB (7765356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f830cb40f934a3cbdbfacac3a427f98a4c626eef5f4d35ebd527ef9f7afbcbc0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:f1fd4d2e6682ba6c3ba30f9ee5aa60405bbe32e861de4e060650d39412658e26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:82cc9bad23d5659d4e562379cd062708cd499ad66bfbf0bb82bf086b9d6ea5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179090720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e08e781f668c2916444f1ba3ed534613553ea30dcf91ffeda05f2e7754cd1`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe29766ae26f5e2e8f3589f65f27cf061a2d052c89ad59d461908ec410809dc`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6243ca2bba13d55ddd7a400f05e5fed627ea9ddaf3514fce16b56927b0635c27`  
		Last Modified: Tue, 17 Dec 2024 19:47:33 GMT  
		Size: 42.3 MB (42332885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a085b5d94b19c2eb3ca49296297374854fb428195d68f7bb636735767661e938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0b86f995be4d490629e235a3673ff08587a4fc313609efec70fea77ade34a5`

```dockerfile
```

-	Layers:
	-	`sha256:5c2cbce4ecc9de489f67d9f377a149718fbf9234ed92ee4ebcc4d2277e815995`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 7.8 MB (7758951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4e1f64b206d6ca9a385b443dac373b699447d7382742411f25ccbe8f635e7e`  
		Last Modified: Tue, 17 Dec 2024 19:47:32 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:9e572fa986d127e967de7b730ed7a2d3b6b5e6b2989bb9838636df843e8fb2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176683667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cfd851f88de83b788c3b899d4f23712be8185725dd50a72b0e00823d5ad9d5`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd53db722957ccbb80cf3d0297408699bbf0ffd643d46fe671f4be49cbbd11d`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694298081aa06f62a897b3493923597fda95522876fa450a65006f5fbe4c0201`  
		Last Modified: Wed, 18 Dec 2024 00:08:30 GMT  
		Size: 40.6 MB (40601080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bc952e1a5911a7cc1d34368887490823b7175ca1ec0e0b557bc637145c213a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1a452cbbec8546b07fbed76b611d5a895000f7fe6f872d4ec07e3a8cf0bdf2`

```dockerfile
```

-	Layers:
	-	`sha256:9d4bfd9f1ac59b5b8ca3989161d3bb434587860436452a05ea887c7bf0bae3d0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 7.8 MB (7765356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f830cb40f934a3cbdbfacac3a427f98a4c626eef5f4d35ebd527ef9f7afbcbc0`  
		Last Modified: Wed, 18 Dec 2024 00:08:29 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json
