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
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json
