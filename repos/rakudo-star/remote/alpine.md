## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:ab31840bd6003fe439568d84da7153589303715dd3a6c590ebeb337ffb02ee82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b287c453e6b08cdbe1aff083828df6820f6f6b329ccd117dfd48b4b80a0b5515
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32643692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc68b92cd51ac4524bc3b1ad426fa4d1fe17496a69dabae8fe79ca5a469eac`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 19:45:01 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Mon, 09 Jan 2023 19:45:01 GMT
ARG rakudo_version=2022.12-01
# Mon, 09 Jan 2023 19:45:01 GMT
ENV rakudo_version=2022.12-01
# Mon, 09 Jan 2023 19:53:26 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Mon, 09 Jan 2023 19:53:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 09 Jan 2023 19:53:26 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d66389e4e1c6f3611c13f7c7e33413ba144ff09745db442913d3e6aca8818f`  
		Last Modified: Mon, 09 Jan 2023 19:53:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0cfa73c6b81456b1bba6c3844d8706fdd048161a54fc49785d8a445a7ddb4f`  
		Last Modified: Mon, 09 Jan 2023 19:53:52 GMT  
		Size: 29.3 MB (29271799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:2e0cff46e65850e31c68425a767f15621fef1e908cf3452760afbd54d5e74f07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32359184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087e93692b32eb063599150b3066729fd94ccf46e60664d37b1eb9ad8642afde`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:11:30 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Sat, 11 Feb 2023 05:11:30 GMT
ARG rakudo_version=2022.12-01
# Sat, 11 Feb 2023 05:11:30 GMT
ENV rakudo_version=2022.12-01
# Sat, 11 Feb 2023 05:17:37 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Sat, 11 Feb 2023 05:17:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sat, 11 Feb 2023 05:17:37 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddcc3a39a5eae9441a03a3dd406fc94de4df0c258db00c745055d0d350170a8`  
		Last Modified: Sat, 11 Feb 2023 05:18:01 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1369931f8a055a8ad4daa4085a41f3a8ccaed4fcfa71de41f9565ca8509e0d`  
		Last Modified: Sat, 11 Feb 2023 05:18:06 GMT  
		Size: 29.1 MB (29095960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
