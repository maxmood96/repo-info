## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:71def8c2fff7781217b4a32dbe0f67f6524d1fa0237b72b3c5ca538f8afc5bd2
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
$ docker pull rakudo-star@sha256:c32068d663f018b2d7a1a325668ae75664f94bcdf616e1aab959685394821459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49185146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ca45691bd01f1831d813f25d3915486636e4c8e1171151052cf073b5ba2066`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 28 Oct 2024 03:18:11 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Mon, 28 Oct 2024 03:18:11 GMT
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8fd22b15bb95ff4b8fed27cd01a43e7dfae12eb0a5aee0549fc676a61da89e`  
		Last Modified: Thu, 05 Dec 2024 22:52:02 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb47a25bff72c4d1320ab206dd2af8d7aa99d577415e0ac393d45d058784d08`  
		Last Modified: Thu, 05 Dec 2024 22:52:04 GMT  
		Size: 45.2 MB (45191000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:be794b8fca5d0f9a994f22df61622479e7c464132b2b5fd1fe37136f641bc1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5505a5adf34e33992b3c51ca610fc3b8ea5d259ee0f3ae6d740e060969ea9b`

```dockerfile
```

-	Layers:
	-	`sha256:1020f54ca7e152f0ce054bd4cae2fd1e0964019a705bd67a117e446fbe97ebe3`  
		Last Modified: Thu, 05 Dec 2024 22:52:03 GMT  
		Size: 120.8 KB (120819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeffddb1f9a842d611d2ac5608f47eac671fa9b23e5b184cddde22e9c8fd025e`  
		Last Modified: Thu, 05 Dec 2024 22:52:02 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json
